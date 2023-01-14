# [Docker Essentials: A Developer Introduction](https://courses.cognitiveclass.ai/courses/course-v1:IBMDeveloperSkillsNetwork+CO0101EN+v1/course/)


## Run your first container

### What is container?
- A group of process running in isolation, and on same kernel
- Isolation is provided by namespaces, each container has its own set of "namespaces"
    - **PID** - Process IDs
    - **USER** - User and group Ids
    - **UTS** - Hostname and domain name
    - **NS** - Mount points
    - **NET** - Network devices, stacks, ports
    - **IPC** - Inter-process communications, message queues
- cgroups - Controls limits and monitoring of resources

### VM vs Container
- VM runs on hyper visor and each VM has its own OS, they are heavy and slow to start
- Container does not have a fully blown OS, is lightweight and fast to start

### What is docker?
- Docker is tooling to manage containers
- Enables and simplify the container to be use by masses
- Creates a '*build once, run anywhere*' model

### Why Containers are appealing to users
- No more "Works on my machine", since we are packaging our dependency
- Its lightweight and fast
- Better resource utilization, we can fit more container than VM in a system
- Ecosystem and tooling: Takes care of orchestrations

### Run a container
- Open a terminal on your local computer and run this command: `docker container run -t ubuntu top`
- Docker container `run` command is used to run a container with the Ubuntu image and execute the `top` command. The `-t` flag allocates a pseudo-TTY, which you need for the `top` command to work correctly.
- `top` is a Linux utility that prints the processes on a system and orders them by resource consumption. Notice that there is only a single process in this output: it is the top process itself. 
- You don't see other processes from the host in this list because of the PID namespace isolation.

- Containers uses Linux namespaces to provide isolation of system resources from other containers or the host. 
- The PID namespace provides isolation for process IDs. 
- If you run `top` while inside the container, you will notice that it shows the processes within the PID namespace of the container, which is much different than what you can see if you ran top on the host.

- Even though we are using the Ubuntu image, it is important to note that the container does not have its own kernel. 

- It uses the kernel of the host and the Ubuntu image is used only to provide the file system and tools available on an Ubuntu system.

- Inspect the container: `docker container exec`. This command allows you to enter a running container's namespaces with a new process.

- In the new terminal, get the ID of the running container that you just created: `docker container ls `

- Use that container ID to run bash inside that container by using the `docker container exec` command. Because you are using bash and want to interact with this container from your terminal, use the `-it` flag to run using interactive mode while allocating a pseudo-terminal: `docker container exec -it <container id> bash`
- `-i` is used for interactive mode
- Using `docker container exec` with bash is a common way to inspect a Docker container
- namespaces provides the isolation for containers that allows them to run together securely and without conflict with other containers running on the same system.

### Run multiple containers
- The Docker Store is the public central registry for Docker images. Anyone can share images there publicly. The Docker Store contains community and official images that can also be found on the *Docker Hub*.
- Store images include content that has been verified and scanned for security vulnerabilities by Docker. Go one step further and search for Certified images that are deemed enterprise-ready and are tested with Docker Enterprise Edition.
- Run an NGINX server by using the official NGINX image from the Docker Store: `docker container run --detach --publish 8080:80 --name nginx nginx`
- The `--detach` flag will run this container in the background. The `--publish` flag publishes port 80 in the container (the default port for NGINX) by using port 8080 on your host. Remember that the *NET* namespace gives processes of the container their own network stack. The `--publish` flag is a feature that can expose networking through the container onto the host.
- In general, the documentation for the verified images is very good, and you will want to refer to it when you run containers using those images.
- `--name` flag names the container. Every container has a name. If you don't specify one, Docker will randomly assign one for you.
- Specifying your own name makes it easier to run subsequent commands on your container because you can reference the name instead of the id of the container. For example, you can specify `docker container inspect nginx` instead of `docker container inspect 5e1` (where 5e1 is the container ID).
- Containers are self-contained and isolated, which means you can avoid potential conflicts between containers with different system or runtime dependencies.
- For example, you can deploy an app that uses Java 7 and another app that uses Java 8 on the same host. Or you can run multiple NGINX containers that all have port 80 as their default listening ports. *(If you're exposing on the host by using the --publish flag, the ports selected for the host must be unique.)* 
- Isolation benefits are possible because of Linux namespaces. 
- Running multiple containers on the same host gives us the ability to use the resources (CPU, memory, and so on) available on single host. This can result in huge cost savings for an enterprise.

### Remove the containers
- Get a list of the running containers: `docker container ls`
- Stop the containers by running this command for each container in the list: `docker container stop <container id>`
- You can also use the names of the containers that you specified before
- You need to enter only enough digits of the ID to be unique. Three digits is typically adequate.
- Remove the stopped containers. The following command removes any stopped containers, unused volumes and networks, and dangling images: `docker system prune`

### Summary
- Containers are composed of Linux namespaces and control groups that provide isolation from other containers and the host.
- Because of the isolation properties of containers, you can schedule many containers on a single host without worrying about conflicting dependencies. This makes it easier to run multiple containers on a single host: using all resources allocated to that host and ultimately saving server costs.
- That you should avoid using unverified content from the Docker Store when developing your own images because these images might contain security vulnerabilities or possibly even malicious software.
- Containers include everything they need to run the processes within them, so you don't need to install additional dependencies on the host.


### Graded Lab 1 quiz
Q.) Containers achieve isolation because of what feature in the Linux kernel?\
A.) Namespaces

Q.) What is the difference between a Docker container and a Docker image?\
A.) An image is the blueprint for spinning up containers. An image is a TAR of a file system, and a container is a file system plus a set of processes running in isolation.

Q.) Control groups (cgroups) limit and monitor resources.?\
A.) True

Q.) Which statement is not true about Docker?\
A.) Docker invented containers and Linux namespaces.

Q.) What tool makes it possible to run Docker containers on operating systems other than Linux?\
A.) 


## Add CI/CD value with Docker images
### Creating custom docker images from docker files
- What is a docker image?
    - It is a tar file containing a container's filesystem + metadata
    - We create this images to share/distribute this images across to other users and environment
    - After downloading the image we can create multiple container from it
    - Images are cached on host
- How to share images
    - To share images we need a central registry like *docker hub*, we can push and pull images to it
    - Default registry used by docker engine is *docker hub*, it is a public registry
    - On enterprise level, we can set up private registry ie. self host or cloud provider.
    - Docker registry is also available as docker image, ie. we can execute `docker run registry` to run our private registry

- How to create a docker image
    - we can create docker image with help of docker file
    - Docker file is a list of instructions on how to construct the container/image.
    - After we create docker file we pass it to docker build `docker build -f Dockerfile` and docker engine builds our image 
    - Example of docker file for ubuntu image
    ```docker
    From ubuntu
    ADD myapp /
    EXPOSE 80
    ENTRYPOINT /myapp
    ```
    - we are inheriting from the base of ubuntu image
    - we are adding myapp folder/application to / 
    - we are exposing port 80 so port 80 on host machine can interact with the application
    - We specify the entry point, it specifies the starting process of our container to be execute when container start

### Docker image layers
- Each line in docker files is a new image layer
- These layers are cached
- Each layer is built on pervious layer
- If you only change last line of docker file it will use the cache of first 3 layer and rebuild only the last layer
- Docker push works the same and only push the updated layer
- In term of CI/CD, after initial push all subsequent pushes would be quick
- To optimize, structure the docker file such that line that change the most is at the end of the file
- Image layers are read only, when we create a container we create a read/write layer on top of the image layers
- Allows us to reuse image in multiple instances and many images share same base image container
- This is achieved by
    1. Union File system (UFS) 
        - Union files system merge image layers into a single file system for each container
    2. Copy on write
        - Copies files that are changes in each container to its writable container layer
        - Each writable layer is exclusive for container
        - Helps keep layer read only
- Building docker image
    - `docker image build -t <image name> .`
        - `-t` parameter to name your image
        - Verify the image by running `docker image ls`
- Running docker image
    - `docker run -p 5001:5000 -d <image name>`
    - `-p` flags maps a port running inside container to our host, in this case, port 5001 of host is mapped/linked to port 5000 of the container
- Check the log output of the container.
    - `docker container logs <container id>`
    - By default, docker container logs prints out what is sent to standard out by your application

- Advantage 
    1. More container per host
    2. Faster start up/download time since bsae image are cached

### Push to a central registry
 - create a free account on *docker hub*
 - Use `docker login` tp login on terminal
 - Tag the image with username `docker tag <image name> <docker hub username>/<image name>`
 - Use `docker push <docker hub username>/<image name>` to send push image to docker hub registry
 - Navigate to Docker Hub and go to your profile to see your uploaded image

### Deploy a change
 - Rebuild the app by using your Docker Hub username in the build command using `docker image build -t <docker hub username>/<image name> .`
 - Use `docker push <docker hub username>/<image name>` to send push image to docker hub registry
 - There is a caching mechanism in place for pushing layers too. ie. it only pushes layers that has changed/modified

### Understand image layers

- One of the important design properties of Docker is its use of the union file system.
```docker
FROM python:3.6.1-alpine
RUN pip install flask
CMD ["python","app.py"]
COPY app.py /app.py
```
- Each line is a layer and each layer contains only the delta, or changes from the layers before it. 
 - To put these layers together into a single running container, Docker uses the *union file system* to overlay layers transparently into a single view.

- Each layer of the image is read-only except for the top layer, which is created for the container.
- The read/write container layer implements "*copy-on-write*", which means that files that are stored in lower image layers are pulled up to the read/write container layer only when edits are being made to those files. Those changes are then stored in the container layer

- The "*copy-on-write*" function is very fast and in almost all cases, does not have a noticeable effect on performance. 
- You can inspect which files have been pulled up to the container level with the `docker diff` command. 
-  For more information, see the command-line reference on the `docker diff` command.

- To look more closely at layers, you can use the `docker image history` command of the Python image you created

### Remove the containers

- Get a list of the containers running by executing the command `docker container ls`

- Execute `docker container stop <container id>` for each container in the list that is running

- Remove the stopped containers by running `docker system prune`

### Summary 
- Use the Dockerfile to create reproducible builds for your application and to integrate your application with Docker into the CI/CD pipeline.
- Docker images can be made available to all of your environments through a central registry. The *Docker Hub* is one example of a registry, but you can deploy your own registry on servers you control.
- A Docker image contains all the dependencies that it needs to run an application within the image. This is useful because you no longer need to deal with *environment drift (version differences)* when you rely on dependencies that are installed on every environment you deploy to.
- Docker uses of the *union file system* and "*copy-on-write*" to reuse layers of images. This lowers the footprint of storing images and significantly increases the performance of starting containers.
- Image layers are cached by the Docker build and push system. There's no need to rebuild or re push image layers that are already present on a system.
- Each line in a Dockerfile creates a new layer, and because of the layer cache, the lines that change more frequently, for example, adding source code to an image, should be listed near the bottom of the file.

### Graded Lab 2 quiz
Q) Which file should you use to create reproducible builds for Docker images?\
A) Dockerfile

Q) To rebuild and re-push images quickly, you should optimize your Dockerfile for what?\
A) The layer cache: put lines that change more frequently near the end of the file

Q) You must use Docker Hub as the central registry to share the Docker images that you create.\
A) False

Q) What's the purpose of the FROM line in a dockerfile? Select all that apply.\
A) It's required as the first line in a Dockerfile.
A) It specifies the starting image to build other image layers on top of.

Q) What does this command do: $ `docker system prune`.\
A) Removes containers that are already stopped

## Orchestrate applications with Docker Swarm

### Overview 
- A number of problems come with building an application for production, for example:
    - Scheduling services across distributed nodes
    - Maintaining high availability
    - Implementing reconciliation
    - Scaling
    - Logging

- Several orchestration solutions are available to help you solve some of these problems. One example is the IBM Cloud Kubernetes Service, which uses Kubernetes to run containers in production.

- Docker Swarm is the orchestration tool that is built in to the Docker Engine.

### Create your first swarm

- Initialize the swarm using `docker swarm init --advertise-addr eth0`

- To add a worker to this swarm, run the following command:

    `docker swarm join --token <token from docker swarm init> <ip address for eth0>:<port>`

- To add a manager to this swarm, run `docker swarm join-token manager` and follow the instructions

- Docker Swarm is a special mode that is activated by the command: `docker swarm init`.
- The `--advertise-addr` option specifies the address in which the other nodes will use to join the swarm.

- `docker swarm init` command generates a join token. 
- The token makes sure that no malicious nodes join the swarm.
- You need to use this token to join the other nodes to the swarm. 

- Use `docker node ls` to verify nodes in cluster
- The asterisk (*) next to the ID of the node represents the node that handled that specific command (`docker node ls` in this case).


### Deploy your first service

- Now that you have your node Swarm cluster initialized, you'll deploy some containers.
- To run containers on a Docker Swarm, you need to create a service.
- A service is an abstraction that represents multiple containers of the same image deployed across a distributed cluster.

- Deploy a service by using NGINX: \
`docker service create --detach=true --name nginx1 --publish 80:80  --mount source=/etc/hostname,target=/usr/share/nginx/html/index.html,type=bind,ro nginx:1.12`

- This command statement is declarative, and Docker Swarm will try to maintain the state declared in this command unless explicitly changed by another `docker service` command.
- This behavior is useful when nodes go down, for example, and containers are automatically rescheduled on other nodes. 

- The `--mount` flag is useful to have NGINX print out the hostname of the node it's running on. this is used for load balancing between multiple containers of NGINX that are distributed across different nodes in the cluster and you want to see which node in the swarm is serving the request.

- The `--publish` command uses the swarm's built-in *routing mesh*. In this case, port 80 is exposed on every node in the swarm. The routing mesh will route a request coming in on port 80 to one of the nodes running the container.

- Inspect the service using the command `docker service ls` to inspect the service you just created

- To take a deeper look at the running tasks, use the command `docker service ps`. A task is another abstraction in Docker Swarm that represents the running instances of a service

- You can use the command `docker container ls` to see the container running on that specific node

### Scale your service

- In production, you might need to handle large amounts of traffic to your application, so you'll learn how to scale

- Use the `docker service` command to update the NGINX service that you created previously to include 5 replicas. 

- This is defining a new state for the service.
`docker service update --replicas=5 --detach=true nginx1`

- When this command is executed, the following events occur:
    - The state of the service is updated to 5 replicas, which is stored in the swarm's internal storage.
    - Docker Swarm recognizes that the number of replicas that is scheduled now does not match the declared state of 5.
    - Docker Swarm schedules 5 more tasks (containers) in an attempt to meet the declared state for the service.

- This swarm is actively checking to see if the desired state is equal to actual state and will attempt to reconcile if needed

- After a few seconds, you should see that the swarm did its job and successfully started 9 more containers. 
- Notice that the containers are scheduled across all three nodes of the cluster.
- *The default placement strategy that is used to decide where new containers are to be run is the emptiest node, but that can be changed based on your needs.*
- Execute `docker service ps nginx1` to see running task in *nginx1*

- The routing mesh acts as a load balancer for these containers, alternating where it routes requests to.

- You should see which node is serving each request because of the useful `--mount `command you used earlier

- Another easy way to see which nodes those requests were routed to is to check the aggregated logs. 
- You can get aggregated logs for the service by using the command `docker service logs <service name>`. 
- This aggregates the output from every running container, that is, the output from `docker container logs <container name>`.
ex. `docker service logs nginx1`

### Apply rolling updates

- Now that you have your service deployed, you'll see a release of your application. You are going to update the version of NGINX to version 1.13

 - Run the docker service update command: `docker service update --image nginx:1.13 --detach=true nginx1`

 - This triggers a rolling update of the swarm. Quickly enter the command `docker service ps nginx1` over and over to see the updates in real time.

- You can fine-tune the rolling update by using these options:
    1. `--update-parallelism`: specifies the number of containers to update immediately (defaults to 1).
    2. `--update-delay`: specifies the delay between finishing updating a set of containers before moving on to the next set.

- After a few seconds, run the command `docker service ps nginx1` to see all the images that have been updated to nginx:1.13

### Reconcile problems with containers

- The *inspect-and-then-adapt* model of Docker Swarm enables it to perform reconciliation when something goes wrong.
- For example, when a node in the swarm goes down, it might take down running containers with it. 
- The swarm will recognize this loss of containers and will attempt to reschedule containers on available nodes to achieve the desired state for that service
- Command to leave the swarm cluster: `docker swarm leave`\
*Tip: This is the typical way to leave the swarm, but you can also kill the node and the behavior will be the same*

### Determine how many nodes you need

- In this lab, your Docker Swarm cluster consists of one master and two worker nodes. 
- This configuration is not highly available. 
- The manager node contains the necessary information to manage the cluster, but if this node goes down, the cluster will cease to function. 
- For a production application, you should provision a cluster with multiple manager nodes to allow for manager node failures.

- *You should have at least three manager nodes but typically no more than seven.*

- Manager nodes implement the *raft consensus algorithm*, which requires that more than 50% of the nodes agree on the state that is being stored for the cluster. If you don't achieve more than 50% agreement, the swarm will cease to operate correctly.
- For this reason, note the following guidance for node failure tolerance:
    - Three manager nodes tolerate one node failure.
    - Five manager nodes tolerate two node failures.
    - Seven manager nodes tolerate three node failures.
- It is possible to have an even number of manager nodes, but it adds no value in terms of the number of node failures. 
- For example, four manager nodes will tolerate only one node failure, which is the same tolerance as a three-manager node cluster.
- However, the more manager nodes you have, the harder it is to achieve a consensus on the state of a cluster.

- While you typically want to limit the number of manager nodes to no more than seven, you can scale the number of worker nodes much higher than that.
- Worker nodes can scale up into the thousands of nodes. 
- Worker nodes communicate by using the *gossip protocol*, which is optimized to be perform well under a lot of traffic and a large number of nodes.

### Summary
- Docker Swarm schedules services by using a declarative language.
- You declare the state, and the swarm attempts to maintain and reconcile to make sure the actual state equals the desired state.
- Docker Swarm is composed of manager and worker nodes.
- Only managers can maintain the state of the swarm and accept commands to modify it.
- Workers have high scalability and are only used to run containers.
- By default, managers can also run containers.
- The routing mesh built into Docker Swarm means that any port that is published at the service level will be exposed on every node in the swarm.
- Requests to a published service port will be automatically routed to a container of the service that is running in the swarm.
- You can use other tools to help solve problems with orchestrated, containerized applications in production, including *Docker Swarm* and the *IBM Cloud Kubernetes Service*.


### Quiz
Q) What is the operational model used by Docker Swarm for managing a cluster?\
A) Declarative

Q) What effect does the routing mesh have on a Docker swarm cluster?\
A) Requests that are sent to a published port on any node of the swarm will automatically be routed to a node that is running a container for that service.

Q) The "docker swarm init command" generates a join token. What is the purpose of that token?\
A) It makes sure that no malicious nodes join the swarm.

Q) When you run the following command, which of the following events does not occur?\
A) This command checks aggregated logs on the updated replicas.

Q) The more manager nodes you have, the easier it is to achieve a consensus on the state of a cluster.\
A) False

**EXTRAS**
- Alpine images are smaller than the alternative flavour of linux
- A smaller image means it will download (deploy) much faster, and it is also more secure because it has a smaller attack surface.
- If version number is not specified latest version of image is taken
- It is best practice to use a specific tag when inheriting a parent image
- Official images found in the Docker Hub, or non community images found in the Docker Store are vetted to meet certain security requirements and have good documentation
- `CMD` is the command that is executed when a container is started
- There can be only one `CMD` per Dockerfile. If you specify more than one `CMD`, then the last `CMD` will take effect
- **Remember**: Docker images contain all the dependencies that they need to run an application within the image. This is useful because you no longer need to worry about environment drift (version differences) when you rely on dependencies that are installed on every environment you deploy to. You also don't need to follow more steps to provision these environments. Just one step: install docker, and that's it.
- Although you control the swarm directly from the node in which its running, you can control a Docker swarm remotely by connecting to the Docker Engine of the manager by using the remote API or by activating a remote host from your local Docker installation (using the $DOCKER_HOST and $DOCKER_CERT_PATH environment variables).
- This will become useful when you want to remotely control production applications, instead of using SSH to directly control production servers.
- **Limits of the routing mesh**: The routing mesh can publish only one service on port 80. If you want multiple services exposed on port 80, you can use an external application load balancer outside of the swarm to accomplish this.
- [Docker documentation](https://docs.docker.com/).
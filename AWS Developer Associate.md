<!-- # AWS Developer

## How to log in?

Login to acloud guru (even mobile allowed)

1. Incognitive mode - To avoid previous AWS record/ cache / presonal account.
2. goto [acloud.guru](https://learn.acloud.guru/login?redirect_to=https%3A%2F%2Flearn.acloud.guru%2F)
3. Email ID is accenture email id
4. Login

We have playgroud to play around.

Complete Topics

1. Introduction to AWS (If you are new to AWS)
2. AWS certified developer associate. (What we need to complete)

Complete markTest(practice Exam with 75%) to get Exam vocher
marktest can be repeated but not the real exam

Learning approach is given in PPT

For more AWS Understanding additional courses is in [percipio](accenture.percipio.com)

--- -->

# Introduction To AWS

## Overview 1 : Network & Compute

What do you need to know to pass the Certified Solutions Architect Associate Exam?

- Messaging\*
- Desktop & App Streaming\*\*
  Direct Connect is a way of connecting up office or physical datacenter using dedicated telephone line to AWS. It can be due to security but mainly it's because you need a very reliable internet connection.
- Security & Identity\*
- Management Tools~
- Storage\*\*\*
  CloudFront is the storage of AWS but is moved to Networking & Content Delivery.

- Databases\*\*\*

- Compute\*\*\*
  EC2 stands for elastic Compute Cloud. It is avirtual machine in the cloud. It is highly scalable , high performance container management service that support docker container which allows to run application on a managed EC2 Instances.(out of scope for exam). You can SSH or RDP into it i.e. we have access of the system and we can install softwares.  
  Elastic Beanstalk - If you don't know anything about AWS and want to upload code to AWS you can upload it to Elastic Beanstalk and it will provision underlyinh infrastructure underneath it.  
  Lambda - It is serverless i.e. we don't have access to the host. We upload our code and it respond to event.  
  Light Sail - Will deploy wordpress type sites and we can customize it.
- Networking & Content Delivery\*\*\*
  **VPC** stands for virtual private cloud as a virtual data center where we deploy are asset. We can have multiple VPCs per region. Can interact with each other.
- AWS Global Infrastructure\*\*\*
  It is physical structure AWS runs on. Divide into 3
  a.) Region
  Is a geographical region. Each region has two or more availability zones.
  b.) Availability zone
  Is a data center or collection of data center.
  c.) Edge locations.
  Content Delivey Network for cloudfront, to cache very large media objects in the cloud.
  Route 53 is Amazon's DNS Service. You can register domains from route 53.

## Overview 2 : Storage, Databases, Migration & Analytics

### Storage

- S3(Simple Storage Service) is a virtual disk in a cloud where we can store object like files/videos/etc and not a place to install database or application. This is an object based storage. For database or application you need block-based storage.
- Glacier is a place in which you archive S3 files. Eg. A file uploaded would be stored in S3 but after some years we know we don't require immigate access to it so we move it to archive which opens some space for a new file in S3.
- EFS Elastic File Service is a file based storage and you can share it.
- Storage Gateway is a way of connecting up S3.

### Databases

- RDS Relation Database Service. Has numbers of different database technology.
- **DynamoDB** is a non-relational database. Is NoSQL database and scalable.
- Redshift is amazon dataware housing.
- Elasticache is a way of caching data to the cloud.

### Migration

- Snowball was a import/export application. after snowbasll edge it added computing to it making it a AWS data centers.
- DMS database migration services. Migrate on-Premis database to cloud.
- Server Migration Service (SMS) is same as DMS but targets virtual machine instead of databases.

### Analytics

- Athena allows you to run SQL queries on S3. Turn flat file like JSON and CSV to searchable databases by allowing queries to run on it.
- EMR (Elastic MapReduce) big data processing uses hadoop framework.
- Cloud Search & Elastic Search create search engine for the website/application. Cloud seach is fully managed service where as Elastic search is Open source
- Kinesis is a way of streaming and analyzing real time data, on massive scale.
- Data pipeline allows move data from one place to another.
- Quick sight is a buisness analytic tool it helps to create visualizations and rich sort of data that exist in AWS

## Overview 3 : Security, Management Tools, Application Services, Developer Tools, Mobile Services & IoT

- Security and Identity :

  - IAM : Is fundamental components of AWS. How we sign in ,setup new user, add new user group. Identity and Access Management service.
  - Inspector : Is a application we install on virtual machine and does security reporting.
  - Certificate Manage : Gives freee SSL certificate for domain names.
  - Directory Service : Is a way of using active directory in AWS.
  - WAF : Web Application Firewall.
  - Artifact : Is a place in AWS console where you get the documentation/compliance certifcates.

- Management Tools:

  - Cloud Watch: Used to monitor performance of AWS environment.
  - Cloud Formation : Is a way we convert our infrastructure to code. Instead of having load balancer, firewall etc. this document describe our AWS environment. We have cloud formation template so we can provision entire production environment in Cloud Formation Template and just deploy them at will. Can be done using command line. has auto scaleing and failover.
  - Cloud Trail : is a way to audit AWS resources. Works as logging.
  - Opswork : automate deployment using Shift.
  - Config : Monitor the environment and gives warnings when environment might break specific configuration that we set.
  - AWS service catalog : Allows us to decide what services are authorized and which are not.
  - Trusted Advisor : Is a way of automating customer requirement made by AWS solution architect. Gives tips about optimization.

- Appilication Services:

  - Step function : is a way to visualize whtas going on inside application.
  - SWF (Simple Work Flow) : Way to coordinate between automate tasks and human-led tasks.
  - API Gateway : Allow to create, publish, maintain and monitor and secure APIs at scale. Is a way of front-end connecting to back-end.
  - AppStream : Is a way of streaming desktop application to the users.
  - Elastic Transcoder : Changes video format to play on multiple devices.

- Developer Tools:

  - CodeCommit : Is a GitHub.
  - CodeBuild : Compiles the code and you pay by minute.
  - CodeDeploy : Is a way to deploy the code to EC2 instances.
  - Code Pipeline : keeps track of different version of codes(test, production, etc).

- Mobile Services:

  - Mobile Hub : Let's us add, configure, design feature for mobile apps. Include things like user authentication, data storage, backend logic, push notifications, content delivey and analytics.
  - Cognito : Makes it easy for user to sign up and sign in. Uses Social Identity provider.
  - Device Farm : Improve quality of android, iOS, Fire OS apps by quickly and securely testing it on hundreds of real smartphones.
  - Mobile Analytics : Simply and cheaply collect and analyze app usage data.
  - Pinpoint : Gather user data.

- Bussiness Productivity :

  - Workdocs : save work documents in the cloud like S3 but with added security.
  - WorkMail : Sending and receiving emails.

- IOT : Maintain information on devices

- Desktop & App streaming :

  - Workspaces : Is a VDI. Haveing desktop in the cloud.
  - AppStream 2.0 : Is a way of streaming desktop application to users.

## Overview 4 : A.I. Messaging & Conclusion

- Artifical Intelligence

  - Alexa : Communicate to alexa using an echo. Has lex inside?
  - Polly : Takes any text and turns into voice.
  - Machine learning : Provide a dataset and the output of those dataset and predict outcome for future data.
  - Rekognition : Upload a picture and it gives you object tags and face recognition.

- Messageing
  - SNS : Simple Notification Service is a way of notifing via email/text.
  - SQS : Simple Queue Service. Decouple application. Is a queue system for jobs.
  - SES : Simple Email Service. For sending and receiving mails using AWS.

# AWS Certified Developer - Associate 2020

## Chapter 1 : Introduction

### What Can I Skip

- Chapter 2 - IAM (Basic how to setup user, groups, policies etc.)
- Chapter 3 - EC2 (Basic provisioning EC2 Instances, RDS Instances etc.)
- Parts of Chapter 5 (Serverless websites, alexa skill)

### Exam BluePrint

| Objective                               | Weighting |
| --------------------------------------- | --------- |
| Domain 1: Deployement                   | 22%       |
| Domain 2: Security                      | 26%       |
| Domain 3: Development wirh AWS Services | 30%       |
| Domain 4: Refactoring                   | 10%       |
| Domain 5:Monitoring and Troubleshooting | 12%       |

[AWS Certified Developer–Associate(DVA-C01) Examination Guide](https://d1.awsstatic.com/training-and-certification/docs-dev-associate/AWS_Certified_Developer_Associate-Exam_Guide_EN_1.4.pdf)

**NEVER USE SECRET AND ACCESS KEYS IN THE CODE INSTEAD USING IAM ROLES**  
**NEVER USE SECRET AND ACCESS KEYS IN THE CODE INSTEAD USING IAM ROLES**  
**NEVER USE SECRET AND ACCESS KEYS IN THE CODE INSTEAD USING IAM ROLES**

#### About the Exam

- 130 Minutes in Length
- 65 Questions
- Results Immediately
- Passing 720/1000
- Valid for 2 years
- Consist of Multiple choice and scenario based question.

## Chapter 2

### IDENTITY ACCESS MANAGEMENT 101

What is IAM ?
IAM allows us to manage users and their access to AWS Console.

What does IAM give us?

- Centralized control of our AWS account.
- Shared Access to your AWS account.
- Granular Permissions : Enable different level of access to users in our organization.
- Identity Federation
- Multi Factor Authentication
- Provides temporary access for users/device and services as necessary.
- Allow to setup own password rotation policy.
- Integrates with many different AWS services.
- Supports PCI DSS Compliance.

Features of IAM:

- Fine-grained access control to AWS resources
- Integrates with existing active directory account allowing single sign on
- Centralized control of your AWS account
- **DO NOT STORE KEYS IN EC2**  
  Critical Terms :

- Users : End Users (people logging into AWS console and interacting with running API command)
- Groups : A collection of users under one set of permissions.
- Roles : You can create roles and can then assign them to AWS resources.
- Policies : A document that defines one or more permissions. And it can be attach to a user, group or a role.

Quiz:

<!--
  &#10004; = Tick
  &#10005; = Cross
  &#8594; = Arrow
-->

1. What is an IAM Policy?  
   A JSON document which defines one or more permissions.

2. Which of the following is NOT a feature of IAM?
   Allows you to set up biometric authentication, so that no passwords are required

3. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).
   False

4. In AWS, what is IAM used for?  
   &#10004;Creating and managing users and groups.  
   &#10004;Assigning permissions to allow and deny access to AWS resources.  
   &#10005;Secure VPN access to AWS.  
   &#10004;Managing access to AWS services.

5. Which statement best describes IAM?
   IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.

6. Which is the best way to enable your EC2 instance to read files in an S3 bucket?
   Create an IAM role with read-access to S3 and assign the role to the EC2 instance

7. Which IAM entity can you use to delegate access to your AWS resources to users, groups or services?
   IAM Role

## Chapter 3 : EC2

### EC2 101

Amazon Elastic Compute Cloud(EC2) is a web service that provides resizable compute capacity in the cloud. Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change. Changes the economics of computing by allowing you to pay only for capacity that you actually use. EC2 provides developers the tools to build failure resilient applications and isolate themselves from common failure scenatios.
_
Introduces pay per use rather than pay upfront.
Is basically a VM machine in cloud.
_

Pricing Option:

- On Demand : allows to pay fixed rate by hour or by second with no commitment.
- Reserved : Enter in contract for a year or 3 and it gives discount in hourly charge.
- Spot : enables you to bid whatever price you want for instance capacity providing for even greater saving if your applications have flexible start and end times.
- Dedicated Hosts : Physical EC2 server dedicated for your use. Dedicated hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.

- On Demand:

  - Perfect for users that want the low cost and flexibility of Amazon EC2 without any up front payment or long-term commitment.
  - Applications with short term, spiky, or unpredictable workloads that cannot be interrupted.
  - Applications bering developed or tested on amazon EC2 for the first time.

- Reserved:

  - app with steady state or predictable usage.
  - Application that require reserved capacity.
  - Users can make up-front payments to reduce their total computing costs even further.

- Spot Instances:

  - Applications that have flexible start and end times.
  - Applications that are only feasible at very low compute prices.
  - Users with an urgent need for large amounts of additional computing capacity.
  - Eg. You bid a instance price of 100 and the price come down to 90 you would get that instance and when the price gove above 100 the instance would be terminated. You will be charged by hour and not parial hour of usage. That is you don't need to pay for the hour the instance is terminated but if you terminate the instance your selves you would be charged for the complete hour in which the instance ran.

- Dedicated Host:

  - Useful for regulatort requirements that may not support multi-tenant virtualization.
  - Great for licensing which does not support multi-tenancy or cloud deployments.
  - Can be purchased on demand and on reservation.

- EC2 Instance Type
  | Family | EC2 Instance Types |
  | ------ | ------------------------------------ |
  | F | FGPA |
  | I | IOPS |
  | G | Graphics |
  | H | High Disk Throughput |
  | T | Cheap general purpose |
  | D | Density |
  | R | RAM |
  | M | Main Choice for general purpose apps |
  | C | Compute |
  | P | Graphics |
  | X | Extreme Memory |

What is EBS?
EBS stands for Elastic Block Storage.It is a virtual Disk. Allows to create storage volume and attach to EC2 instances. EBS is store in availability zone and is duplicate i.e. data can be accessed incase of a failure of a single component/disk. EBS vloume that is attached to EC2 instance is called root device volume and we can have additional volume on it.

EBS Volume Types:

- General Purpose SSD (GP2)

  - Balances both price and performance.
  - Ratio of 3 IOPS per GB with upto 10,000 IOPS and the ability to burst up to 3000 IOPS for extended periods of time for volumes at 3334GiB and above. If in exam you get you want less than 10000 IOPS you want GP2.

- Provisioned IOPS SSD(IO1)

  - Designed for I/O intensive applications such as large relational or NoSQL databases or anything where you need extreme performance.
  - Used if you need more than 10,000 IOPS.
  - Can provision upto 20000 IOPS per volume.

- Throughput Optimized HDD (ST1)

  - Used for big data, data warehouses, log processing.
  - Cannot be a boot volume i.e. It has to be additional volume.

- Cold HDD (SC1)

  - Lowest Cost Storage for infrequent accessed workloads.
  - Used for file server.
  - Cannot be a boot volume.

- Magnetic (Standard)
  - Lowest cost per gigabytes of all EBS volume types that is bootable.
  - Idal for workload where data is accessed infrequently and applications where the lowest storage cost is important.

_Just think as in a disk in cloud which you can attach to the EC2 instance._

### EC2 Lab

In top right change region to closest to your.

In top left click on services and In compute select EC2.
Click Launch instance.
_Instances are create form amazon machine images_
Select **Amazon Linix AMI**
Select t2.micro (EC2 family instance type comes in).
configure as you like.
on shutdown stop and not terminate.
configure storage.
configure tags like name, department, etc.
Configure security group. (Imagine a virtual firewall)
Lauch and create a new keypair for ssh.( ssh is how we connect if we lose this we can't connect to instance).
Change the key.pem permission using `chmod 400 key.pem`
and we have our linux cloud server.
we can set an service to start on machine startup by using `chkconfig <service_name> on` where for a webserver the service would be apache or httpd

### How to use Putty and PuttyKeyGen (Only for windows)

- Douwnload putty and puttygen.
- Create a new AWS key pair (line 365).
- open putttygen.
- click load and open pem file.
  _Putty uses ppk format but we receive a pem format hence it would not be visible. To select pem file change the search criteria to all files._
- To use the key with putty you need to use the "Save private key" in putty. Click save private key and add keypharse for production.
- save it as .ppk file.
- In EC2 Management console open the instance and copy the public IP.
- In putty put hostname in format `username@IP` (default username could be ec2-user) and in the catefories select Connection -> SSH -> Auth.
- Click on browse and select the private key in ppk format.
- And click connect and we are connected.

To create this to web server run and install apache. If you dont see the html in browser after entering the pubic IP check whether the file exist in `/var/www/html` and if the security group in EC2 allows HTTP and HTTPS by adding a new rule.

### Elastic Load Balancer (ELB)

What is a load balancer?
A load balancer simply help us balance our load acroos multiple different servers. Eg. We have a multiple webserver we can balance the load by distributing it across each webserver so that one server is not overloaded. This prevent server crashing.
We have 3 type of load balancer.

1. Application Load Balancer
   Operate at level 7 of OSI.
   Can make clever desicion.
   They are intelligent and one can create advanced request routing, sending specific requests to specific web servers.
   Can see all the way up to application layer i.e. application-aware.
   Best suited for HTTP and HTTPS traffic.
   Used in web application and operate on request level.

2. Network Load Balancer
   Operate on level 4 of OSI
   Used for extreme performance.
   Gives super fast performance and super fast speed.
   Is amazon's most expensive load balancer but is what one would use in production especially if latency is a issue.
   Best suited for TCP traffic where extreme performance is required.
   Capable of handling millions of requests per second, while maintaining low latencies.
   Used in Ultra high performace and static IP for the application.

3. **Classic Load Balancer**
   Not recommended
   Only exist for legacy purposes.
   Developer associate exam test mostly on classic load balancers.
   Can load balance HTTP/HTTPS application and use layer 7 - specific features, like X-Forwarded and sticky sessions.
   One can also use strict layer 4 load balanceing for applications that rely purely on TCP.
   Also know as elastic load balancer.

Load Balancer Errors:

- Classic Load Balancers
  If the application stops responding, the ELB (Classic load balancer) responds with a 504 error i.e. tje application is having issues. It could be web server layer or the database layer. After identidying wehre the application is failing, we can scale it up or out. The error doesn't mean load balancer is having an issue it something below the load balancer is not getting response and that means we need to troubleshoot the layers. 504 is a gateway timeout error.

X-Forwarded or X-Forwared-For Header.
Imagine a client on public IP 102.13.5.192 would do a DNS request and hit out load balancer. The load balancer would take the request and it's private IP say 10.0.0.2 and send it to EC2 Instance. Now, EC2 instance only see the private IP of the load balancer and not the public IP of the client. This could cause issue because we want to know where in the world client is. To get the public IP we look into X-Forwared-For Header.

_ Exam tips _

- 3 type of load balancers
  - Application Load Balancer.
  - Network Load Balancer.
  - Classic Load Balancers.
- 504 Error means Gateway timeout error. Thsi meanss that the application is not responding within the idle timeout period.
  - Troubleshoot whether it is web server or databse server.
- If you need IPv4 address of end user / client, look for X-Forwareded-For header.

### Register Domain Name using route 53

What is it?
It is Amazon's DNS Service. It allows to map the domain names to EC2 Instances, Load Balancers, S3 Buckets.
Login to AWS Console goto Services and in network select Route 53.
In the left column select Register Domain and buy the domain.
Then Goto Dashboad and select hosted zones and we can see our domain in there.
Select `Goto record sets` and here we create DNS Records.
_We can create our `A record`, 'A record' is essentially like a phonebook but instead of name it takes domain name and instead of phone number it takes IP address._
To Create a new record click on `Create Record set`

| Type of records | Record Set                            |
| --------------- | ------------------------------------- |
| A               | IPv4                                  |
| CNAME           | Canonical Name                        |
| MX              | Mail Exchange                         |
| AAAA            | IPv6                                  |
| TXT             | Text                                  |
| PTR             | Pointer                               |
| SRV             | Service Locator                       |
| SPF             | Sender Policy Framework               |
| NAPTR           | Name Authority Pointer                |
| CAA             | Certification Authority Authorization |
| NS              | Name Server                           |

What is a naked domain name?
Instead of www.google.com we could use google.com . It is also called Zone apex record.

In order to create a naked domain, we have to use an alias. It is supoorted only for A (Ipv4) and AAAA(IPv6). We have multiple options for alias target in our case we will select ELB Application load balancer and put our EC2 Instance behind that load balancer and then come back to Record set to create a DNS name.

If you don't see the instance then check the zone selected in top right.

Goto Console -> Services -> EC2
In Left column go down to load balancer and click it. Then click on Create Load balancer.
We woud create application load balancer.
In Listener we decide which port to listen on and in Availbility zone select all to get maximum redundancy.
In Configure Security Settings. `not using secure listener` means we are not using `HTTPS`.
Assign a security group
In Configure Routing, we setup route requests to a target in target group.
After setting this up we go back to `route 53`.

Now in alais target in create record set we can see our load balancer.

### CLI DEMO LAB

Log into EC2 Instance using ssh and elevate to root (`sudo su`).

Whenever using command line start with AWS followed by service we want to use.
`aws s3 ls` command list everything in s3 buckets.
It may return `Unable to locate credentials. You can configure them by running "aws configure"`.
When we run `aws configure` it will ask us for access keyID and secret access key.
To create new user go to IAM(Identity Access Management). Select create user with access type programmatic access for access KEY ID and secret key.
**Secret access key can only be seen once when it is created so it is important to note it down somewhere. Access Key ID on other hand can be foud in users -> security configurations**
Note: AWS Management console access should only be given to user who are admin/sudo and should be able to make changes from this Management console.
To set the permission it is best if you could create a group for each type of user and instead of giving permission to users we define the permisions for the group.
**Only for this practise to go smoother we will give the user god mode by attaching Administrative Access policy to a group and add the user to it.**

To Create S3 Bucket From Console
`aws s3 mb s3://<Bucket_Name>`
here `aws s3` identify that the command is for s3 buckets, `mb` is like `mkdir` but creates buckets instead. `s3://<Bucket_Name>` is the path.
So we could use normal linux command as well like
`aws s3 ls s3://<Bucket_Name>` or `aws s3 cp file.txt s3://<Bucket_Name>`

Incase you forgot the secret key:
go to user -> security credentials and mark the status as inactive and then you would see a X mark for deletion. Now the user have no access key and no security key. So Generate new keys and store it safely.

[AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/index.html)

_Exam Tips_
**Least Priviledge** - Always give users the minimum amount of access required.
**Create Groups** - Always create groups and assign user to group. User will automatically inherit the permissions of the group. The groups permissios are assigned using policy documents.
**Secret Access Key** - You will see this only once. If you do not save it, you can delete the key pai (Access Key ID and Secret Access key) and regenerate it. You will new to run `aws configure` again.
**Do not use just one access key** - Do not use just one access key and share it with all the developers. If someone leaves the company on bad terms, then you will need to delete the key and create a new one and every developer would then need to update their keys. Instead create one key pair per developer.
If you upload these on git or inside your code consider the key as compromised and generate a new key.
**You can use the cli on your PC** - You can install CLI on your machine.

### EC2 With S3 Roles

'Goto IAM -> got to Users' and remove the keys.
Now goto Roles.
IAM roles are a a secure way to grant permission to entities that you trust.
i.e. you can create a role that allow your ec2 instance to talk to s3.
Click on 'create a role'
Select AWS Service and then select EC2 which is the most common role.
then click 'next:Permission' since we want to follow least privledge we will not give it admin access but instead AmazonS3FullAccess.

_Should know how to read JSON policies_

then click next and five the role a name and description.
Now that its done go to EC2 instance (Management Console -> services->EC2)
go to action -> instance settings -> attach/replace IAM role and click apply.

_Exam tips_

- Roles allow you to not use keys.
- Roles are referred from a security perspective
- Roles are controlled by policies.
- You can change a policy on a role and it will take immediate affect.
- You can attach and detach roles to running EC2 instances without having to stop or terminate the instances.
- Between access keys and roles always choose roles.
- Roles are controlled by Policy which is json and has key value pair.

### How to encrypt an EBS Volume attached to EC2

We are gonna create a new volume so we goto services -> EC2 -> In left column select volumes under ELASTIC BLOCK STORAGE -> Click Create volume.
YOu should create the volume in the same availablity zone as that of the instance. and create new volume.

**Volumes created from encrypted snapshot are encrypted automatically and vice versa**

To attach this volume to instance click on actions -> attach volumes -> select the instance and add.
If you cant see the instance that means the volume is created in another availability zone.

Now that the volume is added we want the instance to know about this. So we ssh into the instance and run `lsblk` to see available volumes.
Before mounting we need to check if the volume has a file system if not we need to put a file system on this volume. To check if volume has a file system already we run the command `file -s /dev/<name_of_volume_from_lsblk>`. If you see just data that means no data on this volume and we are safe to create a file system on there. To create the file system we run command `mkfs -t ext4 /dev/<name_of_volume_from_lsblk>`. mkfs stands for make file system `-t ext4` specify the type of file system be ext4 and the block of dev we want to create in.

Now the volume has a file system we can mount it by running the command `mount /dev/<name_of_volume_from_lsblk> <path_to_mount>`. The path to mount could be directory in home or in /mnt but it needs to be a directory.
To unmount we run command `umount -d /dev/<name_of_volume_from_lsblk>`

To Create a snapshot:
unmount the volume and in aws console detach the volume. then go to action and then create snapshot. In the left column select snapshot and create volume from that snapshot.
and the volume is created now attach the vloume to instance again. Now we can mount this volume from the terminal.

To Encrypt the root volume:
Create a snapshot of the root volume. Go to action and select copy snapshot and then select encrypt this snapshot.
Then create a image from the snapshot

_EXAM TIPS_

- You can encrypt the root device volume using OS level encryption.
- You can encrypt the root device volume using snapshots.
- You can encrypt additional attached volumes using the console.

### RDS 101 (Relational database service)

What is a relational database?
Relational database are what most of us are all used to.
It has databases, tables, rows, feilds (Columns).

Types of RDS provided by amazon are

- SQL Server
- Oracle
- MySQL Server
- Postgre SQL
- Amazon Aurora
- MariaDB

What is non-relational databases?
Is a database consisting of collection(table), Document(row), key value pairs(feilds).

What is data ware housing?
Used for buisness intelligence. Used to pull in very large and complex data sets. Usually used by management to do queries on data.

OLTP vs OLAP
Online Transaction Processing (OLTP) differs from OLAP Online Analytics Processing (OLAP) in terms of the types of queries you will run.
OLTP is simple and OLAP is complex.

What is Elasticache?

ElastiCache is a web service that makes it easy to deploy, operate and scale an in-memory cache in the cloud. The service improves the performace of web applications by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slower disk-based databases.

ElastiCache supports two open-source in-memory caching engines:

- memcached
- redis
  Used to create cache of database to reduce the load on database.

_Summary_

- RDS - OLTP
  - SQL
  - MySQL
  - PostgreSQL
  - Oracle
- DynamoDB - NoSQL
- RedShift - OLAP
- Elasticache - In Memory Caching:
  - Memcached
  - Redis

### RDS LAB

In services under databases select RDS then select the engine like MySQL. DB instance identifier is the name of our RDS instance inside AWS. In credentials settings define master username, master password and confirm password. Then we decide DB instance size to burstable classes to db.t2.micro (Cheapest). Create a new Security group. In Additional configuration change the initial database name to one we like.

Create a new EC2 Instance with default and in advanced details we run a boot script. It is a script with shebang(#!) which runs commands as root in cronological order.
(It is provided in the attachment of 3.10 RDS LAB)

Sign into EC2 instance locate connect.php in /var/www/html and change you hostname. To get the hostname goto services->RDS->Instances->yourdatabase->scroll down to endpoint and copy the endpoint address.
The Instance would not be able to connect because it is in different security group than the RDS. And communication betweeb the two is not allowed yet.

To allow communication between two security group:
GO to Security Groups, select RDS Security group and in inboud press edit. Then add a rule of type MYSQL, source custom and instead of IP enter ethe groupID of web server group.

_AMAZON AURORA IS NOT FREE TIER_
_EXAM TIP_
You've got an EC2 instance in one security group, and RDS in another security group and it's not coonecting thats because you need to open port 3306 to the security group RDS instance is in to security group my EC2 instance is in.

### RDS - BackUps, Multi-AZ and Read Replicas

Two type of Backups:

- Automated Backup
  Allows to recover the database to any point in time within a "retention period". The retention period can be between 1 to 35 days. It will take full daily snapshot and stroe transaction logs throughtout the day. When you do a recovery, AWS will choose the most recent daily backup, and then apply transaction logs relevant to that day. It is enabled by default. The backup data is stored in S3 and you get free storage space equal to the size of database. so if ou have an RDS of 10GB you will get 10GB worth of storage. Backups are taken within a defined window. Backups are taken within a defined window. During the backup window, storage I/O may be suspended while your data is being backed up and you may experience elevated latency.

- Database Snapshot
  DB Snapshots are done manually (i.e. they are user initiated.) They are stored even after you delete the original RDS instance, unlike automated backups.

  _If you delete an RDS then automated backups are also deleted while snapshots are kept_

Restoring Backup
Whenever you restore either an automatic backup or a manual snap shot, the restored version of the database will be a new RDS instance with a new DNS endpoint.

Encryption
Encryption is supported for all DB and is done using AWS key management service. Once the RDS Instance is encrypted, the data stored at rest in the storage is encrypted as are the automated backup, read replicas, and snapshots.

What is a Multi A-Z?
If our database is in US-EAST-1A and some changes are made then it would also be sync on US-EAST-1B. This is done for disaster recovery i.e. if US-EAST-1A is not avaialable then we can use US-EAST-1B
It allows to have an exact copy of your production database in another availability zone. AWS handles the replication for us, so when production database is written to, this write will automatically be sncy to the stand by database. In the event of planned database maintenace DB instance failure or an availability Zone faiulure, Amazon RDS will automatically failover to the stand by so that database operation can resume quickly without admin intervention,
Note :
It is not primarily used for improving performance. For performance improvement, you need Read Replicas.
Available for SQL Server, Oracle, MySQL Server, PostgreSQL, MariaDB.

What is Read Replica?
When we write to a RDS database it is pushed to other copies of database. You can have 5 read replicas per production by default. Used to balance load from a single database. It allow you to have a read-only copy of production database. This is achieved by using Async replication from primary RDS instance to the read replica. You use read replicas primary for ver read-heavy database workloads.
Not available for SQL Server or Oracle.
Used for :

- scaling, not for Disaster recovery.
- Must have automatic backups turned on in order to deploy a read replica.
- You can have upto 5 read replica copies of any database.
- You can have read replicas that have multi-AZ.
- You can create read replicas of multi-AZ source databases.
- Each read replicas will have its own DNS end point.
- Read replicas can be promoted to be their own databases. This breaks the replication. This should be done if you have a analysis task which can create a load on database we promote read replica to database and analyze it rather than production database.
- Read replica can exist in another region.

### Elasticache 101

Elasticache is a web service that makes it easy to deploy, opertate and scake an in-memory cache in the cloud. The service improves the performance of web application by allowing us to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slower disk-based databases.
Amazon elasticache can be used to significantly improve latency and throughput for many read-heavy application workloads or conpute intensive workloads. Caching improves application performance by storing critical pieces of data in memory for low-latency access. Cached information may include the results of I/O intensive database queries or the results of computationally-intensive calculations.
The more we cache the less load on database.

Type of memcached:

- Memcached: A widely adopted memory object caching system. ElastiCache is protocol compliant with Memcached, so popular tools that you use today existing Memcached environments will work seamlessly with the service.

- Redis: A popular open-source in-memory key-value store that supports data structures such as sorted serts and lists. ElastiCache supports Master/Slave replication and multi-AZ which can be used to achieve cross AZ redundancy.

Redis is used if we want multi-AZ access or redundancy other wise memcached is used.
Although both memcached and redis appear similar on the surface, they are actually quite different in practice. Because of the replication and persistence features of redis. ElastiCache manages redis more as a relational database. Redis ElastiCache clusters are managed as stateful entities that include failover similar to how amazon RDS manages database failover.
Use cases:

- Are you looking for more advanced data types, such as lists, hashes, and sets? If so use redis.
- Does sorting and ranking datasets in memory help you, such as with leaderboards? If so, use redis.
- Is persistence of your key store important? If so, use Redis.
- Do you want to run in multiple AWS availability zone (Multi-AZ) with fail over? If so use redis.

Memcached
Becaused Memcached is designed as a pure caching solution with no persistence, elastiCache manages memcached nodes as a pools that acan grow and shrink similar ro an amazon EC2 AutoScaling Group. Individual nodes are expendable and ElastiCache provides additional capabilities here, such as automatic node replacement and auto discovery.
Use cases:

- Is object caching your primary goal, eg:offload the database? if so use Memcached.
- Are you intrested in as simple a caching model as possible? If so, use memcached.
- Are you planning on running large cache nodes and require multi threaded performance with utilization of multiple cores? If so, use memcached.
- Do you want the ability to scale your cache horizontally as you grow? If so, use memcached.

_Exam Tips_
Typically, you will be given a scenario where a particular database is under a lot of stree/load. You may be asked which service should use to alleviate this.
Elasticache is a good choice if your database is particularly read-heavy and not prone to frequent changing.
Redshift is a good answer if the reason your database is feeling stress is beacause management keep running OLAP transaction on it etc.

## Chapter 4: S3

## S3 101

What is S3?
S3 stands for simple storage service. S3 provides developers and IT teams with secure, durable, highly-scalable object storage storage i.e. it is a ibject storage it is really for files, images, webpages etc and not for OS and databases. It is easy to use, with a simple web service interface to store and retrieve any amount of data from anywhere on the web. The data is spread across multiple devices and facilities. A faulty S3 service should not lose the data and we could still access our files.

S3 - Basics

- S3 is Object based i.e. allows for file upload.
- File can be from from 0 bytes to 5 TB.
- THere is unlimited storage.i.e. we dont have to predict the space or allocating the space we need in S3. It grows dynamically.
- Files are stored in buckets. Buckets are similar to folder. It is the name AWS uses for the location where we are storing the file and name of bucket is user defined.
- S3 is a universal namespace. That is, buckets names must be unique globally similar to DNS or internet address.
- The url of s3 is divided into parts such as `<protocal>://s3-<region>.amazonaws.com/<bucket_name>` eg:`https://s3-eu-west-1.amazonaws.com/acloudguru`.
- When upload is successfull we will get the response of HTTP 200 Code.

Data consistency Model for S3

- Read after write consistency for PUTS of new object - Once the file is uploaded it is available for reading Immediately.
- Eventual Consistency for overwrite PUTS and DELETES - If we want to modify an file or delete a file it will take some time to propogate.

S3 Is a key-value store

- S3 is object based consisting of key value pairs where key is the name of the object/file and value is the data in bytes.It also hase version ID which helps mainting multiple version of same file like git and allows rollback in pervious data. We can add our own custom meta data. We also have sub resources which is bucket-specific configuration like bucket policy and access control list. CORS (Cross Origin Resource Sharing) allows file from one bucket be available to other bucket. Transfer acceleration is a service allows to maximise the speed when uploading multiple files into S3.

- Built for 99.99% availability for S3 i.e. uptime.
- Amazon gurantees 99.(11\*9s) durability for s3 information. Durability is amount of data you can expect to loose over a given year.
- Different tier are available to store different type of data.
- Lifecycle management: Allows to set rules around moving the data between different storage tiers.
- Versioning
- Encryption : multiple ways to encryt the data.
- Secure data using access control lists and bucket policies.

S3 - Storage Tier/Classes

- S3: 99.9% availability, 99.9999999999% durability, stored redundantly acreoss multiple device in multiple facilities, and is designed to sustain the loss of 2 facilities concurrently. i.e. S3 can handle hardware failure, device failure but mot only in one location but multiple locations.
- S3 - IA(Infrecuently accessed): For data that is access less frequently like once a year or once a quarter, but requires rapid access when needed. Lower fees than s3, but you are charged a retrival fee.
- S3 - One Zone IA ; Same as IA but is stored only in single availability zone only, with same durability but only 99.5% availability. Cost is 20% less than regular S3 - IA.i.e. you would lose access for data if the availability zone if offline and will get back once it comes back online.
- Reduced Redundancy Storage : Design with 99.99% durability and availability of object for a given year. Used for data that can be recreated if lost. Eg: We stores thumbnails here while the original are stored in more durable storeage.
- Glacier : Very Cheap, but used for archival only. Optimised for data that is infrequently accessed and it takes 3-5 hours to restore from glacier. So we dont want to put out data in here which we would be accessing on frequent basis.
- Intelligent Tiering: used for unknown or unpredictable access patterns. It has 2 tiers - Frequent and infrequent access. It automatically moves the data to most cost-effective tier based on how frequently you access each objects. If a data is not access in 30 days it moves to infrequent access but once it is accessed it moves to frequent access. Same availability as S3 - IA. No fees for accessing your data but a monthly fee for monitoring / automation.

S3 - Charges

- Charged For
  - Storage per GB
  - Requests (Get, Put, Copy, etc.)
  - Storage Management Pricing
    - Inventory, Analytics, and Object Tags
  - Data Management Pricing
    - Data transferred out of S3
  - Transefer Accelleration - Uses cloud front to optimize transfers.
    We can tag objects with department or clients if we want to charge the department or team for that project. We can transfer data into s3 for free of cost but they do charge for when we transfer data out.

### S3 Security

- By default, all newly created buckets are PRIVATE.
- Only the creator can read and modify the data and there is no public access by default.
  - We can allow set of users or group to access a S3 bucket by using bucket policies. And it is applied at bucket level so it is applied to all objects in the bucket. We have generator to create the bucket policies.
  - Access control list applied on object level. we can define the accounts or groups who can access the object. also the type of access like read, write or full controll.
- S3 buckets can be configured to create access logs, which logs all requests made to S3 buckets. These logs could be written to another bucket.

### S3 ACLs & Policies

From services select s3 and create a new s3 bucket.
By deafult all files added to buckets is private and only visible to the owner, to make it public you can uncheck the box in permission and grant public read access to the file from permissions tab.
You can not add a public file to a private bucket it would contradict the policies. To change the bucket policy open the bucket and select permissions an uncheck the permissions blocking the public ACLs.
To view the file we have two ways:

- Click the file and select open.
  When you open it the console uses the AWS credential to check if you are the owner hence allowing private file to be viewd as well.
- Click the file and select the link.
  While the link opens in browser it is treated as public (anonymous) access and you cant use link if the file is private ACLs.

To create a bucket policy open the bucket and click bucket policy and it gives a editor where you can write JSON policies. It also provides a policy generator.

### S3 Encryption

There are 2 type of encryption:

- In Transit
  - SSl/TLS
- At Rest
  - Server Side Encryption
    - S3 Managed Keys - SSE-S3
      Each object is encrypted using its own unique key using strong multi-factor encryption. They also encrypt the key with a master key which they regularly rotate for us. It is AES-256 bit encryption.
    - AWS Key Management Service, Mangaed keys, SSE-KMS
      KMS (Key management service) is similar but comes with some additional benefits:
      - We get permission for use of addditional key called envelope key which encrypt the key we use to encrypt data.
      - We get audit trail i.e.record the use of encryption key so we can see when the key has been used, who used it and why.
    - Server Side Encryption with Customer Provided Keys - SSE-C
      - We manage our own key
      - AWS manages encryption and decryption.
  - Client Side Encryption
    - We encrypt the file itself before uploading and we choose our own encryption methaodology.

Enforcing Encryption on S3 Buckets

- Every time a file is uploaded to S3, a PUT request is initiated.
- Expect: 100 - continnue in the PUT request states the do not send request body until receive acknowledgement. This means S3 can reject your request based on the content of our header.
- If the file is to be encrypted at upload time, the `x-amz-server-side-encryption` parameter will be included in the request header. There are two options currently available:
  - `x-amz-server-side-encryption: AES256` for S3 Managed keys
  - `x-amz-server-side-encryption: ams:kms` for KMS managed keys
- When this parameter is included in the header it tells S3 to encrypt the object at the upload time using specific encryption method.
- We can enforce a bucket policy which can denies any S3 PUT request which does not include `x-amz-server-side-encryption` parameter in header.
  To do this open bucket and select policy generator. Add a statement with:
  - effect : deny
  - principal : \* (Principal means user where \* means everyone)
  - AWS Service : S3
  - Action : put objects
  - Amazon Resource Name found in S3 bucket permission.
  - add conditions:
    - condition : String not equals
    - Key : s3:x-amz-server-side-encrtpyion
    - value : aws:kms

Note: It sometimes gives error that Action does not apply to any resources(s) in statement.
This is because some services does not let us specify specific actions for individual resources. This however can be solved by adding a wildcard(/\*) to Amazon Resource Name(ARN).

### CORS Configuration Lab

Allows to acces file in one S3 bucket to see another file in another S3 bucket.
for eg we want the bucket b2 to be accessible in b1
To setup CORS open the bucket b2 goto permission and slect CORS Configuration. In Allowed Origin replace \* with the b1 bucket adddess (would look like "http://b1.s3-website.eu-centeral-1.amazonaws.com")

### CloudFront

What is CDN?
CDN stands for Content Delivery Network is a system of distributed servers that delivers webpages and other web content to a user based on the geogtaphical locations of the user, the origin of web page and content delivery server.
Cloud front is focused on content delivery i.e. more efficient reads and downloads where as transfer acceleration is all about enabling faster uploads into S3.
Imagine you are hosting a webpage and the user is distributed on the other side of the world then the latency would differ for each user and would be worst for the farest user. To avoid this AWS introduces concept called edge locations. An edge location is a collection of servers which are in geographically dispersed data centers and are used by cloud front to keep a cache of our objects and instead of a user requesting content from server it would request it from the closest edge location. The edge location then downloads the file from server and cache it so that next time any user request the file they can access it from edge location this provides a faster response time. After time to live is up the cache is automatically cleared from cache.

Cloud front key Terminology:

- Edge location : This is the location where content is cachced and can also be written. Separate to an AWS Region/AZ.
- Origin: This is the origin of all the files that the CDN will distribute. Origins can be an S3 bucket, an EC2 Instance, an Elastic Load Balancer, or Route53.
- Distribution: This is the name given the CDN, which consists of a collection of Edge locations.
- Web Distribution - Typically used for websites. You cannot share adobe flash multimedia content as it is a media file and so must use RTMP, In web sistribution origin can be S3 or HTTP/HTTPS server .
- RTMP(Real time messaging protocol) - used for media streaming.

What is cloudfront?
Amazon cloud front can be used to deliver entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations. Requests for out content are automatically routed to the nearest edge location, so content is delivered with the best possible performance.

Amazon S3 Transfer Accelration enables fast, easy, and secure transfer of files over long distances between your end users and an S3 bucket. Transfer acceleration takes advantage of amazon cloud front's globally distributed edge location. As the data arrives ar an edge location, data is routed to amazon S3 over optimized network path.

_EXAM TIPS_

- Edge locations - This is the location where content will be cached. This is separate to AWS Region/AZ
- Origin - This is the origin of all the files that the CDN will distribute. Origins can be an S3 bucket, an EC2 Instance, an Elastic Load Balancer, or route 53.
- Distribution - THis is the name given to the CDN, which consist of a collection of Edge locations.
  - Web Distribution
  - RTMP
- Edge location are not just READ only - we can WRITE to them too.
- CloudFront Edge Locations areutilised by S3 Transfer Acceleration to reduce latenct for S3 uploads.
- Objects are cached for the life of the TTL( Time To Live ).
- We can clear cached objects, but you will be charged.

### Cloud front lab

Restrict Bucket access :

- yes : all request for bucket must come from cloud front only. (Recommended)
- No : Public access is allowed.

Origin Access Identity : Is a special cloud front user given permission to access S3 buckets. Select Create a new Identity for it.
Grant Read Permission on bucket: We need to select yes to automatically update permission or it will not work and you have to manually update permissions..
In Viewer protocol policy, Select redirect HTTP to HTTPS so that any http request is changed to HTTPS

Allow HTTP Method : user can upload data to cloud front and amazon manages the file transfer from cloud front to bucket. Hence, POST,PUT,DELETE are possible.

**Restrict Viewer Access :**
**We can choose wether cloud front require users to access the content using a signed URL or a signed cookie. This is useful for paid to view content.**

Go to Distribution to see the cloudfront distribution and click on ID to view details. The domain name appears in the general tab in here and this domain name is used to access the cloud front distribution.
In restriction we can blacklist and whitelist specific country for the users.

How to access using cloud front?
Remove the read permission for the file from the s3 bucket(select group everyone and deny read permission).

### S3 Performance Optimization

S3 supports very high request rates. However if S3 buckets are routinely receiveing > 100 PUT/LIST/DELETE or > 300 GET requests per second, then there are some best practice guidelines that will help optimize S3 performance.
The guidance is based on the type of workload you are running:

- GET-Intensive Workloads - use CloudFront content delivery service to get best performance. CloudFront will cache our most frequent accessed objects and will reduce latency for your GET requests.
- Mixed Request Type workloads - A mix of GET, PUT, DELETE - the keynames you use for your objects can impact performance for intensive workloads.
- S3 uses the key name to determine which partiotion an object will be stored in.
- The use of sequential key names e.g. names prefiexed with a time stamp or alphabetical sequence increases the likelihood of having multiple objects stored on the same partition.
- FOr heavy workloads this can cause I/O issues and contention.
- By using a random prefix to key names we can force S3 to distribute kets across multiple partitions, distributing the I/O workload.

_EXAM TIPS_

1. Amazon S3 now provides increased performance to support at least 3,500 requests per second to add data and 5,500 requests per second to retrieve data. This negates the previous optimisation guidance for randomising your object key names to increase throughput
2. What is the largest size file you can transfer to S3 using a PUT operation? 5GB
3. Which of the following options allows users to have secure access to private files located in S3?
   There are three options in the question which can be used to secure access to files stored in S3 and therefore can be considered correct. Signed URLs and Signed Cookies are different ways to ensure that users attempting access to files in an S3 bucket can be authorised. One method generates URLs and the other generates special cookies but they both require the creation of an application and policy to generate and control these items. An Origin Access Identity on the other hand, is a virtual user identity that is used to give the CloudFront distribution permission to fetch a private object from an S3 bucket. Public S3 buckets should never be used unless you are using the bucket to host a public website and therefore this is an incorrect option.
4. The minimum file size allowed on S3 is 1 byte.
   FALSE
5. You are using S3 in AP-Northeast to host a static website in a bucket called "acloudguru". What would the new URL endpoint be?
   http://acloudguru.s3-website-ap-northeast-1.amazonaws.com
6. You are hosting a static website in an S3 bucket that uses Javascript to reference assets in another S3 bucket. For some reason, these assets are not displaying when users browse to the site. What could be the problem?
   You haven't enabled Cross-origin Resource Sharing (CORS) on the bucket where the assets are stored.

## Chapter 5 : Introduction to Serverless Computing

### Lambda

What is lambda?
AWS Lambda is a compute service where you can upload code and create a Lambda function. AWS Lambda takes care of provisioning and managing the servers that we use to run the code. You don't have to worry about OS, patching, scaling, etc. We can use Lambda in the following ways.

- As an event-driven compute service where AWS Lambda runs our code in response to events. These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table. These events are called triggers.
- As a compute service to run our code in response to HTTP requests using Amazon API gateway or API calls made using AWS SDKs.

What language are asupported by Lambda?

- Node.js
- Java
- Python
- C#
- Go

How is Lambda Priced?

- Number of requests
  - First 1 million requests are free. \$0.20 per million requests thereafter.
- Duration
  - Duration is calculated from the time our code begins executing untils it returns or otherwise terminates, rounded up to the nearest 100ms. The price depends on amount of memory we allocate to our function. We are chared \$0.00001667 for every GB-second used.

Why is lambda cool?

- We don't have to manage any servers, don't need any system administrator, network administrator, database administrator.
- It scales automatically, we don't have to manually scale it.
- It is cheap

_EXAM TIPS_

- Lambda scales out (not up) automatically. i.e. we can have multiple function in parallel at same time but if we wun out of memory we need to update the amount of memory.
- Lambda function are independent, 1 event = 1 function
- Lambda is serverless.
- Lambda is a compute service
- What services are serverless
  - Lambda
  - API Gateway
  - S3
  - DynamoDB
  - RDS and EC2 is not serverless
- Lambda functions can trigger other lambda functions, 1 event can = x function if functions trigger other functions.
- Architecture can get extremelt complicated, AWS X-ray allows us to debug whats happening.
- **AWS X-ray is used to debug lambda**
- Lambda can do things globally, you can use it to backup S3 buckets to other S3 buckets etc.
- Know Lambda triggers

### API Gateway

An API is an application programming interface.

Type of APIs

- REST (REpresentational State Transfer)
  - Typically uses JSON
- SOAP (Simple Object Access Protocol)
  - Uses XML

What is API Gateway?
Amazon API Gateway is a fully managed service that makes it easy for developers to publish, maintain, monitor, and secure APIs at any scale. With a few clicks in the AWS Management Console, We can create an API that acts as a "front door" for application to access data, buisness logic, or functionality from our back-end services, such as applications running on Amazon Elastic Compute Cloud, code running on AWS Lambda, or any web application.

What can API Gateways do?

- Expose HTTPS endpoints to define a RESTful API.
- Allows serverless-ly connect to service like Lambda & DynamoDB.
- Runs efficiently with low cost.
- Scale effortlessly.
- We can track and control usage by API key.
- Throttle request to pervent attacks.
- Connect to cloud watch to log all requests for monitoring.
- Maintain multiple versions of our API.

How to configure an API?

- Define an API (container)
- Define Resourses and nested Resources.(URL PATHS)
- For each resource :
  - we can select supported HTTP methods.
  - Set security
  - Choose targert (such as EC2, Lambda, DynamoDB, etc.)
  - Set request and response transformations.
- Deploy API to a stage like production, development etc.
  - Uses API Gateway domain, by default.
  - Can use custom domain.
  - Now supports AWS Certificate Manage: free SSL/TLS certificates.

What is API Caching?
You can enable API caching in Amazon API Gateway to cahce our endpoint's response. With caching, we can reduce the number of calls made to our endpoint and also improve the latency of the requests to our API. When we enable caching for a stage, API Gateway caches responses from our endpoint for a specified time-to-live (TTL) period, in seconds. API Gateway then responds to the request by looking up the endpoint response from the cache instead of maing a request to your endpoint.

Same Origin Policy
In computing, the same-origin policy is an important concept in the web application security model. Under the policy, a web browser permits scripts contained in a first web page to access data in a second webpage but only if both web pages have the same origin. This is done to prenvent Cross-site Scripting (XSS) attacks.

- Enforced by Web browser.
- Ignored by tools like Postman and CURL

Cross-Origin Resource Sharing (CORS)
Cross-Origin Resource Sharing (CORS) is one way the server at the other end (not the client code in the browser) can relax the same-origin policy.
Cross-Origin resource sharing is a mechanism that allows restricted resources on a web page to be requested from another domain outside the doamin form which the first resource was served.

_Exam Tips_

- API Gateway has caching capabilities to increase performance.
- API Gateway is low cost and scales automatically.
- We can throttle API Gateway to prevent attacks.
- We can log results in CloudWatch.
- If we are using multiple domains with API Gateway, ensure that we have CORS on API Gateway.
- CORS is enforced by client.

### Build a simple serverless website with route 53, API Gateway, Lambda, and S3

S3 static web bucket name must me same as domain name.

How to create a lambda service ?
Goto compute -> Lambda -> create a lambda function -> Create role -> Set policy template to "Simple Microservice permissions" (It allows lambda to execute) -> Click on create function
Now we need to add our function code here. The cloud IDE provided is called `cloud9`. So we can write our lambda code directly in here. Below is the code we are using:

```python
def lambda_handle(event,context):
  print("In Lambda handler")
  resp = {
    "statusCode":200,
    "headers":{
      "Access-Control-Allow-Origin":"*",
    },
    "body":"Name"
  }
  return resp
```

Save the function and add the triggers.

Trigger we want to add is `API Gateway`.
Configure the trigger -> Create new API -> give out API name -> set name of API deployment stage -> Select security. -> save everything.
Security has options

- AWS IAM : only IAM user can call it.
- Open : Any one can use it
- Open with access key : open but will have to supply access key with it.

Now that the API Gateway is added click on details.
Invoke URL is our API endpoint but it is not configured yet. Click on the API Name and it should open out API gateway.
To configure the API:

- Click on Actions and select the HTTP method.
- Set the integration type to lambda function.
- Allow the "USe Lambda Proxy Integration"
- Lambda Region to the region where we have created the lambda function
- In Lambda function only function exsiting in that region would be shown.

To deploy:

- Click on Actions and select deploy API
- Select deploymnet stage from drop down
- Give a meaning full description.
- Click Deploy

Try to memorize lambda triggers from here.
Triggers are :

- API Gateway
- AWS IoT
- Alexa Skills Kit
- Alexa Smart Home
- CloudFront
- CloudWatch Events
- CloudWatch Logs
- CodeCommit
- Cognitio Sync Trigger
- DynamoDB
- Kinesis
- S3
- SNS

### Version Control in lambda

When we use versioning in AWS Lambda, we can publish one or more version of our Lambda function. As a result, we can work with different variation of your lambda function in our development workflow such as development beta and production. Each lambda function version has a unique amazon resource name (ARN). After we publish a version, it is immutable. AWS Lambda maintains our latest function code in the $LATEST version. When you update your function code, AWS Lambda replaces the code in the $LATEST version of the lambda function.
WE can refer to this function using its amazon resource name. Two type of ARNs associated with this initial version:

- Qualified ARN - The function ARN with the version suffix.
  eg: arn:aws:lambda:aws-region:acct-id:function:name:\$LATEST
- Unqualified ARN - The function ARN without the version suffix.
  eg: arn:aws:lambda:aws-region:acct-id:function:helloworld

Alias
After inititaly createing a Lambda function, we can publish a version 1 of it. By creating an alias name PROD that points to version 1, we can now use the PROD alias to invoke version 1 of the lambda function. When we publish an improved version we can promote version 2 to production by remapping the PROD alias so that it points version 2. If we find anything wrong we can eaisly roll back the production version to version 1 by remapping the PROD alias so that it points to version 1.

_EXAM TIPS_

- Can have multiple versions of lambda functions
- Latest version will use \$latest.
- Qualified version will use \$latest, unqualified will not have it.
- Versions are immutable (Cannot be changed).
- Can split traffic using aliases to different versions
  - Cannot split traffic with \$latest, instead create an alias to latest.

### Step Functions

Step Functions allows you to visualize and test our serverless applications. Step Functions provides a graphical console to arrange and visualize the components of your application as a series of steps. This makes it simple to build and run multi step applications. Step Functions automatically triggers and tracks each step, and tetries when there are errors, so your application executes in order and as expected. Step Functions logs the state of each step, so when things do go wrong, you can diagnose and debug problems quickly.

### X -RAY

What is X-Ray?
AWS X-Ray is a service that collects data about requests that our application serves and provides tools and we can use to view filter and gain insights into that data to identify issues and opprtunites for optimization. For any traced request to our application, we can see detailed information not only about the request and response, but also about calls that out application makes to downstrean AWS resources, microservices, databases and HTTP web APIs.

X-Ray SDK
The X-Ray SDK provides:

- Interceptor to add to our code to trace incoming HTTP requests.
- Client handlers to instrument AWS SDK clients that your application uses ti call other AWS services.
- An HTTP client to use to instrument calls to other internal and external HTTP web services.

X-Ray Integration
The X-Ray Integrates with the following AWS services:

- Elastic Load Balancing
- AWS Lambda
- Amazon API Gateway
- Amzon Elastic Compute Cloud
- AWS Elastic Beanstalk

X-Ray supported languages(Same As Lambda):

- Java
- Go
- Node.js
- Python
- Ruby
- .net

### Advance API Gateway

Import APIs
We can use the API Gateway Import API feature to import an API from an external definition file into API Gateway. Currently, the import API feature supports Swagger v2.0 definition files. With the import API, you can either create a new API by submitting a POST request that includes a Swagger definition in the payload and endpoint configuration, or you can update an existing API by using a PUT request that contains a Swagger definition in the payload. You can update an API by overwriting it with a new definition, or merge a definition with an existing API. You specify the options using a mode query parameter in the request URL.

API Throttling
By default, API Gateway limits the steady-state request rate to 10,000 requests per second (rps). The maximum concurrent requests is 5000 request across all APIs within an AWS account. If you go over 10,000 requests per second or 5000 concurrent requests you will receive a 429 Too Many Request error response.

_EXAM TIPs_

1. You have created a serverless application which converts text into speech using a combination of S3, API Gateway, Lambda, Polly, DynamoDB and SNS. Your users complain that only some text is being converted, whereas longer amounts of text do not get converted. What could be the cause of this problem? - Your Lambda function needs a longer execution time. You should check how long is needed in the fringe cases and increase the timeout inside the function to slightly longer than that.
2. Which of the following services does X-Ray integrate with?

- API Gateway&#10004;
- Elastic Load Balancer&#10004;
- Lambda&#10004;
- S3

3. How does API Gateway deal with legacy SOAP applications ?
   SOAP applications send their responses in XML format. API Gateway supports SOAP applications but only provides pass-through. API gateway does not transform or convert the responses.

## DynamoDB

### Introduction to dynamoDB

What is DynamoDB?
Amazon DynamoDB is a fast and flexible NoSWL database service for all applications that need consistent, single-dgit millisecond latency at anu scale. It is afully managed database and supports both document and key-value data model. Its flexible data model and reliable performance make it a great fit for mobile, web, gaming, ad-tech, IoT, and many other applications. It is also serverless, fully managed and configured to auto scale. Integrates well with lambda and is developers choice for serviceless app.
DynaomoDB is store on SSD storage giveing fast read and write. Hardware is spread across 3 geographically distinct data centers to avoid single point of failure.
Threre are 2 consistency models for read operations:

- Eventual Consistency Reads(Default)
  - Consistency across all copies of data is usally reached within a second. Repeating a read after a short time should return the updated data. ( Best read performance )
- Strongly Consistent Reads
  - A stronglt consistent read returns a result that reflects all writes that received a successful response prior to the read.

DynamoDB is made of:

- Tables
- Items (row)
- Attibutes (column)
- Supports key-value and document data structures
- Key = name of data, value = data itself
- Documents can be written in JSON, HTML or XML

How to query in DynamoDB?
DynamoDB - Primary Keys

- DynamoDB stores and retrieves data based on a primary key.
- 2 types of primary key are:
  - Partition Key
    - Unique attribute eg. userID
    - Value of the partition key is input to an internal hash function which determines the partition or physical location on which the data is stored.
    - If we want to use the primary key as our primary key, then no two items can have the same Partition key.
  - Composite Key (Partion key + Sort key)
    - eg.Same user posting multiple time to a forum
    - primary key would be a composite key consisting of :
      - Primary Key - User ID
      - Sort key - Timestamp of the post
    - 2 items may have the same partition key, but they must have a different sort key.
    - All items with the same partition key are stored together, then sorted according to the sort key value.
    - Allows you to store multiple items with the same partition key.

DynamoDB Access Control

- Authentication and Access Control is managed using AWS IAM.
- You can create an IAM user withing your AWS account which has a specific permissions to access and create DynamoDB tables.
- You can create an IAM role which enables you to obtain temporary access keys which can be used to access DynamoDB.
- You can also use a special IAM Condition to restrict user access to only their own records.

DynamoDB - IAM Conditions Example

- Imagine using a mobile gaming applications with millions of users.
- Users need to access the high scores for each game they are playing.
- Access must be restricted to ensure they cannot view anyone else's data.
- This can be done by adding a condition to an IAM Policy to allow access only to items where the Partition Key value matches their User ID.

_Exam Tips_

- Amzon DynamoDB is a low latency NoSQL database.
- Consistes of tables items and attributes.
- Supports both document and key-value data models.
- Supported document formats are JSON, HTML, XML
- 2 types of Primary key - Partition Key and Combination of Partition Key + Sort Key (Composite Key).
- 2 Consistent Models are - Stronglt Consistent and evetually consistent.
- Access is controlled using IAM policies
- Fine grained access control using IAM condition paramerter `dynamodb:LeadingKeys` to allow users to access only the item where the partition key value matches their userID.

### Indexes Deepdive

What is an index?
In SQL database, an index is a data structure which allows you to perform fast queries on specific columns in a table. You select the columns thtat you want to include in the index and run our serches on the index - rathre than on entire dataset. In dynamoDB, 2 types of index aresupported to help speed-up our dynamoDB queries:

- Local Secondary Index
  - Can only be created when you are createing a table.
  - Cannot add, remove, modify it later.
  - It has the same Partition Key as your original table.
  - Gives you a different view of your data, organised according to an alternative sort key.
  - Any queries based on this Sort key are much faster using the index than the main table.
  - eg. Partition key: userID, Sort Key:account creation date.
- Global Secondary Index
  - can create at table creation or add it later.
  - Different Partition Key as well as Different Sort Key.
  - Gives a completely different view of the data.
  - Speeds up any queries relating to this alternative Partition and Sort Key.
  - Eg. Partition Key: email address, Sort key : last log-in date.

_Exam Tips_

- Indexes enable fast queries on specific data columns.
- Give you a different view of your data, based on alternative Partition / Sort Keys
- Important to understand the differences.

  | Local Secondary Index                         | Global Secondary Index                            |
  | --------------------------------------------- | ------------------------------------------------- |
  | Must be created at when you create your table | Can careate any time - at table creation or after |
  | Same Partition Key as your table              | Different Partition Key                           |
  | Different Sort Key                            | Different Sort Key                                |

### Scan vs Squery API Call

What is a query?

- A query operation finds items in a table based on the Primary Key attribute and a distinct value to search for.
- e.g. Select an item where the user ID is equal to 212, will select all the attributes for that item, e.g. first name, surname, email etc.
- Use an optional Sort Key name and value to refine the results.
- e.g. if Sort Key is a timestamp, we can refine the query to only select items with a time stamp of the last 7 days.
- By default, a Query returns all the attributes for the items but you can use the ProjectionExpression parameter if you want the query to only return the specific attributes we want.
- e.g. if we only want to see the email address rather than all the attributes.
- Results are always sorted by the Sort Key.
  - Numeric order - by default in ascending order.
  - ASCII character code values in ascending order.
- We can reverse the order by setting the `ScanIndexForward` parameter to false.
- By default, Queries are Eventually Consostent.
- You need to explicitly set the query to be Strongly Consistent.

What is a Scan?

- A Scan operation examines every item in the table.
- By default returns all data attributes.
- Use the `ProjectionExpression` parameter to refine the scan to only return the attributes you want.

Query or Scan, What to use?

- Query is more efficient than a Scan.
- Scan dumps the entire table, then filters out the values to provide the desired result - removing the unwanted data.
- This adds an extra step of removing the data we don't want.
- As the table grows, the scan operation takes longer.
- Scan operation on a large table can use up the provisioned throughput for a large table in just a single operation.

How to improve performance

- We can reduce the impact of a query or scan by setting a smaller page size which uses a fewer read operations.
- eg. set the page size to return 40 items.
- Larger number of smaller operations will allow other requests to succed without throttling.
- Avaid using scan operation if we can: design tables in a way that can use the Query, Get or BatchGetItem APIs.
- By deafult, a scan operation processes data sequentially in returning 1MB increments before moving on to retrieve the next 1 MB of data. It can only scan one partition at a time.
- You can configure dynamoDB to use parallel scans instead by logically dividing a table or index into segments and scanning each segment in parallel.
- Best to avoid parallel scans if your table or index is already incurring heavy read / write activity from other applications.

_Exam Tips_

- A query operation finds items in a table using only the primary key attribute.
- We can provide the Primary Key name and a distinct value to search for.
- A Scan operation examines every item in the table.
- By default returns all data attributes.
- Use the ProjectionExpression parameter to refine the results.
- Query results are always sorted by the Sort Key if there is one.
- Sorted in ascending order.
- Set `ScanIndexForaward` parameter to false to rever the order - queries only.
- Query operation is generally more efficient than a Scan.
- Reduce the impact of a query or scan by setting a smaller page size which uses fewer read operations.
- Isolate scan operations to specific tables and segregare them from our mission-critical traffic.
- Try parallel scans, rather than the default sequential scan.
- Avaid using scan operation if we can: design tables in a way that can use the Query, Get or BatchGetItem APIs.

### DynamoDB Provisioned Throughput

What is DynamoDB Provisioned Throughput?
Is the mechanism used to define capacity and performance requirements in dynamoDB.

DynamoDB Read and Write Capacity Units

- DynamoDB Provisioned Throughput is measured in Capacity Units.
- When you create your table, you specify your requirements in terms of Read Capacity Units and Write Capacity Units. assuming it is not auto scalable.
- 1 x Write Capacity = 1 x 1 KB Write per second.
- 1 x Read Capacity Unit = 1 x Strong Consistent Read of 4KB per second OR 2 x Eventually Consistent Reads of 4KB per second(Default).

Strongly Consistent Reads Calculation

- Say you applicaiton needs to read 80 items (rows) per second.
- Each item is 3KB in size.
- We need Strongly Consistent Reads.

- Calculate how many Read Capacity Units are needed for each read i.e. size of each item / 4KB.so 3KB/4Kb = 0.75
- Rounded-up to the nearest whole number, each read will need 1 x Read Capacity Unit per read operation.
- Multiplied by the number of reads per second = 80 Read Capacity Units required.

Eventually Consistent Reads Calculation

- Calculate Stronly Consistent Reads and divide by 2.

Write Capacity Units Calculation

- You want to wrtie 100 items per second.
- Each item 512 bytes in size.

- Calculate how many Capacity Units for each write: Size of each item / 1KB (for Write Capacity Units) 512 bytes / 1KB = 0.5
- Rounded-up to the nearest whole number, each write will need 1 x Write Capcity Unit per write operation.
- Multiplied by the number of writes per second = 100 Write Capacity Units required.

### DynamoDB On-Demand Capacity Option

- Charges apply for: Reading, Writing and Storing data.
- With On-Demand, we don't need to specify our requirements.
- DynamoDB instantly scales up and down based on the activity of our application.
- Great for unpredictable workloads
- pay per use.

Which pricing model should I use?

| On-Demand Capacity                | Provisioned Capacity                                      |
| --------------------------------- | --------------------------------------------------------- |
| Unknown workloads                 | Can forecast read and write capacity requirements         |
| Unpredictable application traffic | Predictable application traffic                           |
| You want a pay per use mdoel      | Applicaition traffic is consistent or increases gradually |
| Spiky, short lived peaks          |                                                           |

We can convert dynamoDB from On-Demand to Provisionsed and vice versa once per day.

### DynamoDB Accelerator - DAX

What is DAX?

- DyanamoDB Accelerator (DAX) is a fully managed, clustered in-memory cache for DynamoDB.
- Delivers upto a 10x read performance improvement.
- Microsecond performance for millions of requests per second.
- Ideal for Read-Heavy and bursty workloads.
- e.g. auction applications, gaming and retail sites during black friday promotions.

How does it work?

- DAX is a write through caching service - this means data is written to the cache as well as the back end store at the same time.
- Allows to point our dynamoDB API calls at the DAX cluster
- IF the item are quering is in the cache, DAX returns the result to the application.
- If the item is not available then DAX performs an Eventually Consistent GetItem operation againse DynamoDb
- Retrival of data from DAX reduces the read load on dynamoDB tables.
- Maybe able to reduce Provisioned Read Capacity.

What is not suitable for?

- Caters for Eventuallt Consistent reads only - so not suitable for applications that require Strongly Consistent reads
- Write intensive applications.
- Applicaitons that do not perform many read operations.
- Application that do not require microsecond response times.

### ElastiCache

It is in-memory caching which can be use with any RDS and dynamoDB.

- Is in memory cache in the cloud.
- Improves performacn==nce of web applications, allowing to retrive information from fast in-memory cahces rather than slower disk based databases.
- Sits between applications and the database:
  - e.g. an application frequently requesting specific product information for best selling products.
- Takes the load off our databases.
- Good if your databse is particularly read-heavy and the data is not changing frequently.

Benefits and Use Cases

- Improves performance for read-heavy workloads
- Frequent-accessed data is stored in-memory for low latency access, improving the overall performance of application.
- Also good for compute heavy workloads.
- Can be used to store results of I/O intensive database queries or output of compute-intensive calculations.

2 types of Elasticache

- Memcached
  - Widely adopted memory object caching system.
  - Multi-threaded
  - No Multi-AZ capability
- Redis
  - Open-source in-memory key-value store.
  - Supports more complex data structures: sorted sets and lists
  - Support Master / Slave replication and multi-AZ for cross AZ redundancy.

Caching Strategies

- Lazy Loading

  - loads the data into the cache only when necessaty.
  - If requested data is in the cache, Elasticache returns the data to the application.
  - If data is not in cache or has expired, Elasticache return a null.
  - Application then fetches the data from the database and writes the data received into the cache so that it is available next time.
  - | Advandage                                                                                  | Disadvantage                                                                                                                                           |
    | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | Only requested data cached.Avoid filling up cache with useless data.                       | Cache miss penalty: Initial request,Query to database, Writing of data to the cache                                                                    |
    | Node failure are not fatal a new empty node will just have a lot of cache misses initially | Stale data - If data is only ipdated when there is a cache miss, it can become stale. Doesn't automatically update if the data in the databasechanges. |

- TTL

  - Specifies the number of seconds until the key expires to avoid keeping stale data in the cache.
  - Lazy loading treats an expired key as a cache miss and causes the application to retrieve the data from the database and subsequently write the data into the cache with a new TTL.
  - Does not eliminate statle data - but helps to avoid it.

- Write-Through
  - adds or updates data to cache whenever data is written to the database.
  - | Disadvantages                                                                                    | Advantages                                                                                         |
    | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
    | Write penalty: Every write invloves a write to the cache as well as wrtie to databse             | Data in the cache is never statle                                                                  |
    | If a node failse and a new one is spun up, data is missing until added or updated in the databse | Users are generally more tolerant of additional latency when updating data than when retrieving it |
    | Wasted resources if most of the data is never read                                               |                                                                                                    |

### DynamoDB Transactions

- ACID Transaction (Atomic, Consistent,Isolated,Durable)
- Read or Write multiple items accross multiple tables as an all or nothing operation.
- Check for a pre-requisie condition before writing to a table.

## DynamoDB TTL

- Time to live attribute defines an expiry time for our data
- Expired items marked for deletion
- Great for removing irrelevant or old data:
  - Session Data
  - Event logs
  - Temporary data
- Reduces cost by automatically removing data which is no longer relevant.

Session Data Table

| userID  | sessionId      | creationTime | expirationTIme | sessionData |
| ------- | -------------- | ------------ | -------------- | ----------- |
| 5346747 | 67634678235789 | 1544016418   | 1544023618     | {JSOn}      |

- TTL expressed as epoch time.
- Expiration is set for 2 hours after the session began.
- When the current time is greater than the TTL, the item will be expiered and marked for deletion.
- Filter out expired items from your queries and scans.

### DynamoDB Streams

- Time-ordered sequence of item level modifications.
- Logs are encrypted at rest and stored for 24 hours
- Accessed using a dedicated endpoint.
- By default the Primary Key is recorded.
- Before and After images can be captured.

Processing DynamoDB Streams

- Events are recored in near real-time.
- Application can take actions based on contens.
- Event source for Lambda
- Lambda polls the DynamoDB stream.
- Executes Lambda code based on a DynamoDB Streams event.

Quiz:

1. In DynamoDB, a scan operation is used for which of the following?

- Find items in a table based on the Sort Key attribute.
- Return the entire contents of a table. &#10004;
- Return the entire contents of a table filtered on the Primary Key attribute.
- Find items in a table based on the Primary Key attribute.

  A Scan returns the entire contents of a table whereas a query finds items based on the Primary Key.

2. Which of the following are recommended ways to optimise a query or scan in DynamoDB?

- Filter your results based on the Primary Key and Sort Key.
- Run parallel scans.&#10004;
- Reduce the page size to return fewer items per results page.&#10004;
- Set your queries to be eventually consistent.

  A smaller page size means uses fewer read operations and creates a "pause" between each request which reduces the impact of a query or scan operation. A larger number of smaller operations can allow other critical requests to succeed without throttling. For large tables, a parallel scan can complete much faster than a sequential one, if the table's provisioned read throughput is not already being fully used.

3. DynamoDB is a No-SQL database provided by AWS.

- True&#10004;
- False

4. You have a motion sensor which writes 600 items of data every minute. Each item consists of 5KB. What should you set the write throughput to?

- 10
- 20
- 40
- 50 &#10004;
  1 write Capacity Unit allows you to write 1KB of data per second. To calculate the write capacity: 600 / 60 = 10 writes per second x 5KB = 50KB written per second Therefore 50 WCU.

5. You are running a query on your Customers table in DynamoDB, however you only want the query to return CustomerID and EmailAddress for each item in the table, how can you refine the query so that it only includes the required attributes?

- Run a query based on the Primary Key and filter the results using a Sort Key of EmailAddress
- Use a scan operation instead
- Create a Global Secondary Index which only includes the attributes you need and run the query on the Global Secondary Index
- Use the ProjectionExpression parameter &#10004;
  When using Query, or Scan, DynamoDB returns all of the item attributes by default. To get just some, rather than all of the attributes, use a Projection Expression.

6. You have an application that needs to read 25 items of 13KB in size per second. Your application uses eventually consistent reads. What should you set the read throughput to?

- 10 RCU
- 50 RCU &#10004;
- 100 RCU
- 25 RCU
  Each Read Capacity unit represents 1 x 4KB Strongly Consistent Read. 13KB / 4KB = 3.25 rounded up to 4 multiply by 25 = 100 which gives you the figure for Strongly consistent reads. Divide that by 2 for Eventually consistent. So the answer is 50 RCU.

7. Your low latency web application needs to store its session state in a scalable way so that it can be accessed quickly. Which service do you recommend?

- In memory on your EC2 instance
- DynamoDB &#10004;
- RDS
- Elastic File Store
  Using DynamoDB for session storage alleviates issues that occur with session handling in a distributed web application by moving sessions off of the local file system and into a shared location.

8. What does the error "ProvisionedThroughputExceededException" mean in DynamoDB?

- The DynamoDB table is unavailable.
- You exceeded your maximum allowed provisioned throughput for a table or for one or more global secondary indexes. &#10004;
- Your EC2 instance has run out of CPU or memory
- The DynamoDB table has exceeded the allocated space.
  This error means that you have exceeded your maximum allowed provisioned throughput for a table or for one or more global secondary indexes.

9. You have an application which reads 80 items of data every second. Each item consists of 3KB. Your application uses eventually consistent reads. What should you set the RCU read throughput to?

- 40 RCU &#10004;
- 80 RCU
- 20 RCU
- 60 RCU
  Each Read Capacity Unit represents 2 x Eventually consistent 4KB reads per second. 3KB / 4KB = 0.75 and round up to 1. Multiply that by 80 to give you the figure for Strongly consistent reads. Divide that by 2 to get Eventually consistent reads. Therefore the answer is 40 RCU.

10. Your application is storing customer order data in DynamoDB. Which of the following pairs of attributes would make the best composite key to allow you to query DynamoDB efficiently to find a customer order that was placed on a specific day?

- CustomerID + Size
- CustomerID + OrderDate &#10004;
- CustomerID + ProductCategory
- CustomerID + ProductID
  To find an order placed on a specific date, use CustomerID and OrderDate as the composite key.

11. Using the AWS portal, you are trying to Scale DynamoDB past its pre-configured maximums. Which service limit can you increase by raising a ticket to AWS support?

- Global Secondary Indexes
- Provisioned throughput limits &#10004;
- Item Sizes
- Local Secondary Indexes

12. Which of the following attributes would make a good Sort Key?

- InvoiceDate &#10004;
- OrderNumber
- CustomerID
- EmailAddress
  Every DDB table and index requires a key of unique values. This can be in the form of a Partition key or a Partition key and a range of unique Sort keys. A sort key is typically as sequence of values. Uniques Dates or times, or subdivisions of the Partition key such as a version number. CustomerID, EmailAddress, and OrderNumber would all make good Partition Keys.

13. In terms of performance, a scan is more efficient than a query.

- True
- False &#10003;
  In most cases a query is preferable to a scan operation. A scan is generally less efficient & more expensive.

14. Which DynamoDB feature can be used to define an expiry date and time for a data record in your table?

- TTL &#10004;
- Exponential Backoff
- DynamoDB Streams
- DynamoDB Expiry
  TTL or Time To Live is used to set an expiry time on your record

15. Which of the following approaches is used in AWS to improve flow control by retrying failed requests using progressively longer waits between retries?

- Exponential Retry
- Exponential Backoff &#10004;
- Backoff With Jitter
- Linear Backoff
  Each AWS SDK implements an exponential backoff algorithm for better flow control. The idea behind exponential backoff is to use progressively longer waits between retries for consecutive error responses.

16. Your application is storing customer order data in a DynamoDB table. You need to run a query to find all the orders placed by a specific customer in the last month, which attributes would you use in your query?

- The Partition Key of OrderDate and Sort Key of CustomerName
- A composite Primary Key made up of the CustomerName and OrderDate
- The Partition Key of OrderDate and a Sort Key of CustomerID
- The Partition Key of CustomerID and a Sort Key of OrderDate &#10004;
  CustomerName is unlikely to be a unique value in the database, CustomerID is a better choice as will be a unique value. To identify all the orders placed in the last month by a customer, use OrderDate as the Sort Key.

17. By default, a DynamoDB query operation is used for which of the following?

- Find items in a table based on the Sort Key attribute
- Return the entire contents of a table
- Find items in a table based on the Primary Key attribute &#10004;
- Return the entire contents of a table filtered on the Primary Key attribute
  A query finds items based on the Primary Key, whereas a Scan returns the entire contents of a table.

18. Which feature can you use to capture a time-ordered sequence of all the activity which occurs on your DynamoDB table - e.g. insert, update, delete?

- DynamoDB Streams &#10004;
- Kinesis Streams
- CloudWatch
- CloudTrail

19. Your DynamoDB table is throwing a ProvisionedThroughputExceeded error, what could be the problem?

- Your instance is too small
- You are experiencing network contention
- Your application's request rate is too high &#10004;
- You are running out of disk space
  ProvisionedThroughputExceededException means that your application is sending more requests to the DynamoDB table than the provisioned read / write capacity can handle.

20. Which of the following are ways of remediating a ProvisionedThroughputExceeded error from DynamoDB?

- Reduce the frequency of requests to the DynamoDB table&#10004;
- Increase the frequency of requests to the DynamoDB table
- Move your application to a larger instance type
- Exponential Backoff&#10004;
  ProvisionedThroughputExceeded means that your request rate is too high. Reduce the frequency of requests using Error Retries and Exponential Backoff.

21. What is the API call to retrieve multiple items from a DynamoDB table?

- BatchGetItem &#10004;
- BatchGet
- BatchGetItems
- GetItems

22. What is the difference between a Global Secondary Index and a Local Secondary Index?

- You can create a Global Secondary Index at any time but you can only create a Local Secondary Index at table creation time. &#10004;
- You can delete a Local Secondary Index at any time.
- You can create a Local Secondary Index at any time but you can only create a Global Secondary Index at table creation time.
- You can delete a Global Secondary Index at any time. &#10004;
  Only Global secondary Indexes can be created or deleted at anytime. Local Secondary Indexes must be created when you first create the table and they cannot be modified or deleted.

23. You have an application that needs to read 25 items of 13KB in size per second. Your application uses strongly consistent reads. What should you set the read throughput to?

- 100 &#10004;
- 50
- 25
- 10
  Each Read Capacity unit represents 1 x 4KB Strongly Consistent Read. 13 / 4 = 3.25 rounded up to 4KB multiply by 25 = 100.

24. Which of the following services provides in-memory write-through cache optimized for DynamoDB?

- Read-replica
- DAX&#10004;
- CloudFront
- Elasticache
  DAX or DynamoDB Accelerator is highly available, in-memory cache which is optimized for DynamoDB. DAX currently only offers write-through cache. ElastiCache is supported for use with DynamoDB, however it is not specifically optimized for use with DynamoDB. CloudFront is a Content Delivery Network which caches content like files, web pages, videos etc, but cannot be used to cache Database data. Read-Replicas are used to scale read operations for RDS instances.

25. Which of the following attributes would make a good Partition Key?

- ProductType
- WarehouseLocation
- Size
- ProductID &#10004;
  It is good practice to use high-cardinality attributes for Partition Keys. in other words, attributes with values that are very uncommon or unique. e.g. ID number, email address, phone number, Social Security Number etc.

## Chapter 7 : KMS

### KMS 101

KMS stands for Key Management Service. AWS KMS is a managed service that makes it easy for us to create and control the encryption keys used to encrypt our data. AWS KMS is integrated with other AWS services including, EBS, S3, Amazon Redshift, Amazon Elastic Transcoder, Amazon WorkMail, Amazon Relational Database Service (Amazon RDS), and others to make it simple to encrypt our data with encryption keys that we manage.
Encryption Keys are regional.Encryption key of a region and decryption key in another region will not work. The Customer Master Key cannot leave the KMS i.e. can NEVER be exported. If we want to export the keys we need Cloud HSM. KMS uses multi-tenant hardware where as Cloud HSM is dedicated for us.
The Customer Master Key consist of

- alias
  The name we give to it.
- Creation Date
- Description
- Key State
- Key Material (either customer provided or AWS provided).

Setup a Customer Master Key:

- Goto IAM and create alias and description.
- Define Key Administrative Permissions.
  - IAM users/roles that can administer (but not use) the key through the KMS API.
- Define Key Usage Permissions
  - IAM users/roles that can use the key to encrypt and decrypt data.

### KMS API Calls (important)

**EXAM TIPS**

- aws kms encrypt
- aws kms decrypt
- aws kms re-encrypt
- aws kms enable-key-rotation

### KMS Envelope Encryption

IT is the process of encrypting the envelope key. Envelope key is the key we use to encrypt/decrypt out data.

### KMS EXAM TIPS

- What is KMS
- Customer Master Key
- Setup Customer master key
- Key material options
- Know API calls
- Envelope Encryption

_Quiz_

1. Which of the following statements is correct in relation to KMS?

- You can export your customer master key.
- KMS encryption keys are global.
- You cannot export your customer master key. &#10004;
- KMS encryption keys are regional. &#10004;
  Master keys are created and used only within AWS KMS to help ensure their security, enable your policies to be consistently enforced, and provide a centralized log of their use. Keys are only stored and used in the region in which they are created. They cannot be transferred to another region. For example; keys created in the EU-Central (Frankfurt) region are only stored and used within the EU-Central (Frankfurt) region.

2. Which command can you use to encrypt a plain text file using a CMK?

- aws kms encrypt. &#10004;
- aws iam encrypt.
- aws encrypt.
- aws kms-encrypt.
  Use the aws kms encrypt command to encrypt files.

3. Which of the following statements are correct about AWS Managed Customer Master Keys?

- The Customer Master Key is used to encrypt and decrypt plain text files.
- The Customer Master Key is used to encrypt and decrypt the Envelope Key or Data Key. &#10004;
- The Envelope Key or Data Key is used to encrypt and decrypt the Customer Master Key.
- The Envelope Key or Data Key is used to encrypt and decrypt plain text files. &#10004;
  The Customer Master Key is used to encrypt and decrypt the Data Key or Envelope Key. The Data Key or Envelope Key is used to encrypt and decrypt your files. AWS Managed Customer Master Keys cannot be used to directly encrypt and decrypt files, since permissions cannot be changed to them. Customer Managed Customer Master Keys can be used with the KMS command to encrypt the file, when Key Usage rights are given.

4. Which of the following is an encrypted key used by KMS to encrypt your data?

- Envelope Key &#10004;
- Customer Master Key
- Customer Managed Key
- Encryption Key
  Your Data key (also known as the Envelope key) is encrypted using the master key. This approach is known as Envelope encryption.

5. You are working on a project which requires a Key Management Solution. Your Security Architect has confirmed that a multi-tenant solution is fine. Which solution do you recommend?

- S3 Encryption.
- Client-Side Encryption.
- CloudHSM.
- KMS. &#10004;
  KMS is multi-tenant whereas CloudHSM is dedicated hardware. S3 Encryption and Client-Side encryption are not Key Management Solutions

6. You need to re-encrypt a file with a new customer master key, which API call can you use to do this?

- encrypt.
- re-encrypt. &#10004;
- enable-key-rotation.
- decrypt and encrypt.
  The re-encrypt API call encrypts data on the server side with a new customer master key (CMK) without exposing the plaintext of the data on the client side.

7. You would like KMS to rotate your encryption keys on a yearly basis, which API command can you use to configure this?

- chkconfig key-rotation on.
- configure-key-rotation.
- setup-key-rotation -y.
- enable-key-rotation. &#10004;
  Use the aws kms enable-key-rotation command to configure key rotation. This can also be enabled in the console.

8. Which of the following is a managed service that allows you to create and control the encryption keys used to encrypt your data?

- RDS Encryption
- CMS
- KMS &#10004;
- S3 Encryption

## Chapter 8 : Other AWS Services

### SQS (Simple Queue Service)

What is SQS?
Amazon SQS is a web service that gives us access to message queue that can be used to store messages while waiting for a computer to process them. Amazon SQS is a distributed queue system that enables web service applications to quickly and reliably queue messages that one component in the application generates to be consumed by another component. A queue is a temporary repository for messages that are awaiting processing.
eg.Meme Generator: When a user adds a image in s3 bucket a lambda function is called and it passes the data as the s3 bucket address, meme text etc. This then sits in the queue until an EC2 instance picks it up, process it and store it in an EC2 Instance. When the task is completed the entry is removed from the SQS but incase EC2 instance failed then the job is retained in the SQS and next EC2 instance would handle it. SQS is always a pull-based system. If you need push-based system use SNS (Simple Notification Service).
When an EC2 instance is processing a query(job) from SQS it is marked as invisible but will be in a queue. The time period it is invisible is called visibility timeout window. When ever the timeout is finished it will be visible and another EC2 instance would pick it up and process the job.
Using Amazon SQS, We can decouple the components of an application so they run independently, easing message management between components. Any component of a distributed application can store messages in the queue. Messages can contain upto 256 KB of text in any format. Any component can later retrieve the messages programaticaaly using the Amazon SQS API.
The Queue acts as a buffer between the component producing and saving data, and the component receiving the data for processing. This means the queue resolves issues that arise if the producer is producing work faster that the consumer can process it, or if the producer or consumer are only intermittently connected to the network.
This means that if we have 2 EC2 Instance for this queue and suddenly lots of messages are comming then auto scaling groupto monitor SQS add more EC2 instance if no. of messsages is reached or if the only one message is in the queue then we can scale down to only 1 EC2 instance.
2 Types of Queues are :

- Standard Queues (default)
  A standard queue lets you have a nearly-unlimited number of transactions per second. Standard queues guarantee that a message is delivered at least once. However, occasionally (because of the highly-distributed architecture that allows high throughput), more than one copy of a message might be delivered out of order. Standard queues provide best-effort ordering which ensures that messages are generally delivered in the same order as they are sent.
- FIFO Queue
  The order in which the messages are sent and received is strictly preserved and a message is delivered once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue. FIFO also supports message groups that allow multiple ordered message groups within a single queue. FIFO are limited to 300 transactions per second(TPS), but have all the capabilities of standard queues.

SQS Key Facts:

- SQS is a pull-based and not pushed-based.
- Messages are 256KB in size.
- Messages can be kept in the queue from 1 minute to 14 days.
- Default retention period is 4 days.
- SQS guarantees that your messages will be processed at least once.

SQS Visibility Timeout

- The visibility timeout is the amount of time that the message is invisible in the SQS queue agete a reader picks up that message. Provided the job is processed before the visibility time expires, the message will then be deleted from the queue. If the job is no processed withing that time the message will become visible again and another reader will process it. This could result in the same message being delivered twice.
- Default visibility Timeout is 30 seconds.
- Increase it if task takes >30 seconds.
- Maximum is 12 hours.

SQS Long Polling

- Amazon SQS long polling is a way to retrieve messages from Amazon SQS queues.
- While the regular shot polling return immediately (even if the message queue being polled is empty), long polling doen't return a response until a message arrives in the message queue, or the long poll times out.
- As such, long polling can save you money.

_EXAM TIPS_

- SQS is a distributed message queueing system.
- Allows you to decouple the components of an application so that they are independent.
- Pull-based, not push-based.
- Standard Queue (default) - best-effort ordering; message delivered at least once.
- FIFO Queues (First In First Out) - ordering strictly preserved, message delivered once, no duplicates. e.g. good for banking transactions which need to happen in strict order.
- Visibility Timeout
  - Default is 30 seconds - increase if it takes >30 seconds to complete.
  - Max is 12 hours
- Short Polling - returned immediately even if no messages are in the queue.
- Long Polling - Pools the queue periodically and only return a response when a mesage in the queue or the timout is reached.

### SNS (Simple Notification Service)

What is SNS?
Amazon Simple Notification Service is a web service that makes it easy to setup, operate, and send notifications from the cloud. It provides developers with a highly scalable, flexible, and cost-effective capabilitiy to publish messages from an application and immediately deliver them to subscribers or other applications. We can have push notification to Apple, Goole, Fire OS, and Windows devices, as well as Android devices in china with Baidu Cloud Push.
Besides pushing cloud notification directly to mobile devices, Amazon SNS can also deliver notifications by SMS text message or email to Amazon Simple Queue Service (SQS) queues, or to any HTTP endpoint.
SNS notifications can also trigger Lambda functions: When a message is published to an SNS topic that has a lambda function subscribed to it, the Lambda function is invoked with the payload of the published message. The Lambda function receives the message payload as an input parameter and can manipulate the information in the message, publish the message to another SNS topic, or send the message to other AWS Services.

SNS Topics
SNS allows you to group multiple recipients using topics. A topic is an "access point" for allowing recipients to dynamically subscribe for identical copies of the same notification. One topic can support deliveries to multiple endpoint types - for example, you can group together iOS, Android and SMS recipients. When you publish once to a topic, SNS delivers appropriately formatted copies of our message to each subscriber. To prevent messages from being lost, all messages published to Amazon SNS are stored redundantly across multiple availability zones.

SNS Benefits:

- Instantaneous, push-based delivery (no polling)
- Simple APIs and easy integration with applications
- Flexible message delivey over multiple transport protocols.
- Inexpensive, pay-as-you-go model with no up-front costs.
- Web based AWS Management Console offers the simplicity of a point-and-click interface.

SNS VS SQS

| SNS        | SQS               |
| ---------- | ----------------- |
| Push based | Pull based(polls) |

Amazon SNS follows the "publish-subscribe" messaging paradigm, with notification being delivered to clients using a "push" mechanism that eliminates the need to periodically check or "poll" for new information and updates. With simple APIs requiring minimal up-front development effot, no maintenance or management overhead and pay-as-you-go pricing, Amazon SNS gives developers an easy mechanism to incorporate a powerful notification system with their applications.

_EXAM TIPS_

- SNS is a scalable and highly available notification service which allows you to send push notifications from the cloud.
- Variety of message formats supported: SMS text message, email, Amazon Simple Queue Service (SQS) queues, any HTTP endpoint.
- publish-subscribe model whereby users subscript to topics.
- It is a push mechanish, rather than a pull (poll) mechanism.

### Amazon SES

Amazon SES (Simple Email System) is a scalable and highly available email service designed to help marketing teams and application developers send marketing notification and transactional emails to their customers using a pay as you go model. Can also be used to receive emails: incoming mails can be delivered automatically to an S3 Bucket. Incoming mails can be used to trigger Lambda functions and SNS notifications.
Use Cases :

- Automated emails
- Purchase Confirmations, shipping notifications, order status updates
- e.g. a mobile phone company that needs to send automated confirmation email every time a customer purchases pre-paid mobile phone minutes.
- Marketing communications, advertisements, newsletters, special offers.
- e.g. An online retail buissness that needs to let customer know about sales promotion and discounts.

| SES                                                                          | SNS                                                              |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Email messaging service                                                      | Pub/Sub messaging service, formats include SMS, HTTP,SQS,email   |
| Can trigger lambda function or SNS notification                              | Can be used to trigger Lambda function                           |
| Can be used for both incoming and outgoing email                             | Can fan out messages to large number of recipients.              |
| An email address is all that is required to start sending messages to a user | Consumers must subscribe to a topic to receive the notification. |
| Async                                                                        | Sync                                                             |

### Kinesis 101

What is streaming data?
Streaming Data is data that is generated contibuously by thousand of data sources, which typically send in the data records simultaneously, and in small sizes (order of Kilobytes). eg, game data, GPS data etc.

What is kinesis?
Amazon Kinesis is a plotform on AWS to send our streaming data too. Kinesis make it easy to load and analyze streaming data, and also providing the ability for us to build own custom application for our business needs.

What are the core kinesis Services?

- Kinesis Streams
- Kinesis Firehose
- Kinesis Analytics

What is kinesis streams?
EC2 Instance, mobile, laptop etc. are called "data producers" or "producers". Kineses streams basically store this data, by default for 24 hours but hte retention can be extended upto 7 days. In kinesis the data is stored in shards. Then we have EC2 Instances which act as a consumers. These consumer takes data from shard and turn it usefull by either aggerrating, doing data mining, analysis etc. Once consumer are done processing it is sent to be stored in variety of AWS services.

- Kinesis Streams consist of shards
  - 5 transaction per second for reads, up to a maximum total data read rate of 2 MB per second and upto 1000 records per second for writes, upto a maximum total data write rate of 1 MB per second ( including partition keys ).
  - The data capacity of your stream is a function of the number of shards that you specify for the stream. The total capacity of the stream is the sum of the capacities of its shards.

What is Kinesis Firehose?
Similar to Kineses Streams we have producer. They send the data to Kinesus Firehose. In Kinesis Firehose we don't have to worry about shards,streams or manually adding in shards etc. It is automated. We can analyze the data using lambda in real time and once data is analyzed we can send them to S3 directly. Since the analyzing is done in real time we don't have a need for a retention window. To store in any other storage the data should be copied from S3. Here, we only have lambda as consumer.

_Exam Tips_

- Know the difference between Kinesis Streams and Kinesis Firehose. You will be given scenatio question and you must choose the most relevant service. If it is talking about shards then it is kinetic streams because Firhose has no shards whereas if it talks about lambda then it is kinetic Firehose

### Elastic Beanstalk 101

What is Elastic Beanstalk?
Elastic Beanstalk is a service for deploying and scaling web applications developed in many popular languages: JAVA, .NET, PHP, Node.js, Python, Ruby, Go and Docker onto widely used application server platforms like Apache Tomcat, Nginx, Passenger, amd IIS.
Developers can focus on writing code and don't need to worry about any of the underlying infrastructure needed to run the application.
i.e. We can send some code in a zip file and it will go and detect, or go in and configure an environment for you, or go and configure the web servers, might put them behind an auto scaling group, configuire own RDS environment.
We upload the code and Elastic Beanstalk will handle deployment, capacity provisioning, load balancing, auto-scaling and application health. You retain full controll of the underlying AWS resources powering our application and you pay only for the AWS resources required to store and run our applications.

- It is fastest and simplest way to deploy your application in AWS.
- Automatically scales our application up and down.
- You can select the EC2 instance type that is optimal for our application.
- We can retain full administrative control over the resources powering our application, or have Elastic Beanstalk do it for us.
- Managed Platform Updates feature automatically applies updates our Operating System, JAVA, PHP, Node.js, etc.
- Monitor and manage application health via a dashboard.
- Integrated with CloudWatch and X-Ray for performance data and metrics.

_EXAM TIPS_

- Deploys and scales our web applications including the web application server platform where required.
- Supports widely used programming technologies - JAVA, PHP, Python, Ruby, Go,Docker, .NET, Node.js
- And application server platform like Tomcat, Passenger, Puma and IIS.
- Provisions the underlying resources for us.
- Can fully manage the EC2 instance for you or you can take full administrative control.
- Updates, monitoring, metrics and health checks all included.

### Elastic Beanstalk ( EBS ) Deployment Policies

Elastic Beanstalk supports several options for processing deployements:

- All at once
  - Deploys the new version to all instances simultaneously.
  - All of our instances are out of service while the deployement takes place.
  - We will experience an outage while the deployment is taking place - not ideal for mission-critical production systems
  - If the update fails, we need to roll back the changes by re-deploying the original version to all our instances.
  - Mostly used in test/dev environment.
- Rolling
  - Deploys the new version in batches
  - Each batch of instances is taken out of service while the deployment takes place.
  - Our environment capacity will be reduced by the number of instances in a batch while the deployment takes place.
  - Not ideal for performance sensitive systems.
  - If the update fails, you need to perform an additional rolling update to roll back the changes.
- Rolling with additional batch
  - Launces an additional batch of instances
  - Deploys the new version in batches
  - Maintain full capacity during the deployment process
  - If the update fails, we need to perform an additional rolling update to rollback the changes.
  - Used when we want zero downtime or is performance-sensitive then we use this.
- Immutable
  - Deploys the new version to a fresh group of instances in their own new autoscaling group.
  - When the new instances pass their health checks, they are moved to our existing auto scaling group; and finally, the old instances are terminated.
  - Mantains full capacity during the deployment process.
  - The impact of a failed update is far less, and the rollback process requires only terminating the new auto scaling group.
  - Prefferred option for Mission Critical production systems.

_EXAM TIPS_

- Remember the 4 different deployment approaches:
  - All at once
    - Service interruption while we update the entire environment at once.
    - To roll back, perform a further all at All at Once upgrade.
  - Rolling
    - Reduced capacity during deployment.
    - To rollback, perform a further rolling update.
  - Rolling with Additional Batch
    - Maintains full capacity.
    - To rollback , perform a further rolling update.
  - Immutable
    - Preferred option for mission critical production systems.
    - Maintains full capacity
    - To roll back, just delete the new instances and autoscaling group

### Advance Elastic Beanstalk

Configuring Elastic Beanstalk
we can customize our Elastic Beanstalk environment using Elastic Beanstalk configuration files. ( we can define packages to install, create linux users and groups, run shell commands, specify services to enable or configure your load balancer, etc.)
These are files written in YAML or JSON format. They can have a filename of your choice but must have a .config extension and be saved inside a folder called .ebextensions.

Location of Configuration Files
The .ebextensions folder must be included in the top-level directory of our application source code bundle.
This means that the configuration files can be placed under source control along with the rest of our application code.

_EXAM TIPS_

- We can customize our Elastic Beanstalk environment by adding configuration files.
- The files are written in YAML or JSON.
- Files have a .config extension.
- The .config files are saved to the .ebextensions folder.
- Our .ebextension folder must be located in the top level directory of our application source code bundle.

### RDS & Elastic Beanstalk

Elastic Beanstalk supports two ways of integrating and RDS database with our Beanstalk environment. We can launch the RDS instance from withing the elastic beanstalk console, which means the RDS instance is created withing our elastic beanstalk environment - a good option for Dev and Test deployments. However this may not be ideal for production environments because it means the lifecycle of your database is tied to the lifecycle of our application environment. If we terminate the environment, the database instance will be terminated too.
For production environments, the preffered option is to decouple the RDS instance from our EBS environment: i.e. launch it outside of Elastic Beanstalk, directly from the RDS section of the console. This option gives you a lot more flexibility, allows you to connect multiple environments to the same database, provides a wider choice of database types, and allows you to tear down our application environment without affecting the database instance.

Access to RDS from Elastic Beanstalk
To allow the EC2 instances in our Elastic Bean stalk environment to connect to an outside database, there are two additional configuration steps required:

- An additional Security Group must be added to our environment's auto scaling group.
- We'll need to provice connection string configuration information to our application servers (endpoint, password using Elastic Beanstalk environment properties).

_EXAM TIPS_

- Two different options for launcing RDS instance:
  - Launch Withing Elastic Beanstalk
    - When we terminate the Elastic Beanstalk environment, the database will also be terminated.
    - Quick and easy to add our database and get started.
    - Suitable for Dev and Test environments only.
  - Launch outside of ELastic Beanstalk
    - Additional configuration steps required - Security Group and Connection information.
    - Suitable for Production environments, more flexibility.
    - Allows connection from multiple environments, we can tear down the application stack without impacting the database.

### AWS System Manager Parameter Store

Imagine you work for a bank as a systems administrator. We need to store confidential information such as users, passwords, license keys etc. This information needs to be passed to EC2 as a bootstrap script, while maintaining the confidentiality of the information.
AWS System Manager Parameter Store is under EC2 in services.
Use Secure String.

_EXAM TIPS_

- Confidential information such as passwords, database connection strings, and license codes can be stored in SSM Parameter Store.
- We can store values as plain text or you can encrypt the data using KMS.
- you can the nreference these values by using their names.
- You can use this service with EC2, CloudFormation, Lambda, EC2 Run Command etc.

_Quiz_

1. What is the maximum retention period for an SQS message?

- 1 day
- 1 hour
- 12 hours
- 14 days &#10004;
  The SQS queue is an ephemeral store and is not intended for long term storage of messages.

2. Elastic Beanstalk is object-based storage.

- True
- False &#1004;

3. SQS was the first service on the AWS platform?

- False
- True &#1004;

4. What is the maximum long poll time out?

- 5 minutes
- 20 seconds &#1004;
- 1 hour
- 50 seconds

5. Elastic Beanstalks charges you both for the resources you deploy, but also charges you a separate cost for deploying it

- True
- False &#1004;
  Elastic Beanstalk is free to use, just like CloudFormation. You only pay for the resources which are deployed as part of it

6. Your EC2 instances download jobs from an SQS queue. However, they are taking too long to process the messages. What API call can you use to extend the length of time to process the jobs?

- ExtendMessageTime
- ChangeMessageVisibility &#10004;
- SetMessageVisibility
- AlterMessageTime
  Changes the visibility timeout of a specified message in a queue to a new value. The maximum allowed timeout value is 12 hours.

7. SNS is pull-based rather than push-based

- True
- False &#10004;

8. A FIFO SQS message can be delivered multiple times.

- True
- False &#10004;
  AWS - 'Unlike standard queues, FIFO queues don't introduce duplicate messages'

9. Which Amazon service can you use in conjunction with SQS to "fan out" SQS messages to multiple queues?

- SES

- SWF

- SNS &#10004;

- ElastiCache

10. AWS provides a number of security related managed services. From the options below, select which AWS service is related to protecting your infrastructure from which security issue.

- AWS WAF protects from Cross-site Scripting attacks &#10004;
- AWS WAF blocks IP addresses based on rules &#10004;
- AWS Shield protects from SQL Injection attacks
- Amazon Macie uses Machine Learning to protect sensitive data &#10004;
- AWS Shield protects from Distributed Denial-of-Service attacks &#10004;
  AWS Shield has two options listed above, but only one is correct. AWS Shield operates on layer 3 and 4 of the ISO network model and its primary purpose is to protect against DDoS attacks. It does not have any affect against SQL Injection attacks which are dealt with by AWS WAF. WAF also protects against Cross-site Scripting and can block traffic from IP addresses based on rules and therefore these options are also correct. Finally, Amazon Macie tackles a different problem related to Data Loss Prevention and protects sensitive data and so this answer is also correct. (N.B. these services will not appear on every exam, but it is worthwhile being familiar with these services.

11. You run a video-hosting website with two types of members: premium, fee-paying members; and free members. Each video that is uploaded is processed by a fleet of EC2 instances, which poll an SQS queue as videos are uploaded. However, you need to ensure that the videos uploaded by your premium, fee-paying members have a higher priority than those of your free members. How might you work with SQS to ensure priority treatment of the premium members' videos?

- SQS would not be suitable for this scenario. It would be much better to use SNS to encode the videos.
- SQS allows you to set priorities on individual items within the queue, so simply set the fee-paying members at a higher priority than your free members.
- Create two SQS queues — one for premium members, and one for free members. Program your EC2 fleet to poll the premium queue first and, if empty, to then poll your free members SQS queue. &#10004;

12. You have been asked to decouple an application by utilising SQS. The application dictates that messages on the queue can be delivered more than once, but must be delivered in the order that they have arrived, and also must allow for efficient, repeated polling of the queue. Which of the following options are most suitable?

- Configure a FIFO SQS queue and enable long polling &#10004;
- Configure a standard SQS queue and use long polling
- Configure a standard SQS queue and use default polling
- Configure a FIFO SQS queue and enable short polling
  This question has two parts which need to be considered, the type of queue and the type of polling. The question states that messages, "CAN be delivered more than once" but, "MUST be delivered in the order that they have arrived". MUST is mandatory, while CAN is optional. Since you cannot accommodate both, you address the Mandatory requirements 1st. and then try to accomodate the Optional after. A FIFO queue is required for the Mandatory requirement as it is the only SQS type which will deliver messages in order. The question also states that the queue, "MUST allow for efficient polling" and in this case long polling is the most efficient and cost effective option in situations where the queue will be polled constantly. The correct answer is therefore to configure a FIFO SQS queue with long polling enabled.

13. What is the default visibility timeout for a message in an SQS queue?

- 30 seconds &#10004;
- 15 minutes
- 1 minute
- 1 year
  While a message is being processed it is hidden from other Workers.

14. You have a list of email addresses to which you need to push emails on a periodic basis. What do you subscribe them to?

- A Subreddit
- A topic &#10004;
- A Subject
- A Message

15. Which of these is a protocol NOT supported by SNS:

- HTTP
- FTP &#10004;
- Email-JSON
- Email

16. You can use SNS in conjunction with SQS to fan a single message out to multiple SQS queues.

- False
- True &#10004;

17. Which native AWS service will act as a file system mounted on an S3 bucket?

- Amazon Elastic File System
- AWS Storage Gateway &#10004;
- Amazon S3
- Amazon Elastic Block Store
  The Storage Gateway service is primarily used for attaching infrastructure located in a Data center to the AWS Storage infrastructure. The AWS documentation states that; "You can think of a file gateway as a file system mount on S3." Amazon Elastic File System (EFS) is a mountable file storage service for EC2, but has no connection to S3 which is an object storage service. Amazon Elastic Block Store (EBS) is a block level storage service for use with Amazon EC2 and again has no connection to S3.

18. SNS messages cannot be customized by protocol type.

- True
- False &#10004;

19. You are designing a new application that processes payments and delivers promotional emails to customers. You need to ensure that the payment process takes priority over the creation and delivery of emails. How might you use SQS to achieve this?

- Use 2 SQS queues for the platform. Have the EC2 fleet poll the promotional emails SQS queue first. If this queue is empty, then poll the payment emails queue.
- Use 2 SQS queues for the platform. Have the EC2 fleet poll the payment SQS queue first. If this queue is empty, then poll the promotional emails queue. &#10004;
- Use 1 SQS queue for the platform. Use the HighPriority API call to ensure that all payment SQS messages take priority over the promotional email messages.
- Use 1 SQS queue for the platform. Use the SetPriority API call to ensure that all payment SQS messages take priority over the promotional email messages.

20. You have a fleet of EC2 instances that are constantly polling empty SQS queues, burning CPU cycles and costing your company money. What should you do?

- Enable SQS Long Polling. &#10004;
- Delete the entire EC2 fleet so that they no longer poll the queue.
- Consider using ElastiCache to cache the messages, rather than SQS.
- Enable SQS Short Polling.

21. What languages and development stacks are not currently supported by AWS Elastic Beanstalk?

- Apache Tomcat for Java applications
- Passenger for Ruby applications
- Jetty for JBoss applications &#10004;
- Apache HTTP Server for PHP applications

22. How large can an SQS message be?

- 128KB
- 512KB
- 256KB &#10004;
- 64KB

23. What is the maximum visibility timeout of an SQS message in a queue?

- 1 day
- 1 hour
- 12 hours &#10004;
- 14 days
  While a message is being processed it is hidden from other Workers. This can be set or reset to a maximum of 12 hours

## Chapter 9 : Developer Theory

### Introduction to CI/CD

What is CI/CD?
It is software developement best practice. Stand for Continuous Integration and Continuous Deployement. One of the main characteristics of CI/CD is that it requires you to make small changes and automate everything.For example, code integration, build, test, and deployment tasks, and by doing that, it's possible to make very frequent code releases on a regular basis. with CI/CD, we're making small, incremental changes, and testing our changes before integrating with the main code base. And this allows you to catch bugs when they're small and really simple to fix.
Continuous Delivery is when the project is ready for deployment and human intervention is need as to where and when it should be deployed.
Continuous Deployment is when the project is ready and deployed without human intervention.

Amazon tools that provides CI/CD?

- Code Commit

  - provides source and version control for our code.
  - Source control service enables teams to collaborate on code, html pages, scripts, images and binaries.
  - It is fully managed private git repository.

- Code Build

  - Automates build
  - Compiles source code, run tests, and produces packages that are ready to deploy.

- Code Deploy

  - Automates Deployment
  - Automates code deployment to any instance, including EC2, Lambda and on-premises.

- Code Pipeline
  - Manages the workflow
  - End-to-end solution, build, test, and deploy our application every time there is a code change.

_EXAM TIPS_

- continuous integration
  is all about integrating or merging code changes frequently, at least once per day, and the service they provide for this is CodeCommit.

- continuous delivery,
  and that's all about automating the build, test, and deployment functions of your release process. So think CodeBuild an CodeDeploy.

- continuous deployment,
  and that's the fully automated release process where code is deployed into staging or production as soon as it's successfully passed through the release pipeline. And the service they provide for that is called CodePipeline.

### CodeComit 101

- It is a central code repository like git.
- Allows multiple developer to work on code at same time.
- Manages updates from multiple sources
- Enables collaborations.
- Tracks and manages code changes.
- Maintains version history.

### Code Deploy 101

- Is aautomated deployment
- Works with EC2 Instances, on-premises & Lambda.
- Quickly release new feature.
- Avoid downtime during deployment.
- Avoid the risks associated with manual processes.
- 2 type of CodeDeploy Deployment approach are:
  - In-Place:
    - Application is stopped on each instance and the new release is installed. Also known as rolling update.
    - When CodeDeploy installs the new version, it is known as a Revision.
    - If we change our mind and want to rollback then we'll need to re-deploy the previous version which is time consuming.
  - Blue/Green:
    - New instances are provisioned and the new release is installed on the new instances. Blue represents the active deployment, green is the new release.
    - Traffic is routed from blue environment to green environment.
    - If we want to rollback, we just need the load balancer to direct traffic back to original(blue) environment. **Note**: this is only possible if we didn't already terminate our old environment.
- | In-Place                              | Blue/Green                                                  |
  | ------------------------------------- | ----------------------------------------------------------- |
  | Capacity is reduced during deployment | No capacity reduction                                       |
  | Lambda is not supported               | Green instances can be created ahead of time                |
  | Rolling back invokes a re-deploy      | Easy to switch between old and new                          |
  | Great when deploying the first time   | We pay for 2 environment until we terminate the old server. |

### CodeDeploy AppSpec File

- It is a codedeploy file which defines the parameter to be used during a CodeDeploy deployment.
- For EC2 and on-premises systems the AppSpec file can be written in YAML only.
- For Lambda, YAML and JSON are supported.
- File structure depends on whether we are deploying to Lambda or EC2.
- AppSpec.yml file structure
  - Version
    - Reserved for future use.
    - Currently allowed value is 0.0
  - OS
    - Operating System Version
    - The Operating System Version we are using, e.g. linux, windows.
  - files
    - Replate to configuration files and packages used during deployment.
    - Use to define the location of application file that need to be copied and where they should be copied to.
  - hooks
    - Also called as lifecycle event hooks
    - They are scripts that need to run at set points in the deployment lifecycle.
    - Hooks have a specific run order.
- Scripts that we might run during a deployment
  - Unzip Files : Unzip applicaiton files prior to deployment.
  - Run Tests : Runs functional tests on a newly deployed application.
  - Deal with Load Balancing : De-register and re-register instances with load balancer.
- We create a folder for the revision of our application so everything we need during the deployment is in the folder. Typical folder setup:
  - In the root of the folder we have appspec.yml
  - scripts in Scripts folder
  - config in Config folder
  - source in Source folder

### CodeDeploy Lifecycle Event Hooks

run order is the order the lifecycle event hooks runs in.
It is divided in 3 phases:

- Phase 1

  - De-register instances from a load balancer.

- Phase 2

  - The real nuts & bolts of the application deployment i.e. all activity need to deploy the application itself.

- Phase 3
  - Re-Register instances with the load balancer.

| Phase | Lifecycle event hook | Description                                                                                                             |
| ----- | -------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| 1     | BeforeBlockTraffic   | Covers all the task we want to run on instances before they are de-registerd.                                           |
| 1     | BlockTraffic         | This is where we actually de-register the instance from load balancer.                                                  |
| 1     | AfterBlockTraffic    | This is where we put task that we want to run after on EC2 instance after it has be de-registered from a load balancer. |
| 2     | ApplicationStop      | Gracefully stop the application. So the scripts we need to run in order to gracefully shutdown the application.         |
| 2     | Download Bundle      | CodeDeploy agent copies the application revision files to a temporary location.                                         |
| 2     | BeforeInstall        | Pre-installation scripts, e.g. backing up the current version, decrypting files. Like backup.                           |
| 2     | Install              | Copy application revision files to final location                                                                       |
| 2     | After Install        | Post-install scripts e.g. configuration, file permissions etc.                                                          |
| 2     | ApplicationStart     | Start any services that were stopped during application stop.                                                           |
| 2     | ValidateService      | Run tests to validate the service.                                                                                      |
| 3     | BeforeAllowTraffic   | Task we want to run on instances before they are registered with the load balancer                                      |
| 3     | AllowTraffic         | Register instance with a load balancer                                                                                  |
| 3     | AfterAllowTraffic    | Tasks we want to run on instances after they are registered with a load balancer                                        |

### CodePipeline

- CodePipeline is a fully managed CI/CD service which orchestrates build, test & deployment of our software release process.
- We can configure it to trigger everytime there's a change to out code.
- Due to this autoamated release process it is fast, consistent and with fewer mistakes. It enables quick release of new features and bug fixes.
- It does this by integrating with other AWS tools and some 3rd party tools like CodeCommit, CodeBuild, CodeDeploy, Github, Jenkins, Elastic Beanstalk, CloudFormation, Lambda, Elastic Container Service(allows to run container such as docker as well as windows container).

### Elastic Container Service

Allows the use of containers
What are containers?
It is a virtual operating environment.It is a standardized unit with everything the software needs to run e.g. libraries, system tools, code, and runtime. Applications are created using independent stateless components or meicroservices running in containers. We use docker to create linux containers and Windows container for windows workload.

Architecture of a docker container:
A docker container consist of code, libraries, and a virtual kernel. These container need docker to be installed to run on.

Advantages of containers

- Highly Scalable
  - If the application becomes over loaded, scale only the services we need to.
  - A single error in one container shouldn't bring down the entire app.
  - Easier to maintain/

What is ECS?
A container orchestration service which supports docker and windows container. It quickly deploy and sclae containerized workloads without having to install, configure, manage and scale our own oechestation platform.

we have 3 options to deploy the container:

- Clusters of virtual machine
  - ECS will run our container on clusters of virtual machines.
- Fargate for serverless
  - use fargate for serverless containers and we don't need to worry about the underlying EC2 instances!
- EC2 For More Control
  - If you want to control the installation, configuration and management of our compute environment.

If we have a docker container ready we need to create an ECR (Elastic Container Registry).
ECS is a place/registry where we store our container images.

_EXAM TIPS_
Containers are virtual operating environment with everything the software needs to run including libraries, system tools, code and runtime.
Allows application to be built using independent stateless components or microservices running in multiple containers.
ECS is container orchestration and allows to run container on clusters of virtual machines.
we can use fargate for severless option.
for more control select ec2 option.
ECT is where we store container images.

### Docker and CodeBuild Lab

- Docker is an open source technology which allows you to create applications based on either linux or windows containers.
- A container is a lightweight standalone executable software package which includes everything the software needs to run - code, runtime environment, libraries, environment settings etc.
- AWS provides Elastic Container Service as a fully managed clustered platform which allows us to run our docker images in the cloud.
- AWS Code build is a fully managed build service which runs a set of commands that we define, e.g. compiles code runs tests and produces artifacts that are ready to deploy.

### CloudFormation

- CloudFormation is a service that allows us to manage, configure and provision our AWS infrastructure as code.
- Resources are defined using a CloudFromation template.
- CloudFormation interprets the template and makes the appropriate API calls to create the resources we have defiend
- supports YAML or JSON
- Benefits
  - Infrastructure is provisioned consistently, with fewer mistakes
  - Less time and effort than configuring things manually.
  - We can version control and peer review our template.
  - Free to use(charge for what we create)
  - Can be used to manage updates & dependencies.
  - Can be used to rollback and delete the entire stack as well.
- CloudFormation Template
  - YAML or JSON template used to describe the endstate of the infrastructure we are provisioning or changing.
  - After creating the template, we upload it to CloudFormation using S3.
  - CloudFormation reads the template and makes the API calls on our behalf.
  - The resulting resources are called a Stack.
  - Resources is the only mandatory section of the CloudFormation template.
  - Transfpr, section is used to reference additional code stored in S3, allowing for code re-use, e.g. lambda code or template snippets.

_EXAM TIPS_

- CloudFormation allows us to manage, configure and provision AWS infrastructure as code.
- Remember the main sections in the Cloud Formation Template:
  - Parameter - input custom values
  - Conditions - e.g. provision resources based on environment.
  - Resources - mandatory - the AWS resources to create
  - Mappings - create custom mappings like Region: AMI
  - Transforms - reference code located in S3 e.g. Lambda code or reusable snippets of CloudFormation code.

### Serverless Application Model(SAM)

- Serverless Application Model (SAM) is an extension to CloudFormation used to define serverless applications.
- Simplified syntax for defining serverless resources: APIs, Lambda Functions, DynamoDB Tables etc.
- Use the SAM CLI to package our deployment code, upload it to S3 and deploy our serverless application.

_EXAM TIPS_

- SAM is the serverless application model.
- Allows you to define and provision serverless applications using CloudFormation.
- Uses the SAM CLI commands to package and deploy:
  - sam package - packages our application and uploads to S3
  - sam deploy - deploys our serverless app using CloudFormation.

### CloudFormation Nested Stacks

- Nested Stacks allow re-use of CloudFormation code for common use cases.
- e.g. Standard configuration for a load balancer, web server, application server etc.
- Instead of copying out the code each time , create a standard template for each common use case and reference from within CloudFormation Template.
- Really usefull for frequently used configurations, e.g. for load balancer, web or application servers.

_QUIZ_

1. Which of the following approaches allows you to re-use pieces of CloudFormation code in multiple templates, for common use cases like provisioning a load balancer or web server?

- Copy and paste the code into the template each time you need to use it
- Use a CloudFormation nested stack &#10004;
- Store the code you want to re-use in an AMI and reference the AMI from within your CloudFormation template
- Share the code using an EBS volume

2. When deploying application code to Lambda, the AppSpec file can be written in which language?

- Python
- JSON &#10004;
- XML
- YAML &#10004;

3. You want to receive an email whenever a user pushes code to your CodeCommit repository, how can you configure this?

- Configure a CloudWatch Events rule to send a message to SQS which will trigger an email to be sent whenever a user pushes code to the repository
- Configure a CloudWatch Events rule to send a message to SES which will trigger an email to be sent whenever a user pushes code to the repository
- Configure Notifications in the console, this will create a CloudWatch Events rule to send a notification to an SNS topic which will trigger an email to be sent to the user &#10004;
- Create a new SNS topic and configure it to poll for CodeCommit events. Ask all your users subscribe to the topic to receive notifications

4. You are deploying a number of EC2 and RDS instances using CloudFormation. Which section of the CloudFormation template would you use to define these?

- Resources &#10004;
- Outputs
- Transforms
- Instances
  The Resources section defines the resources you are provisioning. Outputs is used to output user defined data relating to the resources you have built and can also used as input to another CloudFormation stack. Transforms is used to reference code located in S3.

5. You are using CloudFormation to create a new S3 bucket, which of the following sections would you use to define the properties of your bucket?

- Parameters
- Conditions
- Outputs
- Resources &#10004;

6. When deploying application code to EC2, the AppSpec file can be written in which language?

- JSON
- XML
- JSON or YAML
- YAML &#10004;
  Appspec files for EC2/On-Prem should be written in YAML. AppSpec files for Lambda can also be written in JSON

7. Which two things can you define using the Transforms section of the CloudFormation template?

- To re-use code located in S3 &#10004;
- To specify the use of the Serverless Application Model for Lambda deployments &#10004;
- To transform API responses to a supported format
- To convert between YAML and JSON format templates
  Transforms is used to reference code located in S3 and also for specifying the use of the Serverless Application Model (SAM) for Lambda deployments.

8. Which AWS service can be used to fully automate your entire release process?

- CodeCommit
- CodeBuild
- CodePipeline &#10004;
- CodeDeploy

9. Part of your CloudFormation deployment fails due to a mis-configuration, by default what will happen?

- CloudFormation will ask you if you want to continue with the deployment
- Failed components will remain available for debugging purposes
- CloudFormation will rollback only the failed components
- CloudFormation will rollback the entire stack &#10004;

10. Which AWS service can be used to centrally store and version control your application source code, binaries and libraries?

- ElasticFileSystem
- CodeCommit &#10004;
- CodePipeline
- CodeBuild

11. In the CodeDeploy AppSpec file, what are hooks used for?

- To specify files that you want to copy during the deployment
- Hooks are reserved for future use
- To reference AWS resources that will be used during the deployment
- To specify code, scripts or functions that you want to run at set points in the deployment lifecycle &#10004;

12. Which AWS service can be used to compile source code, run tests and package code?

- CodeDeploy
- CodeCommit
- CodeBuild &#10004;
- CodePipeline

13. You want to use the output of your CloudFormation stack as input to another CloudFormation stack. Which section of the CloudFormation template would you use to help you configure this?

- Transforms
- Outputs &#10004;
- Exports
- Resources
  Outputs is used to output user defined data relating to the resources you have built and can also used as input to another CloudFormation stack. The Resources section defines the resources you are provisioning. Transforms is used to reference code located in S3.

14. You have some code located in an S3 bucket that you want to reference in your CloudFormation template. Which section of the template can you use to define this?

- Transforms &#10004;
- Files
- Inputs
- Resources
  Transforms is used to reference code located in S3 and also for specifying the use of the Serverless Application Model for Lambda deployments. The Resources section defines the resources you are provisioning. Inputs and Files are not part of the supported template syntax.

15. Which of the following practices allows multiple developers working on the same application to merge code changes frequently, without impacting each other and enables the identification of bugs early on in the release process?

- Continuous Development
- Continuous Integration &#10004;
- Continuous Delivery
- Continuous Deployment

16. Which AWS service can be used automatically install your application code onto EC2, on-premises systems and Lambda?

- CodeCommit
- CodeDeploy &#10004;
- X-Ray
- CodeBuild

17. Your company has moved to AWS so it can use "Infrastructure as Code". You would like to apply version control to your infrastructure, so that you can roll back infrastructure to a previous stable version if needed. You would also like to quickly deploy testing and staging environments in multiple regions. What services should you use to achieve this?

- OpsWorks and CodeCommit.
- Elastic Beanstalk and CodeCommit.
- DynamoDB and CloudFront.
- EC2 and RDS.
- CloudFormation and CodeCommit. &#10004;
- CloudWatch and CodeCommit.

18. How can you prevent CloudFormation from deleting your entire stack on failure?

- Set the 'Rollback on failure' radio button to No in the CloudFormation console &#10004;
- Set Termination Protection to Enabled in the CloudFormation console
- Use the --enable-termination-protection flag with the AWS CLI
- Use the --disable-rollback flag with the AWS CLI &#10004;

19. You are deploying an application to a number of EC2 instances using CodeDeploy. What is the name of the file used to specify source files and lifecycle hooks?

- buildspec.json
- appspec.yml &#10004;
- appspec.json
- buildspec.yml

## Chapter 10 : Advanced IAM

### Web Identity Federation

Web Identity Federation let us give our users access to AWS resources after they have successfully authenticated with a wen-based identity provider like Amazon, Facebook, or Google. Following successful authentication, the user receives an authentication code from the Web ID provider, which they can trade for temporary AWS security credentials.

AmazonCognito
AmazonCognito provides Web Identity Federation with the following features:

- Sign-up and sign-in to our apps.
- Access for guest users
- Acts as an Identity Broker betweeb our application and Web ID providers, so we don't need to write any additional code.
- Synchronizes user data for multiple devices
- Recommended for all mobile applications AWS services.
- The recommended approach for Web Identity Federation using social media accounts like facebook, google and amazon as well.
- Cognito brokers between the app and facebook or google to provide temporary credentials which map to an IAM role allowing access to the required resources. No need for the application to embed or store AWS credentials locally on the device and it gives users a seamless experience across all mobile devices.

### Cognito User Pools

User Pools are user directories used to manage sign0up and sign-in functionality for mobile and web applications. Users can sign-in directly to the User Pool, or indirectly via an identity provider like Facebook, Amazon, or Google. Cognito acts as an Identity Broker between the ID provider and AWS. Successful authentitcation generates a number of JSON web tokens.
Identity Pools enable us to create unique identities for our user and authenticate them with identity providers. With an identity, we can obtain temporary, liited-privilege AWS credentials to access other AWS services.

Push Synchroniztion
Cognito tracks the association between user identity and the various different devices they sign-in from. In order to provide a seamless user experience for our application, cognito uses Push Syncronization to push updates and synchronize user data across multiple devices. Amazon SNS is used to send a silent push notification to all devices assocaiated with a given user identity whenever data stored in the cloud changes.

### Inline Policies vs Managed Policies vs Custom Policies

Advanced IAM Policies
Identity Access Management (IAM) is used to define user access permissions with AWS.There are 3 different types of IAM policies available:

- Managed Policies
  - Is created and administered by AWS.
  - AWS provide managed policies for common use cases based on job function. Eg: AmazonDynamoDBFullAccess.
  - Allows us to assign appropriate permission to users, groups and roles without having to write the policy ourself.
  - A single managed policy can be attached to multiple users, groups, or roles within the same AWS account and across different accounts.
  - We cannot change the permissions defined in an AWS managed policy.
- Customer Managed Policies
  - A Customer Managed Policy is a standalone policy that we can create and administed inside our own AWS account. We can attach this policy to multiple users, groups, and roles - but only withing our own account.
  - In order to create a Customer Managed Policy, we can copy existing AWS Managed Policy and customize it to fit the requirements of our organization.
  - Recommended for use cases where the existing AWS Managed Policies don't meet the need of our environment.
- Inline Policies
  - An inline policy is an IAM policy which is actually embedded within the user group, or role to which it applies. There is a strict 1:1 relationship between the entity and the policy.
  - When we delete the user, group, or role in which the inline policy is embedded, the policy will also be deleted.
  - AWS recommend managed policies over inline policies.
  - Inline policies are useful when we want to be sure that the permission in a policy are not inadvertently assigned to nay other user, group, or role than the one for which they're intended.

### STS Assume Role With Web Identity

AssumeRoleWithWebIdentity

- assume-role-with-web-identity is an API provided by STS(Security Token Service).
- Returns temporary security credentials for users authenticated by a mobile or web application or using a Web ID Provider like Amazon, Facebook, Google
- For mobile applications, Cognitio is recommended
- Regular web applications can use the STS assume-tole-with-web-identity API

### Cross Account Access

What is Cross Account Access?
Many AWS customers use separate AWS accounts for their development and production resources. This separation allows them to cleanly seperate different types of resources and can also provide some security benefits. Cross Account Access make it easier for us to work productively within a multi-account AWS environment by making it easy for us to switch roles withing the AWS Management Console. We can now sign in to the console using our IAM username then switch the console to manage another account without having to enter another username and password.

_Quiz_

1. Which statement best describes IAM?

- IAM allows you to manage users' passwords only. AWS staff must create new users for your organization. This is done by raising a ticket.
- IAM stands for Improvised Application Management, and it allows you to deploy and manage applications in the AWS Cloud.
- IAM allows you to manage permissions for AWS resources only.
- IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform. &#10004;

2. Amazon Cognito provides Web Identity Federation with which of the following features?

- Sign-up and sign-in to your applications &#10004;
- Single sign-on for Active Directory users
- Synchronization of user data across multiple device types &#10004;
- Multi-Factor Authentication

3. What does Cognito use to manage sign-up and sign-in functionality for mobile and web applications?

- Identity Pools
- IAM Groups
- IAM Users
- User Pools &#10004;

4. Which of the following services can be used to securely store confidential information like credentials and license codes so that they can be accessed by EC2 instances?

- KMS
- Systems Manager Parameter Store &#10004;
- DynamoDB
- IAM
- AWS Systems Manager Parameter Store provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, and license codes as parameter values.

5. You are working on a mobile phone app for an online retailer that stores customer data in DynamoDB. You would like to allow new users to sign-up using their Facebook credentials. What is the recommended approach?

- Embed encrypted AWS credentials into the application code, so that the application can access DynamoDB on the user's behalf.
- Write your own custom code which allows the user to log in via Facebook and receive an authentication token, then calls the AssumeRoleWithWebIdentity API and exchanges the authentication tokens for temporary access to DynamoDB
- After the user has authenticated with Facebook, allow them to download encrypted AWS credentials to their device so that the mobile app can access DynamoDB
- After the user has successfully logged in to Facebook and received an authentication token, Cognito should be used to exchange the token for temporary access to DynamoDB &#10004;

6. Which of the following are provided by AWS to allow you to easily assign IAM permissions to your users based on pre-defined common use cases?

- Custom Policy
- Inline Policy
- Common Policy
- Managed Policy &#10004;

7. Which of the following correctly describes an Inline Policy?

- It is embedded in a user, group or role &#10004;
- The policy will be deleted if you delete the user, group or role it is associated with &#10004;
- You cannot change the permissions defined in the policy
- It can be attached to multiple users and groups within your AWS account

8. Amazon Cognito is recommended for which use case?

- Anonymous access to AWS resources
- Web Identity Federation for mobile applications &#10004;
- Secure storage of database connection strings
- Identity Federation with Active Directory

9. Which of the following API calls can be used to enable a user authenticated by Facebook to access your web application hosted in AWS?

- STS get-federation-token
- STS assume-role
- STS assume-role-with-saml
- STS assume-role-with-web-identity &#10004;

10. You are developing a new mobile application to share photos, which AWS technology can you use to ensure your users have a seamless experience across all their devices?

- IAM
- Web Identity Federation
- Multi-Factor Authentication
- Cognito &#10004;

11. What does Cognito use to create unique identities for users and authenticate them with Web ID providers?

- Identity Pools &#10004;
- IAM Users
- User Pools
- IAM Groups

12. Which of the following correctly describes a Customer Managed Policy?

- It is managed by you &#10004;
- It can be assigned to multiple users, groups or roles in your account &#10004;
- It is created and administered by AWS
- The policy will be deleted if you delete the user, group or role it is associated with

13. Which of the following features of IAM allows you to have your users Authenticate using Facebook, Google or Amazon?

- Web Identity Federation &#10004;
- AWS Single Sign-On (SSO)
- Multi-Factor Authentication
- The IAM HTTPS API

14. How can you allow a user from one AWS account to access and manage resources in another AWS account?

- Configure cross-origin resource sharing
- Configure Cognito
- Configure web identity federation
- Configure cross-account access &#10004;

15. What is the name of the service that allows users to use their social media account to gain temporary access to the AWS platform?

- Active Directory Authentication Services
- Web Identity Federation &#10004;
- Web Confederation Services
- Facebook Sign-In Service

16. Which of the following applies to an AWS Managed Policy?

- It can only be assigned to a single user, group or role in your account &#10004;
- It can be assigned to multiple users, groups or roles &#10004;
- It is available for use by any AWS account
- You can change the default permissions defined in the policy
- AWS occasionally updates the permissions defined in an AWS managed policy &#10004;

17. When using Web Identity Federation to allow a user to access an AWS service (such as an S3 bucket), which of the following is the correct order of steps?

- A user makes the AssumeRoleWithWebIdentity API Call. The user is then redirected to Facebook to authenticate. Once authenticated, the user is given an ID token. The user is then granted temporary access to the AWS platform.
- A user authenticates with Facebook first. They are then given an ID token by Facebook, which they can then trade for temporary security credentials. &#10004;
- Users cannot use Facebook credentials to access the AWS platform.
- A user logs in to the AWS platform using their Facebook credentials. AWS authenticate with Facebook to check the credentials. Temporary Security Access is granted to AWS.

18. When would you use an Inline Policy over a Managed Policy?

- To add IAM permissions that can be applied to multiple AWS accounts that you own
- To add IAM permissions for common use cases like giving your DBAs full access to DynamoDB
- When you want to manage the policy yourself
- To add permissions that are only ever intended to be used for a single user in your account &#10004;

## Chapter 11 : Monitoring

### Introduction to CloudWatch

Amazon CloudWatch is a monitoring service to monitor our AWS resources, as well as the application that runs on AWS.
CloudWatch can monitor things like :

- Compute
  - Autoscaling Groups
  - Elastic Load Balancers
  - Route53 Health Checks
- Storage & Content Delivery
  - EBS Volumes
  - Storage Gateways
  - CloudFront
- Database & Analytics
  - DynamoDB
  - Elasticache Nodes
  - RDS Instances
  - Elastic MapReduce Job Flows
  - Redshift
- Other
  - SNS Topics
  - SQS Queues
  - Opsworks
  - CloudWatch Logs
  - Estimated Charges on AWS Bill.

Host Level Metrics Consist of:

- CPU
- Network
- Disk
- Status Check

How Long can is it retention?
we can retrive data using GetMetricStatstics API or by using a thrid party tools offered by AWS partners. We can store our log data in CloudWatch Logs for as long as we want. By default, CloudWatch Logs will store our log data indefinitely. We can change the retention for each Log Group at any time.

Metric Granularity?
It depends on the AWS service. Many default metrics for many default services are 1 minute, but it can be 3 or 5 minutes depending on the service.

CloudWatch Alarms
We can create an alarm to monitor any amazon cloudwatch metric in our account. This can include EC2 CPU Utilization, Elastic Load Balancer Latency or even the charges on our AWS bill. We can set the appropriate thresholds in which to trigger the alarms and also set what actions should be taken if an alarm state is reached. This will be covered in a subsequent lecture.

_EXAM TIP_
RAM Utilization is a custom metric~ By default EC2 monitoring is 5 minute intervals, unless you enable detailed monitoring which will then make it 1 minute intervals.
`We can retrive data from any terminated EC2 or ELB instance after its termination.`
For Custom metrics the minimum granularity that we can have is 1 minute.
CloudWatch can be used on premise - Not restricted to just AWS resources. Can be on premise too. Just need to download and install the SSM agent and Cloudwatch agent.

### CloudWatch vs CloudTrail vs Config

CloudWatch monitors performance like CPU, memory, Disk utilzation or RAM Utilization.
CloudTrail monitors the API calls in the AWS platform like if we provision any EC2 instance, S3 bucket or DynamoDB table. Records the time it was provisioned, what was provisioned, wether it was provisioned successfully etc.
AWS Config records the state of your AWS environment and can notify we changes. It records the state of AWS environment and will notify of change.

_Quiz_

1. Which of the following tools can be used to determine who provisioned an EC2 instance and what time they made the API call?

- CloudFormation
- CloudTrail &#10004;
- IAM
- CloudWatch

2. Which of the following services can you use to monitor and report on performance metrics for your AWS Infrastructure?

- CloudWatch &#10004;
- CloudFormation
- CloudTrail
- X-Ray

3. Which of the following tools can you use to monitor CPU utilization metrics for your EC2 instances?

- CloudFormation
- CloudTrail
- X-Ray
- It can only be assigned to a single user, group or role in your account
- CloudWatch &#10004;

4. Which of the following services can you use to monitor all API activity in your AWS account?

- IAM
- CloudFormation
- CloudWatch
- CloudTrail &#10004;

## Chapter 12 : Course Updates Based on Student Feedback

### SQS Delay Queue & Managing Large Messages

- SQS Delay Queues

  - Postpone delivery of new messages to a queue for a number of seconds.
  - Messages sent to the delay queue remain invisible to consumers for the duration of the delay period.
  - Default delay is 0 seconds, maximum is 900 seconds.
  - For standard queues, changing the setting doesn't affter the delay of messages already in the queue, only new messages.
  - For FIFO queues, this affecs the delay of messages already in the queue.
  - When to use the delay queue?
    - Large distributed applications which may need to introduce a delay in processing.
    - You need to apply a delay to an entire queue of messages.
    - e.g. adding a delay of a few seconds, to allow for updates to our sales and stock control databases before sending a notification to a customer confirming an online transaction.

- Managing large SQS Messages
  - Best practice for Managing Large SQS Messages Using S3
    - For large SQS messages - 256KB upto 2GB in size.
    - Use S3 to store the messages
    - Use Amazon SQS Extended Client Library for Java to manage them. It allows us to
      - Specify that messages are always stored in Amazon S3 or only messages > 256 KB
      - Send a message which references a message object stored in S3
      - Get a message object from S3
      - Delete a message object from S3
    - We will also need the AWS SDK for JAVA - provides an API for S3 bucket and object operations.
    - Can't be done using AWS CLI, AWS management Console / SQS Console, SQS API.

### AWS CLI Pagination

- We can contorl the number of items included in the output when we run a CLI command.
- By default, the AWS CLI uses a page size of 1000.
- i.e. if we run aws s3api list-objects my_bucket - on a bucket with 2,500 objects, the CLI actually makes 3 API calls to S3...but displays the entire output in one go.
- If we esee errors when running list commands on a large number of resources the default page size of 1000 might be too high.
- We are most likely to see "timed out" error, because the API call has exceeded the maximum allowed time to fetch the required results.
  - To fix this, use the --paze-size option to have the CLI request a smaller number of items from each API call.
  - The CLI still retrieves the full list, but performs a larger number of API calls in the backgroud and retrieves a smaller number of items with each call.

### Testing IAM permission

- IAM Policy Simulator
  - Test the effect of IAM policies before commiting them to production.
  - Validate that the policy works as expected.
  - Test policies already attached to existing users - great for troubleshooting an issue which use suspect is IAM related.
  - [http://policysim.aws.amazon.com](http://policysim.aws.amazon.com)

### Kinesis Shards vs Consumers

- The Kinesis Client Library running on our consumers creates a record processor for each shard that is being consumed by our instance.
- If we increase the number of shards, the KCL will add more record processors on our consumers.
- CPU utilisation is what should drive the quantity of consumer instance we have, NOT the number of shards in our kinesis stream.
- Use an Auto Scaling group, and base scaling decisions on CPU load on our comsumers.

### Lambda Concurrent Execution Limit

- Concurrent Executions
  - Not necessary to memorize lots of limits for the exam.
  - Be aware that there is a concurrent execution limit for lambda.
  - Safety feature to limit the number of concurrent executions across all functions in a given region per account.
  - Default is 1000 per region.
  - If we exceed it we get `TooManyRequestsException` error message wit hHTTP Status Code 429.
  - We can request AWS support to exceed the request throughtput limit.
  - If we have many lambda functions running in the same region and we suddenly start seeing new invocation requests being rejected, then we may have hit our limit.
  - Request an increase on this limit by submitting a request to the AWS Support Center.
  - Reserved concurrency guarantees that a set number of executions which will alaways be available for our critical function, howeve this also acts as a limit.

### Lambda Versions

- When we create a lambda function, there is only one version: \$LATEST
- When we upload a new version of the code to Lambda, this version will become \$LATEST
- We can create multiple versions of our function code and use aliases to reference the version we want to use as part of the ARN.
- e.g. In a developement environment we might want to maintain a few versions of the same function as we develop and test our code.
- An alias is like a pointer to a specific version of the function code.

### Lambda and VPCs

- Enabling lambda to access our VPC resources.
  - Some use case require Lambda to access resources which are inside a private VPC.
  - e.g. read or write to an RDS database, or shutdown an EC2 instance in response to a security alert.
  - to enable this, we need to allow the function to connect the private subnet.
  - Lambda needs the following VPC configuration information so that it can connect to the VPC:
    - Private subnet ID
    - Security group ID (with required access)
    - Lambda uses this information to setup ENIs (Elastic Network Interface) using an available IP address from our private subnet.
  - we can add VPC information to our Lambda function config using the vpc-config parameter. `aws lambda update-function-configuration --function-name my-function --vpc=config SubnetIds=subnet-1122aabb,SecurityGroupIds=sg-51530134`

### X-Ray Configuration

- X-ray integrates with many AWS services like DynamoDB, Lambda, API Gateway, etc.
- we can also instrument our own applications to send data to X-Ray.
- Applications can be running on EC2, Elastic Beanstalk environments, on-premises systems and ECS.
- For ECS, run the X-Ray daemon in it's own Docket image, running alongside our application.
- We need 3 things to get started:
  - X-Ray SDK
  - X-Ray daemon
  - Instrument our application using the SDK to send the required data to X-Ray, e.g. data about incoming HTTP requests to our application.
- If we want to also record application specific information in the form of key-value pairs, use annotations to add user defiened key-value pairs to our X-Ray data - allows us to filter, index and search within X-Ray, e.g. game_name=TicTacToe, game_id=2645445842

### Deploying Docker using Elastic Beanstalk

- Elastic Beanstalk & Docker Containers
  - Elastic Beanstalk supports the deployment of Docker containers.
  - Docker containers are self-contained and include all the configuration and software our web application requires to run.
  - Elastic Beanstalk handles the capacity provisioning, load balancing, scaling, and application health monitoring.
  - when using Elastic Beanstalk, we can deploy our dowcker container to a single EC2 instance.
  - we can also deploy multiple docker instances to ECS cluster.
  - To deploy a docker application just upload your code bundle to Elastic Beanstalk.
  - To upgrade our application to a new version, it's one easy step in the console to upload and deploy our new version.
  - Code can be uploaded directly from our local machine or public S3 bucket.
  - We can also store our code in CodeCommit - but must use the Elastic Beanstalk CLI

### Additional Study Material

- FAQs on [aws.amazon.com/faqs](aws.amazon.com/faqs)
  - Serverless
    - Lambda
    - API Gateway
    - DynamoDB
    - ElasticCache
    - S3
  - Automation & Monitoring
    - ElasticBeanStalk, CloudFormation, CloudWatch, X-Ray
  - Dev Tools
    - CodeCommit, CodePipeline, CodeDeploy, CodeBuild
  - Containers
    - ECS and ECR
  - Security
    - IAM, Cognito, KMS
  - Messaging & Streaming
    - SQS, Kinesis
- Whitepapers
  - Practicing CI / CD on AWS
  - Introduction to DevOps on AWS
  - Blue/Green Deployments on AWS
  - Serverless Architectures with Lambda
  - Docket on AWS: Running Containers in the Cloud
  - Running Containerized Microservices on AWS
  - Optimizing Enterprise Economics with Serverless Architectures
  - AWS Security Best Practices

_Quiz_

1. You would like to enable your Lambda function to access EC2 instances in your own private VPC. How can you configure Lambda to allow this?

- Update the permissions in your VPC to allow Lambda to access the EC2 instances
- Launch the Lambda function inside the VPC so that it can access the EC2 instances
- Update the EC2 instance role to allow Lambda to access the EC2 instances
- Provide VPC config information using the Lambda console or CLI &#10004;
  By default, Lambda runs your functions in a secure VPC with access to AWS services and the internet. However, by default, it does not have access to resources created in your private VPCs. To connect your function to a VPC during creation, or to update an existing function, you can use the vpc-config option with a list of private subnet IDs and security groups. Please note that AWS are simplifying this, so that it will become easier and changes are to be rolled our on a per region basis. This was announced in September 2019 and we are not expecting the exam to be updated for at least 6 months. (The exams usually run at least 6-12 months behind latest announcements). So unfortunately, you may well still see questions relating to providing VPC config information to Lambda functions.

2. Your application is running on EC2 and consuming click stream data from a Kinesis stream, using the Kinesis Client Library. You have recently increased the number of shards in your Kinesis stream. When should you consider increasing the number of EC2 instances consuming the stream?

- You should add more instances as soon as you reshard
- You should base scaling decisions on appropriate metrics for your application, like CPU utilization &#10004;
- You should add more instances before you reshard
- You should base scaling decisions on if issues are experienced after the resharding
  When resharding increases the number of shards in the stream, the corresponding increase in the number of record processors increases the load on the EC2 instances that are hosting them. If the instances are part of an Auto Scaling group, and the load increases sufficiently, the Auto Scaling group adds more instances to handle the increased load. You should configure Auto Scaling to automatically scale your instances based on appropriate metrics, e.g. CPU utilization.

3. What is an SQS Delay Queue?

- A Delay Queue is a queue that lets you postpone the delivery of new messages until a critical application function has been acknowledged as completed.
- A Delay Queue is designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated.
- A Delay Queue is a queue that lets you postpone the delivery of new messages to a queue for a number of seconds. &#10004;
- A Delay Queue is a queue that lets you postpone the delivery of new messages indefinitely.
  Delay queues let you postpone the delivery of new messages to a queue for a number of seconds. If you create a delay queue, any messages that you send to the queue remain invisible to consumers for the duration of the delay period. The default (minimum) delay for a queue is 0 seconds. The maximum is 15 minutes.

4. Your web application is running on Lambda, API Gateway, DynamoDB and S3 and you have recently seen a significant increase in traffic to your website. The application support team are now reporting that Lambda invocations are being rejected with a 429 HTTP status code. What could be causing this?

- You have reached the default concurrent executions limit for Lambda &#10004;
- You have reached the default concurrent requests limit for API Gateway
- You have reached the default concurrent requests limit for S3
- You have reached the default concurrent requests limit for DynamoDB
  AWS Lambda limits the amount of compute and storage resources that you can use to run and store functions, including a Concurrent Executions limit, which is set to 1000 per region, by default. To request an increase, use the Support Center console.

5. You would like to use X-Ray to monitor your application which runs on a number of Docker containers. Where should you deploy and run the X-Ray daemon?

- The X-Ray daemon will already be installed on the underlying EC2 instance by default
- Install the X-Ray daemon on Lambda
- Use a dedicated Docker container build from an image which includes the X-Ray daemon &#10004;
- Install the X-Ray daemon on the underlying EC2 instance
  X-Ray provides a Docker container image that you can deploy alongside your application. For custom configuration, you may need to define your own Docker image.

6. You have been asked to suggest a solution for storing large SQS messages. Which of the following is the most suitable?

- EC2
- RDS
- ElastiCache
- DynamoDB
- S3 &#10004;
  You can use Amazon S3 and the Amazon SQS Extended Client Library for Java to manage Amazon SQS messages. This is especially useful for storing and consuming messages up to 2 GB in size. Unless your application requires repeatedly creating queues and leaving them inactive or storing large amounts of data in your queue, consider using Amazon S3 for storing your data. This cannot be done natively with any of the other listed services

7. Which of the following can you use to test that an IAM policy attached to a user, group or role works as expected?

- IAM Policy Simulator &#10004;
- IAM Tester
- Lambda
- Trusted Advisor
  You can use the IAM Policy Simulator test policies that are attached to IAM users, groups, or roles in your AWS account. If more than one policy is attached to the user, group, or role, you can test all the policies, or select individual policies to test. You can test which actions are allowed or denied by the selected policies for specific resources.

8. You are trying to configure X-Ray to monitor Java applications running on your EC2 instances. Which of the following will be required in order to get X-Ray working?

- You will need to restart your application
- You will need to Instrument your application &#10004;
- You will need to restart your instance
- The X-Ray SDK will need to be installed on your EC2 instances &#10004;
- You will need to install the CloudWatch agent
- The X-Ray daemon will need to be installed and running on your EC2 instances &#10004;
  Both the X-Ray SDK and X-Ray Daemon, and you need to Instrument your application. Your application will need to be deployed with the additional code, specifying the details you want AWS X-Ray to capture. This is done using the X-Ray SDK, which provides a programmatic interface for your application to send information to the X-Ray Daemon. Once the X-Ray Daemon has received the information, it will send the information to AWS X-Ray to be reviewed. This requires both the X-Ray SDK and X-Ray Daemon to be installed. You will not need to restart your instance, since any additional IAM Roles can be added without shutting down the instance. Your may not need to restart your application, depending on its architecture. CloudWatch is a separate service, and it's agent is not required for X-Ray

9. You are running your application using Docker provisioned with Elastic Beanstalk. You would like to upgrade the application to a new version. How should you approach this?

- Create a new Docker image using the latest code, deploy it using Elastic Beanstalk, then terminate your old environment
- Bundle your code into a zip file, upload and deploy it using Cloud Formation
- Bundle your code into a zip file, upload and deploy it using the Elastic Beanstalk console &#10004;
- Create a new Docker image using the latest code, log in to the underlying EC2 instance and install the new Docker image
  Elastic Beanstalk supports the deployment of web applications from Docker containers. With Docker containers, you can define your own runtime environment. Each time you upload a new version of your application with the Elastic Beanstalk console or the EB CLI, Elastic Beanstalk creates an application version. When using the console you can choose to upload and deploy your code in a single step. Elastic Beanstalk will manage the previous version of your code so you can revert back to it if necessary.

10. You see a "timed out" error when using the AWS CLI to list all the files in an S3 bucket containing thousands of files. What is the reason for this?

- Too many results are being returned which is causing the command to time out &#10004;
- You have not installed the AWS CLI correctly
- You don't have the correct permission to run the command
- Your network connection is too slow
  If you see issues when running list commands on a large number of resources, the default page size of 1000 might be too high. This can cause calls to AWS services to exceed the maximum allowed time and generate a "timed out" error. To avoid this, you can use the --page-size option to specify that the AWS CLI request a smaller number of items from each call to the AWS service.

11. Your application relies on a number of Lambda functions. During testing, you would like to make sure you are always using the the latest version of the function. How can you ensure that your application always launches the very latest version of your code?

- Publish a new version of your function based on the specific version of code that you would like to use
- Reference the function using the \$LATEST suffix &#10004;
- Create a qualified ARN which points to the specific version of code that you would like to use
- Create an alias and reference the function using the alias
  When you create a Lambda function, there is only one version—the $LATEST version. You can use either the qualified or unqualified ARN in your event source mapping to invoke the $LATEST version. If you always want to use the latest version of code, avoid using your own alias or any specific Lambda version as these will not be updated when new code is uploaded to Lambda.

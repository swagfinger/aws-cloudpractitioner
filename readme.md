# AWS Cloud Practitioner
* CLF-C01
* Learning about AWS eco-system and AWS features.
---

## Table of contents

### 01. [Create an AWS account](#01-create-an-aws-account)

### 02. [Summary](#02-summary)

### 03. [Cloud Computing](#03-cloud-computing)
  + [5 characteristics of cloud computing](#5-characteristics-of-cloud-computing)
  + [6 advantages of cloud computing](#6-advantages-of-cloud-computing)
  + [problems solved by the cloud](#problems-solved-by-the-cloud)
  + [Types of cloud computing](#types-of-cloud-computing)
  + [pricing of the cloud](#pricing-of-the-cloud)
  + [AWS Global infrastructure](#aws-global-infrastructure)
  
### 04. [IAM (identity and access management)](#04-iam-identity-and-access-management)
  + [IAM Policies](#iam-policies)
    + [IAM policy structure](#iam-policy-structure)
  + [Protecting user accounts](#protecting-user-accounts)
    + [Password policy](#password-policy)
    + [Multi Factor Authentication (MFA)](#multi-factor-authentication-mfa)
  + [3 ways to access AWS](#3-ways-to-access-aws)
  + [Access keys](#access-keys)
  + [AWS CloudShell](#aws-cloudshell)
  + [IAM roles for AWS Services](#iam-roles-for-aws-services)
  + [IAM security tools](#iam-security-tools)
  + [IAM Shared responsibility model](#iam-shared-responsibility-model)
  + [Summary](#iam-summary)

### 05. [EC2 - Elastic Compute Cloud](#05-ec2-elastic-compute-cloud)
  + [What can you do with EC2?](#what-can-you-do-with-ec2)
  + [EC2 Virtual server - options](#ec2-virtual-server-options)
  + [creating an EC2 instance with EC2 User Data](#creating-an-ec2-instance-with-ec2-user-data)
  + [7 different types of EC2 instances](#7-different-types-of-ec2-instances)
  + [Security Groups](#security-groups)
    - [Ports you need to know](#ports-you-need-to-know)
  + [SSH](#ssh)
  + [Instance Launch types](#instance-launch-types)
  + [Shared responsibility model](#shared-responsibility-model)
  + [Summary](#summary)
  
### 06. [EC2 - Instance Storage](#06-ec2-instance-storage)
  + [EBS Volume](#ebs-volume)
  + [EBS Snapshot](#ebs-snapshot)
  + [AMI](#ami)(
  + [EC2 Image Builder](#ec2-image-builder)
  + [EC2 Instance Store](#ec2-instance-store)
  + [EFS (Elastic file system)](#efs-elastic-file-system)
  + [EBS vs EFS](#ebs-vs-efs)
  + [Shared responsibility model for EC2 Storage](#shared-responsibility-model-for-ec2-storage)
  + [Amazon FSx](#amazon-fsx)
  + [Summary](#ec2-instance-storage-summary)

### 07. [ELB & ASG - Elastic Load Balancing & Auto Scaling Groups](#07-elb-and-asg-elastic-load-balancing-and-auto-scaling-groups)
  + [High availability, Scalability, elasticity](#high-availability-scalability-elasticity)
  + [Elastic Load Balancing (ELB)](#elastic-load-balancing-elb)

### 08. [S3](#08-s3)

### 09. [Databases and Analytics](#09-database-and-analytics)

### 10. [Other compute services](#10-other-compute-services)
  + [what is docker?](#what-is-docker)
  + [ECS, Fargate & ECR Overview](#ecs-fargate-&-ecr-overview)
    + [ECS (for Docker)](#ecs-for-docker)
    + [Fargate (for Docker)](#fargate-for-docker)
    + [ECR](#ecr)
  + [Serverless](#serverless)
  + [Why lambda?](#why-lambda)
  + [Benefits of Lambda](#benefits-of-lambda)
  + [AWS lambda language support](#aws-lambda-language-support)
  + [API Gateway Overview](#api-gateway-overview)
  + [Batch overview](#batch-overview)
  + [Lightsail overview](#lightsail-overview)
  + [summary-Other compute services](#summary-10-other-compute-services)

### 11. [Deploying and managing infrastructure at scale](#11-deploying-and-managing-infrastructure-at-scale)

  ###### Deployment services
  + [CloudFormation](#cloudformation)
  + [cloud development kit CDK](#cdk)
  + [Beanstalk](#beanstalk)
  + [AWS Systems Manager (SSM)](#aws-systems-manager-ssm)
  + [Systems Manager - SSM Session Manager](#systems-manager-ssm-session-manager)
  + [Opsworks](#opsworks)

  
  ###### Developer Services
  + [AWS CodeDeploy](#aws-codedeploy)
  + [AWS CodeCommit](#aws-codecommit)
  + [AWS CodeBuild](#aws-codebuild)
  + [AWS CodePipeline](#aws-codepipeline)
  + [AWS CodeArtifact](#aws-codeartifact)
  + [AWS CodeStar](#aws-codestar)
  + [AWS Cloud9](#aws-cloud9)

### 12. [Leveraging AWS Global infrastructure](#12-leveraging-aws-global-infrastructure)

  + [Why use global applications?](#why-use-global-applications)
  
  ###### Global Applications in AWS
  + [Global DNS (Route53)](#global-dns-route53)
  + [Global CDN (CloudFront)](#global-cdn-cloudfront)
    + [CloudFront vs Cross Region Replication?](#cloudfront-vs-cross-region-replication)
  + [S3 Transfer Acceleration](#s3-transfer-acceleration)
  + [AWS Global accelerator](#aws-global-accelerator)
    + [Global Accelerator vs CloudFront?](#global-accelerator-vs-cloudfront)
  + [AWS Outposts](#aws-outposts)
  + [AWS Wavelength](#aws-wavelength)
  + [AWS Local Zones](#aws-local-zones)
  --
  + [Global Applications Architecture](#global-applications-architecture)
  + [Summary - Leveraging AWS Global Infrastructure](#summary-leveraging-the-aws-global-infrastructure)

### 13. [Cloud Integrations](#13-cloud-integrations)
  + [SQS (Simple Queue service)](#sqs-simple-queue-service)
  + [SNS (Simple notification services)](#sns-simple-notification-services)
  + [Kinesis](#kinesis)
  + [Amazon MQ](#amazon-mq)
  + [Summary](#summary-13-cloud-integrations)

### 14. [Cloud monitoring](#14-cloud-monitoring)

### 15. [VPC & Networking](#15-vpc-and-networking)

### 16. [Security and Compliance](#16-security-and-compliance)

### 17. [Machine Learning](#17-machine-learning)

### 18. [Account management, Billing and support](#18-account-management-billing-and-support)

### 19. [Advanced Identity](#19-advanced-identity)

### 20. [Other Services](#20-other-services)

### 21. [AWS architecting and Ecosystem](#21-aws-architecting-and-ecosystem)

---
---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 01. Create an AWS account

* does need a credit card, to verify identity (authorization)
* Stay on the AWS free tier
* root user account / password


---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 02. Summary

#### Summary - 04. IAM Section
* users: mapped to a physical user; has a password for AWS Console
* groups: contain users only
* policies: JSON document that outlines permissions for users or groups
* Roles: for EC2 instances or AWS services
* Security: MFA + password policy
* AWS CLI: manage your AWS services using the command line
* AWS SDK: manage your AWS services using a programming language
* Access keys: access AWS using CLI or SDK
* Audit: Credential Reports & IAM Access advisor

#### Summary - 05. EC2 Elastic Compute cloud
* EC2 instances: AMI (OS) + instance size (CPU+RAM) + storage + security groups + EC2 user data
* Security groups: firewall attached to EC2 instance
* EC2 user data: script launched at first start of instance
* SSH: start a terminal into our EC2 instances (port 22)
* EC2 instance role: link to IAM roles
* purchasing options: on-demand, spot, reserved(standard + convertible + scheduled), dedicated hosts , dedicated instance.

#### Summary - 06. EC2 Instance Storage
* EBS volumes
  - network drives attached to one EC2 instance at a time
  - mapped to AZ
  - can use EBS snapshot for backups / transfering EBS volumes across AZ
* AMI - create ready-to-use EC2 instances within our customizations
* EC2 Image builder - automatically build, test, distribute AMI's
* EC2 instance store - high performance harddrive attached to EC2
  - lost if instance is stopped /terminated
* EFS - network file system, can be attached to 100s of instances in a region
* EFS-IA - cost-optimized storage class for infrequent accessed files
* FSx for windows - Network file system for Windows server.

#### Summary - 07. ELB and ASG
* High Availability vs Scalibility (vertical vs horizontal) vs Elasticity vs agility in the cloud
* Elastic Load Balancers(ELB)
  - Distribute traffic across backend EC2 instances, can be multi-Az
  - support health checks
  - 3 types: Application LB (http-L7), Network LB (TCP-L4), Classic LB (old)
* Auto Scaling group (ASG)
  - implement the elasticity of application, across multiple AZ.
  - scale EC2 instances based on the demand of your system, replace unhealthy
  - integrated with ELB

#### Summary - 10. Other Compute services
* Docker - container technology allowing you to run applications
* ECS - run docker containers on EC2 instances
* Fargate - run docker containers without provisioning the infrastructure - serverless (no EC2 instances)
* ECR - private docker images repository
* Batch - run batch jobs on AWS across managed EC2 instances
* lightsale - predictable & low pricing for simple application & db stack
* lambda - serverless FaaS (function as a service), seamless scaling, reactive
  * Lambda billing - by time run * RAM provisioned
  * number of invocations
  * invocation time up to 15min
  * use cases: 
      * create thumbnails for images uploaded to AWS S3
      * CRON job
  * API gateway exposes lambda functions as http APIs

#### Summary - 12. Leveraging the AWS Global Infrastructure
* Global DNS: Route 53
  - greate to route users to closest deployment with least latency
  - great for disaster recovery strategies
* Global Content Delivery Network (CDN): CloudFront
  - Cache common requests - improves user experience and decreased latency
* S3 Transfer Acceleration
  - Accelerate global uploads and downloads into Amazon S3
* AWS Global Accelerator
  - improve global application availability and performance using the AWS global network.
* AWS Outposts
  - Deploy Outpost racks into your own Data centers to extend AWS services
* AWS WaveLength
  - Brings AWS services to the edge of 5g networks
  - Ultra low latency applications
* AWS Local Zone
  - Bring AWS Resources (Compute, database, storage) closer to your users
  - Good for Latency-sensitive applications.

#### summary - 13. cloud integrations
* SQS 
  - queue service in AWS
  - multiple producers, messages are kept up to 14 days.
  - multiple consumers share the read and delete messages when done.
  - used to decouple applications in AWS

* SNS
  - Notification service in AWS
  - Subscribers: Email, lambda, SQS, HTTP, Mobile etc
  - Multiple subscribers -> send all messages to all of them
  - no message retention

* Kinesis: real-time data streaming, persistence and analysis
* Amazon MQ: Managed Apache MQ in the cloud (MQTT, AMQP etc ...protocols)
--- 
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 03. Cloud computing
* Cloud computing is the on-demand delivery of compute power, database storage, applications and other IT resources.
* Cloud allows pay-as-you-go-pricing
* provision exact type and size of computing
* instance access
* AWS cloud has nice interface to access these services.
* AWS owns and maintains the network-connected hardware requried for these application services, while you provision and use what you need via a web application.
The Cloud is the solution to externalize all the problems with traditional data centers.
* the cloud has its own data center, servers.

How Websites work
* a server hosts a website
* a have a client that makes a request via browser for resource on server
* network routes packets (data) to server - request
* server makes a response
* client views the website

for client to find server and server to respond to client, both need IP addresses for routing.

#### what makes a Server  
* CPU
* memory (RAM)
* Storage data
* database (formatted data)
* network aspect: routers, switch, DNS server

#### problems with traditional data centers
* rent space
* pay for power, cooling, maintenance
* time to add/replace servers
* scaling is limited
* hire someone 24/7 to monitor infrastructure

#### deployment models of the cloud
private cloud 
* eg. Rackspace
* service used by single organization, not exposed to public. complete control, security.

public cloud 
* AWS / Google cloud / Microsoft Axure
* cloud resources owned by 3rd party cloud service provider are delivered over the internet.

Hybrid Cloud
* keep some servers on premises, extend capabilities to cloud.

##### 5 characteristics of cloud computing
* on demand service - users can provision these resources without intervention from AWS.
* broad network access - access to resources
* multi-tenancy and resource pooling - multiple customers can benefit from same infrastructure + security
* rapid elasticity and scalibility - quickly acquire and dispose resources / scale on demand
* measured service - pay for what you use

##### 6 advantages of cloud computing
1. trade capital expense (CAPEX) for operational expense (OPEX)
    - pay on demand - don't own hardware
    - reduce total cost of ownership (TCO) and Operational Expense (OPEX)
2. benefit from advantages of scale
    - prices lower because more effienct due to large scale use
3. stop guessing capacity
    - scale based on actual measured usage
4. increase speed and agility
5. no data center costs (running and maintaining)
6. go global in minutes - leverages the AWS global infrastructure.

##### problems solved by the cloud
* flexibility
* cost effective
* scalability
* elasticity
* high-availability
* agility

#### Types of cloud computing

##### infrastructure as a service (IaaS)
  - networking, computers, data storage space
  - we care about application and data and runtime / middleware / OS
  - eg. Amazon EC2 

##### platform as a service (PaaS)
  - removes need for organization to manage the infrastructure
  - we only care about the application and data
  - eg. Elastic Beanstalk, Heroku, Google App Engine (GCP), MS Axure

##### Software as a service (SaaS)
  - completed product that is run and managed by service provider
  - many aws service eg. Rekognition, machine learning, google apps, dropbox

#### Pricing of the cloud
3 pricing fundamentals
* Compute - pay for compute time
* storage - pay for data stored in the cloud
* networking - pay for data transferred out of the cloud

#### AWS Global infrastructure

[https://infrastructure.aws](https://infrastructure.aws)
##### AWS regions
- named eg. us-east-1
- region is a cluster of data centers
- most AWS services are region scoped

  ##### How to choose an AWS Region?
  * compliance - data governance and legal requirements, data never leaves the region
  * proximity - closer to users for lower latency
  * available service within a region - new services arent available in every region
  * pricing - pricing differs region to region
  
##### AWS availability Zones
* each region has many availability zones (AZ)
* usually 3, min 2, max 6 
* eg. if region is ap-souteast-2, az will be named a,b,c eg. ap-souteast-2a
* these AZ are separate from each other to isolate from disasters


##### AWS Data Centers
* each AZ is one ore more data centers
* connected with highbandwidth, ultralow latency networking.

##### AWS Edge Locations / Points of presence
* AWS has more than 216 points of presence (205 edge locations, 11 regional caches)
in 84 cities across 42 countries.

#### AWS shared responsibility model
AWS responsible: security OF the cloud - software, infrastructure, internal security

Customer responsible: security IN the cloud - what you use in the cloud, security, data, OS

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 04. IAM (identity and access management)
* Global service - where we create users and assign them to a group
* users can belong to group(s) or no-group
* groups only contain users (cant belong inside another group)
* a policy (JSON) - we can allow these groups/users certain permissions 
* least priviledge principle - dont give permission more than user needs.

User
* need to add user to a group.
* permissions are inherited from Group(s) user is added to.
* tags are information that help you track something
* .CSV will have credentials
* create an account alias
* sign in url created for account alias

User Group
* When creating a group, you need to create a policy
* Attach policy - AdministratorAccess

### IAM Policies
* policies attached at group level get inherited by every member of group.
* inline-policies can be attached to individual users.

#### IAM policy structure 
JSON
* version (required)
* Id: identifier for policy (optional)
* Statement: one or more in individual statements (required)

Statement consists:
* Sid: identifier for statement (optional)
* Effect: whether statement allows or denies access (allow, deny)
* Principal: account / user /role to which this policy applied to
* Action: list of actions this policy allows or denies
* Resource: list of resources to which the actions applied to.
* Condition: conditions for when this policy is in effect (optional)

```json
// example of a JSON policy

{
  "version":"2012-10-17",
  "Id":"S3-Account-Permissions",
  "Statement":[
    {
      "Sid":"1",
      "Effect":"Allow",
      "Principle":{
        "AWS":["arn:aws:iam::1234345345435:root"]
      },
    "Action":[
      "s3:GetObject",
      "s3:PutObject"
    ],
    "Resource":["arn:aws:s3::mybucket/*"]
    }
  ]
}

```
### Protecting user accounts
#### password policy
Protect users in groups with password policies:

* set minimum length
* require specific character types
  - include uppercase letters
  - lowercase letters
  - numbers
  - non-alphanumeric characters
* allow all IAM users to change their own passwords
* require users to change their own passwords after sime time (password expiration)
* prevent password reuse

#### Multi-factor authentication (MFA)
MFA - is a combination of using a password you know + a security device (token generator) you own.
eg. Authy (multidevice), Google Authenticator (phone only)

Types of MFA devices
* universal 2nd factor (U2F) Security key
* Hardware Key Fob MFA Device
* Hardware Key Fob MFA device for AWS GovCloud (US)

### 3 ways to access AWS
* AWS management console - protected by password + MFA
* Accessing AWS using CLI (command line interface) protected by access keys
  - install AWS CLI v2
  ```cmd
    aws configure
  ```
* AWS software develop Kit (SDK) - language specific APIs for coding protected by access keys

#### Access keys
* Access keys are generated by AWS Management Console.
* do not use Root account to create security credentials.
* users are responsible for their own access keys.
* useful if you will use CLI or SDK in some programing language for AWS

#### AWS CloudShell
An alternative to using the cmd terminal to access AWS in the cloud.
* available in some regions only

### IAM roles for AWS Services
* just like we have policies for users, we have IAM Roles for AWS services
* giving AWS permission to perform tasks on our behalf

Common roles:
* EC2 instance roles
* lamda function roles
* roles for cloudFormation

### IAM Security Tools
* IAM credentials report (account-level)
  - report listing all accounts users and status of various credentials
* IAM Access Advisor (user-level)
  - shows service permissions granted to a user and when those services were last accessed

### IAM Shared responsibility model
###### AWS
* infrastructure (global network security)
* configation and vulnerability analysis
* compliance vaildation

###### User
* users, groups, roles, policies, management and monitoring
* enable MFA on all accounts
* rotate all your keys often
* use IAM tools to apply appropriate permissions
* analyze access patterns and review permissions

### IAM Summary
[Summary - IAM Section](#summary-iam-section)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 05. EC2 - Elastic Compute Cloud
* make sure user has access to 'Billing and cost management dashboard'
* login to root user
* my billing dashboard -> activate IAM access - allows IAM administrators are allowed to access billing data (ensures you enable IAM user and role access to billing information)
* know how to create a budget.
* EC2 (Elastic Compute cloud) - infrastructure as a service

#### What can you do with EC2?
* rent virtual machines (EC2)
* storing data on virtual drives (EBS)
* distribute load across machines (ELB)
* scaling service using auto-scaling group (ASG)

#### EC2 Virtual server - options
* windows or linux, mac
* CPU
* RAM
* storage 
    - network attached (EBS or EFS)
    - hardware (EC2 instance store)
* network card (performance), speed and public IP address
* firewall rules (security group)
* Bootstrap script (configure first launch) (EC2 User Data - runs as root user)
  - automate boot tasks
    - installing updates
    - installing software
    - downloading common files from internet

#### creating an EC2 instance with EC2 User Data
* EC2 
* instances => choose AMI (Amazon *linux 2)
* instance type => t2.micro (free tier eligible)
* number of instances => 1
* network, subnet, auto-asign public IP => default
* IAM role => 
* EC2 User Data (launched during first boot)


##### EC2 User Data
```
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

### EC2 Instance types
```
https://aws.amazon.com/ec2/instance-types/

http://instances.vantage.sh

```

#### 7 different types of EC2 instances
* General purpose
  - great for diverity of workload such as web servers or code repositories
  - balance between: compute, memory, networking
  - T2.micro *(up to 720 hrs processing with T2.micro)

* pcompute optimized (names generally start with C class)
  use cases:
  - great for compute-intensive tasks that require high performance
  - batch processing workloads
  - media transcoding
  - high performance web servers
  - high performance computuing (HPC)
  - scientific modeling & machine learning
  - dedicated gaming servers

* memory optimized (names generally start with R class (r for Ram), X1, High Memory, Z1)
  - fast performance for workloads that process large data sets in memory
  use cases:
  - high performance for relational/non-relational databases
  - distributed web scale cache stores
  - in-memory databases optimized for BI (business intelligence)
  - application performing real-time processing of big unstructured data

* storage optimized (class names I, D, H1)
  - great for storage-intensive tasks that require high, sequencial read and write access to large datasets on local storage.
  use cases:
  - high frequency online transaction processing (OLTP) systems
  - relational and noSQL databases
  - cache for in-memory databsaes (eg. Redis)
  - Data warehousing applications
  - Distributed file systems

* accelerated Computing
* instance features
* measuring instance performance

#### naming convention
m5.2xlarge

m: instance class
5: generation (AWS improves over time)
2xlarge: size within the instance

### Security Groups
* security group is a firewall around EC2 instance.
* security groups are the fundamental of network security in AWS.
* control how traffic is allowed in or out of our EC2 instances.
* security groups only have "allow" rules
* security rules can reference by IP or by security group.
* they regulate: 
  - access to ports
  - authorised IP ranges - IPV4 and IPV6
  - control inbound network
  - control outbound netowkr

* type, protocol, port, source, description
* HHTP, TCP, 80, 0.0.0.0/0 (everything can gain entrance), test http page

* note on source: 
  * 0.0.0.0/0 - everywhere on IPv4
  * ::/0 - everywhere on IPv6

#### Ports you need to know
* 22 = SSH (secure shell) - log into a linux instance.
* 21 = FTP (file transfer protocal)
* 22 = SFTP (secure file transfer protocal) - upload files using SSH
* 80 = HTTP (access unsecure websites)
* 443 = HTTPS (access secure websites)
* 3389 = RDP (Remote Desktop Protocol) - log into a windows instance

### SSH
can connect to server using public IP (eg. 35.180.100.144). security groups need allow inbound port 22, source: 0.0.0.0/0

connecting to servers:

Mac:          SSH,                   EC2,  instance connect
Linux:        SSH,                   EC2,  instance connect
Win < 10                 putty,      EC2,  instance connect
Win > 10:     SSH,       putty,      EC2,  instance connect

##### SSH with Linux or Mac:
* need .pem file to access machine (created when creating user) eg. EC2Tutorial.pem
* give chmod permission to key
* 'ec2-user' linux user into amazon machine (default)
* *EXAM *problem permissions 0644 too open. solution -> chmod 044 key.pem

```
chmod 0400 EC2Tutorial.pem                              //0400. Allows the owner to read.
ssh -i EC2Tutorial.pem ec2-user@35.180.100.144          //let only someone with key into E2 machine at that IP.
```

##### SSH into EC2 Windows
* SSH allows you to control a remote machine using a command line.
* configure required parameters for doing SSH on windows using Putty.
* PuttyGen to generate a key which putty likes. 
  * load private key -> .pem file -> save private key as .ppk file
* Putty -> enter IP address (public) from AWS EC2 instance ... host name: ec2-user@35.180.100.144 port: 22
* save session with name
* link private key file...connection -> SSH -> Auth -> private key file for authentication -> browse for .ppk file
* go back to session -> save (this saves the ppk authentication file)

##### SSH into Windows 10
* AWS ec2 linux default user is always 'ec2-user'
* if error because permission denied -> go to the .pem file -> right click -> security -> advanced -> the owner of the key is yourself (logged in user) -> disable inheritance -> remove any other user other than youself.
* make sure youself has full control of the file.
```
ssh -i c:\users\Swagfinger\Downloads\Ec2Tututorial.pem ec2-user@35.180.242.162

```

##### instance connect
* note ec2-user only works for Amazon linux 2 or ubuntu EC2 instances at this moment
* the instance connect still relies on SSH so port 22 needs to be enabled.
connect to instance -> select EC2 instance connect -> username -> ec2-user 
 
##### Instance Roles
* NB never run aws configure on an EC2 instance (other users who do the same will gain access to your credentials)
* use IAM roles -> right click on EC2 instance -> attach / replace IAM role -> attach role
* Roles are a way to allow EC2 instances to issue commands against AWS.

### Instance Launch types
*EXAM
* On-Demand instances: short workload, predictable pricing
* Reserved: (minimum 1 year)
  1. reserved instances: long workloads
  2. convertible reserved instances: long workloads with flexible instances
  3. scheduled reserved instances - every thursday between 3 and 6pm 
* spot instances - short workloads, cheap, can lose instances (less reliable).
* dedicated hosts: book anb entire physical server, control instance placement.

##### On-demand
* pay for what you use
* linux or windows billing per second, after the first minute. all other OS - billing per hour.
* has highest cost but no upfront payment
* no long-term commitment
* recommended for short-term and un-interrupted workloads, where you can't predict how the application will behave.

##### reserved
* up to 75% discount compared-to on demand
* 1 year (discount) or 3 year (more discount)
* no upfront, partial upfront (more discount), all upfront ( even more discount)
* reserve a specific instance type
* recommended for steady-state usage applications (databases)
* convertible reseverd instance (can change EC2 type) up to 54% discount
* schedule reserve instance - launch within time window you reserve. when you require a fraction of day/week/month over 1->3 yrs.

##### Spot instances
* can get up to 90% compared to on-demand
* you can loose instance at any time if the price you are willing to pay is less than the current spot price.
* most cost-efficient in AWS.
* useful for workloads resilient to failure: batch jobs, image processing, data analysis, distributed workload.
* not for critical job or database.

##### EC2 dedicated HOSTS
* Amazon EC2 dedicated host is a physical server with EC2 instance capacity fully dedicated to your use. dedicated hosts can help you address compliance requirements. using your existing server-bound software licenses.
* 3yr reservation period.
* more expensive.
* per host billing.

##### EC2 dedicated Instance
* dedicated instance vs dedicated host (*there is a difference)
* instances runing on hardware dedicated to you
* per instance billing
* may share hardware with other instances in same account
* automatic instance placement

### Shared responsibility model
##### AWS
* infrastructure (global network security)
* isolation of physical hosts
* replacing faulty hardware
* compliance validation

##### your responsibility
* security in the cloud (security group rules)
* OS patches and updates
* software on EC2
* IAM roles & IAM user access management
* data security on your instances.

### Summary
[Summary - 05- EC2 Elastic compute cloud](#summary-05-ec2-elastic-compute-cloud)

---
###### <Div style="text-align:right">[table of contents](#table-of-contents)</div>
## 06. EC2 - Instance Storage
### EBS Volume
* EBS (Elastic block store)
* network drive that you can attach to instances while they run,
* allows persisting data even after instance terminated
* can only be attached to one EC2 at a time (cloud practitioner level). 
  - one EC2 instance can have multiple EBS volumes.
* EBS volumes are bound to a AZ (availability zone). To move volume -> you create a snapshot.
* "Network usb stick"
* 30gb free EBS storage of type general purpose (SSD) or magnetic per month
* have to provision capacity in advance.
* delete on termination attribute - controls how EBS gets handled when EC2 terminated
  - default -> root EBS volume is terminated / other attached EBS volumes are not deleted.
  -> these can be controlled.

### EBS Snapshot
* make a backup of EBS volume at a point in time by taking a snapshot of EBS
* not necessary to first detach from EC2 instance 
* restore by attach EBS volume to another AZ.

### AMI 
* Amazon Machine Image
* represent a customization of an EC2 instance.
* AMIs are created for a specific region then copied across regions

##### You can launch EC2 instances from:
* public AMI (provided by AWS)
* your own AMI (you make and maintain)
* an AWS Marketplace AMI (someone else makes and sells)

##### AMI process from EC2
* Start EC2 intance and customize
* stop the instance (data integrity)
* Build an AMI - this creates EBS snapshots
* Launch instances from other AMIs

### EC2 Image Builder
* EXAM
* used to automate the creation of virtual machines or container images.
* Automate the creation, maintain, validate and test EC2 AMIs
* EC2 Image Builder 
  1. creates EC2 instance (builder EC2 instance) - builds components 
  2. New AMI created 
  3. Test EC2 instance
  4. distribute AMI to multiple regions
* EC2 builder can run on a schedule
* free service (only pay for resources used)

#### Image builder hands on
##### 1. Specify Pipeline details
* create new pipeline
* build schedule is how often should run (or if there are new dependencies)

##### 2. Choose Recipe
* recipe is a document that defines how Source image is customized (docker vs  AMI)
* Select image: Managed Images vs. Custom AMI
* Image OS: Amazon Linux
* Image Origin: Quickstart Amazon Managed -> Amazon Linux 2 x86
* Components: build components pre-created onto image; can set order components install

##### 3. define infrastructure configuration 
  -> create new infrastructure configuration 
  - create IAM role -> attach policy ->  
  (looking at default IAM instance profile...)
  1. EC2InstanceProfileForImageBuilder
  2. EC2InstanceProfileForImageBuilderECRContainerBuilds
  3. AmazonSSManagedInstanceCore
* Create Role 
* select IAM role we created
* we can customize AWS infrastructure -> t2.micro 

##### 4. Define distribution settings
* can create own distribution setting to automatically distribute AMI to multi regions
* create pipeline

### EC2 Instance Store
* higher performance than EBS (network drive)
* is a hardware disk attached to EC2 instance
* better I/O performance
* EC2 instance store lose their storage if they're stopped (ephermeral)
* good for buffer / cache / stratch data / temporary content
* risk of data loss if hardware fail
* backups and replication are your responsibility

### EFS (Elastic file system)
* Elastic File System
* Managed NFS (network file system) that can be mounted to 100s of EC2 at a time
* shared network file system
* EFS works only with Linux EC2 in multi-AZ
* highly available, scalable, expensive (3x gp2), pay per use, no capacity planning

##### EFS-IA
* EFS-IA (storage class) cost optimized for infrequently accessed
* if EFS-IA is enabled, is automatically managed by EFS.
* EFS is 92% lower clost compared to EFS standard
* infrequrently used files are moved to EFS-IA

### EBS vs EFS 
* EXAM
* EBS can only connect to one EC2 bound to one AZ.
* EBS can snapshot a copy 

* EFS whatever is on drive is shared by all EC2 instances
* Shared file system

### Shared responsibility model for EC2 Storage
##### AWS
* infrastructure
* replication for data for EBS volumes & EFS drives
* replacing faulty hardware
* ensure AWS employees cannont access your data

##### your responsibility
* setting up backup / snapshot procedures
* setting up data encryption
* responsibility of any data on the drives
* risk of EC2 instance store - can lose drive if faulty hardware, if you stop 
EC2 instance with instance store,data will be lost (it is your responsibility to backup in first place)

### Amazon FSx
* managed service to get 3rd party high-performance file systems on AWS.
* incase you dont want to use EFS or S3

3 options
* FSx for Lustre 
  - fully mananged, high-performance, scalable file storage for high performance computing (HPC)
  - 100 gb/s millions of IOPS, sub-ms latencies.
* FSx for Windows File Server
  - Fully managed, highly reliable, scalable Windows shared file system.
  - built on windows file server
  - support for SMB protocol and Windows NTFS
  - integration with MS active directory
* FSx for NetApp ONTAP

### EC2 Instance Storage Summary
[Summary - 06. EC2 Instance Storage](#summary-06-ec2-instance-storage)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 07. ELB and ASG - Elastic Load Balancing and Auto Scaling Groups
### High Availability, Scalability, Elasticity
#### Availability
* goes hand-in-hand with horizontal scaling.
* goal is to survice data center loss.
* running instances of same application in atleast 2 availability zones.
  * auto scaling group in mutli AZ.
  * load balancer multi AZ.

#### Scalability
* It can handle greater loads by adapting.
* 2 kinds: vertical scalability, horizontal scalability (elasticity)
  * Vertical: increase size of the instance eg. t2.micro -> t2.large. 
    common for non-distributed systems such as databases. 
    vertical scale has hardware limit.
  * Horizontal: increase number of instances / systems for application
    implies distributed system. common for web applications /modern applications. AWS allows this by: EC2 and auto scaling groups / load balancers

#### Elasticity
* Once a system is scalable, elasticity means that there will be some "auto-scaling" so that the system can scale based on the load.
* This is is "cloud-friendly': pay per use, match demand, optimize costs.

#### Agility (distractor)
* IT resources only a click away with reduced time to make those resources available to developers from weeks to minutes.

### Load Balancing
* Load balancers are servers that forward internet traffic to multiple servers (EC2 instances) downstream.
* helps with Elasticity
* more users, more it will balance load across multiple EC2 instances

##### Why use load balancer?
* spread load across multiple downstream instances
* expose a single point of acess (DNS) to your application
* seamlessly handle failure of downstream instances
* do regular health checks on instances
* provide SSL termination (HTTPS) for your websites
* high available across zones

### ELB (Elastic Load Balancer)
* An ELB (Elastic Load Balancer) is a managed load balancer
  - AWS guarantees that it will be working
  - AWS takes care of upgrades, maintainence, high availability
  - AWS provides only a few configuration knobs
* It costs less to setup your own load balancer but it will be a lot more effort on your end (maintenance, integrations)

##### AWS offers 3 kinds of load balancers
1. Application load balancer - HTTP and HTTPS only - layer 7
2. Network Load Balancer - ultra high performance, allows for TCP - layer 4
3. Classical load balancer - layer 4 and 7 (previous gen, older model before split into 7 and 4)
4. Gateway load balancer - *new

##### ALB - hands on
* if you start 2 EC2 instances, their IP's are different, using a load balancer will manage a target group of EC2 (select EC2 instances...)

### Auto Scaling Group
* once you have an application that can be load balanced with a load balancer, 
* use ASG to automatically create servers in backend.
* eg. a website's load that has more traffic at certain times
* scales out and scales in to adjust to requirements
* automatically register new instances to a load balancer
* ASG can detect and replace unhealthy instacnes
* cost savings - only run at optimal capacity
* ASG has a minimum, desired and maximum capacity for Instances
* ASG works hand-in-hand with load balancer, web traffic directed by load balancer, as more instances added, load balancer can use them to share load.
* create an Auto Scaling policy to ensure 

#### ASG hands-on
* note: you create a launch-template note an instance so the ASG knows how to create instances.
* Scaling policies - Target tracking scaling policy (automatic scaling) vs none (self managed scaling)
* terminating an instance to lower than the desired instances will cause ASG to launch new instance to match desired capacity. ie. ASG creates instances automatically. 
* to stop creation of new EC2 instances to match capacity, delete the ASG / loadbalancer

### ASG strategies
  1. Manual scaling - update the size of an ASG manually
  2. Dynamic scaling - respond to changes on demand
    - when a cloudwatch alarm is triggered eg. CPU usage > 70% then add 2 units
    - when a cloudwatch alarm is triggered eg. CPU usage < 30% then remove 1
  3. target tracking scaling
    - wanting avg ASG cpu to stay around 40%
  4. scheduled scaling
    - anticipate scaling based on known usage patterns. eg. scale up at 5pm on friday.
  5. predictive scaling
    - uses machine learning to predict future traffic ahead of time
    - automatically provision the right number of EC2 instances in advance.
    - based off predictable patterns

### Summary
[Summary - 07. ELB and ASG](#summary-07-elb-and-asg)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 08. S3 

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 09. Database and analytics

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 10. Other compute services

### what is Docker
* software development platform to deploy apps.
* apps are packaged into containers that can run on any OS
* makes use of containers that will run consistent on any platform.
* can scale containers up and down
* docker images are stored in docker repositories 
- public - Docker Hub
- private - Amazon ECR (Elastic container Registry)
- alternatives Kubernetes

diff between Docker vs virtual machine VM
* each VM needs an OS via Hypervisor
* whereas docker uses a Docker Daemon that makes use of many containers sharing the same resources dont need full VM or OS.

### ECS, Fargate & ECR Overview
#### ECS (for Docker)
* Elastic container service
* used to launch docker container service on AWS
* must provision and maintain infrastructure yourself (EC2 instances) *created in advance
* AWS takes care of starting / stopping containers
* has integration with Application Load Balancer
* So you will have multiple EC2 instances, anytime there is a new docker container, ECS is smart enought to figure out which EC2 instance to add the docker container.

#### Fargate (for Docker)
* Also used to launch Docker containers on AWS.
* unlike ECS, simpler - as you dont need to provision infrastructure (EC2 instances)
* serverless 
* AWS just runs containers for you, based on CPU / RAM you need.

#### ECR
* ECR stands for Elastic Container Registry
* a container registry - used to store these docker images so they can be run on AWS.
* private docker registry on AWS.
* where you store Docker images so they can be run on ECS or Fargate.
* Fargate / ECS able to look at these images and create a container from them and run them directly on Fargate service.

Exam: know difference between ECS, Fargate, ECR

### Serverless
* paradigm where developers dont manage the servers anymore.
* they just deploy code / functions
* initially Serverless meant (FaaS - Functions as a service)
* serverless was pioneered by AWS Lamda (running functions in the cloud), but now also includes anything that's managed: databases, messaging, storage, etc.
* serverless does NOT mean there are no servers, it means you just dont manage / provision / see them.

serverless examples: S3, dynamoDB, Fargate, Lambda

### Why Lambda?
With EC2:
* virtual servers in cloud
* limited by RAM and CPU
* continuously running
* scaling means intervention to add / remove servers

With Lambda: 
* virtual functions - no servers to manage
* limited by time - short executions
* run on-demand
* scaling is automated

### Benefits of Lambda
* easy pricing (price per request and compute time) *EXAM
* free tier 1,000,000 AWS lambda requests 400,000GB soconds compute time.
* integrated with AWS services
* event driven (reactive type service) - functions get invoked when needed.
* Integrated with many programing languages
* easy monitoring through AWS CloudWatch
* easy to get more resources per function (up to 10 gb of ram)
* increasing RAM will also increase CPU and Network quality

### AWS lambda Language support
* Node.js (JS)
* Python
* Java
* C#
* Golang
* Powershell
* Ruby
* Custom Runtime API (eg. Rust)
* Lambda container Image 
  - Allow you to run docker images ontop of Lambda (must implement Lambda runtime API which is not every Docker image)

#### Example Lambda usage
* serverless thumbnail creation
* serverless CRON job (CRON allows you to define a schedule eg. day, month etc to run a script). by default CRON job is run on a LINUX machine, with Serverless, to solve this using the cloud, we use Cloudwatch Events (Event Bridge) which triggers Lambda function.

### API Gateway overview
* use case: when you want to build a serverless http API <b>*EXAM</b>
  - example: Lambda CRUD using DynamoDB but we want external clients to be able to access Lambda function. But Lambda functions arent exposed unless...
* Exposing REST APIs from AWS to client using API gateway
* API Gateway proxy's request to lambda function.
* fully managed service for developers to easily create, publish, maintain, monitor and secure APIs
* Serverless and scalable
* supports RESTful APIs and WebSocket APIs
* support for security, user authentication, API throttling, API keys, monitoring

### Batch Overview
* AWS Batch is a fully managed batch processing service
* efficiently run 100,000s of computing batch jobs on AWS.
* A batch job has a start and an end
* dynamically launch EC2 instances or Spot instances.
* AWS Batch provisions the right amount of compute / memory
* You submit or schedule batch jobs and AWS does the rest.

What is it? 
Batch jobs are defined as Docker Images and run on ECS service.

##### Batch vs Lambda?
Lambda: 
  * time limit (15min)
  * limited to few programming languages
  * limited disk space
  * serverless

Batch:
* no time limit
* any runtime as long as it is packaged into Docker image
* rely on EBS for disk storage
* not serverless. rely on EC2 (can be managed by AWS)

### Lightsail Overview
* single access point, simpler alternative
* low predicatable pricing
* little to no cloud experience <b>*EXAM</b>
* can setup notifications and monitoring of your lightsale resources.
* use case: simple web applications, websites, dev/test env
* has high availability but no autoscaling
* limited AWS integration

### Other Compute - Summary
[summary-10-other-compute-services](#summary-10-other-compute-services)

---

###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 11. Deploying and managing infrastructure at scale
ways to deploy workloads onto AWS

## Deployment services

### CloudFormation
* declarative way (via code) to outline AWS infrastructure (say what you need)
* used when you want to repeat an architecture in different environments, regions, or AWS accounts.
* create a stack from template
* can also update template
* deleting a stack cleans up all resources associated with stack.

summary - cloudformation is an easy way to define resources, infrastructure as code. you can take the same template and deploy it to many AWS regions or AWS accounts.

### Cloud development kit (CDK)
* defining cloud infrastructure using familiar coding language(js, node, java, python, .net)
* code will be compiled into cloudformation template (JSON/YAML) to be used by CloudFormation

### Beanstalk
* typical deployment in a 3tier architecture:
  * user talks to load balancer
  * load balancer forwards traffic to multiple instances (managed by ASG)
  * using RDS Database to read and write data / ElastiCache to store/retrieve session data (cached data)

* Beanstalk does all this for you (developer centric)
* it uses all these services (EC2, ASG, ELB, RDS etc)
* still have full control over configuration.
* Platform as a service (PaaS)
* developer centric meaning developer is only responsible for application code
* has full monitoring suite within Beanstalk

Beanstalk VS Cloudformation?
CloudFormation (infrastructure focused) you can do anything. not just App
with Beanstalk (application focused) the first thing you do is upload your code.

3 architecture models
1. single instance deployment - good for dev environment
2. Load Balancer + Auto Scaling Group - for production/pre-production web apps
3. ASG only - good for non-web app


### AWS Systems Manager (SSM)
Helps you manage EC2 and on-premises systems at scale.
* hybrid service
* Patching automation (patch fleet of EC2 instances or on-premises servers)
* run commands across entire fleet of servers
* store parameter configuration with SSM Parameter store
* works both for Windows and Linux OS.

How does it work?
you install an SSM agent on systems we control (EC2 instance or On-Premise VM)
* installed by default on Linux AMI

### Systems Manager - SSM Session Manager
* Allows SSH on EC2 and on-premise servers; 
* WITHOUT ssh access, Bastion hosts (special purpose comupter on a network designed and configured to withstand attacks), SSH keys.
* port 22 closed

How does it work?
* EC2 has a SSM agent; which is connected to Session manager.
* create IAM role with SSM access (role: AmazonSSMMangedInstanceCore)
* using SSM Secure Shell, we able to have SSH directly from AWS.

* users can access through session manager service the EC2 instance and execute commands on it.
* can send log data to S3 or CloudWatch logs.

### OpsWorks

* Chef / Puppet - tools that help you perform server configuration, or repetitive actions.
(designed to work great with EC2 and on-premises VM)

* AWS Opsworks was created to manage Chef and Puppet in the cloud.

* the reason you would use OpsWorks is if you were already using Chef or Puppet before migrating to the AWS Cloud and you wanted to reuse your chef and Puppet templates to work on AWS.

* alternative to AWS SSM.

* can only provision standard AWS resources (EC2 instances, Databases, Load Balances, EBS Volumes)

How OpsWorks Works?
* you have the OpsWorks Stack. and on it you have:
  1. ELB (elastic load balancer) Layer - ALB
  2. Aplication server layer - EC2 instances (gets info from Cookbook repository), Application from App Repository.
  3. Database Layer - RDS Database

---

## Developer Services

### AWS CodeDeploy
allows you to upgrade your EC2 instances, applications, and on premises servers applications from versions from 1 to 2 automatically from a single interface

Can be used to automatically deploy app. 
independent - doesnt need to use CloudFormation or Beanstalk 
hybrid service - works with EC2 instances AND on-premises servers
these servers must be provisioned/configured ahead of time

### AWS CodeCommit 
* github like service which stores repositories.
* lives within aws account (security)
* integrated with AWS services

### AWS CodeBuild
* Allows you to build code in the cloud.
* Compiles source code, runs test, produces packages to be ready for deployed *eg by CodeDeploy.
* Fully managed, Serverless
* Scalable + highly available
* Secure
* pay for build time

### AWS CodePipeline
* way to orchestrate pipeline (the steps to have code automatically pushed to production).
* Code-> Build-> Test-> Provision-> Deploy
* basis for CICD (continuous integration & continuous delivery) 
    CICD - every time code is updated on repository, code is built, tested, and prepared for deployment
* fully managed

### AWS CodeArtifact
* Software usually has code dependencies.
* Artifact management - process of storing and retrieving these dependencies.
* CodeArtifact is an artifact management system.
* All modern dependency management tools eg. npm, yarn can work with CodeArtifact.
* Developers retrieve dependencies straight from CodeArtifact.
* CodeBuild can also retrieve these dependencies from CodeArtifact.

### AWS CodeStar
* Unified UI to easily manage software development activities in one place.
* answers: "How do i setup CodeCommit, CodeBuild, and then CodeDeploy and unify everything with CodePipeline?" - using CodeStar
* Dashboard interface with - CodeRepository, CodeBuild, CodeDeploy, CodePipeline, Beanstalk, EC2 etc
* Central service allows developers to quickly start development using best CICD practices.

### AWS Cloud9
* integrated Cloud IDE for writing, running and debugging code.
* code-collaboration, pair programming
* pushing in Cloud9 goes directly to repository.

---

###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 12. Leveraging AWS Global infrastructure

### Why use global applications?
* [infrastructure.aws](http://infrastructure.aws)
* A Global application is an application deployed in multiple geographies.
* On AWS: deployed to regions or Edge locations.

#### Benefits:
* Decreased latency (faster)
* disaster recovery (DR)
* attack protection (difficult to attack mutli regions at once)

### Global Applications in AWS
#### Global DNS (Route53)
route users to closest deployment with least latency
* great for disaster recovery strategies
* Managed DNS (Domain Name System) 
  - a collection of rules and records which help clients understand how to reach a server through URLs.

##### Common records
* 'A' record - mapping a url (eg. www.google) to IPv4
* 'AAAA' record - mapping a url to IPv6
* CNAME - hostname to hostname - eg. search.google.com to www.google.com
* Alias record - hostname to AWS resource (ELB, CloudFront, S3, RDS, etc...)

##### Routing policies
* Simple routing policy - no health checks
* weighted routing policy - distribute traffic across multiple EC2 instances (type of load balancing as weights are applied to EC2 instances)
* latency routing policy - looks at where user is located, redirects user to server closest based on latency.
* failover routing policy - has primary EC2 instance and failover EC2 instance. DNS system does health check and incase primary fails, routed to failover. 

#### Global CDN (CloudFront)
* CloudFront is a CDN
* caching content at edge locations improves read performance of website 
* caching decreases latency, improves user experience
* DDoS Protection, also using Shield, AWS Web Application Firewall

##### Where can CloudFront Cache from?

###### S3 Buckets
* CloudFront can cache from S3 buckets
* CloudFront given enhanced security using Origin Access Identity (OAI) option to access S3
* CloudFront used to upload files to S3 
 
###### Custom origin (http)
* Application load balancer
* EC2 Instance
* S3 Website
* any http backend on premises

##### How does it work?
* CloudFront has edge location all around the world. 
* Connects to origin (source data - S3 or HTTP)
* client connects and does http request from edge location.
* edge location checks if its in cache, if its not, fetches it from origin
* caches result in local cache.

use case:
* if we created a S3 bucket in australia with a website in the bucket.
* and a user requests this from America
* user will request the content from an edge location in America using CloudFront.
* CloudFront fetches this information from Australia.
* if another user in America requests the same content, it will be served from the edge as it is cached.


##### CloudFront vs Cross Region Replication?

###### CloudFront:
  * CDN (cache content all around the world)
  * Global edge network
  * files are cached for a TTL (maybe a day) TTL = cache auto expires
  * great for static content everywhere around world.

###### S3 Cross Region Replication:
  * replicate an entire bucket into another region
  * must be set up for each region you want replication to happen
  * files updated in near real-time
  * only for read only
  * great for dynamic content that needs to be available at low-latency in a few regions

#### S3 Transfer Acceleration
* accelerate global uploads and downloads into Amazon s3
* usually s3 buckets associated with only one region. Sometimes you want to transfer files from all around the world into one specific S3 bucket in the target region.
* Transfer acceleration only used if you're uploading/downloading from an S3 bucket far away.

##### How it works?
Say you want to upload from USA to S3 bucket in Australia, you will upload file to edge location in USA and using the internal network (faster).
The edge location will upload the file with a more reliable and faster connection.

#### AWS Global accelerator
* improve global application availability and performance using the AWS global network.
* requests are routed through AWS internal network
* Leverage the AWS internal network to optimize the route to your application.
* up to 60% improvement.

##### How it works?
* if an application load balancer (ALB) has been deployed in India, and users from all around world want to access our application.
* Using the Global accelerator, users will actually connect to an edge location and edge location routes traffic into India.
* Benefit is traffic only happens between user in eg. USA and closest edge location, and it leverages AWS private network to speed up connection from edge location to application.
* 2 Anycast IP are created for your application, and traffic is sent through edge locations.

##### Global Accelerator vs CloudFront?
* Both use AWS global network and edge locations from around the world.
* Both integrate with AWS Shield for DDoS protection
* CloudFront is a CDN (cache content at edge, and served at edge)
* Global Accelerator there is no caching, all requests get passed on from the edge locations back to application in your regions. makes requests go faster and go through AWS internal network globally.

#### AWS Outposts

* Way to extend the AWS cloud directly onto own infrastructure on-premises system.
* hybrid cloud is when businesses keep an on-premises infrastructure alongside a cloud infrastructure.

##### therefore, 2 ways of dealing with IT systems (hybrid):
  1. AWS cloud (aws console, cli, AWS API's)
  2. On-Premises infrastructure

* Outposts are server racks that come packaged with AWS infrastructure, services, API's and tools to build your own applications on-premises just like in the cloud.

* AWS will setup servers "outpost racks" on premises with the AWS infrastructure which you can then extend onto your own on-premises servers.

* difference between cloud and outpost racks is now you are responsible for the outpost racks physical security.

##### Benefits?
* low latency
* local data processing (data doesnt leave your servers)
* easier migration to the clouyd
* fully managed service

#### AWS Wavelength 
* enabled via 5G networks.

* Wavelength zones are infrastructure deployments embedded within the telecommunications providers' datacenters at the edge of the 5G networks.

* Wavelength enables deployment of AWS services onto edge of 5G networks to get ultra low latency to applications via 5G; eg. deploying EC2, EBS, VPC to wavelength zone.

* say you have a carrier with 5g network with a Wavelength Zone, via a carrier gateway you will deploy an EC2 instance on that zone.
* that zone belongs to the 5g network.
* When an user accesses your wavelength zone via 5G, there is low latency because the application is already deployed at the edge.
* Traffic doesnt leave the Communication service provider (CSP) network.
* if you need connection to parent AWS region, you can. its secure.
* no additional costs or service agreements.
* use cases: smart cities, ML-assisted diagnostics, connected vehicles, interactive live video streams, AR/VR, real-time gaming.

#### AWS Local Zones
allows you to place AWS compute, storage, database, and other AWS Services closer to end user to run latency-sensitive applications.

* idea is to extend VPC (virtual private cloud) to more locations (extensions of AWS regions)
 extending AZ's with more local zones

#### Global Applications Architecture
* Single region, single AZ
  - bad availability
  - bad global latency
  - easy to setup

* Single region, multi AZ
  - good availability
  - bad global latency
  - more difficult to setup (not much)

* multi-region, active passive
  - 2 regions each region has one or multiple AZ
  - the one region the EC2 instances will be ACTIVE (read/write), all other regions are passive (read only).
  - improved read latency
  - difficult to setup

* multi-region, active-active
  - each EC2 instance can take writes/reads
  - replacation within these instances
  - more difficult to setup

### Summary - Leveraging the AWS Global Infrastructure
[Summary - 12. Leveraging the AWS Global Infrastructure](#summary-12-leveraging-the-aws-global-infrastructure)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 13. Cloud Integrations
* when you have multiple applications, they will have to communicate with each other
* 2 patterns of application communication
  * synchronous communication (application to application)
  * asynchronous / event based (application to queue to application) 

* async (decoupled) application design removes problems with spikes in traffic by introducing a queue
  - SQS (queue model)
  - SNS (pub/sub model)
  - Kinesis (realtime data streaming)
* these services scale independently from application

### SQS (Simple Queue service)
  
##### Whats a queue?
* we have producer(s) -> sending data into a SQS queue -> read by consumer(s) polling (requesting messages) from the queue
* consumers share the work (each consumer gets different messages), when done processing message, it's deleted from queue.

##### SQS 

* high through-put message queuing service.
* fully managed (serverless) used to <b>decouple</b> applications. <b>*EXAM</b>
* Scales
* default retention (4days, max 14 days)
* no limit to messages in queue.
* messages deleted after they are read
* low latency (< 10ms on publish and receive)
* consumers share the work to read messages and scale horizontally.

Example:
* Web Servers Layer - taking requests through Application Load Balancer, served through EC2 instances in an Auto Scaling Group, and users who want videos processed. 
SQS Queue - Instead of sending requests directly to video application,
requests get sent to a SQS Queue.
Video Processing Layer - made of auto scaling group of EC2 instances. these EC2 Instances read from the queue and process videos.
* the 2 Auto Scaling groups can scale independently of each other (decoupling)

### SNS (Simple notification services)
What if you wanted to send 1 message to many receivers.

Method 1: Direct integration
* Buying service talking to 
  -> 1. email notification 
  -> 2. fraud service 
  -> 3. shipping service 
  -> 4. SQS queue. 
  this is quite complicated because we need to write 4 direct integrations.

Method 2: pub/sub type integration
* Buying service sending message to -> SNS Topic
* SNS Topic will be smart enough to send notification to 
  -> 1. email notification 
  -> 2. fraud service 
  -> 3. shipping service 
  -> 4. SQS queue.

* The "Event publishers" only sends messages to one SNS topic.
* As many "event subscribers" can listen to the SNS topic notifications.
* Each subscriber will get all the messages.
* Up to 10,000,000 subscriptions per topic. 100,000 topic limit.
* SNS Subscribers can be: 
  - Http/https endpoint
  - email / SMS messages / mobile notifications
  - SQS queue
  - Lambda functions (write your own integration)

### Kinesis
* real-time big-data streaming <b>*EXAM</b>
* Managed service to collect, process, and analyze real-time streaming data at any scale.

##### Subservices of Kinesis
* Kinesis Data Stream - low latency streaming to ingest data at scale from hundreds of thousands of sources.
* Kinesis Data Firehose - load streams into S3, Redshift, Elastic Search, etc
* Kinesis Data Analytics - perform realtime analytics on streams using SQL
* Kinesis Video Streams - monitor realtime video streams for analytics or ML

Flow:
1. Kinesis Streams receive data from multi types of sources
2. Kinesis Analytics can then be used to analyze data and produce output in realtime
3. then can use Kinesis Firehouse to send this data outputs directly into destinations.

### Amazon MQ
* SNS, SQS are native AWS services using proprietary protocols from AWS.
* traditional applications running from on-premises may use open protocols
  such as: MQTT, AMQP, STOMP, Openwire, WSS
* So sometimes when a company is migrating to the cloud, instead of re-engineering the application to use SQS and SNS, we can use Amazon MQ.
* Amazon MQ will usually only be used IF a company is migrating to the cloud and needs to use one of these open protocals such as: MQTT, AMQP, STOMP, Openwire, WSS
otherwise they should use SQS and SNS as they scale a lot better and a lot more integrated with AWS. 
* Amazon MQ = Managed Apache ActiveMQ
* Amazon MQ doesnt scale as much as SQS/SNS
* Amazon MQ runs on a dedicated machine (not serverless)
* Amazon MQ has both features queue SQS, and notification SNS

### Summary
[Summary - 13. cloud integrations](#summary-13-cloud-integrations)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 14. Cloud monitoring
* getting a better understanding of performance of our cloud deployments
* CloudWatch provide metrics for every service in AWS
* Metric is a variable to monitor (eg CPUUtilization, NetworkIn)
* metrics have time-stamps
* can create a dashboard of metrics

##### Important Metrics
* EC2 instances: CPU Utilization, Status Checks, Network (not RAM)
  - Default metrics every 5 mins
  - option for detailed monitoring ($$$) metric every minute
* EBS Volumes: Disk Read/Writes
* S3 Buckets: BucketSizeBytes, NumberOfObjects, AllRequests
* Billing: Total Estimate Charge (only in US-east-1)
* service limits: how much you've been using a service API
* custom metrics: push your own metrics

### Cloudwatch Alarms
* alarms are used to trigger notifications for any metric
* alarm actions: 
  - auto scaling: increase or decrease EC2 instances "desired" count
  - EC2 Actions: stop, terminate, reboot, or recover an EC2 instance
  - SNS notifications: send a notification into an SNS topic
* various options for the alarm (sampling, %, max, min etc)
* choose period on which to evaluate an alarm
* create a billing alarm on CloudWatch Billing metric
* Alarm status: OK, INSUFFICIENT_DATA, ALARM

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 15. VPC and Networking

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 16. Security and Compliance

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 17. Machine Learning

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 18. Account management, Billing and support

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 19. Advanced Identity

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 20. Other Services

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 21. AWS architecting and Ecosystem


---

## Source

+ Stephane maarek [Ultimate AWS Certified Cloud Practitioner - 2021](https://www.udemy.com/course/aws-certified-cloud-practitioner-new/)

---
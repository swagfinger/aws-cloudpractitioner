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

### 05. [EC2 - Elastic Compute Cloud](#05-ec2-elastic-compute-cloud)

### 06. [EC2 - Instance Storage](#06-ec2-instance-storage)

### 07. [ELB & ASG - Elastic Load Balancing & Auto Scaling Groups](#07-elb-and-asg-elastic-load-balancing-and-auto-scaling-groups)

### 08. [S3](#08-s3)

### 09. [Databases and Analytics](#09-database-and-analytics)

### 10. [Other compute services](#10-other-compute-services)
  + [what is docker?](#what-is-docker)
  + [ECS](#ecs)
  + [lamda](#lamda)
  + [batch](#batch)
  + [lightsail](#lightsail)

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

### 13. [Cloud Integrations](#13-cloud-integrations)

### 14. [Cloud monitoring](#14-cloud-monitoring)

### 15. [VPC & Networking](#15-vpc-and-networking)

### 16. [Security and Compliance](#16-security-and-compliance)

### 17. [Machine Learning](#17-machine-learning)

### 18. [Account management, Billing and support](#18-account-management-billing-and-support)

### 19. [Advanced Identity](#19-advanced-identity)

### 20. [Other Services](#20-other-services)

### 21. [AWS architecting and Ecosystem](#21-aws-architecting-and-ecosystem)

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 01. Create an AWS account

* does need a credit card, to verify identity (authorization)
* Stay on the AWS free tier
* root user account / password


---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 02. Summary

#### IAM Section
* users: mapped to a physical user; has a password for AWS Console
* groups: contain users only
* policies: JSON document that outlines permissions for users or groups
* Roles: for EC2 instances or AWS services
* Security: MFA + password policy
* AWS CLI: manage your AWS services using the command line
* AWS SDK: manage your AWS services using a programming language
* Access keys: access AWS using CLI or SDK
* Audit: Credential Reports & IAM Access advisor
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

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 05. EC2 - Elastic Compute Cloud

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 06. EC2 - Instance Storage

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 07. ELB and ASG - Elastic Load Balancing and Auto Scaling Groups

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
* makes use of containers that will run consistent on any platform.
* can scale containers up and down
* docker images can be stored in docker repositories 
- public - Docker Hub
- private - Amazon ECR (Elastic container Registry)

diff between Docker vs virtual machine VM
* each VM needs an OS
* docker makes use of many containers sharing the same resources dont need full VM or OS.

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

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 13. Cloud Integrations

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 14. Cloud monitoring

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
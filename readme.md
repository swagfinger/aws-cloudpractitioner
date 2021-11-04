# AWS Cloud Practitioner

Learning about AWS eco-system and AWS features.

## Summary

---

## Table of contents

### 01. [Create an AWS account](#01-create-an-aws-account)

### 02. [code and slides](#02-code-and-slides)

### 03. [Cloud Computing](#03-cloud-computing)

### 04. [IAM (identity and access management)](#04-iam-identity-and-access-management)

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

### 14. Cloud monitoring

### 15. VPC & Networking

### 16. Security and Compliance

### 17. Machine Learning

### 18. Account management, Billing and support

### 19. Advanced Identity

### 20. Other Services

### 21. AWS architecting & Ecosystem

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 01. Create an AWS account

Stay on the AWS free tier


---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 02. Code and slides


---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>

## 03. Cloud computing

---
###### <div style="text-align:right">[table of contents](#table-of-contents)</div>
## 04. IAM (identity and access management)


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
## 15. VPC & Networking

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
## 21. AWS architecting & Ecosystem


---

## Source

+ Stephane maarek [Ultimate AWS Certified Cloud Practitioner - 2021](https://www.udemy.com/course/aws-certified-cloud-practitioner-new/)

---
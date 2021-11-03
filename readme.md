# AWS Cloud Practitioner

## Source
+ Stephane maarek [Ultimate AWS Certified Cloud Practitioner - 2021](https://www.udemy.com/course/aws-certified-cloud-practitioner-new/)

---

## Table of contents

10. [Other compute services](#10-ecs-lamda-batch-lightsail)
  + [what is docker?](#what-is-docker)
  + [ECS](#ecs)
  + [lamda](#lamda)
  + [batch](#batch)
  + [lightsail](#lightsail)

11. [Deploying and managing infrastructure at scale](#11-deploying-and-managing-infrastructure-at-scale)


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

12. [Leveraging AWS Global infrastructure](#12-leveraging-aws-global-infrastructure)

---

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
## 12. Leveraging AWS Global infrastructure

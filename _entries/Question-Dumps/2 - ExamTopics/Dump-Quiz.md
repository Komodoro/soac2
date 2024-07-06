---
sectionid: ExamTopicsDump
sectionclass: h3
parent-id: Questions
title: 2 - ExamTopics
number: 2200
---

### Question 1

*  A company has an internal web application that runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto
Scaling group in a single Availability Zone. A SysOps administrator must make the application highly available.
Which action should the SysOps administrator take to meet this requirement?

    A. Increase the maximum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    B. Increase the minimum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    C. Update the Auto Scaling group to launch new instances in a second Availability Zone in the same AWS Region.
    D. Update the Auto Scaling group to launch new instances in an Availability Zone in a second AWS Region.

**Correct Answer: C**

### Question 2

*  A company hosts a website on multiple Amazon EC2 instances that run in an Auto Scaling group. Users are reporting slow responses during peak times between
6 PM and 11 PM every weekend. A SysOps administrator must implement a solution to improve performance during these peak times.
What is the MOST operationally efficient solution that meets these requirements?

    A. Create a scheduled Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function to increase the desired capacity before peak times.
    B. Configure a scheduled scaling action with a recurrence option to change the desired capacity before and after peak times.
    C. Create a target tracking scaling policy to add more instances when memory utilization is above 70%.
    D. Configure the cooldown period for the Auto Scaling group to modify desired capacity before and after peak times.



**Correct Answer: C**

### Question 3/71

* A company wants to improve the overall availability and performance of its applications that are hosted on AWS.
Which AWS service should the company use?

A. AWS Global Accelerator

B. Amazon Lightsail

C. Amazon Connect

D. AWS Storage Gateway

**Correct Answer: A**

### Question 4/71

* A company runs a web application on Amazon EC2 instances. The application must run constantly and is expected to run indefinitely without interruption.
Which EC2 instance purchasing options will meet these requirements MOST cost-effectively? (Select TWO.)

A. On-Demand Instances

B. Spot Instances.

C. Reserved Instances

D. Savings Plans

E. Dedicated Hosts

**Correct Answer: C,D**

Amazon EC2 provides the following purchasing options to enable you to optimize your costs based on your needs:
* On-Demand Instances - Pay, by the second, for the instances that you launch.
* Savings Plans - Reduce your Amazon EC2 costs by making a commitment to a consistent amount of usage, in USD per hour, for a term of 1 or 3 years.
* Reserved Instances - Reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years.
* Spot Instances - Request unused EC2 instances, which can reduce your Amazon EC2 costs significantly.
* Dedicated Hosts - Pay for a physical host that is fully dedicated to running your instances, and bring your existing per-socket, per-core, or per-VM software licenses to reduce costs.
* Dedicated Instances - Pay, by the hour, for instances that run on single-tenant hardware.
* Capacity Reservations - Reserve capacity for your EC2 instances in a specific Availability Zone for any duration.


If you require a capacity reservation, purchase Reserved Instances or Capacity Reservations for a specific Availability Zone.

Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if they can be interrupted. 

Dedicated Hosts or Dedicated Instances can help you address compliance requirements and reduce costs by using your existing server-bound software licenses.


### Question 5/71

* A company that is migrating to the AWS Cloud wants to reduce the operational costs of running its databases. Which combination of actions should the company take to achieve this goal (Select TWO.)

A. Deploy resources across multiple Availability Zones.

B. Activate Amazon DynamoDB Accelerator (DAX)

C. Use the AWS global infrastructure to benefit from economies of scale

D. Decrease operational tasks by using AWS managed services.

E. Automate changes and responses to events.

**Correct Answer: D,E**

### Question 6/71

* A company needs to transfer 60 TB of data to the AWS Cloud in a secure manner.
Which of the following should the company use to meet these requirements?

A. AWS Snowball Edge device

B. Amazon Elastic Block Store (Amazon EBS)

C. Amazon Elastic File System (Amazon EFS)

D. Amazon S3

**Correct Answer: A**
* https://aws.amazon.com/blogs/storage/migrating-hundreds-of-tb-of-data-to-amazon-s3-with-aws-datasync/


### Question 7/71

* Which AWS service provides managed DDoS protection?

A. Amazon Inspector

B. Amazon GuardDuty

C. AWS Firewall Manager

D. AWS Shield

**Correct Answer: D**


### Question 8/71

* A company wants to offer direct phone and chat channels for customer service. The company needs a pay-as-you-go solution that remote customer service agents can use to create and manage voice and chat contact flows.
Which AWS service will meet these requirements?

A. Amazon Connect

B. AWS Direct Connect

C. Amazon Cognito

D. Amazon EventBridge (Amazon CloudWatch Events)

**Correct Answer: A**

### Question 9/71

* Which AWS service provides an isolated virtual network to connect AWS services and resources?

A. Amazon EC2

B. Amazon DynamoDB

C. Amazon Lightsail

D. Amazon VPC

**Correct Answer: D**

* Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined. This virtual network closely resembles a traditional network that you'd operate in your own data center, with the benefits of using the scalable infrastructure of AWS.


### Question 10/71

* A company stores several terabytes of data in an Amazon S3 bucket. The company needs to query the data by using standard SQL and does not want to set up infrastructure. Which AWS service should the company use to meet these. requirements?

A. Amazon Athena

B. Amazon EC2

C. Amazon Redshift

D. Amazon RDS

**Correct Answer: A**


### Question 11/71

* Which solution provides a fast, automated and repeatable method of deploying AWS Cloud infrastructure to multiple AWS Regions?

A. Use AWS CodeStar to set up a continuous delivery toolchain for automated deployment

B. Create and use an AWS CloudFormation template

C. Use AWS Systems Manager to automate management tasks such as creating Amazon EC2 Amazon Machine images (AMIS) and applying patches

D. Create and launch an Amazon EC2 Amazon Machine Image (AMI) containing the source code with butt-m deployment hooks lo launch other AWS services

**Correct Answer: B**

### Question 12/71

* Which of the following are AWS best practice recommendations for the use of AWS Identity and Access Management (IAM)? (Select TWO.)

A. Use the AWS account root user for daily access.

B. Use access keys and secret access keys on Amazon EC2.

C. Rotate credentials on a regular basis.

D. Create a shared set of access keys for system administrators.

E. Configure multi-factor authentication (MFA).

**Correct Answer: C,E**
* If you do have an access key for your AWS account root user, delete it. If you must keep it, rotate (change) the access key regularly. To delete or rotate your root user access keys, go to the My Security Credentials page in the AWS Management Console and sign in with your account's email address and password. You can manage your access keys in the Access keys section. For more information about rotating access keys, see Rotating access keys.


### Question 13/71

* A company implements an Amazon EC2 Auto Scaling policy along with an Application Load Balancer to automatically recover unhealthy applications that run on Amazon EC2 instances.
Which pillar of the AWS Well-Architected Framework does this action cover?

A. Performance efficiency

B. Security

C. Reliability

D. Operational excellence

**Correct Answer: C**


### Question 14/71

* Which approach will enhance a user's security on AWS?

A. Create a hybrid architecture by using AWS Direct Connect.

B. Use Multi-AZ deployments with Amazon RDS.

C. Monitor application-specific information with AWS X-Ray.

D. Encrypt data by using AWS Key Management Service (AWS KMS).

**Correct Answer: D**

### Question 15/71
* A company needs to report on events that involve the specific AWS services that the company uses.
Which AWS service or resource can the company use with Amazon CloudWatch to meet this requirement?

A. Amazon Inspector

B. AWS Personal Health Dashboard

C. AWS Trusted Advisor

D. AWS CloudTrail logs

**Correct Answer: D**

### Question 16/71

* Which service enables customers to audit API calls in their AWS accounts?

A. AWS CloudTrail

B. AWS Trusted Advisor

C. Amazon Inspector

D. AWS X-Ray

**Correct Answer: A**
* AWS Audit Manager is integrated with AWS CloudTrail, a service that provides a record of actions taken by a user, role, or an AWS service in Audit Manager. CloudTrail captures all API calls for Audit Manager as events.

### Question 17/71
* A company is moving its on-premises NoSQL database to the AWS Cloud Which AWS service should the company use for the NoSQL database?

A. Amazon Redshift

B. Amazon Quantum Ledger Database (Amazon QLDB)

C. Amazon DynamoDB

D. Amazon RDS for MySQL

**Correct Answer: C**


### Question 18/71
* A company is undergoing a security audit. The audit includes security validation and compliance validation of the AWS infrastructure and services that the company uses. The auditor needs to locate compliance-related information and must download AWS security and compliance documents. These documents include the System and Organization Control (SOC) reports.
Which AWS service or group can provide these documents?

A. AWS Config

B. AWS Support

C. AWS Abuse team

D. AWS Artifact

**Correct Answer: D**


### Question 19/71

* Which Reserved Instance (Rl) provides the HIGHEST average cost savings compared to an On-Demand Instance?

A. 1-year. No Upfront. Standard Rl

B. 3-year. No Upfront. Convertible Rl

C. 1-year. All Upfront. Convertible Rl

D. 3-year. All Upfront, Standard Rl

**Correct Answer: D**

### Question 20/71

* A company wants a cost-effective option when running its applications in an Amazon EC2 instance for short time periods. The applications can be interrupted. Which EC2 instance type will meet these requirements?

A. Spot Instances

B. On-Demand Instances

C. Reserved Instances

D. Dedicated Instances

**Correct Answer: A**
* Spot Instances - Spot Instances are the most cost-effective choice if you are flexible about when your applications run and if your applications can be interrupted.

### Question 21/71

* Which task is the responsibility of the customer according to the AWS snared responsibility model?

A. Patch the Amazon DynamoDB operating system

B. Protect the hardware that runs AWS services

C. Secure Amazon CloudFront edge locations by allowing physical access according to the principle of least privilege

D. Use AWS Identity and Access Management (IAM) according to the principle of least privilege

**Correct Answer: D**

### Question 22/71
* A company plans to create a data lake that uses Amazon S3. Which factor will have the MOST effect on cost?

A. The addition of S3 bucket policies

B. The selection of S3 storage tiers

C. S3 ingest fees for each request

D. Charges to transfer existing data into Amazon S3

**Correct Answer: D**

### Question 23/71
* What is a benefit of using AWS serverless computing?

A. Application deployment and management are not required.

B. Application security will be fully managed by AWS.

C. Monitoring and logging are not needed.

D. Management of infrastructure is offloaded to AWS.

**Correct Answer: D**

* Serverless computing allows you to build and run applications and services without thinking about servers. With serverless computing, your application still runs on servers, but all the server management is done by AWS.

### Question 24/71
* A company runs applications that process credit card information. Auditors have asked if the AWS environment has changed since the previous audit. If the AWS environment has changed, the auditors want to know how it has changed. Which AWS services can provide this information? (Select TWO.)

A. AWS Artifact

B. AWS Trusted Advisor

C. AWS Config

D. AWS Cloud Trail

E. AWS Identity and Access Management (IAM)

**Correct Answer: C,D**

* AWS Artifact is your go-to, central resource for compliance-related information that matters to you. It provides on-demand access to AWS' security and compliance reports and select online agreements.
* AWS Trusted Advisor provides recommendations that help you follow AWS best practices. Trusted Advisor evaluates your account by using checks. These checks identify ways to optimize your AWS infrastructure, improve security and performance, reduce costs, and monitor service quotas.
* AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. Config continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations.
* AWS CloudTrail enables auditing, security monitoring, and operational troubleshooting by tracking user activity and API usage. CloudTrail logs, continuously monitors, and retains account activity related to actions across your AWS infrastructure, giving you control over storage, analysis, and remediation actions.
* AWS Identity and Access Management (IAM) provides fine-grained access control across all of AWS. With IAM, you can specify who can access which services and resources, and under which conditions. With IAM policies, you manage permissions to your workforce and systems to ensure least-privilege permissions.


### Question 25/71
* A company recently mutated to AWS and wants to enable intelligent threat protection and continuous monitoring across all of its AWS accounts.
Which AWS service should the company use lo achieve this goal?

A. Amazon Detective

B. Amazon Macie

C. AWS Shield

D. Amazon GuardDuty

**Correct Answer: D**

### Question 26/71
* A company wants to organize its users so that the company can grant permissions to the users as a group. Which AWS service or tool can the company use to meet this requirement?

A. Resource groups

B. AWS identity and Access Management (IAM)

C. Security groups

D. AWS Security Hub

**Correct Answer: B**

### Question 27/71
* A company is running an Amazon EC2 instance in a VPC.
Which of the following can the company use to route and filter incoming network requests for the EC2 instance?

A. Route tables and web application firewalls

B. Security groups and route tables

C. Route tables and AWS Shield

D. Security groups and a network intrusion system

**Correct Answer: B**

### Question 28/71
* Which of the following are design principles of the reliability pillar of the AWS Well-Architected Framework? (Select TWO.)

A. Perform operations as code.

B. Stop guessing capacity.

C. Make changes to infrastructure by using automation.

D. Use build and deployment management systems.

E. Adopt serverless architecture whenever possible.

**Correct Answer: B,C**

### Question 29/71
* Which AWS service offers threat detection and continuously monitors for malicious activity and unauthorized behavior in AWS accounts?

A. AWS Config

B. Amazon GuardDuty

C. Amazon Made

D. Amazon Inspector

**Correct Answer: B**

### Question 30/71
* Which tasks require use of the AWS account root user? (Select TWO.)

A. Grouping resources in AWS Systems Manager

B. Running applications in Amazon Elastic Kubernetes Service (Amazon EKS)

C. Modifying an Amazon EC2 instance type

D. Changing an AWS Support plan

E. Closing an AWS account

**Correct Answer: D,E**

### Question 31/71

* A company is developing a new Node.js application. The application must have a scalabe NoSQL database to meet increasing demand as the popularity of the application grown.
Which AWS services will meet the requirements for the database?

A. Amazon Aurora Serverless

B. Amazon Redshift

C. Amazon ElastiCache

D. Amazon DynamoDB

**Correct Answer: D**


### Question 32/71
* A company needs to process data from satellite communications without managing any infrastructure.
Which AWS service should the company use to meet these requirements?

A. Amazon CloudWatch

B. Amazon Aurora

C. Amazon Athena

D. AWS Ground Station

**Correct Answer: D**

* AWS Ground Station is a fully managed service that lets you control satellite communications, process data, and scale your operations without having to worry about building or managing your own ground station infrastructure. Satellites are used for a wide variety of use cases, including weather forecasting, surface imaging, communications, and video broadcasts. Ground stations form the core of global satellite networks. With AWS Ground Station, you have direct access to AWS services and the AWS Global Infrastructure including a low-latency global fiber network. For example, you can use Amazon S3 to store the downloaded data, Amazon Kinesis Data Streams for managing data ingestion from satellites, and Amazon SageMaker for building custom machine learning applications that apply to your data sets. You can save up to 80% on the cost of your ground station operations by paying only for the actual antenna time used, and relying on the global footprint of ground stations to download data when and where you need it. There are no long-term commitments, and you gain the ability to rapidly scale your satellite communications on-demand when your business needs it.


### Question 33/71

* A company requires an isolated environment within AWS for security purposes. Which action can be taken to accomplish this?

A. Create an AWS Direct Connect connection between the company and AWS.

B. Create a separate Availability Zone to host the resources.

C. Create a separate VPC to host the resources.

D. Create a placement group to host the resources.

**Correct Answer: C**

### Question 34/71
* A company needs to schedule the rotation of database credentials in the AWS Cloud.
Which AWS service should the company use to perform this task?

A. AWS Identity and Access Management (IAM)

B. AWS Managed Services (AMS)

C. Amazon RDS

D. AWS Secrets Manager

**Correct Answer: D**

* AWS Secrets Manager makes it easier to rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle. The key features of this service include the ability to:
    1. Secure and manage secrets centrally. You can store, view, and manage all your secrets centrally. By default, Secrets Manager encrypts these secrets with encryption keys that you own and control. You can use fine-grained IAM policies or resource-based policies to control access to your secrets. You can also tag secrets to help you discover, organize, and control access to secrets used throughout your organization.
    2. Rotate secrets safely. You can configure Secrets Manager to rotate secrets automatically without disrupting your applications. Secrets Manager offers built-in integrations for rotating credentials for all Amazon RDS databases (MySQL, PostgreSQL, Oracle, Microsoft SQL Server, MariaDB, and Amazon Aurora.) You can also extend Secrets Manager to meet your custom rotation requirements by creating an AWS Lambda function to rotate other types of secrets.
    3. Transmit securely. Secrets are transmitted securely over Transport Layer Security (TLS) protocol 1.2. You can also use Secrets Manager with Amazon Virtual Private Cloud (Amazon VPC) endpoints powered by AWS Privatelink to keep this communication within the AWS network and help meet your compliance and regulatory requirements to limit public internet connectivity.
    4. Pay as you go. Pay for the secrets you store in Secrets Manager and for the use of these secrets; there are no long-term contracts, licensing fees, or infrastructure and personnel costs. For example, a typical production-scale web application will generate an estimated monthly bill of $6. If you follow along the instructions in this blog post, your estimated monthly bill for Secrets Manager will be $1. Note: you may incur additional charges for using Amazon RDS and Amazon Lambda, if you've already consumed the free tier for these services.

* Now that you're familiar with Secrets Manager features, I'll show you how to store and automatically rotate credentials for an Oracle database hosted on Amazon RDS. I divided these instructions into three phases:

    1. Phase 1: Store and configure rotation for the superuser credential

    2. Phase 2: Store and configure rotation for the application credential

    3. Phase 3: Retrieve the credential from Secrets Manager programmatically


### Question 35/71

* A company wants to use a server less compute service for an application.
When AWS service will meet tins requirement?

A. AWS Elastic Beanstalk

B. AWS Lambda

C. AWS CloudFormation

D. Elastic Load Balancing

**Correct Answer: B**

### Question 36/71
* A company needs a centralized, secure way to create and manage cryptographic keys. The company will use the keys across a wide range of AWS services and applications. The company needs to track and document when the keys are created, used, and deleted.
Which AWS service or feature will meet these requirements?

A. AWS Secrets Manager

B. AWS License Manager

C. AWS Systems Manager Parameter Store

D. AWS Key Management Service (AWS KMS)

**Correct Answer: D**

* AWS Key Management Service (AWS KMS) makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications. AWS KMS is a secure and resilient service that uses hardware security modules that have been validated under FIPS 140-2, or are in the process of being validated, to protect your keys. AWS KMS is integrated with AWS CloudTrail to provide you with logs of all key usage to help meet your regulatory and compliance needs.


### Question 37/71
* Which AWS service is a fully hosted version control service?

A. AWS CodeDeploy

B. AWS CodeBuild

C. AWS CodeCommit

D. AWS CodeStar

**Correct Answer: C**

### Question 38/71
* A user needs the ability to access as many resources as are needed. The user also needs the ability to scale up and scale down with only a few minutes of notice. Which benefit of the AWS Cloud describes these abilities?

A. Economy of scale

B. Pay-as-you-go pricing

C. Ratability

D. Elasticity

**Correct Answer: D**

### Question 39/71
* How can a user protect an Amazon EC2 instance from a suspicious IP address?

A. Block the IP on the outbound rule of a security group.

B. Block the IP on the inbound rule of a security group and network ACL.

C. Block the IP on the outbound rule of a security group and network ACL.

D. Block the IP on the inbound rule of a network ACL.

**Correct Answer: D**

### Question 40/71
* Which of the following gives a company the ability to fake advantage of tiered pricing tor services across multiple AWS member accounts?

A. AWS Organizations consolidated billing

B. AWS Organizations service control policies (SCPs)

C. All Upfront Reserved instances

D. Cost Explorer utilization reports

**Correct Answer: A**

### Question 41/71

* Which pillar of the AWS Well-Architected Framework includes the continual improvement of processes and procedures as a priority?

A. Performance efficiency

B. Operational excellence

C. Reliability

D. Cost optimization

**Correct Answer: B**

### Question 42/71

* Which of the following are characteristics of a serverless application that runs in the AWS Cloud? (Select TWO.)

A. Users have a choice of operating systems.

B. The application has built-in fault tolerance.

C. The application can scale based on demand.

D. Users can run Amazon EC2 Spot Instances.

E. Users must manually configure Amazon EC2 instances.

**Correct Answer: B,C**


### Question 43/71
* A company needs to run an application on Amazon EC2 instances. The instances cannot be interrupted at any time. The company needs an instance purch asing option that requires no long-term commitment or upfront payment. Which instance purchasing option will meet these requirements MOST cost-effectively?

A. On-Demand Instances

B. Spot Instances

C. Reserved Instances

D. Dedicated Hosts

**Correct Answer: A**

### Question 44/71
* Which of the following are AWS compute services? (Select TWO.)

A. Amazon Lightsail

B. AWS Systems Manager

C. AWS CloudFormation

D. AWS Batch

E. Amazon Inspector

**Correct Answer: A,D**

* Amazon Lightsail is designed to be the easiest way to launch and manage a virtual private server with AWS. Lightsail plans include everything you need to jumpstart your project - a virtual machine, SSD-based storage, data transfer, DNS management, and a static IP address - for a low, predictable price.

* AWS Batch enables developers, scientists, and engineers to easily and efficiently run hundreds of thousands of batch computing jobs on AWS. AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory-optimized instances) based on the volume and specific resource requirements of the batch jobs submitted. With AWS Batch, there is no need to install and manage batch computing software or server clusters that you use to run your jobs, allowing you to focus on analyzing results and solving problems. AWS Batch plans, schedules, and runs your batch computing workloads across the full range of AWS compute services and features, such as Amazon EC2 and Spot Instances.


### Question 45/71
* A company wants to migrate its on-premises Microsoft SQL Server database server to the AWS Cloud. The company has decided to use Amazon EC2 instances to run this database.
Which of the following is the company responsible for managing, according to the AWS shared responsibility model?

A. Network connectivity of the host server

B. EC2 hypervisor

C. Security patching of the guest operating system

D. Uptime service level agreement (SLA) for the EC2 instances

**Correct Answer: C**

### Question 46/71

* Which Amazon S3 feature or storage class uses the AWS backbone network and edge locations to reduce latencies from the end user to Amazon S3?

A. S3 Cross-Region Replication

B. S3 Transfer Acceleration

C. S3 Event Notifications

D. S3 Standard-Infrequent Access (S3 Standard-IA)

**Correct Answer: B**

### Question 47/71

* Which of the following is available to a company that has an AWS Business Support plan?

A. AWS Health API

B. AWS DDoS Response Team (DRT)

C. AWS technical account manager (TAM)

D. AWS Support concierge

**Correct Answer: A**

### Question 48/71
* Which characteristic of the AWS Cloud helps users eliminate underutilized CPU capacity?

A. Agility

B. Durability

C. Reliability

D. Elasticity

**Correct Answer: D**

### Question 49/71
* A company wants to build an application that consists entirely of microservices.
Which AWS Cloud architecture design principle supports this goal?

A. Think parallel

B. Implement elasticity

C. Decouple components

D. Stop guessing capacity

**Correct Answer: C**

### Question 50/71

* A user has been granted permission to change their own IAM user password. Which AWS services can the user use to change the password? (Select TWO.)

A. AWS Management Console

B. AWS Key Management Service (AWS KMS)

C. AWS Command Line Interface (AWS CLI)

D. AWS Resource Access Manager (AWS RAM)

E. AWS Secrets Manager

**Correct Answer: A,C**

### Question 51/71
* A company recently created its first AWS account.
Which AWS services will require the use of a VPC? (Select TWO.)

A. Amazon Cognito

B. Amazon EC2

C. Amazon DynamoDB

D. Amazon S3

E. Amazon Elastic File System (Amazon EFS)

**Correct Answer: B,E**

### Question 52/71
* A company is running a workload on AWS. The company wants to protect the workload from DDoS attacks.
When AWS service will meet these requirements?

A. Amazon VPC

B. AWS Shield

C. AWS Artifact

D. AWS Identity and Access Management (IAM)

**Correct Answer: B**

### Question 53/71
* Which AWS service should a company use to create a NoSQL database?

A. Amazon DynamoDB

B. Amazon Aurora

C. Amazon Redshift

D. Amazon Neptune

**Correct Answer: A**

### Question 54/71
* Which benefit of cloud computing gives a company the ability to deploy applications to users all over the world through a network of AWS Regions, Availability Zones, and edge locations?

A. Economy of scale

B. High availability

C. Global reach

D. Agility

**Correct Answer: C**

### Question 55/71
* A company discovered unauthorized access to resources in its on-premises data center. Upon investigation, the company found that the requests originated from a resource hosted on AWS. Which AWS team should the company contact to report this issue?

A. AWS Customer Service team

B. AWS Abuse team

C. AWS Sales team

D. AWS Technical Support team

**Correct Answer: D**

### Question 56/71
* Which AWS service supports the analysis, investigation, and identification of the root cause of security events and suspicious activities in an AWS account?

A. Amazon Detective

B. Amazon Inspector

C. Amazon CloudWatch

D. Amazon Macie

**Correct Answer: B**

### Question 57/71
* A company is using Amazon RDS.
Which task is the company's responsibility, according to the AWS shared responsibility model?

A. Apply encryption options for the database.

B. Manage the underlying server hardware on which Amazon RDS runs.

C. Apply patches to the underlying operating system.

D. Apply minor patches to the database.

**Correct Answer: A**

### Question 58/71
* Which AWS service provides intelligent recommendations to improve code quality and identify an application is most expensive lines of code?

A. AWS CodeCommit

B. AWS CodeDeploy

C. Amazon CodeGuru

D. AWS CodeStar

**Correct Answer: C**

### Question 59/71
* Which of the following consists of one or more isolated data centers in the same regional area that are interconnected through low-latency networks?

A. Edge location

B. Private networking

C. AWS Region

D. Availability Zone

**Correct Answer: D**

### Question 60/71
* Which AWS benefit enables users to deploy cloud infrastructure that consists of multiple geographic regions connected by a network with low latency, high throughput, and redundancy?

A. Economies of scale

B. Security

C. Elasticity

D. Global reach

**Correct Answer: D**

* The AWS Global Cloud Infrastructure is the most secure, extensive, and reliable cloud platform, offering over 200 fully featured services from data centers globally. Whether you need to deploy your application workloads across the globe in a single click, or you want to build and deploy specific applications closer to your end-users with single-digit millisecond latency, AWS provides you the cloud infrastructure where and when you need it.


### Question 61/71

* A retail company is building a new mobile app. The company is evaluating whether to build the app at an on-premises data center or in the AWS Cloud. Which of the following are benefits of building this app in the AWS Cloud? (Select TWO.)

A. A large, upfront capital expense and low variable expenses

B. Complete control over the physical security of the infrastructure

C. Increased speed for trying out new projects

D. Ability to pick the specific data centers that will host the application servers

E. Flexibility to scale up in minutes as the application becomes popular

**Correct Answer: C,E**

### Question 62/71

* What are characteristics of AWS IAM users and groups? (Select TWO.)

A. Groups can be nested and can contain other groups.

B. All new users are automatically added to a default group

C. Groups can contain users only and cannot be nested

D. A user can be a member of multiple groups

E. A user can only be a member of a single group at one time.

**Correct Answer: C,D**

### Question 63/71
* A company stores configuration files in an Amazon S3 bucket. These configuration files must be accessed by applications that are running on Amazon EC2 instances.
According to AWS security best practices, how should the company grant permissions to allow the applications to access the S3 bucket?

A. Use the AWS account root user access keys.

B. Use an IAM role with the necessary permissions.

C. Activate multi-factor authentication (MFA) and versioning on the S3 bucket.

D. Use the AWS access key ID and the EC2 secret access key.

**Correct Answer: B**

### Question 64/71
* A company is considering implementing a new workload m the AWS Cloud However, the company first wants to forecast the potential cost.
Which tool should the company use to estimate the cost of the workload?

A. Cost Explorer

B. AWS Billing and Cost Management dashboard

C. AWS Pricing Calculator

D. AWS Cost and Usage Report

**Correct Answer: C**

### Question 65/71

* A company needs steady and predictable performance from its Amazon EC2 instances at the lowest possible cost. The company also needs the ability to scale resources to ensure that it has the right resources available at the right time.
Which AWS service or resource will meet these requirements?

A. Amazon CloudWatch

B. Application Load Balancer

C. AWS Batch

D. Amazon EC2 Auto Scaling

**Correct Answer: D**

* AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

### Question 66/71
* A company has an on-premises Oracle database. The company spends a significant amount of time on database administration activities. The company is moving the database to AWS and needs to minimize the time that is requited lot these administration activities Which AWS service should the company use to meet this requirement''

A. Amazon DynamoDB

B. Amazon ElastiCache

C. Amazon EC2

D. Amazon RDS

**Correct Answer: D**

### Question 67/71
* Which AWS services provide high availability across multiple Availability Zones by default? (Select TWO.)

A. Amazon Redshift

B. Amazon Elastic File System (Amazon EFS)

C. Amazon S3

D. Amazon Elastic Block Store (Amazon EBS)

E. Amazon EC2

**Correct Answer: A,D**


### Question 68/71

* A company is running a Microsoft SOL Server instance on premises and is migrating its application to AWS. The company lacks the resources needed to refactor the application but management wants to reduce operational overhead as part of the migration.
Which database service would MOST effectively support these requirements?

A. Amazon Redshift

B. Microsoft SQL Server on Amazon EC2

C. Amazon DynamoDB

D. Amazon RDS for SQL Server

**Correct Answer: D**

### Question 69/71

* Which of the following are advantages of moving to the AWS Cloud? (Select TWO.)

A. Users can implement all AWS services in seconds.

B. Users experience increased speed and agility.

C. AWS assumes all responsibility for the security of infrastructure and applications.

D. Users benefits from massive economies of scale.

E. Users can more hardware from their data center to the AWS Cloud.

**Correct Answer: B,D**

### Question 70/71

* A company needs to store code in a version control system. The company also needs to continually deploy updated code through a series of automated steps (build test package and deploy).
Which combination of AWS services will meet these requirements? (Select TWO.)

A. AWS CloudFormation

B. AWS CodeCommit

C. AWS Control Tower

D. AWS CodePipeline

E. AWS Elastic Beanstalk

**Correct Answer: B,D**

### Question 71/71

* A company wants to receive alerts when resources that are launched in the company's AWS account reach 80% of their service quotas. Which AWS service should the company use to meet this requirement?

A. AWS Trusted Advisor

B. Amazon inspector

C. AWS Config

D. AWS CloudTrail

**Correct Answer: A**

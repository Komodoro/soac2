---
sectionid: Dump321012023
sectionclass: h2
parent-id: Questions
title: Dump 3 - 21-01-2023
number: 3300
---

NO.1 A retail company is migrating its IT infrastructure applications from on premises to the AWS
Cloud.
Which costs will the company eliminate with this migration? (Select TWO.)

A. Cost of data center operations
B. Cost of application licensing
C. Cost of marketing campaigns
D. Cost of physical server hardware
E. Cost of network management

Answer: A,D

NO.2 Which of the following are AWS best practice recommendations for the use of AWS Identity
and Access Management (IAM)? (Select TWO.)

A. Use the AWS account root user for daily access.
B. Use access keys and secret access keys on Amazon EC2.
C. Rotate credentials on a regular basis.
D. Create a shared set of access keys for system administrators.
E. Configure multi-factor authentication (MFA).

Answer: C,E

Explanation:
If you do have an access key for your AWS account root user, delete it. If you must keep it, rotate
(change) the access key regularly. To delete or rotate your root user access keys, go to the My
Security Credentials page in the AWS Management Console and sign in with your account's email
address and password. You can manage your access keys in the Access keys section. For more
information about rotating access keys, see Rotating access keys.

NO.3 Which AWS service or tool lists all the users in an account and reports on the status of account
details, including passwords, access keys, and multi-factor authentication (MFA) devices?

A. WS Shield
B. AWS Trusted Advisor
C. Amazon Inspector
D. IAM credential report

Answer: D

Explanation:
You can generate and download a credential report that lists all users in your account and the status
of their various credentials, including passwords, access keys, and MFA devices. You can get a
credential report from the AWS Management Console, the AWS SDKs and Command Line Tools , or
the IAM API.
NO.4 Which databases are available on Amazon RDS? (Select TWO.)
A. Sybase
B. Microsoft SQL Server
C. IBM Db2
D. MongoDB
E. PostgreSQL

Answer: B,E

NO.5 Which AWS service supports the analysis, investigation, and identification of the root cause of
security events and suspicious activities in an AWS account?

A. Amazon Inspector
B. Amazon Macie
C. Amazon Detective
D. Amazon CloudWatch

Answer: C

Explanation:
Amazon Detective makes it easy to analyze, investigate, and quickly identify the root cause of
potential security issues or suspicious activities. Ref :
https://aws.amazon.com/it/detective/features/#:~:text=Amazon%20Detective%20makes%20it%20e
asy,security%20issues%20or%20suspicious%20activities.

NO.6 A user has been granted permission to change their own IAM user password. Which AWS
services can the user use to change the password? (Select TWO.)

A. AWS Command Line Interface (AWS CLI)
B. AWS Key Management Service (AWS KMS)
C. AWS Management Console
D. AWS Resource Access Manager (AWS RAM)
E. AWS Secrets Manager

Answer: A,C

NO.7 Which AWS service allows for file sharing between multiple Amazon EC2 instances?
A. AWS Direct Connect
B. AWS Snowball Edge
C. AWS Backup
D. Amazon Elastic File System (Amazon EFS)

Answer: D

Explanation:
Amazon EFS provides shared file storage for use with compute instances in the AWS Cloud and onpremises servers. Applications that require shared file access can use Amazon EFS for reliable file
storage delivering high aggregate throughput to thousands of clients simultaneously.

NO.8 Which AWS service is a relational database compatible with MySQL and PostgreSQL?
A. Amazon Redshift
B. Amazon DynamoDB
C. Amazon Aurora
D. Amazon Neptune

Answer: C

NO.9 A company is reviewing the current costs of running its own infrastructure on premises. The
company wants to compare these on-premises costs to the costs of running infrastructure in the AWS
Cloud.
How should the company make this comparison?

A. Review the AWS shared responsibility model.
B. Audit existing software and hardware licensing costs.
C. Analyze the AWS Well-Architected Framework.
D. Use Migration Evaluator.

Answer: D

NO.10 Elasticity in the AWS Cloud refers to which of the following? (Select TWO.)

A. How quickly an Amazon EC2 instance can be restarted
B. The ability to right size resources as demand shifts
C. The maximum amount of RAM an Amazon EC2 instance can use
D. The pay-as-you-go billing model
E. How easily resources can be procured when they are needed

Answer: B,E

Explanation:
The AWS Well-Architected Framework defines elasticity as: The ability to acquire resources as you
need them and release resources when you no longer need them. In the cloud, you want to do this
automatically

https://dev.to/aws-builders/what-does-elastic-mean-cloud-concepts-explained-4anb#:~:text=The%20AWS%20Well%2DArchitected%20Framework%20defines%20elasticity%20as%3

NO.11 A company is undergoing a security audit. The audit includes security validation and
compliance validation of the AWS infrastructure and services that the company uses. The auditor
needs to locate compliance-related information and must download AWS security and compliance
documents. These documents include the System and Organization Control (SOC) reports.
Which AWS service or group can provide these documents?

A. AWS Abuse team
B. AWS Artifact
C. AWS Support
D. AWS Config

Answer: B

Explanation:
* Portal that provides customers with on-demand access to AWS compliance documentation and
AWS agreements * Artifact Reports - Allows you to download AWS security and compliance
documents from third-party auditors, like AWS ISO certifications, Payment Card Industry (PCI), and
System and Organization Control (SOC) reports * Artifact Agreements - Allows you to review, accept,
and track the status of AWS agreements such as the Business Associate Addendum (BAA) or the
Health Insurance Portability and Accountability Act (HIPAA) for an individual account or in your
organization * Can be used to support internal audit or compliance

NO.12 A company is running an Amazon EC2 instance in a VPC.
Which of the following can the company use to route and filter incoming network requests for the
EC2 instance?

A. Route tables and web application firewalls
B. Security groups and route tables
C. Security groups and a network intrusion system
D. Route tables and AWS Shield

Answer: B

NO.13 Which of the following are aspects of the AWS shared responsibility model? (Select TWO.)

A. Configuration management of infrastructure devices is the customer's responsibility.
B. For Amazon S3, AWS operates the infrastructure layer, the operating systems, and the platforms.
C. AWS is responsible for protecting the physical cloud infrastructure.
D. AWS is responsible for training the customer's employees on AWS products and services.
E. For Amazon EC2, AWS is responsible for maintaining the guest operating system.

Answer: A,C

Explanation:

AWS responsibility "Security of the Cloud" - AWS is responsible for protecting the infrastructure that
runs all of the services offered in the AWS Cloud. This infrastructure is composed of the hardware,
software, networking, and facilities that run AWS Cloud services.
Customer responsibility "Security in the Cloud" - Customer responsibility will be determined by the
AWS Cloud services that a customer selects. This determines the amount of configuration work the
customer must perform as part of their security responsibilities. For example, a service such as
Amazon Elastic Compute Cloud (Amazon EC2) is categorized as Infrastructure as a Service (IaaS) and,
as such, requires the customer to perform all of the necessary security configuration and
management tasks. Customers that deploy an Amazon EC2 instance are responsible for management
of the guest operating system (including updates and security patches), any application software or
utilities installed by the customer on the instances, and the configuration of the AWS-provided
firewall (called a security group) on each instance. For abstracted services, such as Amazon S3 and
Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and
customers access the endpoints to store and retrieve data. Customers are responsible for managing
their data (including encryption options), classifying their assets, and using IAM tools to apply the
appropriate permissions.


NO.14 What is the customer ALWAYS responsible for managing, according to the AWS shared
responsibility model?

A. Software licenses
B. Networking
C. Customer data
D. Encryption keys

Answer: C

NO.15 A company wants to improve the overall availability and performance of its applications that
are hosted on AWS.
Which AWS service should the company use?

A. Amazon Connect
B. Amazon Lightsail
C. AWS Global Accelerator
D. AWS Storage Gateway

Answer: C

NO.16 Which AWS service keeps track of SSL/TLS certificates, creates new certificates, and processes
renewals?

A. AWS Identity and Access Management (1AM)
B. AWS Certificate Manager (ACM)
C. AWS Config
D. AWS Trusted Advisor

Answer: B

Explanation:

AWS Certificate Manager helps manage the challenges of maintaining SSL/TLS certificates, including
certificate renewals so you don't have to worry about expiring certificates. Learn more about
provisioning, managing, and deploying public and private SSL/TLS certificates.

NO.17 A company has a global website with static content.
Which AWS service will deliver the static content with low latency?

A. AWS Lambda
B. Amazon CloudFront
C. Amazon EC2 Auto Scaling
D. AWS Compute Optimizer

Answer: B

NO.18 Which of the following does Amazon CloudFront use to distribute content to users around
the world?

A. Amazon VPC
B. AWS Local Zones
C. Edge locations
D. Availability Zones

Answer: C

Explanation:

CloudFront delivers your content through a worldwide network of data centers called edge locations.
The regional edge caches are located between your origin web server and the global edge locations
that serve content directly to your viewers.

NO.19 Which design principles of the AWS WelI-Architected Framework help increase reliability?
(Select TWO.)

A. Automatically recover from failure.
B. Enable traceability.
C. Scale horizontally to increase workload availability.
D. Automate security best practices.
E. Keep people away from data.

Answer: A,C

Explanation:

Reliability
The Reliability pillar encompasses the ability of a workload to perform its intended function correctly
and consistently when it's expected to. This includes the ability to operate and test the workload
through its total lifecycle. You can find prescriptive guidance on implementation in the Reliability
Pillar whitepaper.
Design Principles
There are five design principles for reliability in the cloud:
Automatically recover from failure
Test recovery procedures
Scale horizontally to increase aggregate workload availability
Stop guessing capacity
Manage change in automation
https://aws.amazon.com/blogs/apn/the-6-pillars-of-the-aws-well-architected-framework/

NO.20 A company that uses AWS needs to transfer 2 TB of data.
Which type of transfer of that data would result in no cost for the company?

A. Inbound data transfer from the internet
B. Outbound data transfer to the internet
C. Data transfer between AWS Regions
D. Data transfer between Availability Zones

Answer: B

NO.21 A company uses a database that has a simple sign-up page to create users, and a basic login
form to authenticate users so they can access the database. The company wants to give users the
ability to store personal information, but user access must be controlled in a more secure and reliable
way.
Which AWS service or feature will meet these requirements?

A. Security groups
B. Amazon GuardDuty
C. AWS Secrets Manager
D. Amazon Cognito

Answer: D

Explanation:
aws.amazon.com/cognito/

NO.22 A company wants to offer direct phone and chat channels for customer service. The company
needs a pay-as-you-go solution that remote customer service agents can use to create and manage
voice and chat contact flows.
Which AWS service will meet these requirements?

A. Amazon EventBridge (Amazon CloudWatch Events)
B. Amazon Connect
C. Amazon Cognito
D. AWS Direct Connect

Answer: B

NO.23 A user has an AWS account with a Business-level AWS Support plan and needs assistance with
handling a production service disruption. Which action should the user take?

A. Contact the dedicated AWS technical account manager (TAM).
B. Contact the dedicated AWS Concierge Support team.
C. Open a business-critical system down support case.
D. Open a production system down support case.
Answer: C

NO.24 Which characteristic of the AWS Cloud helps users eliminate underutilized CPU capacity?

A. Agility
B. Elasticity
C. Reliability
D. Durability

Answer: B

NO.25 A company wants to accelerate migration from its data center to the AWS Cloud.
Which combination of AWS services should the company use to meet this requirement? (Select
TWO.)

A. Amazon Connect
B. AWS Direct Connect
C. AWS Server Migration Service (AWS SMS)
D. Amazon Route 53
E. AWS Organizations

Answer: B,C

NO.26 A company has stopped all of its Amazon EC2 instances but monthly billing charges continue
to occur. What could be causing this? (Select TWO.)
A. Amazon Elastic Block Store (Amazon EBS) storage charges
B. Operating system charges
C. Hardware charges
D. Elastic IP charges
E. Input/output (I/O) charges

Answer: A,D

NO.27 Which pillar of the AWS Well-Architected Framework refers to the ability of a system to
recover from infrastructure or service disruptions and dynamically acquire computing resources to
meet demand?

A. Security
B. Reliability
C. Performance efficiency
D. Cost optimization

Answer: B

NO.28 A company runs a web application on Amazon EC2 instances. The application has consistent
usage and is expected to run indefinitely. Which EC2 instance purchasing option will meet these
requirements MOST cost-effectively?

A. 1-year All Upfront Reserved Instances
B. 1-year No Upfront Reserved Instances
C. 3-year All Upfront Reserved Instances
D. 3-year No Upfront Reserved Instances

Answer: C

NO.29 A company needs to automatically protect its Amazon EC2 instances from distributed denial
of service (DDoS) attacks. Which AWS service or tool will provide this protection?

A. Network access control list (ACL)
B. AWS Shield
C. Security group
D. Amazon GuardDuty

Answer: B

NO.30 Which guidelines are key AWS architectural design principles? (Select TWO.)
A. Design for fixed resources.
B. Build scalable architectures.
C. Use tightly coupled components.
D. Use managed services when possible.
E. Design for human interaction.

Answer: B,D

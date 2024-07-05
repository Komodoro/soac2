---
sectionid: Dump102022023
sectionclass: h2
parent-id: Questions
title: 1 - Miguel Fidalgo Questions
number: 3100
---

### Question 1/71





* A company needs to deploy an Amazon EC2 instance and attach a storage mount for the operating system and application files. Which AWS service will meet these requirements?

A. Amazon Elastic File System (Amazon EFS)

B. Amazon Elastic Block Store (Amazon EBS)

C. AWS Backup

D. Amazon S3

**Correct Answer: D**

### Question 1/299

* "A company has an internal web application that runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group in a single Availability Zone. A SysOps administrator must make the application highly available. 
Which action should the SysOps administrator take to meet this requirement?"	

**Correct Answer: Update the Auto Scaling group to launch new instances in a second Availability Zone in the same AWS Region.**


"A company hosts a website on multiple Amazon EC2 instances that run in an Auto Scaling group. Users are reporting slow responses during peak times between
6 PM and 11 PM every weekend. A SysOps administrator must implement a solution to improve performance during these peak times.
What is the MOST operationally efficient solution that meets these requirements?"	Configure a scheduled scaling action with a recurrence option to change the desired capacity before and after peak times

"A company is running a website on Amazon EC2 instances behind an Application Load Balancer (ALB). The company configured an Amazon CloudFront distribution and set the ALB as the origin. The company created an Amazon Route 53 CNAME record to send all traffic through the CloudFront distribution. As an unintended side effect, mobile users are now being served the desktop version of the website.
Which action should a SysOps administrator take to resolve this issue?"	Configure the CloudFront distribution behavior to forward the User-Agent header.

"A SysOps administrator has enabled AWS CloudTrail in an AWS account. If CloudTrail is disabled, it must be re-enabled immediately.
What should the SysOps administrator do to meet these requirements WITHOUT writing custom code?"	Create an AWS Config rule that is invoked when CloudTrail configuration changes. Apply the AWS-ConfigureCloudTrailLogging automatic remediation action.

"A company hosts its website on Amazon EC2 instances behind an Application Load Balancer. The company manages its DNS with Amazon Route 53, and wants to point its domain's zone apex to the website.
Which type of record should be used to meet these requirements?"	An alias record for the domain's zone apex

"A company must ensure that any objects uploaded to an S3 bucket are encrypted.
Which of the following actions will meet this requirement? (Choose two.)"	"Implement Amazon S3 default encryption to make sure that any object being uploaded is encrypted before it is stored.      
        Implement S3 bucket policies to deny unencrypted objects from being uploaded to the buckets"

"A company has a stateful web application that is hosted on Amazon EC2 instances in an Auto Scaling group. The instances run behind an Application Load
Balancer (ALB) that has a single target group. The ALB is configured as the origin in an Amazon CloudFront distribution. Users are reporting random logouts from the web application.
Which combination of actions should a SysOps administrator take to resolve this problem? (Choose two.)"	"Configure cookie forwarding in the CloudFront distribution cache behavior. 
Enable sticky sessions on the ALB target group."

"A company is running a serverless application on AWS Lambda. The application stores data in an Amazon RDS for MySQL DB instance. Usage has steadily increased, and recently there have been numerous ""too many connections"" errors when the Lambda function attempts to connect to the database. The company already has configured the database to use the maximum max_connections value that is possible.
What should a SysOps administrator do to resolve these errors?"	Use Amazon RDS Proxy to create a proxy. Update the connection string in the Lambda function.

"A SysOps administrator is deploying an application on 10 Amazon EC2 instances. The application must be highly available. The instances must be placed on distinct underlying hardware.
What should the SysOps administrator do to meet these requirements?"	Launch the instances into a spread placement group in a single AWS Region.

"A SysOps administrator is troubleshooting an AWS CloudFormation template whereby multiple Amazon EC2 instances are being created. The template is working in us-east-1, but it is failing in us-west-2 with the error code:
AMI [ami-12345678] does not exist
How should the Administrator ensure that the AWS CloudFormation template is working in every region?"	Modify the AWS CloudFormation template by including the AMI IDs in the ג€Mappingsג€ section. Refer to the proper mapping within the template for the proper AMI ID

"A SysOps administrator is provisioning an Amazon Elastic File System (Amazon EFS) file system to provide shared storage across multiple Amazon EC2 instances. The instances all exist in the same VPC across multiple Availability Zones. There are two instances in each Availability Zone. The SysOps administrator must make the file system accessible to each instance with the lowest possible latency.
Which solution will meet these requirements?"	Create a mount target in each Availability Zone of the VPC. Use the mount target to mount the EFS file system on the instances in the respective Availability Zone.

"A SysOps administrator has successfully deployed a VPC with an AWS CloudFormation template. The SysOps administrator wants to deploy the same template across multiple accounts that are managed through AWS Organizations.
Which solution will meet this requirement with the LEAST operational overhead?"	Use AWS CloudFormation StackSets from the management account to deploy the template in each of the accounts.

"A company is running distributed computing software to manage a fleet of 20 Amazon EC2 instances for calculations. The fleet includes 2 control nodes and 18 task nodes to run the calculations. Control nodes can automatically start the task nodes.
Currently, all the nodes run on demand. The control nodes must be available 24 hours a day, 7 days a week. The task nodes run for 4 hours each day. A SysOps administrator needs to optimize the cost of this solution.
Which combination of actions will meet these requirements? (Choose two.)"	"Purchase EC2 Instance Savings Plans for the control nodes
Use Spot Instances for the task nodes. Use On-Demand Instances if there is no Spot availability."

"A company is supposed to receive a data file every hour in an Amazon S3 bucket. An S3 event notification invokes an AWS Lambda function each time a file arrives. The function processes the data for use by an application.
The application team notices that sometimes the file does not arrive. The application team wants to receive a notification whenever the file does not arrive.
What is the MOST operationally efficient solution that meets these requirements?"	Create an Amazon CloudWatch alarm to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic to alert the application team when the Invocations metric of the Lambda function is zero for an hour. Configure the alarm to treat missing data as breaching.

"A company recently acquired another corporation and all of that corporation's AWS accounts. A financial analyst needs the cost data from these accounts. A
SysOps administrator uses Cost Explorer to generate cost and usage reports. The SysOps administrator notices that ""No Tagkey"" represents 20% of the monthly cost.
What should the SysOps administrator do to tag the ""No Tagkey"" resources?"	Use Tag Editor to find and tag all the untagged resources

"While setting up an AWS managed VPN connection, a SysOps administrator creates a customer gateway resource in AWS. The customer gateway device resides in a data center with a NAT gateway in front of it.
What address should be used to create the customer gateway resource?"	The public IP address of the NAT device in front of the customer gateway device

"A company has a web application that is experiencing performance problems many times each night. A root cause analysis reveals sudden increases in CPU utilization that last 5 minutes on an Amazon EC2 Linux instance. A SysOps administrator must find the process ID (PID) of the service or process that is consuming more CPU.
What should the SysOps administrator do to collect the process utilization information with the LEAST amount of effort?"	Configure the Amazon CloudWatch agent procstat plugin to capture CPU process metrics.

"A SysOps administrator configured AWS Backup to capture snapshots from a single Amazon EC2 instance that has one Amazon Elastic Block Store (Amazon
EBS) volume attached. On the first snapshot, the EBS volume has 10 GiB of data. On the second snapshot, the EBS volume still contains 10 GiB of data, but 4
GiB have changed. On the third snapshot, 2 GiB of data have been added to the volume, for a total of 12 GiB.
How much total storage is required to store these snapshots?"	16 GiB

"A team is managing an AWS account that is a member of an organization in AWS Organizations. The organization has consolidated billing features enabled. The account hosts several applications.
A SysOps administrator has applied tags to resources within the account to reflect the environment. The team needs a report of the breakdown of charges by environment.
What should the SysOps administrator do to meet this requirement?"	Activate the tag keys for cost allocation on the organization's management account

"A company uses an AWS CloudFormation template to provision an Amazon EC2 instance and an Amazon RDS DB instance. A SysOps administrator must update the template to ensure that the DB instance is created before the EC2 instance is launched.
What should the SysOps administrator do to meet this requirement?"	Add the DependsOn attribute to the EC2 instance resource, and provide the logical name of the RDS resource.

"A company hosts a static website on Amazon S3. The website is served by an Amazon CloudFront distribution with a default TTL of 86,400 seconds.
The company recently uploaded an updated version of the website to Amazon S3. However, users still see the old content when they refresh the site. A SysOps administrator must make the new version of the website visible to users as soon as possible.
Which solution meets these requirements?"	Create an invalidation on the CloudFront distribution for the old S3 objects.

"A SysOps administrator is responsible for managing a company's cloud infrastructure with AWS CloudFormation. The SysOps administrator needs to create a single resource that consists of multiple AWS services. The resource must support creation and deletion through the CloudFormation console.
Which CloudFormation resource type should the SysOps administrator create to meet these requirements?"	Custom::MyCustomType

"A new website will run on Amazon EC2 instances behind an Application Load Balancer. Amazon Route 53 will be used to manage DNS records.
What type of record should be set in Route 53 to point the website's apex domain name (for example, `company.com`) to the Application Load Balancer?"	ALIAS

"A company is implementing security and compliance by using AWS Trusted Advisor. The company's SysOps team is validating the list of Trusted Advisor checks that it can access.
Which factor will affect the quantity of available Trusted Advisor checks?"	The AWS Support plan

"A SysOps administrator is investigating issues on an Amazon RDS for MariaDB DB instance. The SysOps administrator wants to display the database load categorized by detailed wait events.
How can the SysOps administrator accomplish this goal?"	Enable Amazon RDS Performance Insights

"A company is planning to host an application on a set of Amazon EC2 instances that are distributed across multiple Availability Zones. The application must be able to scale to millions of requests each second.
A SysOps administrator must design a solution to distribute the traffic to the EC2 instances. The solution must be optimized to handle sudden and volatile traffic patterns while using a single static IP address for each Availability Zone.
Which solution will meet these requirements?"	Network Load Balancer

"A SysOps administrator is using AWS CloudFormation StackSets to create AWS resources in two AWS Regions in the same AWS account. A stack operation fails in one Region and returns the stack instance status of OUTDATED.
What is the cause of this failure?"	The CloudFormation template is trying to create a global resource that is not unique.

"A SysOps administrator must configure Amazon S3 to host a simple nonproduction webpage. The SysOps administrator has created an empty S3 bucket from the
AWS Management Console. The S3 bucket has the default configuration in place.
Which combination of actions should the SysOps administrator take to complete this process? (Choose two.)"	" Turn off the ""Block all public access"" setting. Set a bucket policy that allows ""Principal"": the s3:GetObject action.
Create an index.html document. Configure static website hosting, and upload the index document to the S3 bucket"

"A company is using an Amazon Aurora MySQL DB cluster that has point-in-time recovery, backtracking, and automatic backup enabled. A SysOps administrator needs to be able to roll back the DB cluster to a specific recovery point within the previous 72 hours. Restores must be completed in the same production DB cluster.
Which solution will meet these requirements?"	Use backtracking to rewind the existing DB cluster to the desired recovery point.

"A user working in the Amazon EC2 console increased the size of an Amazon Elastic Block Store (Amazon EBS) volume attached to an Amazon EC2 Windows instance. The change is not reflected in the file system.
What should a SysOps administrator do to resolve this issue?"	Extend the file system with operating system-level tools to use the new storage capacity.

"A SysOps administrator is using Amazon EC2 instances to host an application. The SysOps administrator needs to grant permissions for the application to access an Amazon DynamoDB table.
Which solution will meet this requirement?"	Create an IAM role to access the DynamoDB table. Assign the IAM role to the EC2 instance profile.

"A SysOps administrator wants to protect objects in an Amazon S3 bucket from accidental overwrite and deletion. Noncurrent objects must be kept for 90 days and then must be permanently deleted. Objects must reside within the same AWS Region as the original S3 bucket.
Which solution meets these requirements?"	Enable S3 Versioning on the S3 bucket. Create an S3 Lifecycle policy for the bucket to expire noncurrent objects after 90 days.

"A company has an application that customers use to search for records on a website. The application's data is stored in an Amazon Aurora DB cluster. The application's usage varies by season and by day of the week.
The website's popularity is increasing, and the website is experiencing slower performance because of increased load on the DB cluster during periods of peak activity. The application logs show that the performance issues occur when users are searching for information. The same search is rarely performed multiple times.
A SysOps administrator must improve the performance of the platform by using a solution that maximizes resource efficiency.
Which solution will meet these requirements?"	 Deploy an Aurora Replica for the DB cluster. Modify the application to use the reader endpoint for search operations. Use Aurora Auto Scaling to scale the number of replicas based on load.

"A company uses AWS Organizations to manage multiple AWS accounts. Corporate policy mandates that only specific AWS Regions can be used to store and process customer data. A SysOps administrator must prevent the provisioning of Amazon EC2 instances in unauthorized Regions by anyone in the company.
What is the MOST operationally efficient solution that meets these requirements?"	Create a service control policy (SCP) in AWS Organizations to deny the ec2:RunInstances action in all unauthorized Regions. Attach this policy to the root level of the organization.

"A company's public website is hosted in an Amazon S3 bucket in the us-east-1 Region behind an Amazon CloudFront distribution. The company wants to ensure that the website is protected from DDoS attacks. A SysOps administrator needs to deploy a solution that gives the company the ability to maintain control over the rate limit at which DDoS protections are applied.
Which solution will meet these requirements?"	Deploy a global-scoped AWS WAF web ACL with an allow default action. Configure an AWS WAF rate-based rule to block matching traffic. Associate the web ACL with the CloudFront distribution

"A SysOps administrator developed a Python script that uses the AWS SDK to conduct several maintenance tasks. The script needs to run automatically every night.
What is the MOST operationally efficient solution that meets this requirement?"	Convert the Python script to an AWS Lambda function. Use an Amazon EventBridge (Amazon CloudWatch Events) rule to invoke the function every night. 

"A SysOps administrator must create a solution that immediately notifies software developers if an AWS Lambda function experiences an error.
Which solution will meet this requirement?"	 Create an Amazon Simple Notification Service (Amazon SNS) topic with an email subscription for each developer. Create an Amazon CloudWatch alarm by using the Errors metric and the Lambda function name as a dimension. Configure the alarm to send a notification to the SNS topic when the alarm state reaches ALARM

"A company has a private Amazon S3 bucket that contains sensitive information. A SysOps administrator needs to keep logs of the IP addresses from authentication failures that result from attempts to access objects in the bucket. The logs must be stored so that they cannot be overwritten or deleted for 90 days.
Which solution will meet these requirements?"	Turn on access logging for the S3 bucket. Configure the access logs to be saved in a second S3 bucket. Turn on S3 Object Lock on the second S3 bucket, and configure a default retention period of 90 days.

"A SysOps administrator migrates NAT instances to NAT gateways. After the migration, an application that is hosted on Amazon EC2 instances in a private subnet cannot access the internet.
Which of the following are possible reasons for this problem? (Choose two.)"	"The application is using a protocol that the NAT gateway does not support.
The NAT gateway is not in the Available state"

"A company runs an application on an Amazon EC2 instance. A SysOps administrator creates an Auto Scaling group and an Application Load Balancer (ALB) to handle an increase in demand. However, the EC2 instances are failing the health check.
What should the SysOps administrator do to troubleshoot this issue?"	Verify that the application is running on the protocol and the port that the listener is expecting

"A SysOps administrator has created an AWS Service Catalog portfolio and has shared the portfolio with a second AWS account in the company. The second account is controlled by a different administrator.
Which action will the administrator of the second account be able to perform?"	 Add a product from the imported portfolio to a local portfolio.

"A company has migrated its application to AWS. The company will host the application on Amazon EC2 instances of multiple instance families.
During initial testing, a SysOps administrator identifies performance issues on selected EC2 instances. The company has a strict budget allocation policy, so the
SysOps administrator must use the right resource types with the performance characteristics to match the workload.
What should the SysOps administrator do to meet this requirement?"	 Review and take action on AWS Compute Optimizer recommendations. Purchase Compute Savings Plans to reduce the cost that is required to run the compute resources.

"A SysOps administrator is tasked with deploying a company's infrastructure as code. The SysOps administrator want to write a single template that can be reused for multiple environments.
How should the SysOps administrator use AWS CloudFormation to create a solution?"	Use parameters in a CloudFormation template

"A SysOps administrator is responsible for a large fleet of Amazon EC2 instances and must know whether any instances will be affected by upcoming hardware maintenance.
Which option would provide this information with the LEAST administrative overhead?"	Review the AWS Personal Health Dashboard

"A SysOps administrator is attempting to deploy resources by using an AWS CloudFormation template. An Amazon EC2 instance that is defined in the template fails to launch and produces an InsufficientInstanceCapacity error.
Which actions should the SysOps administrator take to resolve this error? (Choose two.)"	"Modify the AWS CloudFormation template to not specify an Availability Zone for the EC2 instance.
 Modify the AWS CloudFormation template to use a different EC2 instance type."

"A company hosts a web application on Amazon EC2 instances behind an Application Load Balancer (ALB). The company uses Amazon Route 53 to route traffic.
The company also has a static website that is configured in an Amazon S3 bucket.
A SysOps administrator must use the static website as a backup to the web application. The failover to the static website must be fully automated.
Which combination of actions will meet these requirements? (Choose two.)"	" Create a primary failover routing policy record. Configure the value to be the ALB. Associate the record with a Route 53 health check.
Create a secondary failover routing policy record. Configure the value to be the static website."

"A data analytics application is running on an Amazon EC2 instance. A SysOps administrator must add custom dimensions to the metrics collected by the Amazon
CloudWatch agent.
How can the SysOps administrator meet this requirement?"	Create an append_dimensions field in the Amazon CloudWatch agent configuration file to collect the metrics

"A company stores its data in an Amazon S3 bucket. The company is required to classify the data and find any sensitive personal information in its S3 files.
Which solution will meet these requirements?"	Enable Amazon Macie. Create a discovery job that uses the managed data identifier. 

"A company hosts a web portal on Amazon EC2 instances. The web portal uses an Elastic Load Balancer (ELB) and Amazon Route 53 for its public DNS service.
The ELB and the EC2 instances are deployed by way of a single AWS CloudFormation stack in the us-east-1 Region. The web portal must be highly available across multiple Regions.
Which configuration will meet these requirements?"	Deploy a copy of the stack in the us-west-2 Region. Create an additional A record in Route 53 that includes the ELB in us-west-2 as an alias target. Configure the A records with a failover routing policy and health checks. Use the ELB in us-east-1 as the primary record and the ELB in us-west-2 as the secondary record.

"A SysOps administrator is investigating why a user has been unable to use RDP to connect over the internet from their home computer to a bastion server running on an Amazon EC2 Windows instance.
Which of the following are possible causes of this issue? (Choose two.)"	"A network ACL associated with the bastion's subnet is blocking the network traffic
The route table associated with the bastion's subnet does not have a route to the internet gateway."




### Question 2/71

* Which AWS service provides alerts when an AWS event may impact a company's AWS resources?

A. AWS Infrastructure Event Management

B. AWS Trusted Advisor

C. AWS Personal Health Dashboard

D. AWS Service Health Dashboard

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

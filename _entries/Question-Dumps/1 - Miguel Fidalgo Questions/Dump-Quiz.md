---
sectionid: MiguelFidalgoDump
sectionclass: h2
parent-id: Questions
title: Miguel Fidalgo Questions
number: 2100
---
### Question 1

* "A company has an internal web application that runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group in a single Availability Zone. A SysOps administrator must make the application highly available. 
Which action should the SysOps administrator take to meet this requirement?"	

**R: Update the Auto Scaling group to launch new instances in a second Availability Zone in the same AWS Region.**

### Question 2

* "A company hosts a website on multiple Amazon EC2 instances that run in an Auto Scaling group. Users are reporting slow responses during peak times between 6 PM and 11 PM every weekend. A SysOps administrator must implement a solution to improve performance during these peak times.
What is the MOST operationally efficient solution that meets these requirements?"

**R: Configure a scheduled scaling action with a recurrence option to change the desired capacity before and after peak times**

### Question 3

* "A company is running a website on Amazon EC2 instances behind an Application Load Balancer (ALB). The company configured an Amazon CloudFront distribution and set the ALB as the origin. The company created an Amazon Route 53 CNAME record to send all traffic through the CloudFront distribution. As an unintended side effect, mobile users are now being served the desktop version of the website.
Which action should a SysOps administrator take to resolve this issue?"

**R: Configure the CloudFront distribution behavior to forward the User-Agent header.**

### Question 4

* "A SysOps administrator has enabled AWS CloudTrail in an AWS account. If CloudTrail is disabled, it must be re-enabled immediately.
What should the SysOps administrator do to meet these requirements WITHOUT writing custom code?"	

**R: Create an AWS Config rule that is invoked when CloudTrail configuration changes. Apply the AWS-ConfigureCloudTrailLogging automatic remediation action.**

### Question 5

* "A company hosts its website on Amazon EC2 instances behind an Application Load Balancer. The company manages its DNS with Amazon Route 53, and wants to point its domain's zone apex to the website.
Which type of record should be used to meet these requirements?"

**R: An alias record for the domain's zone apex**

### Question 6

* "A company must ensure that any objects uploaded to an S3 bucket are encrypted.
Which of the following actions will meet this requirement? (Choose two.)"	

**R:** 
**1. Implement Amazon S3 default encryption to make sure that any object being uploaded is encrypted before it is stored.**
**2. Implement S3 bucket policies to deny unencrypted objects from being uploaded to the buckets**

### Question 7

* "A company has a stateful web application that is hosted on Amazon EC2 instances in an Auto Scaling group. The instances run behind an Application Load
Balancer (ALB) that has a single target group. The ALB is configured as the origin in an Amazon CloudFront distribution. Users are reporting random logouts from the web application.
Which combination of actions should a SysOps administrator take to resolve this problem? (Choose two.)"	

**R:**
**1. Configure cookie forwarding in the CloudFront distribution cache behavior.**
**2. Enable sticky sessions on the ALB target group.**

### Question 8

* "A company is running a serverless application on AWS Lambda. The application stores data in an Amazon RDS for MySQL DB instance. Usage has steadily increased, and recently there have been numerous "*too many connections*" errors when the Lambda function attempts to connect to the database. The company already has configured the database to use the maximum max_connections value that is possible.
What should a SysOps administrator do to resolve these errors?"	

**R: Use Amazon RDS Proxy to create a proxy. Update the connection string in the Lambda function.**

### Question 9

* "A SysOps administrator is deploying an application on 10 Amazon EC2 instances. The application must be highly available. The instances must be placed on distinct underlying hardware.
What should the SysOps administrator do to meet these requirements?"	

**R: Launch the instances into a spread placement group in a single AWS Region.**

### Question 10

* "A SysOps administrator is troubleshooting an AWS CloudFormation template whereby multiple Amazon EC2 instances are being created. The template is working in us-east-1, but it is failing in us-west-2 with the error code:
AMI [ami-12345678] does not exist
How should the Administrator ensure that the AWS CloudFormation template is working in every region?"	

**R: Modify the AWS CloudFormation template by including the AMI IDs in the ג€Mappingsג€ section. Refer to the proper mapping within the template for the proper AMI ID**

### Question 11

* "A SysOps administrator is provisioning an Amazon Elastic File System (Amazon EFS) file system to provide shared storage across multiple Amazon EC2 instances. The instances all exist in the same VPC across multiple Availability Zones. There are two instances in each Availability Zone. The SysOps administrator must make the file system accessible to each instance with the lowest possible latency.
Which solution will meet these requirements?"	

**R: Create a mount target in each Availability Zone of the VPC. Use the mount target to mount the EFS file system on the instances in the respective Availability Zone.**

### Question 12

* "A SysOps administrator has successfully deployed a VPC with an AWS CloudFormation template. The SysOps administrator wants to deploy the same template across multiple accounts that are managed through AWS Organizations.
Which solution will meet this requirement with the LEAST operational overhead?"	

**R: Use AWS CloudFormation StackSets from the management account to deploy the template in each of the accounts.**

### Question 13

* "A company is running distributed computing software to manage a fleet of 20 Amazon EC2 instances for calculations. The fleet includes 2 control nodes and 18 task nodes to run the calculations. Control nodes can automatically start the task nodes.
Currently, all the nodes run on demand. The control nodes must be available 24 hours a day, 7 days a week. The task nodes run for 4 hours each day. A SysOps administrator needs to optimize the cost of this solution.
Which combination of actions will meet these requirements? (Choose two.)"	

        Purchase EC2 Instance Savings Plans for the control nodes

        Use Spot Instances for the task nodes. Use On-Demand Instances if there is no Spot availability.


### Question 14

* "A company is supposed to receive a data file every hour in an Amazon S3 bucket. An S3 event notification invokes an AWS Lambda function each time a file arrives. The function processes the data for use by an application.
The application team notices that sometimes the file does not arrive. The application team wants to receive a notification whenever the file does not arrive.
What is the MOST operationally efficient solution that meets these requirements?"	

Create an Amazon CloudWatch alarm to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic to alert the application team when the Invocations metric of the Lambda function is zero for an hour. Configure the alarm to treat missing data as breaching.

### Question 15

"A company recently acquired another corporation and all of that corporation's AWS accounts. A financial analyst needs the cost data from these accounts. A
SysOps administrator uses Cost Explorer to generate cost and usage reports. The SysOps administrator notices that ""No Tagkey"" represents 20% of the monthly cost.
What should the SysOps administrator do to tag the ""No Tagkey"" resources?"	

Use Tag Editor to find and tag all the untagged resources

### Question 16

"While setting up an AWS managed VPN connection, a SysOps administrator creates a customer gateway resource in AWS. The customer gateway device resides in a data center with a NAT gateway in front of it.
What address should be used to create the customer gateway resource?"	

The public IP address of the NAT device in front of the customer gateway device

### Question 17

"A company has a web application that is experiencing performance problems many times each night. A root cause analysis reveals sudden increases in CPU utilization that last 5 minutes on an Amazon EC2 Linux instance. A SysOps administrator must find the process ID (PID) of the service or process that is consuming more CPU.
What should the SysOps administrator do to collect the process utilization information with the LEAST amount of effort?"	

Configure the Amazon CloudWatch agent procstat plugin to capture CPU process metrics.

### Question 18

"A SysOps administrator configured AWS Backup to capture snapshots from a single Amazon EC2 instance that has one Amazon Elastic Block Store (Amazon
EBS) volume attached. On the first snapshot, the EBS volume has 10 GiB of data. On the second snapshot, the EBS volume still contains 10 GiB of data, but 4
GiB have changed. On the third snapshot, 2 GiB of data have been added to the volume, for a total of 12 GiB.
How much total storage is required to store these snapshots?"	

16 GiB

### Question 19

"A team is managing an AWS account that is a member of an organization in AWS Organizations. The organization has consolidated billing features enabled. The account hosts several applications.
A SysOps administrator has applied tags to resources within the account to reflect the environment. The team needs a report of the breakdown of charges by environment.
What should the SysOps administrator do to meet this requirement?"	

Activate the tag keys for cost allocation on the organization's management account

### Question 20

"A company uses an AWS CloudFormation template to provision an Amazon EC2 instance and an Amazon RDS DB instance. A SysOps administrator must update the template to ensure that the DB instance is created before the EC2 instance is launched.
What should the SysOps administrator do to meet this requirement?"	

Add the DependsOn attribute to the EC2 instance resource, and provide the logical name of the RDS resource.

### Question 21

"A company hosts a static website on Amazon S3. The website is served by an Amazon CloudFront distribution with a default TTL of 86,400 seconds.
The company recently uploaded an updated version of the website to Amazon S3. However, users still see the old content when they refresh the site. A SysOps administrator must make the new version of the website visible to users as soon as possible.
Which solution meets these requirements?"	

Create an invalidation on the CloudFront distribution for the old S3 objects.

### Question 22

"A SysOps administrator is responsible for managing a company's cloud infrastructure with AWS CloudFormation. The SysOps administrator needs to create a single resource that consists of multiple AWS services. The resource must support creation and deletion through the CloudFormation console.
Which CloudFormation resource type should the SysOps administrator create to meet these requirements?"	

Custom::MyCustomType

### Question 23

"A new website will run on Amazon EC2 instances behind an Application Load Balancer. Amazon Route 53 will be used to manage DNS records.
What type of record should be set in Route 53 to point the website's apex domain name (for example, `company.com`) to the Application Load Balancer?"	

ALIAS

### Question 24

"A company is implementing security and compliance by using AWS Trusted Advisor. The company's SysOps team is validating the list of Trusted Advisor checks that it can access.
Which factor will affect the quantity of available Trusted Advisor checks?"	

The AWS Support plan

### Question 25

"A SysOps administrator is investigating issues on an Amazon RDS for MariaDB DB instance. The SysOps administrator wants to display the database load categorized by detailed wait events.
How can the SysOps administrator accomplish this goal?"

Enable Amazon RDS Performance Insights

### Question 26

"A company is planning to host an application on a set of Amazon EC2 instances that are distributed across multiple Availability Zones. The application must be able to scale to millions of requests each second.
A SysOps administrator must design a solution to distribute the traffic to the EC2 instances. The solution must be optimized to handle sudden and volatile traffic patterns while using a single static IP address for each Availability Zone.
Which solution will meet these requirements?"	

Network Load Balancer

### Question 27

"A SysOps administrator is using AWS CloudFormation StackSets to create AWS resources in two AWS Regions in the same AWS account. A stack operation fails in one Region and returns the stack instance status of OUTDATED.
What is the cause of this failure?"	

The CloudFormation template is trying to create a global resource that is not unique.

### Question 28

"A SysOps administrator must configure Amazon S3 to host a simple nonproduction webpage. The SysOps administrator has created an empty S3 bucket from the
AWS Management Console. The S3 bucket has the default configuration in place.
Which combination of actions should the SysOps administrator take to complete this process? (Choose two.)"	

- Turn off the ""Block all public access"" setting. Set a bucket policy that allows ""Principal"": the s3:GetObject action.

- Create an index.html document. Configure static website hosting, and upload the index document to the S3 bucket"

### Question 29

"A company is using an Amazon Aurora MySQL DB cluster that has point-in-time recovery, backtracking, and automatic backup enabled. A SysOps administrator needs to be able to roll back the DB cluster to a specific recovery point within the previous 72 hours. Restores must be completed in the same production DB cluster.
Which solution will meet these requirements?"	

Use backtracking to rewind the existing DB cluster to the desired recovery point.

### Question 30

"A user working in the Amazon EC2 console increased the size of an Amazon Elastic Block Store (Amazon EBS) volume attached to an Amazon EC2 Windows instance. The change is not reflected in the file system.
What should a SysOps administrator do to resolve this issue?"	

Extend the file system with operating system-level tools to use the new storage capacity.

### Question 31

"A SysOps administrator is using Amazon EC2 instances to host an application. The SysOps administrator needs to grant permissions for the application to access an Amazon DynamoDB table.
Which solution will meet this requirement?"

Create an IAM role to access the DynamoDB table. Assign the IAM role to the EC2 instance profile.

### Question 32

"A SysOps administrator wants to protect objects in an Amazon S3 bucket from accidental overwrite and deletion. Noncurrent objects must be kept for 90 days and then must be permanently deleted. Objects must reside within the same AWS Region as the original S3 bucket.
Which solution meets these requirements?"

Enable S3 Versioning on the S3 bucket. Create an S3 Lifecycle policy for the bucket to expire noncurrent objects after 90 days.

### Question 33

"A company has an application that customers use to search for records on a website. The application's data is stored in an Amazon Aurora DB cluster. The application's usage varies by season and by day of the week.
The website's popularity is increasing, and the website is experiencing slower performance because of increased load on the DB cluster during periods of peak activity. The application logs show that the performance issues occur when users are searching for information. The same search is rarely performed multiple times.
A SysOps administrator must improve the performance of the platform by using a solution that maximizes resource efficiency.
Which solution will meet these requirements?"	 

Deploy an Aurora Replica for the DB cluster. Modify the application to use the reader endpoint for search operations. Use Aurora Auto Scaling to scale the number of replicas based on load.

### Question 34

"A company uses AWS Organizations to manage multiple AWS accounts. Corporate policy mandates that only specific AWS Regions can be used to store and process customer data. A SysOps administrator must prevent the provisioning of Amazon EC2 instances in unauthorized Regions by anyone in the company.
What is the MOST operationally efficient solution that meets these requirements?"	

Create a service control policy (SCP) in AWS Organizations to deny the ec2:RunInstances action in all unauthorized Regions. Attach this policy to the root level of the organization.

### Question 35

"A company's public website is hosted in an Amazon S3 bucket in the us-east-1 Region behind an Amazon CloudFront distribution. The company wants to ensure that the website is protected from DDoS attacks. A SysOps administrator needs to deploy a solution that gives the company the ability to maintain control over the rate limit at which DDoS protections are applied.
Which solution will meet these requirements?"

Deploy a global-scoped AWS WAF web ACL with an allow default action. Configure an AWS WAF rate-based rule to block matching traffic. Associate the web ACL with the CloudFront distribution

### Question 36

"A SysOps administrator developed a Python script that uses the AWS SDK to conduct several maintenance tasks. The script needs to run automatically every night.
What is the MOST operationally efficient solution that meets this requirement?"	

Convert the Python script to an AWS Lambda function. Use an Amazon EventBridge (Amazon CloudWatch Events) rule to invoke the function every night. 

### Question 37

"A SysOps administrator must create a solution that immediately notifies software developers if an AWS Lambda function experiences an error.
Which solution will meet this requirement?"

Create an Amazon Simple Notification Service (Amazon SNS) topic with an email subscription for each developer. Create an Amazon CloudWatch alarm by using the Errors metric and the Lambda function name as a dimension. Configure the alarm to send a notification to the SNS topic when the alarm state reaches ALARM

### Question 38

"A company has a private Amazon S3 bucket that contains sensitive information. A SysOps administrator needs to keep logs of the IP addresses from authentication failures that result from attempts to access objects in the bucket. The logs must be stored so that they cannot be overwritten or deleted for 90 days.
Which solution will meet these requirements?"	

Turn on access logging for the S3 bucket. Configure the access logs to be saved in a second S3 bucket. Turn on S3 Object Lock on the second S3 bucket, and configure a default retention period of 90 days.

### Question 39

"A SysOps administrator migrates NAT instances to NAT gateways. After the migration, an application that is hosted on Amazon EC2 instances in a private subnet cannot access the internet.
Which of the following are possible reasons for this problem? (Choose two.)"	

- The application is using a protocol that the NAT gateway does not support.

- The NAT gateway is not in the Available state

### Question 40

"A company runs an application on an Amazon EC2 instance. A SysOps administrator creates an Auto Scaling group and an Application Load Balancer (ALB) to handle an increase in demand. However, the EC2 instances are failing the health check.
What should the SysOps administrator do to troubleshoot this issue?"	

Verify that the application is running on the protocol and the port that the listener is expecting

### Question 41

"A SysOps administrator has created an AWS Service Catalog portfolio and has shared the portfolio with a second AWS account in the company. The second account is controlled by a different administrator.
Which action will the administrator of the second account be able to perform?"	

Add a product from the imported portfolio to a local portfolio.

### Question 42

"A company has migrated its application to AWS. The company will host the application on Amazon EC2 instances of multiple instance families.
During initial testing, a SysOps administrator identifies performance issues on selected EC2 instances. The company has a strict budget allocation policy, so the
SysOps administrator must use the right resource types with the performance characteristics to match the workload.
What should the SysOps administrator do to meet this requirement?"

Review and take action on AWS Compute Optimizer recommendations. Purchase Compute Savings Plans to reduce the cost that is required to run the compute resources.

### Question 43

"A SysOps administrator is tasked with deploying a company's infrastructure as code. The SysOps administrator want to write a single template that can be reused for multiple environments.
How should the SysOps administrator use AWS CloudFormation to create a solution?"

Use parameters in a CloudFormation template

### Question 44

"A SysOps administrator is responsible for a large fleet of Amazon EC2 instances and must know whether any instances will be affected by upcoming hardware maintenance.
Which option would provide this information with the LEAST administrative overhead?"

Review the AWS Personal Health Dashboard

### Question 45

"A SysOps administrator is attempting to deploy resources by using an AWS CloudFormation template. An Amazon EC2 instance that is defined in the template fails to launch and produces an InsufficientInstanceCapacity error.
Which actions should the SysOps administrator take to resolve this error? (Choose two.)"

- Modify the AWS CloudFormation template to not specify an Availability Zone for the EC2 instance.
 
- Modify the AWS CloudFormation template to use a different EC2 instance type.

### Question 46

"A company hosts a web application on Amazon EC2 instances behind an Application Load Balancer (ALB). The company uses Amazon Route 53 to route traffic.
The company also has a static website that is configured in an Amazon S3 bucket.
A SysOps administrator must use the static website as a backup to the web application. The failover to the static website must be fully automated.
Which combination of actions will meet these requirements? (Choose two.)"

- Create a primary failover routing policy record. Configure the value to be the ALB. Associate the record with a Route 53 health check.

- Create a secondary failover routing policy record. Configure the value to be the static website.

### Question 47

"A data analytics application is running on an Amazon EC2 instance. A SysOps administrator must add custom dimensions to the metrics collected by the Amazon
CloudWatch agent.
How can the SysOps administrator meet this requirement?"

- Create an append_dimensions field in the Amazon CloudWatch agent configuration file to collect the metrics

### Question 48

"A company stores its data in an Amazon S3 bucket. The company is required to classify the data and find any sensitive personal information in its S3 files.
Which solution will meet these requirements?"

Enable Amazon Macie. Create a discovery job that uses the managed data identifier. 

### Question 49

"A company hosts a web portal on Amazon EC2 instances. The web portal uses an Elastic Load Balancer (ELB) and Amazon Route 53 for its public DNS service.
The ELB and the EC2 instances are deployed by way of a single AWS CloudFormation stack in the us-east-1 Region. The web portal must be highly available across multiple Regions.
Which configuration will meet these requirements?"	

**R: Deploy a copy of the stack in the us-west-2 Region. Create an additional A record in Route 53 that includes the ELB in us-west-2 as an alias target. Configure the A records with a failover routing policy and health checks. Use the ELB in us-east-1 as the primary record and the ELB in us-west-2 as the secondary record.**

### Question 50/298

"A SysOps administrator is investigating why a user has been unable to use RDP to connect over the internet from their home computer to a bastion server running on an Amazon EC2 Windows instance.
Which of the following are possible causes of this issue? (Choose two.)"	"A network ACL associated with the bastion's subnet is blocking the network traffic
The route table associated with the bastion's subnet does not have a route to the internet gateway."

### Question 51/298

* "A SysOps administrator is examining the following AWS CloudFormation template"
![Image](q52.jpg)
"Why will the stack creation fail?"

**R: The PrivateDnsName cannot be set from a CloudFormation template.**

### Question 52

"A new application runs on Amazon EC2 instances and accesses data in an Amazon RDS database instance. When fully deployed in production, the application fails. The database can be queried from a console on a bastion host. When looking at the web server logs, the following error is repeated multiple times:
*** Error Establishing a Database Connection
Which of the following may be causes of the connectivity problems? (Choose two.)"

- The security group for the database does not have the appropriate ingress rule from the web server to the database.

- The port used by the application developer does not match the port specified in the RDS configuration.

### Question 53

"A compliance team requires all administrator passwords for Amazon RDS DB instances to be changed at least annually.
Which solution meets this requirement in the MOST operationally efficient manner?"

Store the database credentials in AWS Secrets Manager. Configure automatic rotation for the secret every 365 days.

### Question 54

"A SysOps administrator is responsible for managing a fleet of Amazon EC2 instances. These EC2 instances upload build artifacts to a third-party service. The third-party service recently implemented a strict IP allow list that requires all build uploads to come from a single IP address.
What change should the systems administrator make to the existing build fleet to comply with this new requirement?"

Move all of the EC2 instances behind a NAT gateway and provide the gateway IP address to the service.

### Question 55

"A company uses an Amazon CloudFront distribution to deliver its website. Traffic logs for the website must be centrally stored, and all data must be encrypted at rest.
Which solution will meet these requirements?"

Create an Amazon S3 bucket that is configured with default server-side encryption that uses AES-256. Configure CloudFront to use the S3 bucket as a log destination

### Question 56

"An organization created an Amazon Elastic File System (Amazon EFS) volume with a file system ID of fs-85ba41fc, and it is actively used by 10 Amazon EC2 hosts. The organization has become concerned that the file system is not encrypted.
How can this be resolved?"

Enable encryption on a newly created volume and copy all data from the original volume. Reconnect each host to the new volume

### Question 57

"A company uses an AWS Service Catalog portfolio to create and manage resources. A SysOps administrator must create a replica of the company's existing AWS infrastructure in a new AWS account.
What is the MOST operationally efficient way to meet this requirement?"	

Share the AWS Service Catalog portfolio with the new AWS account. Import the portfolio into the new AWS account. 

### Question 58

"A SysOps administrator must manage the security of an AWS account. Recently, an IAM user's access key was mistakenly uploaded to a public code repository.
The SysOps administrator must identify anything that was changed by using this access key.
How should the SysOps administrator meet these requirements?"	

Search AWS CloudTrail event history for all events initiated with the compromised access key within the suspected timeframe.

### Question 59

"A company runs a retail website on multiple Amazon EC2 instances behind an Application Load Balancer (ALB). The company must secure traffic to the website over an HTTPS connection.
Which combination of actions should a SysOps administrator take to meet these requirements? (Choose two.)"	

- Attach the certificate to the ALB
 
- Create a public certificate in AWS Certificate Manager (ACM).

### Question 60

"A company has a stateful, long-running workload on a single xlarge general purpose Amazon EC2 On-Demand Instance Metrics show that the service is always using 80% of its available memory and 40% of its available CPU. A SysOps administrator must reduce the cost of the service without negatively affecting performance.
Which change in instance type will meet these requirements?"	

Change to one large memory optimized On-Demand Instance

### Question 61

"A company asks a SysOps administrator to ensure that AWS CloudTrail files are not tampered with after they are created. Currently, the company uses AWS
Identity and Access Management (IAM) to restrict access to specific trails. The company's security team needs the ability to trace the integrity of each file.
What is the MOST operationally efficient solution that meets these requirements?"	 

Enable the CloudTrail file integrity feature on the trail. The security team can use the digest file that is created by CloudTrail to verify the integrity of the delivered files

### Question 62

When the AWS Cloud infrastructure experiences an event that may impact an organization, which AWS service can be used to see which of the organization's resources are affected?	 

AWS Personal Health Dashboard

### Question 63

"A company is using an AWS KMS customer master key (CMK) with imported key material. The company references the CMK by its alias in the Java application to encrypt data. The CMK must be rotated every 6 months.
What is the process to rotate the key?"	

Create a new CMK with new imported material, and update the key alias to point to the new CMK.

### Question 64

"The security team is concerned because the number of AWS Identity and Access Management (IAM) policies being used in the environment is increasing. The team tasked a SysOps administrator to report on the current number of IAM policies in use and the total available IAM policies.
Which AWS service should the administrator use to check how current IAM policy usage compares to current service limits?"

AWS Trusted Advisor

### Question 65

"A SysOps administrator is trying to set up an Amazon Route 53 domain name to route traffic to a website hosted on Amazon S3. The domain name of the website is www.example.com and the S3 bucket name DOC-EXAMPLE-BUCKET. After the record set is set up in Route 53, the domain name www.anycompany.com does not seem to work, and the static website is not displayed in the browser.
Which of the following is a cause of this?"

The S3 bucket name must match the record set name in Route 53

### Question 66

"A SysOps administrator has used AWS CloudFormation to deploy a serverless application into a production VPC. The application consists of an AWS Lambda function, an Amazon DynamoDB table, and an Amazon API Gateway API. The SysOps administrator must delete the AWS CloudFormation stack without deleting the DynamoDB table.
Which action should the SysOps administrator take before deleting the AWS CloudFormation stack?"

Add a Retain deletion policy to the DynamoDB resource in the AWS CloudFormation stack.

### Question 67

"A SysOps administrator is notified that an Amazon EC2 instance has stopped responding. The AWS Management Console indicates that the system checks are failing.
What should the administrator do first to resolve this issue?"	

Stop and then start the EC2 instance so that it can be launched on a new host.

### Question 68

"A software development company has multiple developers who work on the same product. Each developer must have their own development environments, and these development environments must be identical. Each development environment consists of Amazon EC2 instances and an Amazon RDS DB instance. The development environments should be created only when necessary, and they must be terminated each night to minimize costs.
What is the MOST operationally efficient solution that meets these requirements?"	

Provide developers with access to the same AWS CloudFormation template so that they can provision their development environment when necessary. Schedule a nightly Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function to delete the AWS CloudFormation stacks. 

### Question 69

"A company is partnering with an external vendor to provide data processing services. For this integration, the vendor must host the company's data in an Amazon
S3 bucket in the vendor's AWS account. The vendor is allowing the company to provide an AWS Key Management Service (AWS KMS) key to encrypt the company's data. The vendor has provided an IAM role Amazon Resources Name (ARN) to the company for this integration.
What should a SysOps administrator do to configure this integration?"	

Create a new KMS key. Add the vendor's IAM role ARN to the KMS key policy. Provide the new KMS key ARN to the vendor

### Question 70

"A SysOps administrator is using AWS Systems Manager Patch Manager to patch a fleet of Amazon EC2 instances. The SysOps administrator has configured a patch baseline and a maintenance window. The SysOps administrator also has used an instance tag to identify which instances to patch.
The SysOps administrator must give Systems Manager the ability to access the EC2 instances.
Which additional action must the SysOps administrator perform to meet this requirement?"

Attach an IAM instance profile with access to Systems Manager to the instances.

### Question 71

"A company hosts its website on Amazon EC2 instances in the us-east-1 Region. The company is preparing to extend its website into the eu-central-1 Region, but the database must remain only in us-east-1. After deployment, the EC2 instances in eu-central-1 are unable to connect to the database in us-east-1.
What is the MOST operationally efficient solution that will resolve this connectivity issue?"	 

Create a VPC peering connection between the two Regions. Add the private IP address range of the instances to the inbound rule of the database security group. 

### Question 72

"A company wants to create an automated solution for all accounts managed by AWS Organizations to detect any security groups that use 0.0.0.0/0 as the source address for inbound traffic. The company also wants to automatically remediate any noncompliant security groups by restricting access to a specific CIDR block that corresponds with the company's intranet.
Which set of actions should the SysOps administrator take to create a solution?"

Create an AWS Config rule to detect noncompliant security groups. Set up automatic remediation to change the 0.0.0.0/0 source address to the approved CIDR block

### Question 73

"A company requires that all activity in its AWS account be logged using AWS CloudTrail. Additionally, a SysOps administrator must know when CloudTrail log files are modified or deleted.
How should the SysOps administrator meet these requirements?"

Enable log file integrity validation. Use the AWS CLI to validate the log files. 

### Question 74

"A company is planning to host its stateful web-based applications on AWS. A SysOps administrator is using an Auto Scaling group of Amazon EC2 instances. The web applications will run 24 hours a day, 7 days a week throughout the year. The company must be able to change the instance type within the same instance family later in the year based on the traffic and usage patterns.
Which EC2 instance purchasing option will meet these requirements MOST cost-effectively?"

Convertible Reserved Instances

### Question 75

"An application runs on Amazon EC2 instances in an Auto Scaling group. Following the deployment of a new feature on the EC2 instances, some instances were marked as unhealthy and then replaced by the Auto Scaling group. The EC2 instances terminated before a SysOps administrator could determine the cause of the health status changes. To troubleshoot this issue, the SysOps administrator wants to ensure that an AWS Lambda function is invoked in this situation.
How should the SysOps administrator meet these requirements?"

Add a lifecycle hook to the Auto Scaling group to invoke the Lambda function through Amazon EventBridge (Amazon CloudWatch Events).

### Question 76

"A company runs an application that hosts critical data for several clients. The company uses AWS CloudTrail to track user activities on various AWS resources. To meet new security requirements, the company needs to protect the CloudTrail log files from being modified, deleted, or forged.
Which solution will meet these requirement?"

Enable CloudTrail log file integrity validation

### Question 77

"A global company operates out of five AWS Regions. A SysOps administrator wants to identify all the company's tagged and untagged Amazon EC2 instances.
The company requires the output to display the instance ID and tags.
What is the MOST operationally efficient way for the SysOps administrator to meet these requirements?"	

Use Tag Editor in AWS Resource Groups. Select all Regions, and choose a resource type of AWS::EC2::Instance. 

### Question 78

"A company needs to upload gigabytes of files every day. The company need to achieve higher throughput and upload speeds to Amazon S3.
Which action should a SysOps administrator take to meet this requirement?"

Enable S3 Transfer Acceleration and use the acceleration endpoint when uploading files.

### Question 79

"A SysOps administrator maintains the security and compliance of a company's AWS account. To ensure the company's Amazon EC2 instances are following company policy, a SysOps administrator wants to terminate any EC2 instance that do not contain a department tag. Noncompliant resources must be terminated in near-real time.
Which solution will meet these requirements?"	

Create an AWS Config rule with the required-tags managed rule to identify noncompliant resources. Configure automatic remediation to run the AWS- TerminateEC2Instance automation document to terminate noncompliant resources

### Question 80

"A company uploaded its website files to an Amazon S3 bucket that has S3 Versioning enabled. The company uses an Amazon CloudFront distribution with the S3 bucket as the origin. The company recently modified the files, but the object names remained the same. Users report that old content is still appearing on the website.
How should a SysOps administrator remediate this issue?"

Create a CloudFront invalidation, and add the path of the updated files.

### Question 81

"A company has two VPC networks named VPC A and VPC B. The VPC A CIDR block is 10.0.0.0/16 and the VPC B CIDR block is 172.31.0.0/16. The company wants to establish a VPC peering connection named pcx-12345 between both VPCs.
Which rules should appear in the route table of VPC A after configuration? (Choose two.)"	"Destination: 10.0.0.0/16, Target: Local
Destination: 172.31.0.0/16, Target: pcx-12345"

### Question 82

"A company analyzes sales data for its customers. Customers upload files to one of the company's Amazon S3 buckets, and a message is posted to an Amazon
Simple Queue Service (Amazon SQS) queue that contains the object Amazon Resource Name (ARN). An application that runs on an Amazon EC2 instance polls the queue and processes the messages. The processing time depends on the size of the file.
Customers are reporting delays in the processing of their files. A SysOps administrator decides to configure Amazon EC2 Auto Scaling as the first step. The
SysOps administrator creates an Amazon Machine Image (AMI) that is based on the existing EC2 instance. The SysOps administrator also creates a launch template that references the AMI.
How should the SysOps administrator configure the Auto Scaling policy to improve the response time?"	Create a custom metric based on the ApproximateNumberOfMessagesVisible metric and the number of instances in the InService state in the Auto Scaling group. Modify the application to calculate the metric and post the metric to Amazon CloudWatch once each minute. Create an Auto Scaling policy based on this metric to scale the number of instances.

### Question 83

"A company runs a multi-tier web application with two Amazon EC2 instances in one Availability Zone in the us-east-1 Region. A SysOps administrator must migrate one of the EC2 instances to a new Availability Zone.
Which solution will accomplish this?"	Create an Amazon Machine Image (AMI) from the EC2 instance and launch it in a different Availability Zone. Terminate the original instance

### Question 84

"A company is expanding its fleet of Amazon EC2 instances before an expected increase of traffic. When a SysOps administrator attempts to add more instances, an InstanceLimitExceeded error is returned.
What should the SysOps administrator do to resolve this error?"	Use Service Quotas to request an EC2 quota increase.

### Question 85

"A company wants to prohibit its developers from using a particular family of Amazon EC2 instances. The company uses AWS Organizations and wants to apply the restriction across multiple accounts.
What is the MOST operationally efficient way for the company to apply service control policies (SCPs) to meet these requirements?"	Add the accounts to an organizational unit (OU). Apply the SCPs to the OU. 

### Question 86

"An application is running on an Amazon EC2 instance in a VPC with the default DHCP option set. The application connects to an on-premises Microsoft SQL
Server database with the DNS name mssql.example.com. The application is unable to resolve the database DNS name.
Which solution will fix this problem?"	 Create an Amazon Route 53 Resolver outbound endpoint. Add a forwarding rule for the domain example.com. Associate the forwarding rule with the VPC. 

### Question 87

"A company's application is hosted by an internet provider at app.example.com. The company wants to access the application by using www.company.com, which the company owns and manages with Amazon Route 53.
Which Route 53 record should be created to address this?"	CNAME record

### Question 88 

"A company expanded its web application to serve a worldwide audience. A SysOps administrator has implemented a multi-Region AWS deployment for all production infrastructure. The SysOps administrator must route traffic based on the location of resources.
Which Amazon Route 53 routing policy should the SysOps administrator use to meet this requirement?"	 Geoproximity routing policy

### Question 89

"A SysOps administrator wants to upload a file that is 1 TB in size from on-premises to an Amazon S3 bucket using multipart uploads.
What should the SysOps administrator do to meet this requirement?"	 Use the s3 cp command

### Question 90

"An application team is working with a SysOps administrator to define Amazon CloudWatch alarms for an application. The application team does not know the application's expected usage or expected growth.
Which solution should the SysOps administrator recommend?"	Create CloudWatch alarms that are based on anomaly detection

### Question 91

"A company runs a stateless application that is hosted on an Amazon EC2 instance. Users are reporting performance issues. A SysOps administrator reviews the 
Amazon CloudWatch metrics for the application and notices that the instance's CPU utilization frequently reaches 90% during business hours. 
What is the MOST operationally efficient solution that will improve the application's responsiveness?"	Create an Auto Scaling group, and assign it to an Application Load Balancer. Configure a target tracking scaling policy that is based on the average CPU utilization of the Auto Scaling group.

### Question 92

"An ecommerce company uses an Amazon ElastiCache for Memcached cluster for in-memory caching of popular product queries on the shopping site. When viewing recent Amazon CloudWatch metrics data for the ElastiCache cluster, the SysOps administrator notices a large number of evictions. 
Which of the following actions will reduce these evictions? (Choose two.)"	"Add an additional node to the ElastiCache cluster.
Increase the individual node size inside the ElastiCache cluster."

### Question 93

"A SysOps administrator wants to provide access to AWS services by attaching an IAM policy to multiple IAM users. The SysOps administrator also wants to be able to change the policy and create new versions. 
Which combination of actions will meet these requirements? (Choose two.)"	"Create a customer managed policy.
Add the users to an IAM user group. Attach the policy to the group."

### Question 94

"A company stores critical data in Amazon S3 buckets. A SysOps administrator must build a solution to record all S3 API activity. 
Which action will meet this requirement?"	Create an AWS CloudTrail trail to log data events for all S3 objects.

### Question 95

"A company runs an application that uses a MySQL database on an Amazon EC2 instance. The EC2 instance has a General Purpose SSD Amazon Elastic Block 
Store (Amazon EBS) volume. The company made changes to the application code and now wants to perform load testing to evaluate the impact of the code changes. 
A SysOps administrator must create a new MySQL instance from a snapshot of the existing production instance. This new instance needs to perform as similarly as possible to the production instance. 
Which restore option meets these requirements?"	Use EBS fast snapshot restore to create a new General Purpose SSD EBS volume from the production snapshot.

### Question 96

"A team of on-call engineers frequently needs to connect to Amazon EC2 instances in a private subnet to troubleshoot and run commands. The instances use either the latest AWS-provided Windows Amazon Machine Images (AMIs) or Amazon Linux AMIs. 
The team has an existing 1AM role for authorization. A SysOps administrator must provide the team with access to the instances by granting IAM permissions to this role. 
Which solution will meet this requirement?"	Add a statement to the 1AM role policy to allow the ssm:StartSession action on the instances. Instruct the team to use AWS Systems Manager Session Manager to connect to the instances by using the assumed IAM role

### Question 97

"A company needs to ensure strict adherence to a budget for 25 applications deployed on AWS. Separate teams are responsible for storage, compute, and database costs. A SysOps administrator must implement an automated solution to alert each team when their projected spend will exceed a quarterly amount that has been set by the finance department. The solution cannot incur additional compute, storage, or database costs. 
Which solution will meet these requirements?"	Use AWS Budgets to create a cost budget for each team, filtering by the services they own. Specify the budget amount defined by the finance department along with a forecasted cost threshold. Enter the appropriate email recipients for each budget.

### Question 98

"A company hosts a static website on Amazon S3. An Amazon CloudFront distribution presents this site to global users. The company uses the Managed- 
CachingDisabled CloudFront cache policy. The company's developers confirm that they frequently update a file in Amazon S3 with new information. 
Users report that the website presents correct information when the website first loads the file. However, the users' browsers do not retrieve the updated file after a refresh. 
What should a SysOps administrator recommend to fix this issue?"	Add a Cache-Control header field with max-age=0 to the S3 object.

### Question 99

"A company has a policy that requires all Amazon EC2 instances to have a specific set of tags. If an EC2 instance does not have the required tags, the noncompliant instance should be terminated. 
What is the MOST operationally efficient solution that meets these requirement?"	Create an AWS Config rule to check if the required tags are present. If an EC2 instance is noncompliant, invoke an AWS Systems Manager Automation document to terminate the instance.

### Question 100

"A SysOps administrator wants to manage a web server application with AWS Elastic Beanstalk. The Elastic Beanstalk service must maintain full capacity for new deployments at all times. 
Which deployment policies satisfy this requirement? (Choose two.)"	"Immutable
Rolling with additional batch"

### Question 101

"A company has an Auto Scaling group of Amazon EC2 instances that scale based on average CPU utilization. The Auto Scaling group events log indicates an 
InsufficientInstanceCapacity error. 
Which actions should a SysOps administrator take to remediate this issue? (Choose two.)"	"Configure the Auto Scaling group in different Availability Zones
Change the instance type that the company is using."

### Question 102

"A SysOps administrator needs to control access to groups of Amazon EC2 instances using AWS Systems Manager Session Manager. Specific tags on the EC2 instances have already been added. 
Which additional actions should the administrator take to control access? (Choose two.)"	"Attach an IAM policy to the users or groups that require access to the EC2 instances. 
Create an IAM policy that grants access to any EC2 instances with a tag specified in the Condition element."

### Question 103

"A company has an AWS Lambda function in Account A. The Lambda function needs to read the objects in an Amazon S3 bucket in Account B. A SysOps administrator must create corresponding IAM roles in both accounts. 
Which solution will meet these requirements?"	In Account A, create a Lambda execution role to assume the role in Account B. In Account B. create a role that the function can assume to gain access to the S3 bucket

### Question 104

"An AWS Lambda function is intermittently failing several times a day. A SysOps administrator must find out how often this error has occurred in the last 7 days. 
Which action will meet this requirement in the MOST operationally efficient manner?"	Use Amazon CloudWatch Logs Insights to query the associated Lambda function logs.

### Question 105

"A company is using Amazon CloudFront to serve static content for its web application to its users. The CloudFront distribution uses an existing on-premises website as a custom origin. 
The company requires the use of TLS between CloudFront and the origin server. This configuration has worked as expected for several months. However, users are now experiencing HTTP 502 (Bad Gateway) errors when they view webpages that include content from the CloudFront distribution. 
What should a SysOps administrator do to resolve this problem?"	Examine the expiration date on the certificate on the origin site. Validate that the certificate has not expired. Replace the certificate if necessary.

### Question 106

"An Amazon CloudFront distribution has a single Amazon S3 bucket as its origin. A SysOps administrator must ensure that users can access the S3 bucket only through requests from the CloudFront endpoint. 
Which solution will meet these requirements?"	Create an origin access identity (OAI). Assign the OAI to the CloudFront distribution. Update the S3 bucket policy to restrict access to the OAI

### Question 107

"A SysOps administrator is designing a solution for an Amazon RDS for PostgreSQL DB instance. Database credentials must be stored and rotated monthly. The applications that connect to the DB instance send write-intensive traffic with variable client connections that sometimes increase significantly in a short period of time. 
Which solution should a SysOps administrator choose to meet these requirements?"	Configure AWS Secrets Manager to automatically rotate the credentials for the DB instance. Use RDS Proxy to handle the increases in database connections.

### Question 108

"A company wants to reduce costs for jobs that can be completed at any time. The jobs currently run by using multiple Amazon EC2 On-Demand Instances and the jobs take slightly less than 2 hours to complete. If a job falls for any reason it must be restarted from the beginning. 
Which solution will meet these requirements MOST cost-effectively?"	Submit a request for Spot Instances with a defined duration for the jobs

### Question 109

"An environment consists of 100 Amazon EC2 Windows instances. The Amazon CloudWatch agent is deployed and running on all EC2 Instances with a baseline configuration file to capture log files. There is a new requirement to capture the DHCP log files that exist on 50 of the instances. 
What is the MOST operationally efficient way to meet this new requirement?"	Create an additional CloudWatch agent configuration file to capture the DHCP logs. Use the AWS Systems Manager Run Command to restart the CloudWatch agent on each EC2 instance with the append-config option to apply the additional configuration file.

### Question 110

"A company has 10 Amazon EC2 instances in its production account. A SysOps administrator must ensure that email notifications are sent to administrators each time there is an EC2 instance state change.
Which solution will meet this requirements?"	Create an Amazon EventBridge (Amazon CloudWatch Events) rule that publishes a message to an Amazon Simple Notification Service (Amazon SNS) topic when an EC2 instance state changes. This SNS topic then sends notifications to its email subscribers.

### Question 111

"A company has an application that runs on a fleet of Amazon EC2 instances behind an Elastic Load Balancer. The instances run in an Auto Scaling group. The application's performance remains consistent throughout most of each day. However, an increase in user traffic slows the performance during the same 4-hour period of time each day.
What is the MOST operationally efficient solution that will resolve this issue?"	Create a scheduled scaling action to scale out the number of EC2 instances shortly before the increase in user traffic occurs

### Question 112

"A company hosts an application on an Amazon EC2 instance in a single AWS Region. The application requires support for non-HTTP TCP traffic and HTTP traffic.
The company wants to deliver content with low latency by leveraging the AWS network. The company also wants to implement an Auto Scaling group with an
Elastic Load Balancer.
How should a SysOps administrator meet these requirements?"	Create an Auto Scaling group with a Network Load Balancer (NLB). Add an accelerator with AWS Global Accelerator with the NLB as an endpoint.

### Question 113

"A SysOps administrator has an AWS CloudFormation template that is used to deploy an encrypted Amazon Machine Image (AMI). The CloudFormation template will be used in a second account so the SysOps administrator copies the encrypted AMI to the second account. When launching the new CloudFormation stack in the second account, it fails.
Which action should the SysOps administrator take to correct the issue?"	Re-encrypt the destination AMI with an AWS Key Management Service (AWS KMS) key from the destination account. 

### Question 114

"A company’s SysOps administrator deploys four new Amazon EC2 instances by using the standard Amazon Linux 2 Amazon Machine Image (AMI). The company needs to be able to use AWS Systems Manager to manage the instances. The SysOps administrator notices that the instances do not appear in the Systems Manager console.
What must the SysOps administrator do to resolve this issue? "	 Attach an IAM instance profile to the instances. Ensure that the instance profile contains the AmazonSSMManagedInstanceCore policy. 

### Question 115

"A SysOps administrator is maintaining a web application using an Amazon CloudFront web distribution, an Application Load Balancer (ALB), Amazon RDS, and Amazon EC2 in a VPC. All services have logging enabled. The administrator needs to investigate HTTP Layer 7 status codes from the web application.
Which log sources contain the status codes? (Choose two.) "	"ALB access logs Most Voted
CloudFront access togs"

### Question 116

"A company wants to be alerted through email when IAM CreateUser API calls are made within its AWS account.
Which combination of actions should a SysOps administrator take to meet this requirement? (Choose two.) "	"Create an Amazon EventBridge (Amazon CloudWatch Events) rule with AWS CloudTrail as the event source and IAM CreateUser as the specific API call for the event pattern.
Use an Amazon Simple Notification Service (Amazon SNS) topic as an event target with an email subscription"

### Question 117

"A database is running on an Amazon RDS Multi-AZ DB instance. A recent security audit found the database to be out of compliance because it was not encrypted.
Which approach will resolve the encryption requirement? "	Take a snapshot of the RDS instance, copy and encrypt the snapshot, and then restore to the new RDS instance. 
"A company using AWS Organizations requires that no Amazon S3 buckets in its production accounts should ever be deleted.

### Question 118

What is the SIMPLEST approach the SysOps administrator can take to ensure S3 buckets in those accounts can never be deleted? "	Use service control policies to deny the s3:DeleteBucket action on all buckets in production accounts.

### Question 119

"A company has an application that is running on Amazon EC2 instances in a VPC. The application needs access to download software updates from the internet. The VPC has public subnets and private subnets. The company’s security policy requires all EC2 instances to be deployed in private subnets.
What should a SysOps administrator do to meet these requirements? "	Add a NAT gateway to public subnet. In the route table for the private subnets, add a route to the NAT gateway. 

### Question 120

"A development team recently deployed a new version of a web application to production. After the release, penetration testing revealed a cross-site scripting vulnerability that could expose user data.
Which AWS service will mitigate this issue? "	AWS WAF

### Question 121

"A SysOps administrator must configure a resilient tier of Amazon EC2 instances for a high performance computing (HPC) application. The HPC application requires minimum latency between nodes.
Which actions should the SysOps administrator take to meet these requirements? (Choose two.) "	"Launch the EC2 instances into a cluster placement group. 
Place the EC2 instances in an Auto Scaling group within a single subnet. "

### Question 122

"A company’s customers are reporting increased latency while accessing static web content from Amazon S3. A SysOps administrator observed a very high rate of read operations on a particular S3 bucket.
What will minimize latency by reducing load on the S3 bucket? "	Create an Amazon CloudFront distribution with the S3 bucket as the origin. 

### Question 123

"A SysOps administrator needs to develop a solution that provides email notification and inserts a record into a database every time a file is put into an Amazon S3 bucket.
What is the MOST operationally efficient solution that meets these requirements? "	Set up an S3 event notification that targets an Amazon Simple Notification Service (Amazon SNS) topic. Create two subscriptions for the SNS topic. Use one subscription to send the email notification. Use the other subscription to invoke an AWS Lambda function that inserts the record into the database. 

### Question 124

"A company hosts a web application on Amazon EC2 instances behind an Application Load Balancer. The instances are in an Amazon EC2 Auto Scaling group. The application is accessed with a public URL.
A SysOps administrator needs to implement a monitoring solution that checks the availability of the application and follows the same routes and actions as a customer. The SysOps administrator must receive a notification if less than 95% of the monitoring runs find no errors.
Which solution will meet these requirements? "	

Create an Amazon CloudWatch Synthetics canary with a script that follows customer routes. Schedule the canary to run on a recurring schedule. Create a CloudWatch alarm that publishes a message to an Amazon Simple Notification Service (Amazon SNS) topic when the SuccessPercent metric is less than 95%. 

### Question 125

"A SysOps administrator uses AWS Systems Manager Session Manager to connect to instances. After the SysOps administrator launches a new Amazon EC2 instance, the EC2 instance does not appear in the Session Manager list of systems that are available for connection. The SysOps administrator verifies that Systems Manager Agent is installed, updated, and running on the EC2 instance.	

The EC2 instance does not have an attached IAM role that allows Session Manager to connect to the EC2 instance. 

### Question 126

"A SysOps administrator is unable to launch Amazon EC2 instances into a VPC because there are no available private IPv4 addresses in the VPC.
Which combination of actions must the SysOps administrator take to launch the instances? (Choose two.) "	

- Associate a secondary IPv4 CIDR block with the VPC. 

- Create a new subnet for the VPC.

### Question 127

"A SysOps administrator is creating an Amazon EC2 Auto Scaling group in a new AWS account. After adding some instances, the SysOps administrator notices that the group has not reached the minimum number of instances. The SysOps administrator receives the following error message:
Launching a new EC2 instance. Status Reason: Your quota allows for 0 more running instance(s).
You requested at least 1. Launching EC2 instance failed.
Which action will resolve this issue? "	Request a quota increase for the instance type family by using Service Quotas on the AWS Management Console.

### Question 128

"A SysOps administrator is creating two AWS CloudFormation templates. The first template will create a VPC with associated resources, such as subnets, route tables, and an internet gateway. The second template will deploy application resources within the VPC that was created by the first template. The second template should refer to the resources created by the first template.
How can this be accomplished with the LEAST amount of administrative effort? "	Add an export field to the outputs of the first template and import the values in the second template.

### Question 129

"A company runs a web application on three Amazon EC2 instances behind an Application Load Balancer (ALB). The company notices that random periods of increased traffic cause a degradation in the application’s performance. A SysOps administrator must scale the application to meet the increased traffic.
Which solution meets these requirements? "	Deploy the application to an Auto Scaling group of EC2 instances with a target tracking scaling policy. Attach the ALB to the Auto Scaling group.

### Question 130

"A company has a high-performance Windows workload. The workload requires a storage volume that provides consistent performance of 10,000 IOPS. The company does not want to pay for additional unneeded capacity to achieve this performance.
Which solution will meet these requirements with the LEAST cost? "

Use a General Purpose SSD (gp3) Amazon Elastic Block Store (Amazon EBS) volume that is configured with 10,000 provisioned IOPS

### Question 131

"A SysOps administrator must create a solution that automatically shuts down any Amazon EC2 instances that have less than 10% average CPU utilization for 60 minutes or more.
Which solution will meet this requirement in the MOST operationally efficient manner? "	 Implement an Amazon CloudWatch alarm for each EC2 instance to monitor average CPU utilization. Set the period at 1 hour, and set the threshold at 10%. Configure an EC2 action on the alarm to stop the instance

### Question 132

"A SysOps administrator is unable to authenticate an AWS CLI call to an AWS service.
Which of the following is the cause of this issue? "	

There is no access key.

### Question 133

"A company requires that all IAM user accounts that have not been used for 90 days or more must have their access keys and passwords immediately disabled. A SysOps administrator must automate the process of disabling unused keys using the MOST operationally efficient method.
How should the SysOps administrator implement this solution? "	Set up an AWS Config managed rule to identify IAM users that have not been active for 90 days. Set up an AWS Systems Manager automation runbook to disable the AWS access keys for these IAM users

### Question 134

"A company creates custom AMI images by launching new Amazon EC2 instances from an AWS CloudFormation template. It installs and configures necessary software through AWS OpsWorks, and takes images of each EC2 instance. The process of installing and configuring software can take between 2 to 3 hours, but at times, the process stalls due to installation errors.
The SysOps administrator must modify the CloudFormation template so if the process stalls, the entire stack will fail and roll back.
Based on these requirements, what should be added to the template? "	CreationPolicy with a timeout set to 4 hours.

### Question 135

"A company runs workloads on 90 Amazon EC2 instances in the eu-west-1 Region in an AWS account. In 2 months, the company will migrate the workloads from eu-west-1 to the eu-west-3 Region.
The company needs to reduce the cost of the EC2 instances. The company is willing to make a 1-year commitment that will begin next week. The company must choose an EC2 instance purchasing option that will provide discounts for the 90 EC2 instances regardless of Region during the 1-year period.
Which solution will meet these requirements?"	 Purchase a Compute Savings Plan.

### Question 136

"A SysOps administrator has created a VPC that contains a public subnet and a private subnet. Amazon EC2 instances that were launched in the private subnet cannot access the internet. The default network ACL is active on all subnets in the VPC, and all security groups allow all outbound traffic.
Which solution will provide the EC2 instances in the private subnet with access to the internet? "	Create a NAT gateway in the public subnet. Create a route from the private subnet to the NAT gateway

### Question 137

"A company plans to run a public web application on Amazon EC2 instances behind an Elastic Load Balancer (ELB). The company’s security team wants to protect the website by using AWS Certificate Manager (ACM) certificates. The ELB must automatically redirect any HTTP requests to HTTPS.
Which solution will meet these requirements? "	 Create an Application Load Balancer that has one HTTP listener on port 80 and one HTTPS protocol listener on port 443. Attach an SSL/TLS certificate to listener port 443. Create a rule to redirect requests from port 80 to port 443

### Question 138

"A company wants to track its AWS costs in all member accounts that are part of an organization in AWS Organizations. Managers of the member accounts want to receive a notification when the estimated costs exceed a predetermined amount each month. The managers are unable to configure a billing alarm. The IAM permissions for all users are correct.
What could be the cause of this issue? "	The management/payer account does not have billing alerts turned on.

### Question 139

"A company is using Amazon Elastic Container Service (Amazon ECS) to run a containerized application on Amazon EC2 instances. A SysOps administrator needs to monitor only traffic flows between the ECS tasks.
Which combination of steps should the SysOps administrator take to meet this requirement? (Choose two.) "	"	Configure VPC Flow Logs on the elastic network interface of each task. Most Voted
Specify the awsvpc network mode in the task definition."

### Question 140

"A company uses AWS Organizations to manage multiple AWS accounts. The company’s SysOps team has been using a manual process to create and manage IAM roles. The team requires an automated solution to create and manage the necessary IAM roles for multiple AWS accounts.
What is the MOST operationally efficient solution that meets these requirements? "	"	Use AWS CloudFormation StackSets with AWS Organizations to deploy and manage IAM roles for the AWS accounts"

### Question 141

"A SysOps administrator needs to configure automatic rotation for Amazon RDS database credentials. The credentials must rotate every 30 days. The solution must integrate with Amazon RDS.
Which solution will meet these requirements with the LEAST operational overhead?"	Store the credentials in AWS Secrets Manager. Configure automatic rotation with a rotation interval of 30 days.

### Question 142

"A company’s SysOps administrator attempts to restore an Amazon Elastic Block Store (Amazon EBS) snapshot. However, the snapshot is missing because another system administrator accidentally deleted the snapshot. The company needs the ability to recover snapshots for a specified period of time after snapshots are deleted.
Which solution will provide this functionality? "	"	Create a Recycle Bin retention rule for EBS snapshots for the desired retention period."

### Question 143

"A SysOps administrator recently configured Amazon S3 Cross-Region Replication on an S3 bucket.
Which of the following does this feature replicate to the destination S3 bucket by default? "	 Object metadata 

### Question 144

"A company has a workload that is sending log data to Amazon CloudWatch Logs. One of the fields includes a measure of application latency. A SysOps administrator needs to monitor the p90 statistic of this field over time.
What should the SysOps administrator do to meet this requirement? "	 Create a metric filter on the log data

### Question 145

"A company wants to archive sensitive data on Amazon S3 Glacier. The company’s regulatory and compliance requirements do not allow any modifications to the data by any account.
Which solution meets these requirements? "	"	Attach a vault lock policy to an S3 Glacier vault that contains the archived data. Use the lock ID to validate the vault lock policy within 24 hours. "

### Question 146

"A company manages an application that uses Amazon ElastiCache for Redis with two extra-large nodes spread across two different Availability Zones. The company’s IT team discovers that the ElastiCache for Redis cluster has 75% freeable memory. The application must maintain high availability.
What is the MOST cost-effective way to resize the cluster? "	Perform an online resizing for the ElastiCache for Redis cluster. Change the node types from extra-large nodes to large nodes.

### Question 147

"A company must migrate its applications to AWS. The company is using Chef recipes for configuration management. The company wants to continue to use the existing Chef recipes after the applications are migrated to AWS.
What is the MOST operationally efficient solution that meets these requirements? "	Use AWS OpsWorks to create a stack and add layers with Chef recipes.

### Question 148

"A company uses AWS Organizations to manage its AWS accounts. A SysOps administrator must create a backup strategy for all Amazon EC2 instances across all the company’s AWS accounts.
Which solution will meet these requirements in the MOST operationally efficient way? "	 Use AWS Backup in the management account to deploy policies for all accounts and resources

### Question 149

"A SysOps administrator is reviewing VPC Flow Logs to troubleshoot connectivity issues in a VPC. While reviewing the logs, the SysOps administrator notices that rejected traffic is not listed.
What should the SysOps administrator do to ensure that all traffic is logged? "	Create a new flow log that has a filter setting to capture all traffic
A company is expanding its use of AWS services across its portfolios. The company wants to provision AWS accounts for each team to ensure a separation of business processes for security, compliance, and billing. Account creation and bootstrapping should be completed in a scalable and efficient way so new accounts are created with a defined baseline and governance guardrails in place. A SysOps administrator needs to design a provisioning process that saves time and resources.	Use AWS Control Tower to create a template in Account Factory and use the template to provision new accounts

### Question 150

"A SysOps administrator noticed that the cache hit ratio for an Amazon CloudFront distribution is less than 10%.
Which collection of configuration changes will increase the cache hit ratio for the distribution? (Choose two.) "	" Ensure that only required cookies, query strings, and headers are forwarded in the Cache Behavior Settings
        Increase the CloudFront time to live (TTL) settings in the Cache Behavior Settings. "

### Question 151

"A SysOps administrator is attempting to download patches from the internet into an instance in a private subnet. An internet gateway exists for the VPC, and a NAT gateway has been deployed on the public subnet; however, the instance has no internet connectivity. The resources deployed into the private subnet must be inaccessible directly from the public internet.

Public Subnet (10.0.1.0/24) Route Table

Destination Target -
10.0.0.0/16 local
0.0.0.0/0 IGW

Private Subnet (10.0.2.0/24) Route Table

Destination Target -
10.0.0.0/16 local

What should be added to the private subnet’s route table in order to address this issue, given the information provided? "	"	0.0.0.0/0 NAT"

### Question 152

"A company is undergoing an external audit of its systems, which run wholly on AWS. A SysOps administrator must supply documentation of Payment Card Industry Data Security Standard (PCI DSS) compliance for the infrastructure managed by AWS.
Which set of actions should the SysOps administrator take to meet this requirement? "	Download the applicable reports from the AWS Artifact portal and supply these to the auditors. 

### Question 153

"A company has an initiative to reduce costs associated with Amazon EC2 and AWS Lambda.
Which action should a SysOps administrator take to meet these requirements? "	"	Use AWS Compute Optimizer and take action on the provided recommendations."

### Question 154

"A company wants to use only IPv6 for all its Amazon EC2 instances. The EC2 instances must not be accessible from the internet, but the EC2 instances must be able to access the internet. The company creates a dual-stack VPC and IPv6-only subnets.
How should a SysOps administrator configure the VPC to meet these requirements?"	Create and attach an egress-only internet gateway. Create a custom route table that includes an entry to point all IPv6 traffic to the egress-only internet gateway. Attach the custom route table to the IPv6-only subnets

### Question 155

"A company has an existing web application that runs on two Amazon EC2 instances behind an Application Load Balancer (ALB) across two Availability Zones. The application uses an Amazon RDS Multi-AZ DB Instance. Amazon Route 53 record sets route requests for dynamic content to the load balancer and requests for static content to an Amazon S3 bucket. Site visitors are reporting extremely long loading times.
Which actions should be taken to improve the performance of the website? (Choose two.)"	"Add Amazon CloudFront caching for static content
Implement Amazon EC2 Auto Scaling for the web servers"

### Question 156

"A company is running an application on premises and wants to use AWS for data backup. All of the data must be available locally. The backup application can write only to block-based storage that is compatible with the Portable Operating System Interface (POSIX).
Which backup solution will meet these requirements? "	"	Use AWS Storage Gateway, and configure it to use gateway-stored volumes."

### Question 157

"A global company handles a large amount of personally identifiable information (PII) through an internal web portal. The company’s application runs in a corporate data center that is connected to AWS through an AWS Direct Connect connection. The application stores the PII in Amazon S3. According to a compliance requirement, traffic from the web portal to Amazon S3 must not travel across the internet.
What should a SysOps administrator do to meet the compliance requirement? "	Provision an interface VPC endpoint for Amazon S3. Modify the application to use the interface endpoint

### Question 158

"A SysOps administrator notices a scale-up event for an Amazon EC2 Auto Scaling group. Amazon CloudWatch shows a spike in the RequestCount metric for the associated Application Load Balancer. The administrator would like to know the IP addresses for the source of the requests.
Where can the administrator find this information? "	"	Elastic Load Balancer access logs"

### Question 159

"A company’s SysOps administrator deploys a public Network Load Balancer (NLB) in front of the company’s web application. The web application does not use any Elastic IP addresses. Users must access the web application by using the company’s domain name. The SysOps administrator needs to configure Amazon Route 53 to route traffic to the NLB.
Which solution will meet these requirements MOST cost-effectively? "	Create a Route 53 alias record for the NLB.

### Question 160

"A company runs an encrypted Amazon RDS for Oracle DB instance. The company wants to make regular backups available in another AWS Region.
What is the MOST operationally efficient solution that meets these requirements? "	"	Modify the DB instance. Enable cross-Region automated backups."

### Question 161

"A company is rolling out a new version of its website. Management wants to deploy the new website in a limited rollout to 20% of the company’s customers. The company uses Amazon Route 53 for its website’s DNS solution.
Which configuration will meet these requirements?"	Create a weighted routing policy. Within the policy, configure a weight of 80 for the record pointing to the original resource. Configure a weight of 20 for the record pointing to the new resource. 

### Question 162

"A SysOps administrator created an AWS CloudFormation template that provisions Amazon EC2 instances, an Elastic Load Balancer (ELB), and an Amazon RDS DB instance. During stack creation, the creation of the EC2 instances and the creation of the ELB are successful. However, the creation of the DB instance fails.
What is the default behavior of CloudFormation in this scenario? "	"	CloudFormation will roll back the stack but will not delete the stack. "

### Question 163

"A SysOps administrator needs to automate the invocation of an AWS Lambda function. The Lambda function must run at the end of each day to generate a report on data that is stored in an Amazon S3 bucket.
What is the MOST operationally efficient solution that meets these requirements? "	 Create an Amazon EventBridge (Amazon CloudWatch Events) rule that has a schedule and the Lambda function as a target.

### Question 164

"A company is releasing a new static website hosted on Amazon S3. The static website hosting feature was enabled on the bucket and content was uploaded; however, upon navigating to the site, the following error message is received:

403 Forbidden - Access Denied

What change should be made to fix this error? "	Add a bucket policy that grants everyone read access to the bucket objects.

### Question 165

"A company is storing media content in an Amazon S3 bucket and uses Amazon CloudFront to distribute the content to its users. Due to licensing terms, the company is not authorized to distribute the content in some countries. A SysOps administrator must restrict access to certain countries.
What is the MOST operationally efficient solution that meets these requirements? "	Enable the geo restriction feature in the CloudFront distribution to prevent access from unauthorized countries

### Question 166

"A SysOps administrator created an Amazon VPC with an IPv6 CIDR block, which requires access to the internet. However, access from the internet towards the VPC is prohibited. After adding and configuring the required components to the VPC, the administrator is unable to connect to any of the domains that reside on the internet.
What additional route destination rule should the administrator add to the route tables? "	"	Route ::/0 traffic to an egress-only internet gateway"

### Question 167

"A company hosts several write-intensive applications. These applications use a MySQL database that runs on a single Amazon EC2 instance. The company asks a SysOps administrator to implement a highly available database solution that is ideal for multi-tenant workloads.
Which solution should the SysOps administrator implement to meet these requirements? "	Migrate the database to an Amazon Aurora multi-master DB cluster

### Question 168

"A company has a memory-intensive application that runs on a fleet of Amazon EC2 instances behind an Elastic Load Balancer (ELB). The instances run in an Auto Scaling group. A SysOps administrator must ensure that the application can scale based on the number of users that connect to the application.
Which solution will meet these requirements? "	Create a scaling policy that will scale the application based on the ActiveConnectionCount Amazon CloudWatch metric that is generated from the ELB.

### Question 169

"A SysOps administrator creates a new VPC that includes a public subnet and a private subnet. The SysOps administrator successfully launches 11 Amazon EC2 instances in the private subnet. The SysOps administrator attempts to launch one more EC2 instance in the same subnet. However, the SysOps administrator receives an error message that states that not enough free IP addresses are available."	 

D. Create a new private subnet to hold the required EC2 instances. Most Voted 

### Question 170

"A company needs to automatically monitor an AWS account for potential unauthorized AWS Management Console logins from multiple geographic locations."

D. Configure Amazon GuardDuty to monitor the UnauthorizedAccess:IAMUser/ConsoleLoginSuccess.B finding.

### Question 171

"A company has an Amazon RDS DB instance. The company wants to implement a caching service while maintaining high availability.
Which combination of actions will meet these requirements? (Choose two.) "	

- Create an Amazon ElastiCache for Redis data store. Most Voted

- D. Enable Multi-AZ for the data store."

### Question 172

"A company monitors its account activity using AWS CloudTrail, and is concerned that some log files are being tampered with after the logs have been delivered to the account’s Amazon S3 bucket.
Moving forward, how can the SysOps administrator confirm that the log files have not been modified after being delivered to the S3 bucket? "	 B. Enable log file integrity validation and use digest files to verify the hash value of the log file. Most Voted 

### Question 173

"A SysOps administrator is reviewing AWS Trusted Advisor warnings and encounters a warning for an S3 bucket policy that has open access permissions. While discussing the issue with the bucket owner, the administrator realizes the S3 bucket is an origin for an Amazon CloudFront web distribution.
Which action should the administrator take to ensure that users access objects in Amazon S3 by using only CloudFront URLs? "	Create an origin access identity and grant it permissions to read objects in the S3 bucket

### Question 174

"A SysOps administrator is reviewing AWS Trusted Advisor recommendations. The SysOps administrator notices that all the application servers for a finance application are listed in the Low Utilization Amazon EC2 Instances check. The application runs on three instances across three Availability Zones. The SysOps administrator must reduce the cost of running the application without affecting the application’s availability or design.
Which solution will meet these requirements? "	Apply rightsizing recommendations from AWS Cost Explorer to reduce the instance size

### Question 175

"A company hosts its website in the us-east-1 Region. The company is preparing to deploy its website into the eu-central-1 Region. Website visitors who are located in Europe should access the website that is hosted in eu-central-1. All other visitors access the website that is hosted in us-east-1. The company uses Amazon Route 53 to manage the website’s DNS records.
Which routing policy should a SysOps administrator apply to the Route 53 record set to meet these requirements? "	Geolocation routing policy

### Question 176

"An organization with a large IT department has decided to migrate to AWS. With different job functions in the IT department, it is not desirable to give all users access to all AWS resources. Currently the organization handles access via LDAP group membership.
What is the BEST method to allow access using current LDAP credentials? "	"	Federate the LDAP directory with IAM using SAML. Create different IAM roles to correspond to different LDAP groups to limit permissions."

### Question 177

"A SysOps administrator has created an Amazon EC2 instance using an AWS CloudFormation template in the us-east-1 Region. The administrator finds that this template has failed to create an EC2 instance in the us-west-2 Region.
What is one cause for this failure? "	The Amazon Machine Image (AMI) ID referenced in the CloudFormation template could not be found in the us-west-2 Region.
 A user has launched two EBS backed EC2 instances in the US-East-1a region. The user wants to change the zone of one of the instances. How can the user change it?	 Create an AMI of the running instance and launch the instance in a separate AZ 

### Question 178

"A SysOps administrator is investigating a company’s web application for performance problems. The application runs on Amazon EC2 instances that are in an Auto Scaling group. The application receives large traffic increases at random times throughout the day. During periods of rapid traffic increases, the Auto Scaling group is not adding capacity fast enough. As a result, users are experiencing poor performance.
The company wants to minimize costs without adversely affecting the user experience when web traffic surges quickly. The company needs a solution that adds more capacity to the Auto Scaling group for larger traffic increases than for smaller traffic increases.
How should the SysOps administrator configure the Auto Scaling group to meet these requirements? "	Create a step scaling policy with settings to make larger adjustments in capacity when the system is under heavy load

### Question 179

"A company has a compliance requirement that no security groups can allow SSH ports to be open to all IP addresses. A SysOps administrator must implement a solution that will notify the company’s SysOps team when a security group rule violates this requirement. The solution also must remediate the security group rule automatically.
Which solution will meet these requirements? "	Activate the AWS Config restricted-ssh managed rule. Add automatic remediation to the AWS Config rule by using the AWS Systems Manager Automation AWS-DisablePublicAccessForSecurityGroup runbook. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to notify the SysOps team when the rule is noncompliant

### Question 180

"A company has an application that runs only on Amazon EC2 Spot Instances. The instances run in an Amazon EC2 Auto Scaling group with scheduled scaling actions. However, the capacity does not always increase at the scheduled times, and instances terminate many times a day. A SysOps administrator must ensure that the instances launch on time and have fewer interruptions.
Which action will meet these requirements? "	Specify the capacity-optimized allocation strategy for Spot Instances. Add more instance types to the Auto Scaling group.

### Question 181

"A company plans to deploy a database on an Amazon Aurora MySQL DB cluster. The database will store data for a demonstration environment. The data must be reset on a daily basis.
What is the MOST operationally efficient solution that meets these requirements? "	Enable the Backtrack feature during the creation of the DB cluster. Specify a target backtrack window of 48 hours. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function on a daily basis. Configure the function to perform a backtrack operation.

### Question 182

"A SysOps administrator is setting up an automated process to recover an Amazon EC2 instance in the event of an underlying hardware failure. The recovered instance must have the same private IP address and the same Elastic IP address that the original instance had. The SysOps team must receive an email notification when the recovery process is initiated.
Which solution will meet these requirements? "	"	Create an Amazon CloudWatch alarm for the EC2 instance, and specify the StatusCheckFailed_System metric. Add an EC2 action to the alarm to recover the instance. Add an alarm notification to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the SysOps team email address to the SNS topic."

### Question 183

"A company has a public website that recently experienced problems. Some links led to missing webpages, and other links rendered incorrect webpages. The application infrastructure was running properly, and all the provisioned resources were healthy. Application logs and dashboards did not show any errors, and no monitoring alarms were raised. Systems administrators were not aware of any problems until end users reported the issues.
The company needs to proactively monitor the website for such issues in the future and must implement a solution as soon as possible.
Which solution will meet these requirements with the LEAST operational overhead? "	Create an Amazon CloudWatch Synthetics canary. Use the CloudWatch Synthetics Recorder plugin to generate the script for the canary run. Configure the canary in line with requirements. Create an alarm to provide alerts when issues are detected

### Question 184

"A SysOps administrator is responsible for a company’s security groups. The company wants to maintain a documented trail of any changes that are made to the security groups. The SysOps administrator must receive notification whenever the security groups change.
Which solution will meet these requirements? "	Set up AWS Config to record security group changes. Specify an Amazon S3 bucket as the location for configuration snapshots and history files. Create an Amazon Simple Notification Service (Amazon SNS) topic for notifications about configuration changes. Subscribe the SysOps administrator’s email address to the SNS topic

### Question 185

"An ecommerce company has built a web application that uses an Amazon Aurora DB cluster. The DB cluster includes memory optimized instance types with both a writer node and a reader node. Traffic volume changes throughout the day. During sudden traffic surges, Amazon CloudWatch metrics for the DB cluster indicate high RAM consumption and an increase in select latency.
A SysOps administrator must implement a configuration change to improve the performance of the DB cluster. The change must minimize downtime and must not result in the loss of data.
Which change will meet these requirements? "	Add an Aurora Replica to the DB cluster

### Question 186

"A company has a simple web application that runs on a set of Amazon EC2 instances behind an Elastic Load Balancer in the eu-west-2 Region. Amazon Route 53 holds a DNS record for the application with a simple routing policy. Users from all over the world access the application through their web browsers.
The company needs to create additional copies of the application in the us-east-1 Region and in the ap-south-1 Region. The company must direct users to the Region that provides the fastest response times when the users load the application.
What should a SysOps administrator do to meet these requirements? "	"	In each new Region, create a new Elastic Load Balancer and a new set of EC2 instances to run a copy of the application. Transition to a latency routing policy."

### Question 187

"A company creates a new member account by using AWS Organizations. A SysOps administrator needs to add AWS Business Support to the new account.
Which combination of steps must the SysOps administrator take to meet this requirement? (Choose two.) "	

        - Sign in to the new account by using IAM credentials. Change the support plan

        - Create an IAM user that has administrator privileges in the new account"

### Question 188

"A SysOps administrator creates two VPCs, VPC1 and VPC2, in a company’s AWS account The SysOps administrator deploys a Linux Amazon EC2 instance in VPC1 and deploys an Amazon RDS for MySQL DB instance in VPC2. The DB instance is deployed in a private subnet. An application that runs on the EC2 instance needs to connect to the database.
What should the SysOps administrator do to give the EC2 instance the ability to connect to the database? "	 Configure VPC peering between the two VPCs.

### Question 189

"A company uses an Amazon S3 bucket to store data files. The S3 bucket contains hundreds of objects. The company needs to replace a tag on all the objects in the S3 bucket with another tag.
What is the MOST operationally efficient way to meet this requirement? "	Use S3 Batch Operations. Specify the operation to replace all object tags.

### Question 190

"A company needs to take an inventory of applications that are running on multiple Amazon EC2 instances. The company has configured users and roles with the appropriate permissions for AWS Systems Manager. An updated version of Systems Manager Agent has been installed and is running on every instance. While configuring an inventory collection, a SysOps administrator discovers that not all the instances in a single subnet are managed by Systems Manager.
What must the SysOps administrator do to fix this issue? "	Ensure that all the EC2 instances have an instance profile with Systems Manager access

### Question 191

"A company stores sensitive data in an Amazon S3 bucket. The company must log all access attempts to the S3 bucket. The company’s risk team must receive immediate notification about any delete events.
Which solution will meet these requirements? "	Enable S3 server access logging for audit logs. Set up an Amazon Simple Notification Service (Amazon SNS) notification for the S3 bucket. Select DeleteObject for the event type for the alert system

### Question 192

"A SysOps administrator receives an alert from Amazon GuardDuty about suspicious network activity on an Amazon EC2 instance. The GuardDuty finding lists a new external IP address as a traffic destination. The SysOps administrator does not recognize the external IP address. The SysOps administrator must block traffic to the external IP address that GuardDuty identified.
Which solution will meet this requirement? "	Create a network ACL. Add an outbound deny rule for traffic to the external IP address. 

### Question 193

"A company’s reporting job that used to run in 15 minutes is now taking an hour to run. An application generates the reports. The application runs on Amazon EC2 instances and extracts data from an Amazon RDS for MySQL database.
A SysOps administrator checks the Amazon CloudWatch dashboard for the RDS instance and notices that the Read IOPS metrics are high, even when the reports are not running. The SysOps administrator needs to improve the performance and the availability of the RDS instance.
Which solution will meet these requirements? "	Deploy an RDS read replica. Update the reporting job to query the reader endpoint.

### Question 194

"A company’s SysOps administrator regularly checks the AWS Personal Health Dashboard in each of the company’s accounts. The accounts are part of an organization in AWS Organizations. The company recently added 10 more accounts to the organization. The SysOps administrator must consolidate the alerts from each account’s Personal Health Dashboard.
Which solution will meet this requirement with the LEAST amount of effort? "	Enable organizational view in AWS Health

### Question 195

"A company runs an application on Amazon EC2 instances. The EC2 instances are in an Auto Scaling group and run behind an Application Load Balancer (ALB). The application experiences errors when total requests exceed 100 requests per second. A SysOps administrator must collect information about total requests for a 2-week period to determine when requests exceeded this threshold.
What should the SysOps administrator do to collect this data? "	"	Use the ALB’s RequestCount metric. Configure a time range of 2 weeks and a period of 1 minute. Examine the chart to determine peak traffic times and volumes"

### Question 196

"A company recently migrated its application to a VPC on AWS. An AWS Site-to-Site VPN connection connects the company’s on-premises network to the VPC. The application retrieves customer data from another system that resides on premises. The application uses an on-premises DNS server to resolve domain records. After the migration, the application is not able to connect to the customer data because of name resolution errors.
Which solution will give the application the ability to resolve the internal domain names? "	Create an Amazon Route 53 Resolver outbound endpoint. Configure the outbound endpoint to forward DNS queries against the on-premises domain to the on-premises DNS server.

### Question 197

"A company’s web application is available through an Amazon CloudFront distribution and directly through an internet-facing Application Load Balancer (ALB). A SysOps administrator must make the application accessible only through the CloudFront distribution and not directly through the ALB. The SysOps administrator must make this change without changing the application code.
Which solution will meet these requirements? "	Add a custom HTTP header to the origin settings for the distribution. In the ALB listener, add a rule to forward requests that contain the matching custom header and the header’s value. Add a default rule to return a fixed response code of 40

### Question 198

"A company runs several workloads on AWS. The company identifies five AWS Trusted Advisor service quota metrics to monitor in a specific AWS Region. The company wants to receive email notification each time resource usage exceeds 60% of one of the service quotas.
Which solution will meet these requirements? "	"	Create five Amazon CloudWatch alarms, one for each Trusted Advisor service quota metric. Configure an Amazon Simple Notification Service (Amazon SNS) topic for email notification each time that usage exceeds 60% of one of the service quotas"

### Question 199

"A company needs to implement a managed file system to host Windows file shares for users on premises. Resources in the AWS Cloud also need access to the data on these file shares. A SysOps administrator needs to present the user file shares on premises and make the user file shares available on AWS with minimum latency.
What should the SysOps administrator do to meet these requirements? "	"	Set up an Amazon FSx File Gateway"

### Question 200

"A company is hosting applications on Amazon EC2 instances. The company is hosting a database on an Amazon RDS for PostgreSQL DB instance. The company requires all connections to the DB instance to be encrypted.
What should a SysOps administrator do to meet this requirement? "	Enforce SSL connections to the database by using a custom parameter group

### Question 201

"A company recently purchased Savings Plans. The company wants to receive email notification when the company’s utilization drops below 90% for a given day.
Which solution will meet this requirement? "	Use AWS Budgets to create a Savings Plans budget to track the daily utilization of the Savings Plans. Configure an Amazon Simple Notification Service (Amazon SNS) topic for email notification when the utilization drops below 90% for a given day

### Question 202

"A company uses an Amazon Simple Queue Service (Amazon SQS) standard queue with its application. The application sends messages to the queue with unique message bodies. The company decides to switch to an SQS FIFO queue.
What must the company do to migrate to an SQS FIFO queue? "	Create a new SQS FIFO queue. Turn on content-based deduplication on the new FIFO queue. Update the application to include a message group ID in the messages

### Question 203

"A company’s SysOps administrator must ensure that all Amazon EC2 Windows instances that are launched in an AWS account have a third-party agent installed. The third-party agent has an .msi package. The company uses AWS Systems Manager for patching, and the Windows instances are tagged appropriately. The third-party agent requires periodic updates as new versions are released. The SysOps administrator must deploy these updates automatically.
Which combination of steps will meet these requirements with the LEAST operational effort? (Choose two.) "	

- "Create a Systems Manager Distributor package for the third-party agent

- Create a Systems Manager State Manager association to run the AWS-ConfigureAWSPackage document. Populate the details of the third-party agent package. Specify instance tags based on the appropriate tag value for Windows with a schedule of 1 day.

### Question 204

"A company runs hundreds of Amazon EC2 instances in a single AWS Region. Each EC2 instance has two attached 1 GiB General Purpose SSD (gp2) Amazon Elastic Block Store (Amazon EBS) volumes. A critical workload is using all the available IOPS capacity on the EBS volumes.
According to company policy, the company cannot change instance types or EBS volume types without completing lengthy acceptance tests to validate that the company’s applications will function properly. A SysOps administrator needs to increase the I/O performance of the EBS volumes as quickly as possible.
Which action should the SysOps administrator take to meet these requirements? "	Increase the size of the 1 GiB EBS volumes

### Question 205

"A company needs to deploy a new workload on AWS. The company must encrypt all data at rest and must rotate the encryption keys once each year. The workload uses an Amazon RDS for MySQL Multi-AZ database for data storage.
Which configuration approach will meet these requirements? "	 Create a new AWS Key Management Service (AWS KMS) customer managed key. Enable automatic key rotation. Enable RDS encryption on the database at creation time by using the KMS key

### Question 206

"A company has an application that is deployed to two AWS Regions in an active-passive configuration. The application runs on Amazon EC2 instances behind an Application Load Balancer (ALB) in each Region. The instances are in an Amazon EC2 Auto Scaling group in each Region. The application uses an Amazon Route 53 hosted zone for DNS. A SysOps administrator needs to configure automatic failover to the secondary Region.
What should the SysOps administrator do to meet these requirements? "	"	Configure Route 53 alias records that point to each ALB. Choose a failover routing policy. Set Evaluate Target Health to Yes"

### Question 207

"A company is implementing a monitoring solution that is based on machine learning. The monitoring solution consumes Amazon EventBridge (Amazon CloudWatch Events) events that are generated by Amazon EC2 Auto Scaling. The monitoring solution provides detection of anomalous behavior such as unanticipated scaling events and is configured as an EventBridge (CloudWatch Events) API destination.
During initial testing, the company discovers that the monitoring solution is not receiving events. However, Amazon CloudWatch is showing that the EventBridge (CloudWatch Events) rule is being invoked. A SysOps administrator must implement a solution to retrieve client error details to help resolve this issue.
Which solution will meet these requirements with the LEAST operational effort?"	

Add an Amazon Simple Queue Service (Amazon SQS) standard queue as a dead-letter queue for the target. Process the messages in the dead-letter queue to retrieve error details

### Question 208

"A company is storing backups in an Amazon S3 bucket. The backups must not be deleted for at least 3 months after the backups are created.
What should a SysOps administrator do to meet this requirement? "	

Enable S3 Object Lock on a new S3 bucket in compliance mode. Place all backups in the new S3 bucket with a retention period of 3 months

### Question 209

"A SysOps administrator needs to track the costs of data transfer between AWS Regions. The SysOps administrator must implement a solution to send alerts to an email distribution list when transfer costs reach 75% of a specific threshold.
What should the SysOps administrator do to meet these requirements? "	

Use AWS Budgets to create a cost budget for data transfer costs. Set an alert at 75% of the budgeted amount. Configure the budget to send a notification to the email distribution list when costs reach 75% of the threshold

### Question 210

"A company needs to archive all audit logs for 10 years. The company must protect the logs from any future edits.
Which solution will meet these requirements? "	

Store the data in an Amazon S3 Glacier vault. Configure a vault lock policy for write-once, read-many (WORM) access. 

### Question 211

"A company’s AWS Lambda function is experiencing performance issues. The Lambda function performs many CPU-intensive operations. The Lambda function is not running fast enough and is creating bottlenecks in the system.
What should a SysOps administrator do to resolve this issue? "	

Increase the amount of memory for the Lambda function

### Question 212

"A company hosts a web application on an Amazon EC2 instance. The web server logs are published to Amazon CloudWatch Logs. The log events have the same structure and include the HTTP response codes that are associated with the user requests. The company needs to monitor the number of times that the web server returns an HTTP 404 response.

What is the MOST operationally efficient solution that meets these requirements? "	Create a CloudWatch Logs metric filter that counts the number of times that the web server returns an HTTP 404 response. 
"A company is attempting to manage its costs in the AWS Cloud. A SysOps administrator needs specific company-defined tags that are assigned to resources to appear on the billing report.

What should the SysOps administrator do to meet this requirement? "	Activate the tags as user-defined cost allocation tags. 
"A company is expanding globally and needs to back up data on Amazon Elastic Block Store (Amazon EBS) volumes to a different AWS Region. Most of the EBS volumes that store the data are encrypted, but some of the EBS volumes are unencrypted. The company needs the backup data from all the EBS volumes to be encrypted.

Which solution will meet these requirements with the LEAST management overhead? "	 Configure a lifecycle policy in Amazon Data Lifecycle Manager (Amazon DLM) to create the EBS volume snapshots with cross-Region backups enabled. Encrypt the snapshot copies by using AWS Key Management Service (AWS KMS). 
"A SysOps administrator creates an Amazon Elastic Kubernetes Service (Amazon EKS) cluster that uses AWS Fargate. The cluster is deployed successfully. The SysOps administrator needs to manage the cluster by using the kubectl command line tool.

Which of the following must be configured on the SysOps administrator’s machine so that kubectl can communicate with the cluster API server? "	The kubeconfig file
"A company wants to collect data from an application to use for analytics. For the first 90 days, the data will be infrequently accessed but must remain highly available. During this time, the company’s analytics team requires access to the data in milliseconds. However, after 90 days, the company must retain the data for the long term at a lower cost. The retrieval time after 90 days must be less than 5 hours.

Which solution will meet these requirements MOST cost-effectively? "	"	Store the data in S3 Standard-Infrequent Access (S3 Standard-IA) for the first 90 days. Set up an S3 Lifecycle rule to move the data to S3 Glacier Flexible Retrieval after 90 days."
"A company’s application currently uses an IAM role that allows all access to all AWS services. A SysOps administrator must ensure that the company’s IAM policies allow only the permissions that the application requires.

How can the SysOps administrator create a policy to meet this requirement? "	Turn on AWS CloudTrail. Generate a policy by using AWS Identity and Access Management Access Analyzer. 
"A company is deploying a third-party unit testing solution that is delivered as an Amazon EC2 Amazon Machine Image (AMI). All system configuration data is stored in Amazon DynamoDB. The testing results are stored in Amazon S3.

A minimum of three EC2 instances are required to operate the product. The company’s testing team wants to use an additional three EC2 instances when the Spot Instance prices are at a certain threshold. A SysOps administrator must implement a highly available solution that provides this functionality.

Which solution will meet these requirements with the LEAST operational overhead? "	Define an Amazon EC2 Auto Scaling group by using a launch template. Use the provided AMI in the launch template. Configure three On-Demand Instances and three Spot instances. Configure a maximum Spot Instance price in the launch template
"A SysOps administrator creates an AWS CloudFormation template to define an application stack that can be deployed in multiple AWS Regions. The SysOps administrator also creates an Amazon CloudWatch dashboard by using the AWS Management Console. Each deployment of the application requires its own CloudWatch dashboard.

How can the SysOps administrator automate the creation of the CloudWatch dashboard each time the application is deployed? "	"	Export the existing CloudWatch dashboard as JSON. Update the CloudFormation template to define an AWS::CloudWatch::Dashboard resource. Include the exported JSON in the resource’s DashboardBody property"
"A company updates its security policy to clarify cloud hosting arrangements for regulated workloads. Workloads that are identified as sensitive must run on hardware that is not shared with other customers or with other AWS accounts within the company.

Which solution will ensure compliance with this policy? "	"	Deploy workloads only to Dedicated Hosts. "
"A user is measuring the CPU utilization of a private data center machine every minute. The machine provides the aggregate of data every hour, such as Sum of data`, `Min value`, `Max value, and `Number of Data points`.
The user wants to send these values to CloudWatch. How can the user achieve this?"	"	Send the data using the put-metric-data command with the statistic-values parameter "
"A SysOps administrator wants to monitor the free disk space that is available on a set of Amazon EC2 instances that have Amazon Elastic Block Store (Amazon EBS) volumes attached. The SysOps administrator wants to receive a notification when the used disk space of the EBS volumes exceeds a threshold value, but only when the DiskReadOps metric also exceeds a threshold value. The SysOps administrator has set up an Amazon Simple Notification Service (Amazon SNS) topic.

How can the SysOps administrator receive notification only when both metrics exceed their threshold values? "	"	Install the Amazon CloudWatch agent on the EC2 instances. Create a metric alarm for the disk space and a metric alarm for the DiskReadOps metric. Create a composite alarm that includes the two metric alarms to publish a notification to the SNS topic."
"A company updates its security policy to prohibit the public exposure of any data in Amazon S3 buckets in the company's account.

What should a SysOps administrator do to meet this requirement? "	Turn on S3 Block Public Access from the account level.
"A company's SysOps administrator needs to change the AWS Support plan for one of the company's AWS accounts. The account has multi-factor authentication (MFA) activated, and the MFA device is lost.

What should the SysOps administrator do to sign in? "	Sign in as a root user by using email and phone verification. Set up a new MFA device. Change the root user password. 
"A company is creating a new multi-account architecture. A SysOps administrator must implement a login solution to centrally manage user access and permissions across all AWS accounts. The solution must be integrated with AWS Organizations and must be connected to a third-party Security Assertion Markup Language (SAML) 2.0 identity provider (IdP).

What should the SysOps administrator do to meet these requirements? "	Enable and configure AWS Single Sign-On with the third-party IdP
"A company is managing many accounts by using a single organization in AWS Organizations. The organization has all features enabled. The company wants to turn on AWS Config in all the accounts of the organization and in all AWS Regions.

What should a SysOps administrator do to meet these requirements in the MOST operationally efficient way? "	 Use AWS CloudFormation Stack Sets to deploy stack instances that turn on AWS Config in all accounts and in all Regions.
"A SysOps administrator needs to delete an AWS CloudFormation stack that is no longer in use. The CloudFormation stack is in the DELETE_FAILED state. The SysOps administrator has validated the permissions that are required to delete the CloudFormation stack.

Which of the following are possible causes of the DELETE_FAILED state? (Choose two.) "	"	There are additional resources associated with a security group in the stack
There are Amazon S3 buckets that still contain objects in the stack
"
"A SysOps administrator needs to configure a solution that will deliver digital content to a set of authorized users through Amazon CloudFront. Unauthorized users must be restricted from access.

Which solution will meet these requirements? "	"	Store the digital content in an Amazon S3 bucket that has public access blocked. Use an origin access identity (OAI) to deliver the content through CloudFront. Restrict S3 bucket access with signed URLs in CloudFront. "
"A SysOps administrator must ensure that a company's Amazon EC2 instances auto scale as expected. The SysOps administrator configures an Amazon EC2 Auto Scaling lifecycle hook to send an event to Amazon EventBridge (Amazon CloudWatch Events), which then invokes an AWS Lambda function to configure the EC2 instances. When the configuration is complete, the Lambda function calls the complete-lifecycle-action event to put the EC2 instances into service. In testing, the SysOps administrator discovers that the Lambda function is not invoked when the EC2 instances auto scale.

What should the SysOps administrator do to resolve this issue? "	"	Add a permission to the Lambda function so that it can be invoked by the EventBridge (CloudWatch Events) rule."
"A company has mandated the use of multi-factor authentication (MFA) for all IAM users, and requires users to make all API calls using the CLI. However, users are not prompted to enter MFA tokens, and are able to run CLI commands without MFA. In an attempt to enforce MFA, the company attached an IAM policy to all users that denies API calls that have not been authenticated with MFA.

What additional step must be taken to ensure that API calls are authenticated using MFA? "	 Require users to use temporary credentials from the get-session token command to sign API calls. 
"A SysOps administrator is configuring AWS Client VPN to connect users on a corporate network to AWS resources that are running in a VPC. According to compliance requirements, only traffic that is destined for the VPC can travel across the VPN tunnel.

How should the SysOps administrator configure Client VPN to meet these requirements? "	"	On the Client VPN endpoint, turn on the split-tunnel option"
"A web application runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The instances run in an Auto Scaling group across multiple Availability Zones. A SysOps administrator notices that some of these EC2 instances show up as healthy in the Auto Scaling group but show up as unhealthy in the ALB target group.

What is a possible reason for this issue? "	"	The target group health check is configured with an incorrect port or path"
"A SysOps administrator notices a scale up event for an Amazon EC2 Auto Scaling group. Amazon CloudWatch shows a spike in the RequestCount metric for the associated Application Load Balancer. The administrator would like to know the IP addresses for the source of the requests.

Where can the administrator find this information? "	 Elastic Load Balancer access logs 
"A company plans to migrate several of its high performance computing (HPC) virtual machines (VMs) to Amazon EC2 instances on AWS. A SysOps administrator must identify a placement group for this deployment. The strategy must minimize network latency and must maximize network throughput between the HPC VMs.

Which strategy should the SysOps administrator choose to meet these requirements? "	Deploy the instances in a cluster placement group in one Availability Zone. 
"An errant process is known to use an entire processor and run at 100%. A SysOps administrator wants to automate restarting an Amazon EC2 instance when the problem occurs for more than 2 minutes.

How can this be accomplished? "	Create an Amazon CloudWatch alarm for the EC2 instance with detailed monitoring. Add an action to restart the instance
"A company maintains a large set of sensitive data in an Amazon S3 bucket. The company's security team asks a SysOps administrator to help verify that all current objects in the S3 bucket are encrypted.

What is the MOST operationally efficient solution that meets these requirements? "	"	Create an S3 Inventory configuration on the S3 bucket. Include the appropriate status fields. "
"Users are periodically experiencing slow response times from a relational database. The database runs on a burstable Amazon EC2 instance with a 350 GB General Purpose SSD (gp2) Amazon Elastic Block Store (Amazon EBS) volume. A SysOps administrator monitors the EC2 instance in Amazon CloudWatch and observes that the VolumeReadOps metric drops to less than 10% of its peak value during the periods of slow response.

What should the SysOps administrator do to ensure consistently high performance? "	ctivate unlimited mode on the EC2 instance
"A SysOps administrator is optimizing the cost of a workload. The workload is running in multiple AWS Regions and is using AWS Lambda with Amazon EC2 On-Demand Instances for the computer. The overall usage is predictable. The amount of computer that is consumed in each Region varies, depending on the users' locations.

Which approach should the SysOps administrator use to optimize this workload? "	 Purchase Computer Savings Plans based on the usage during the past 30 days
"A software company runs a workload on Amazon EC2 instances behind an Application Load Balancer (ALB). A SysOps administrator needs to define a custom health check for the EC2 instances.

What is the MOST operationally efficient solution? "	"	Configure the health check on the ALB and ensure that the Health Check Path setting is correct."
"A SysOps administrator is required to monitor free space on Amazon EBS volumes attached to Microsoft Windows-based Amazon EC2 instances within a company's account. The administrator must be alerted to potential issues.

What should the administrator do to receive email alerts before low storage space affects EC2 instance performance? "	Use the Amazon CloudWatch agent to send disk space metrics, then set up CloudWatch alarms using an Amazon SNS topic.
"A company applies user-defined tags to resources that are associated with the company's AWS workloads. Twenty days after applying the tags, the company notices that it cannot use the tags to filter views in the AWS Cost Explorer console.

What is the reason for this issue? "	The company has not activated the user-defined tags for cost allocation.
"A company has a critical serverless application that uses multiple AWS Lambda functions. Each Lambda function generates 1 GB of log data daily in its own Amazon CloudWatch Logs log group. The company's security team asks for a count of application errors, grouped by type, across all of the log groups.

What should a SysOps administrator do to meet this requirement? "	"	Perform a CloudWatch Logs Insights query that uses the stats command and count function."
"A company with multiple AWS accounts needs to obtain recommendations for AWS Lambda functions and identify optimal resource configurations for each Lambda function.

How should a SysOps administrator provide these recommendations? "	 Enable AWS Compute Optimizer and export the Lambda function recommendations
"A company uses AWS CloudFormation templates to deploy cloud infrastructure. An analysis of all the company's templates shows that the company has declared the same components in multiple templates. A SysOps administrator needs to create dedicated templates that have their own parameters and conditions for these common components.

Which solution will meet this requirement? "	"	Develop CloudFormation nested stacks."
"A SysOps administrator is building a process for sharing Amazon RDS database snapshots between different accounts associated with different business units within the same company. All data must be encrypted at rest.

How should the administrator implement this process?"	Update the key policy to grant permission to the AWS KMS encryption key used to encrypt the snapshot with all relevant accounts, then share the snapshot with those accounts
"A SysOps administrator configures an Amazon S3 gateway endpoint in a VPC. The private subnets inside the VPC do not have outbound internet access. User logs in to an Amazon EC2 instance in one of the private subnets and cannot upload a file to an Amazon S3 bucket in the same AWS Region.

Which solution will solve this problem? "	Update the S3 bucket policy to allow s3:PutObject access from the private subnet CIDR block
 A user has created an Auto Scaling group using CLI. The user wants to enable CloudWatch detailed monitoring for that group. How can the user configure this?	By default detailed monitoring is enabled for Auto Scaling 
"A SysOps administrator is helping a development team deploy an application to AWS. The AWS CloudFormation template includes an Amazon Linux EC2 instance, an Amazon Aurora DB cluster, and a hardcoded database password that must be rotated every 90 days.

What is the MOST secure way to manage the database password? "	Use the AWS::SecretsManager::Secret resource with the GenerateSecretString property to automatically generate a password. Use the AWS::SecretsManager::RotationSchedule resource to define a rotation schedule for the password. Configure the application to retrieve the secret from AWS Secrets Manager to access the database
"A company's SysOps administrator maintains a highly available environment. The environment includes Amazon EC2 instances and an Amazon RDS Multi-AZ database. The EC2 instances are in an Auto Scaling group behind an Application Load Balancer.

Recently, the company conducted a failover test. The SysOps administrator needs to decrease the failover time of the RDS database by at least 10%.

Which solution will meet this requirement? "	"	Create an RDS proxy. Point the application to the proxy endpoint."
"A company's VPC has connectivity to an on-premises data center through an AWS Site-to-Site VPN. The company needs Amazon EC2 instances in the VPC to send DNS queries for example.com to the DNS servers in the data center.

Which solution will meet these requirements? "	Create an Amazon Route 53 Resolver outbound endpoint. Create a forwarding rule on the resolver that sends all queries for example.com to the on-premises DNS servers. Associate this rule with the VPC.
"A SysOps administrator is tasked with analyzing database performance. The database runs on a single Amazon RDS DB instance. The SysOps administrator finds that, during times of peak traffic, resources on the database are overutilized due to the amount of read traffic.

Which actions should the SysOps administrator take to improve RDS performance? (Choose two.) "	"Add a read replica 
Modify the application to use Amazon ElastiCache for Memcached"
"A company's SysOps administrator has created an Amazon EC2 instance with custom software that will be used as a template for all new EC2 instances across multiple AWS accounts. The Amazon Elastic Block Store (Amazon EBS) volumes that are attached to the EC2 instance are encrypted with AWS managed keys.

The SysOps administrator creates an Amazon Machine Image (AMI) of the custom EC2 instance and plans to share the AMI with the company's other AWS accounts. The company requires that all AMIs are encrypted with AWS Key Management Service (AWS KMS) keys and that only authorized AWS accounts can access the shared AMIs.

Which solution will securely share the AMI with the other AWS accounts? "	In the account where the AMI was created, create a customer managed KMS key. Modify the key policy to provide kms:DescribeKey, kms:ReEncrypt*, kms:CreateGrant, and kms:Decrypt permissions to the AWS accounts that the AMI will be shared with. Create a copy of the AMI, and specify the KMS key. Modify the permissions on the copied AMI to specify the AWS account numbers that the AMI will be shared with.
"A company is migrating its production file server to AWS. All data that is stored on the file server must remain accessible if an Availability Zone becomes unavailable or when system maintenance is performed. Users must be able to interact with the file server through the SMB protocol. Users also must have the ability to manage file permissions by using Windows ACLs.

Which solution will meet these requirements? "	Create an Amazon FSx for Windows File Server Multi-AZ file system.
"A SysOps administrator needs to create alerts that are based on the read and write metrics of Amazon Elastic Block Store (Amazon EBS) volumes that are attached to an Amazon EC2 instance. The SysOps administrator creates and enables Amazon CloudWatch alarms for the DiskReadBytes metric and the DiskWriteBytes metric.

A custom monitoring tool that is installed on the EC2 instance with the same alarm configuration indicates that the volume metrics have exceeded the threshold. However, the CloudWatch alarms were not in ALARM state.

Which action will ensure that the CloudWatch alarms function correctly?"	Reconfigure the CloudWatch alarms to use the VolumeReadBytes metric and the VolumeWriteBytes metric for the EBS volumes
"A company recently moved its server infrastructure to Amazon EC2 instances. The company wants to use Amazon CloudWatch metrics to track instance memory utilization and available disk space.

What should a SysOps administrator do to meet these requirements? "	"	Install and configure the CloudWatch agent on all the instances. Attach an IAM role to allow the instances to write logs to CloudWatch"
"A company recently deployed MySQL on an Amazon EC2 instance with a default boot volume. The company intends to restore a 1.75 TB database. A SysOps administrator needs to provision the correct Amazon Elastic Block Store (Amazon EBS) volume. The database will require read performance of up to 10,000 IOPS and is not expected to grow in size.

Which solution will provide the required performance at the LOWEST cost? "	Deploy a 2 TB General Purpose SSD (gp3) volume. Set the IOPS to 10,000. 
"A SysOps administrator is setting up a fleet of Amazon EC2 instances in an Auto Scaling group for an application. The fleet should have 50% CPU available at all times to accommodate bursts of traffic. The load will increase significantly between the hours of 09:00 and 17:00, 7 days a week.

How should the SysOps administrator configure the scaling of the EC2 instances to meet these requirements? "	Create a target tracking scaling policy that runs when the CPU utilization is higher than 50%. Create a scheduled scaling policy that ensures that the fleet is available at 09:00. Create a second scheduled scaling policy that scales in the fleet at 17:00.
"A company is running Amazon EC2 On-Demand Instances in an Auto Scaling group. The instances process messages from an Amazon Simple Queue Service (Amazon SQS) queue. The Auto Scaling group is set to scale based on the number of messages in the queue. Messages can take up to 12 hours to process completely. A SysOps administrator must ensure that instances are not interrupted during message processing.

What should the SysOps administrator do to meet these requirements? "	Enable instance scale-in protection for the specific instance in the Auto Scaling group at the start of message processing by calling the Amazon EC2 Auto Scaling API from the processing script. Disable instance scale-in protection after message processing is complete by calling the Amazon EC2 Auto Scaling API from the processing script
An organization is trying to create various IAM users. Which of the below mentioned options is not a valid IAM username?	john#cloud 
"A company is developing a mobile shopping web app. The company needs an environment that is configured to encrypt all resources in transit and at rest.
A security engineer must develop a solution that will encrypt traffic in transit to the company's Application Load Balancer and Amazon API Gateway resources.
The solution also must encrypt traffic at rest for Amazon S3 storage.
What should the security engineer do to meet these requirements?"	Use AWS Certificate Manager (ACM) for encryption in transit. Use AWS Key Management Service for encryption at rest. 
"A SysOps administrator needs to collect the content of log files from a custom application that is deployed across hundreds of Amazon EC2 instances running Ubuntu. The log files need to be stored in Amazon CloudWatch Logs.

How should the SysOps administrator collect the application log files with the LOWEST operational overhead? "	Store a CloudWatch agent configuration in the AWS Systems Manager Parameter Store. Install the CloudWatch agent on each EC2 instance by using Systems Manager. Configure each agent to collect the application log files.
A user wants to upload a complete folder to AWS S3 using the S3 Management console. How can the user perform this activity?	 Use the Enable Enhanced Uploader option from the S3 console while uploading objects 
"A SysOps administrator is creating a simple, public-facing website running on Amazon EC2. The SysOps administrator created the EC2 instance in an existing public subnet and assigned an Elastic IP address to the instance. Next, the SysOps administrator created and applied a new security group to the instance to allow incoming HTTP traffic from 0.0.0.0/0. Finally, the SysOps administrator created a new network ACL and applied it to the subnet to allow incoming HTTP traffic from 0.0.0.0/0. However, the website cannot be reached from the internet.

What is the cause of this issue? "	"	The SysOps administrator did not create an outbound rule that allows ephemeral port return traffic in the new network ACL."
"A company has an application that uses an Amazon Elastic File System (Amazon EFS) file system. A recent incident that involved an application logic error corrupted several files. The company wants to improve its ability to back up and recover the EFS file system. The company must be able to recover individual files rapidly.

Which solution meets these requirements MOST cost-effectively? "	Enable AWS Backup in Amazon EFS to back up the file system to a backup vault. Use a partial restore job to retrieve individual files. 
"A company needs to view a list of security groups that are open to the internet on port 3389.

What should a SysOps administrator do to meet this requirement? "	"	Use AWS Trusted Advisor to find security groups that allow unrestricted access on port 3389."
"A company website contains a web tier and a database tier on AWS. The web tier consists of Amazon EC2 instances that run in an Auto Scaling group across two Availability Zones. The database tier runs on an Amazon RDS for MySQL Multi-AZ DB instance. The database subnet network ACLs are restricted to only the web subnets that need access to the database. The web subnets use the default network ACL with the default rules.

The company's operations team has added a third subnet to the Auto Scaling group configuration. After an Auto Scaling event occurs, some users report that they intermittently receive an error message. The error message states that the server cannot connect to the database. The operations team has confirmed that the route tables are correct and that the required ports are open on all security groups.

Which combination of actions should a SysOps administrator take so that the web servers can communicate with the DB instance? (Choose two.) "	"On the network ACLs for the database subnets, create an inbound Allow rule of type MySQL/Aurora (3306). Specify the source as the third web subnet. 
On the network ACLs for the database subnets, create an outbound Allow rule of type TCP with the ephemeral port range and the destination as the third web subnet."
"A SysOps administrator has been able to consolidate multiple, secure websites onto a single server, and each site is running on a different port. The administrator now wants to start a duplicate server in a second Availability Zone and put both behind a load balancer for high availability.

What would be the command line necessary to deploy one of the sites’ certificates to the load balancer? "	aws elb set-load-balancer-listener-ssl-certificate --load-balancer-name my-load-balancer –-load-balancer-port 443 –-ssl-certificate-id arn:aws:iam::123456789012:server-certificate/new-server-cert 
 A user is creating a Cloudformation stack. Which of the below mentioned limitations does not hold true for Cloudformation?	One account by default is limited to 100 templates 
"An AWS CloudFormation template creates an Amazon RDS instance. This template is used to build up development environments as needed and then delete the stack when the environment is no longer required. The RDS-persisted data must be retained for further use, even after the CloudFormation stack is deleted.

How can this be achieved in a reliable and efficient way? "	Use the Snapshot Deletion Policy in the CloudFormation template definition of the RDS instance
"An organization has created a Queue named `modularqueue` with SQS. The organization is not performing any operations such as SendMessage,
ReceiveMessage, DeleteMessage, GetQueueAttributes, SetQueueAttributes, AddPermission, and RemovePermission on the queue. What can happen in this scenario?"	AWS SQS can delete queue after 30 days without notification 
"A company uses Amazon S3 to aggregate raw video footage from various media teams across the US. The company recently expanded into new geographies in Europe and Australia. The technical teams located in Europe and Australia reported delays when uploading large video files into the destination S3 bucket in the United States.

What are the MOST cost effective ways to increase upload speeds into the S3 bucket? (Choose two.) "	" Use Amazon S3 Transfer Acceleration for file uploads into the destination S3 bucket
Use multipart uploads for file uploads into the destination S3 bucket from the branch offices in Europe and Australia."
"A SysOps administrator needs to provision a new fleet of Amazon EC2 Spot Instances in an Amazon EC2 Auto Scaling group. The Auto Scaling group will use a wide range of instance types. The configured fleet must come from pools that have the most availability for the number of instances that are launched.

Which solution will meet these requirements"	"	Launch the Spot Instances by using the capacity optimized strategy"
"A SysOps administrator creates a custom Amazon Machine Image (AMI) in the eu-west-2 Region and uses the AMI to launch Amazon EC2 instances. The SysOps administrator needs to use the same AMI to launch EC2 instances in two other Regions: us-east-1 and us-east-2.

What must the SysOps administrator do to use the custom AMI in the additional Regions"	Copy the AMI to the additional Regions.
"A company has many accounts in an organization in AWS Organizations. The company must automate resource provisioning from the organization’s management account to the member accounts.

Which solution will meet this requirement? "	Create an AWS CloudFormation stack set. Deploy the stack set to all member accounts
"A company is building an interactive application for personal finance. The application stores financial data in Amazon S3, and the data must be encrypted. The company does not want to provide its own encryption keys. However, the company wants to maintain an audit trail that shows when an encryption key was used and who used the key.

Which solution will meet these requirements? "	Use server-side encryption with AWS KMS managed encryption keys (SSE-KMS) to encrypt the user data on Amazon S3. 
"A company has an AWS CloudFormation template that creates an Amazon S3 bucket. A user authenticates to the corporate AWS account with their Active Directory credentials and attempts to deploy the CloudFormation template. However, the stack creation fails.

Which factors could cause this failure? (Choose two.) "	"The user’s IAM policy does not allow the cloudformation:CreateStack action. 
The user’s IAM policy does not allow the s3:CreateBucket action."
"An Amazon RDS for PostgreSQL DB cluster has automated backups turned on with a 7-day retention period. A SysOps administrator needs to create a new RDS DB cluster by using data that is no more than 24 hours old from the original DB cluster.

Which solutions will meet these requirements with the LEAST operational overhead? (Choose two.) "	"	Identify the most recent automated snapshot. Restore the snapshot to a new RDS DB cluster
Create a read replica instance in the original RDS DB cluster. Promote the read replica to a standalone DB cluster."
"A company is managing a website with a global user base hosted on Amazon EC2 with an Application Load Balancer (ALB). To reduce the load on the web servers, a SysOps administrator configures an Amazon CloudFront distribution with the ALB as the origin. After a week of monitoring the solution, the administrator notices that requests are still being served by the ALB and there is no change in the web server load.

What are possible causes for this problem? (Choose two.) "	"The DNS is still pointing to the ALB instead of the CloudFront distribution.
The default, minimum, and maximum Time to Live (TTL) are set to 0 seconds on the CloudFront distribution."
"A SysOps administrator needs to configure the Amazon Route 53 hosted zone for example.com and www.example.com to point to an Application Load Balancer (ALB).

Which combination of actions should the SysOps administrator take to meet these requirements? (Choose two.) "	"Configure an alias record for example.com to point to the CNAME of the ALB.
Configure an alias record for www.example.com to point to the Route 53 example.com record"
"A company has a hybrid environment. The company has set up an AWS Direct Connect connection between the company's on-premises data center and a workload that runs in a VPC. The company uses Amazon Route 53 for DNS on AWS. The company uses a private hosted zone to manage DNS names for a set of services that are hosted on AWS.

The company wants the on-premises servers to use Route 53 for DNS resolution of the private hosted zone.

Which solution will meet these requirements? "	"	Create a Route 53 inbound endpoint. Ensure that security groups and routing allow the traffic from the on-premises data center. Configure the DNS server on the on-premises network to conditionally forward DNS queries for the private hosted zone's domain name to the IP addresses of the inbound endpoint."
"A SysOps administrator is evaluating Amazon Route 53 DNS options to address concerns about high availability for an on-premises website. The website consists of two servers: a primary active server and a secondary passive server. Route 53 should route traffic to the primary server if the associated health check returns 2xx or 3xx HTTP codes. All other traffic should be directed to the secondary passive server. The failover record type, set ID, and routing policy have been set appropriately for both primary and secondary servers.

Which next step should be taken to configure Route 53?"	Create an A record for each server. Associate the records with the Route 53 HTTP health check.
"A company is building a web application on AWS. The company is using Amazon CloudFront with a domain name of www.example.com. All traffic to CloudFront must be encrypted in transit. The company already has provisioned an SSL certificate for www.example.com in AWS Certificate Manager (ACM).

Which combination of steps should a SysOps administrator take to encrypt the traffic in transit? (Choose two.) "	" For each cache behavior in the CloudFront distribution, modify the Viewer Protocol Policy setting to redirect HTTP to HTTPS. 
nter the alternate domain name (CNAME) of www.example.com for the CloudFront distribution. Select the custom SSL certificate. "
"A company runs an application on hundreds of Amazon EC2 instances in three Availability Zones. The application calls a third-party API over the public internet. A SysOps administrator must provide the third party with a list of static IP addresses so that the third party can allow traffic from the application.

Which solution will meet these requirements? "	Add a NAT gateway in the public subnet of each Availability Zone. Make the NAT gateway the default route of all private subnets in those Availability Zones.
"A company manages its multi-account environment by using AWS Organizations. The company needs to automate the creation of daily incremental backups of any Amazon Elastic Block Store (Amazon EBS) volume that is marked with a Lifecycle: Production tag in one of its primary AWS accounts.

The company wants to prevent users from using Amazon EC2 * permissions to delete any of these production snapshots.

What should a SysOps administrator do to meet these requirements? "	Associate a service control policy (SCP) with the account to deny users the ability to delete EBS snapshots. Create an Amazon EventBridge rule with a 24-hour cron schedule. Configure EBS Create Snapshot as the target. Target all EBS volumes with the specified tags
"A company hosts a Windows-based file server on a fleet of Amazon EC2 instances across multiple Availability Zones. The current setup does not allow application servers to access files simultaneously from the EC2 fleet.

Which solution will allow this access in the MOST operationally efficient way? "	"	Create an Amazon FSx for Windows File Server Multi-AZ file system. Copy the files to the Amazon FSx file system. Adjust the connections from the application servers to use the share that the Amazon FSx file system exposes."
"A company has deployed an application on Amazon EC2 instances in a single VPC. The company has placed the EC2 instances in a private subnet in the VPC.

The EC2 instances need access to Amazon S3 buckets that are in the same AWS Region as the EC2 instances. A SysOps administrator must provide the EC2 instances with access to the S3 buckets without requiring any changes to the EC2 instances or the application. The EC2 instances must not have access to the internet.

Which solution will meet these requirements? "	 Create an S3 gateway endpoint that uses the default gateway endpoint policy. Associate the private subnet with the gateway endpoint.
"A company has a public web application that experiences rapid traffic increases after advertisements appear on local television. The application runs on Amazon EC2 instances that are in an Auto Scaling group. The Auto Scaling group is not keeping up with the traffic surges after an advertisement runs. The company often needs to scale out to 100 EC2 instances during the traffic surges.

The instance startup times are lengthy because of a boot process that creates machine-specific data caches that are unique to each instance. The exact timing of when the advertisements will appear on television is not known. A SysOps administrator must implement a solution so that the application can function properly during the traffic surges.

Which solution will meet these requirements? "	Create e warm pool. Keep enough instances in the Stopped state to meet the increased demand.
"A company hosts an internal application on Amazon EC2 On-Demand Instances behind an Application Load Balancer (ALB). The instances are in an Amazon EC2 Auto Scaling group. Employees use the application to provide product prices to potential customers. The Auto Scaling group is configured with a dynamic scaling policy and tracks average CPU utilization of the instances.

Employees have noticed that sometimes the application becomes slow or unresponsive. A SysOps administrator finds that some instances are experiencing a high CPU load. The Auto Scaling group cannot scale out because the company is reaching the EC2 instance service quota.

The SysOps administrator needs to implement a solution that provides a notification when the company reaches 70% or more of the EC2 instance service quota.

Which solution will meet these requirements in the MOST operationally efficient manner? "	"	Use the Service Quotas console to create an Amazon CloudWatch alarm for the EC2 instances. Configure the alarm with quota utilization equal to or greater than 70%. Configure the alarm to publish an Amazon Simple Notification Service (Amazon SNS) notification when the alarm enters ALARM state."
"A company has a policy that all Amazon EC2 instance logs must be published to Amazon CloudWatch Logs. A SysOps administrator is troubleshooting an EC2 instance that is running Amazon Linux 2. The EC2 instance is not publishing logs to CloudWatch Logs. The Amazon CloudWatch agent is running on the EC2 instance, and the agent configuration file is correct.

What should the SysOps administrator do to resolve the issue? "	Ensure that the IAM role that is attached to the EC2 instance has permissions in CloudWatch Logs for the CreateLogGroup, CreateLogStream, PutLogEvents, and DescribeLogStreams actions. 
"A company runs a workload on an Amazon EC2 instance. The workload needs a temporary cache that contains data that changes frequently. The workload does not need to retain the cache across instance restarts.

Which storage option will provide the HIGHEST performance for the cache? "	EC2 instance store
"A company runs multiple workloads across an organization in AWS Organizations. The company's finance team needs detailed dashboards to track cost changes and provide detailed cost metrics. The finance team needs to track trends as granular as every hour.

What should a SysOps administrator do to meet these requirements in the MOST operationally efficient way? "	Generate an AWS Cost and Usage Report. Store the report in Amazon S3. Use Amazon Athena to query the data. Use Amazon QuickSight to develop dashbosrds based on the data in the AWS Cost and Usage Report. 
"A company has a core application that must run 24 hours a day, 7 days a week. The application uses Amazon EC2. AWS Fargate, and AWS Lambda. The company uses a combination of operating systems across different AWS Regions.

The company needs to maximize cost savings while committing to a pricing model that offers flexibility to make changes.

What should the company do to meet these requirements? "	Purchase a Compute Savings Plan that is based on Savings Plans recommendations
"A company’s architecture team must receive immediate email notification whenever new Amazon EC2 instances are launched in the company's main AWS production account.

‘What should a SysOps administrator do to meet this requirement? "	"	Create an Amazon Simple Notification Service (Amazon SNS) topic and a subscription that uses the email protocol. Enter the architecture team's email address as the subscriber. Create an Amazon EventBridge rule that reacts when EC2 instances are launched. Specify the SNS topic as the rule's target."
"A SysOps administrator needs to update an AWS account name.

What should the SysOps administrator do to accomplish this goal? "	"	Sign in as the AWS account root user to make the change."
"A team of developers is using several Amazon S3 buckets as centralized repositories. Users across the world upload large sets of files to these repositories. The development team's applications later process these files.

A SysOps administrator sets up a new S3 bucket, DOC-EXAMPLE-BUCKET, to support a new workload, The rew S3 bucket also receives regular uploads cf large sets of files from users worldwide. When the new S3 bucket is put into production, the upload performance from certain geographic areas is lower than the upload performance that the existing $3 buckets provide

What should the SysOps administrator do to remediate this issue? "	

"	Enable S3 Transfer Acceleration for the new S3 bucket. Verify that the developers are using the DOC-EXAMPLE-BUCKET.s3-accelerate.amazonaws.com endpoint name in their API calls"

"A user has launched a Windows based EC2 instance. However, the instance has some issues and the user wants to check the log. When the user checks the
Instance console output from the AWS console, what will it display?"	

The last three system events' log errors 

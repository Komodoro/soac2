---
sectionid: ExamTopicsDump
sectionclass: h2
parent-id: Questions
title: ExamTopics
number: 2200
---

September 6, 2023
What Changed with AWS Certified SysOps Administrator – Associate SOA-C02 Exam?

AWS Certified SysOps Administrator – Associate SOA-C02 exam is a great Amazon certification exam that helps organizations identify and develop talent with critical skills for implementing cloud initiatives. As of March 28, 2023, the exam format has been updated, and it will not include exam labs until further notice. Currently, the exam consists of two types of questions: Multiple choices and Multiple responses. The updated SOA-C02 exam dumps are an excellent resource for preparing for the exam. They provide you with the opportunity to practice with actual questions and answers, which can help you identify your strengths and weaknesses. Moreover, they can help you build your confidence and reduce test anxiety, which can improve your performance on the exam.
AWS Certified SysOps Administrator – Associate SOA-C02 Exam Free Dumps
 

Congratulations - you have completed this exam.

Your answers are shown below:

1. A Sysops administrator creates an Amazon Elastic Kubernetes Service (Amazon EKS) cluster that uses AWS Fargate. The cluster is deployed successfully. The Sysops administrator needs to manage the cluster by using the kubect1 command line tool.

Which of the following must be configured on the Sysops administrator's machine so that kubect1 can communicate with the cluster API server?

    The kubeconfig filecorrect
    The kube-proxy Amazon EKS add-on
    The Fargate profile
    The eks-connector.yaml file

Question was not answered
Explanation:

The kubeconfig file is a configuration file used to store cluster authentication information, which is required to make requests to the Amazon EKS cluster API server. The kubeconfig file will need to be configured on the SysOps administrator's machine in order for kubectl to be able to communicate with the cluster API server.

https://aws.amazon.com/blogs/developer/running-a-kubernetes-job-in-amazon-eks-on-aws-fargate-using-aws-stepfunctions/
2. A Sysops administrator needs to configure automatic rotation for Amazon RDS database credentials.

The credentials must rotate every 30 days. The solution must integrate with Amazon RDS.

Which solution will meet these requirements with the LEAST operational overhead?

    Store the credentials in AWS Systems Manager Parameter Store as a secure string. Configure automatic rotation with a rotation interval of 30 days.
    Store the credentials in AWS Secrets Manager. Configure automatic rotation with a rotation interval of 30 days.correct
    Store the credentials in a file in an Amazon S3 bucket. Deploy an AWS Lambda function to automatically rotate the credentials every 30 days.
    Store the credentials in AWS Secrets Manager. Deploy an AWS Lambda function to automatically rotate the credentials every 30 days.

Question was not answered
Explanation:

Storing the credentials in AWS Secrets Manager and configuring automatic rotation with a rotation interval of 30 days is the most efficient way to meet the requirements with the least operational overhead. AWS Secrets Manager automatically rotates the credentials at the specified interval, so there is no need for an additional AWS Lambda function or manual rotation. Additionally, Secrets Manager is integrated with Amazon RDS, so the credentials can be easily used with the RDS database.
3. A company has an application that runs only on Amazon EC2 Spot Instances. The instances run in an Amazon EC2 Auto Scaling group with scheduled scaling actions.

However, the capacity does not always increase at the scheduled times, and instances terminate many times a day. A Sysops administrator must ensure that the instances launch on time and have fewer interruptions.

Which action will meet these requirements?

    Specify the capacity-optimized allocation strategy for Spot Instances. Add more instance types to the Auto Scaling group.correct
    Specify the capacity-optimized allocation strategy for Spot Instances. Increase the size of the instances in the Auto Scaling group.
    Specify the lowest-price allocation strategy for Spot Instances. Add more instance types to the Auto Scaling group.
    Specify the lowest-price allocation strategy for Spot Instances. Increase the size of the instances in the Auto Scaling group.

Question was not answered
Explanation:

Specifying the capacity-optimized allocation strategy for Spot Instances and adding more instance types to the Auto Scaling group is the best action to meet the requirements. Increasing the size of the instances in the Auto Scaling group will not necessarily help with the launch time or reduce interruptions, as the Spot Instances could still be interrupted even with larger instance sizes.
4. A company stores its data in an Amazon S3 bucket. The company is required to classify the data and find any sensitive personal information in its S3 files.

Which solution will meet these requirements?

    Create an AWS Config rule to discover sensitive personal information in the S3 files and mark them as noncompliant.
    Create an S3 event-driven artificial intelligence/machine learning (AI/ML) pipeline to classify sensitive personal information by using Amazon Recognition.
    Enable Amazon GuardDuty. Configure S3 protection to monitor all data inside Amazon S3.
    Enable Amazon Macie. Create a discovery job that uses the managed data identifier.correct

Question was not answered
Explanation:

Amazon Macie is a security service designed to help organizations find, classify, and protect sensitive data stored in Amazon S3. Amazon Macie uses machine learning to automatically discover, classify, and protect sensitive data in Amazon S3. Creating a discovery job with the managed data identifier will allow Macie to identify sensitive personal information in the S3 files and classify it accordingly. Enabling AWS Config and Amazon GuardDuty will not help with this requirement as they are not designed to automatically classify and protect data.
5. A company has an application that customers use to search for records on a website. The application's data is stored in an Amazon Aurora DB cluster. The application's usage varies by season and by day of the week.

The website's popularity is increasing, and the website is experiencing slower performance because of increased load on the DB cluster during periods of peak activity. The application logs show that the performance issues occur when users are searching for information. The same search is rarely performed multiple times.

A SysOps administrator must improve the performance of the platform by using a solution that maximizes resource efficiency.

Which solution will meet these requirements?

    Deploy an Amazon ElastiCache for Redis cluster in front of the DB cluster. Modify the application to check the cache before the application issues new queries to the database. Add the results of any queries to the cache.
    Deploy an Aurora Replica for the DB cluster. Modify the application to use the reader endpoint for search operations. Use Aurora Auto Scaling to scale the number of replicas based on load. Most Votedcorrect
    Use Provisioned IOPS on the storage volumes that support the DB cluster to improve performance sufficiently to support the peak load on the application.
    Increase the instance size in the DB cluster to a size that is sufficient to support the peak load on the application. Use Aurora Auto Scaling to scale the instance size based on load.

Question was not answered
Explanation:

https://docs.amazonaws.cn/en_us/AmazonRDS/latest/AuroraUserGuide/aurora-replicas-adding.html
6. The security team is concerned because the number of AWS Identity and Access Management (IAM) policies being used in the environment is increasing. The team tasked a SysOps administrator to report on the current number of IAM policies in use and the total available IAM policies.

Which AWS service should the administrator use to check how current IAM policy usage compares to current service limits?

    AWS Trusted Advisorcorrect
    Amazon Inspector
    AWS Config
    AWS Organizations

Question was not answered
7. A company has a stateless application that is hosted on a fleet of 10 Amazon EC2 On-Demand Instances in an Auto Scaling group. A minimum of 6 instances are needed to meet service requirements.

Which action will maintain uptime for the application MOST cost-effectively?

    Use a Spot Fleet with an On-Demand capacity of 6 instances.correct
    Update the Auto Scaling group with a minimum of 6 On-Demand Instances and a maximum of 10 On-Demand Instances.
    Update the Auto Scaling group with a minimum of 1 On-Demand Instance and a maximum of 6 On-Demand Instances.
    Use a Spot Fleet with a target capacity of 6 instances.

Question was not answered
8. A SysOps administrator has launched a large general purpose Amazon EC2 instance to regularly process large data files. The instance has an attached 1 TB General Purpose SSD (gp2) Amazon Elastic Block Store (Amazon EBS) volume. The instance also is EBS-optimized. To save costs, the SysOps administrator stops the instance each evening and restarts the instance each morning.

When data processing is active, Amazon CloudWatch metrics on the instance show a consistent 3.000 VolumeReadOps. The SysOps administrator must improve the I/O performance while ensuring data integrity.

Which action will meet these requirements?

    Change the instance type to a large, burstable, general purpose instance.
    Change the instance type to an extra large general purpose instance.
    Increase the EBS volume to a 2 TB General Purpose SSD (gp2) volume.correct
    Move the data that resides on the EBS volume to the instance store.

Question was not answered
9. With the threat of ransomware viruses encrypting and holding company data hostage, which action should be taken to protect an Amazon S3 bucket?

    Deny Post. Put. and Delete on the bucket.
    Enable server-side encryption on the bucket.correct
    Enable Amazon S3 versioning on the bucket.
    Enable snapshots on the bucket.

Question was not answered
10. A SysOps administrator is evaluating Amazon Route 53 DNS options to address concerns about high availability for an on-premises website. The website consists of two servers: a primary active server and a secondary passive server. Route 53 should route traffic to the primary server if the associated health check returns 2xx or 3xx HTTP codes. All other traffic should be directed to the secondary passive server. The failover record type, set ID. and routing policy have been set appropriately for both primary and secondary servers.

Which next step should be taken to configure Route 53?

    Create an A record for each server. Associate the records with the Route 53 HTTP health check.correct
    Create an A record for each server. Associate the records with the Route 53 TCP health check.
    Create an alias record for each server with evaluate target health set to yes. Associate the records with the Route 53 HTTP health check.
    Create an alias record for each server with evaluate target health set to yes. Associate the records with the Route 53 TCP health check.

Question was not answered
11. A SysOps administrator noticed that a large number of Elastic IP addresses are being created on the company's AWS account, but they are not being associated with Amazon EC2 instances, and are incurring Elastic IP address charges in the monthly bill.

How can the administrator identify who is creating the Elastic IP addresses?

    Attach a cost-allocation tag to each requested Elastic IP address with the IAM user name of the developer who creates it.
    Query AWS CloudTrail logs by using Amazon Athena to search for Elastic IP address events.correct
    Create a CloudWatch alarm on the ElPCreated metric and send an Amazon SNS notification when the alarm triggers.
    Use Amazon Inspector to get a report of all Elastic IP addresses created in the last 30 days.

Question was not answered
12. A company has an Amazon CloudFront distribution that uses an Amazon S3 bucket as its origin. During a review of the access logs, the company determines that some requests are going directly to the S3 bucket by using the website hosting endpoint. A SysOps administrator must secure the S3 bucket to allow requests only from CloudFront.

What should the SysOps administrator do to meet this requirement?

    Create an origin access identity (OAI) in CloudFront. Associate the OAI with the distribution. Remove access to and from other principals in the S3 bucket policy. Update the S3 bucket policy to allow access only from the OAcorrect
    Create an origin access identity (OAI) in CloudFront. Associate the OAI with the distribution. Update the S3 bucket policy to allow access only from the OA
    Create a new origin, and specify the S3 bucket as the new origin. Update the distribution behavior to use the new origin. Remove the existing origin.
    Create an origin access identity (OAI) in CloudFront. Associate the OAI with the distribution. Update the S3 bucket policy to allow access only from the OA
    Disable website hosting. Create a new origin, and specify the S3 bucket as the new origin. Update the distribution behavior to use the new origin. Remove the existing origin.
    Update the S3 bucket policy to allow access only from the CloudFront distribution. Remove access to and from other principals in the S3 bucket policy. Disable website hosting. Create a new origin, and specify the S3 bucket as the new origin. Update the distribution behavior to use the new origin. Remove the existing origin.

Question was not answered
13. A SysOps administrator must create an IAM policy for a developer who needs access to specific AWS services.

Based on the requirements, the SysOps administrator creates the following policy:

Which actions does this policy allow? (Select TWO.)

    Create an AWS Storage Gateway.correct
    Create an IAM role for an AWS Lambda function.
    Delete an Amazon Simple Queue Service (Amazon SQS) queue.
    Describe AWS load balancers.correct
    Invoke an AWS Lambda function.correct

Question was not answered
14. A company is trying to connect two applications. One application runs in an on-premises data center that has a hostname of hostl .onprem.private. The other application runs on an Amazon EC2 instance that has a hostname of hostl.awscloud.private. An AWS Site-to-Site VPN connection is in place between the on-premises network and AWS.

The application that runs in the data center tries to connect to the application that runs on the EC2

instance, but DNS resolution fails. A SysOps administrator must implement DNS resolution between on-premises and AWS resources.

Which solution allows the on-premises application to resolve the EC2 instance hostname?

    Set up an Amazon Route 53 inbound resolver endpoint with a forwarding rule for the onprem.private hosted zone. Associate the resolver with the VPC of the EC2 instance. Configure the on-premises DNS resolver to forward onprem.private DNS queries to the inbound resolver endpoint.
    Set up an Amazon Route 53 inbound resolver endpoint. Associate the resolver with the VPC of the EC2 instance. Configure the on-premises DNS resolver to forward awscloud.private DNS queries to the inbound resolver endpoint.
    Set up an Amazon Route 53 outbound resolver endpoint with a forwarding rule for the onprem.private hosted zone. Associate the resolver with the AWS Region of the EC2 instance. Configure the on-premises DNS resolver to forward onprem.private DNS queries to the outbound resolver endpoint.correct
    Set up an Amazon Route 53 outbound resolver endpoint. Associate the resolver with the AWS Region of the EC2 instance. Configure the on-premises DNS resolver to forward awscloud.private DNS queries to the outbound resolver endpoint.

Question was not answered
15. While setting up an AWS managed VPN connection, a SysOps administrator creates a customer gateway resource in AWS. The customer gateway device resides in a data center with a NAT gateway in front of it.

What address should be used to create the customer gateway resource?

    The private IP address of the customer gateway device
    The MAC address of the NAT device in front of the customer gateway device
    The public IP address of the customer gateway device
    The public IP address of the NAT device in front of the customer gateway devicecorrect

Question was not answered
16. A large company is using AWS Organizations to manage its multi-account AWS environment. According to company policy, all users should have read-level access to a particular Amazon S3 bucket in a central account. The S3 bucket data should not be available outside the organization. A SysOps administrator must set up the permissions and add a bucket policy to the S3 bucket.

Which parameters should be specified to accomplish this in the MOST efficient manner?

    Specify "' as the principal and PrincipalOrgld as a condition.correct
    Specify all account numbers as the principal.
    Specify PrincipalOrgld as the principal.
    Specify the organization's management account as the principal.

Question was not answered
Explanation:

https://aws.amazon.com/blogs/security/control-access-to-aws-resources-by-using-the-aws-organization-of-iam-principals/
17. A SysOps administrator is attempting to download patches from the internet into an instance in a private subnet. An internet gateway exists for the VPC, and a NAT gateway has been deployed on the public subnet; however, the instance has no internet connectivity.

The resources deployed into the private subnet must be inaccessible directly from the public internet.

What should be added to the private subnet's route table in order to address this issue, given the information provided?

    0.0.0.0/0 IGW
    0.0.0.0/0 NATcorrect
    10.0.1.0/24 IGW
    10.0.1.0/24 NAT

Question was not answered
18. A SysOps administrator applies the following policy to an AWS CloudFormation stack:

What is the result of this policy?

    Users that assume an IAM role with a logical ID that begins with "Production" are prevented from running the update-stack command.
    Users can update all resources in the stack except for resources that have a logical ID that begins with "Production".correct
    Users can update all resources in the stack except for resources that have an attribute that begins with "Production".
    Users in an IAM group with a logical ID that begins with "Production" are prevented from running the update-stack command.

Question was not answered
19. A company's IT department noticed an increase in the spend of their developer AWS account. There are over 50 developers using the account, and the finance team wants to determine the service costs incurred by each developer.

What should a SysOps administrator do to collect this information? (Select TWO.)

    Activate the createdBy tag in the account.correct
    Analyze the usage with Amazon CloudWatch dashboards.
    Analyze the usage with Cost Explorer.correct
    Configure AWS Trusted Advisor to track resource usage.
    Create a billing alarm in AWS Budgets.

Question was not answered
20. A company website contains a web tier and a database tier on AWS. The web tier consists of Amazon EC2 instances that run in an Auto Scaling group across two Availability Zones. The database tier runs on an Amazon ROS for MySQL Multi-AZ DB instance. The database subnet network ACLs are restricted to only the web subnets that need access to the database. The web subnets use the default network ACL with the default rules.

The company's operations team has added a third subnet to the Auto Scaling group configuration. After an Auto Scaling event occurs, some users report that they intermittently receive an error message. The error message states that the server cannot connect to the database. The operations team has confirmed that the route tables are correct and that the required ports are open on all security groups.

Which combination of actions should a SysOps administrator take so that the web servers can communicate with the DB instance? (Select TWO.)

    On the default ACcorrect
    create inbound Allow rules of type TCP with the ephemeral port range and the source as the database subnets.
    On the default ACL, create outbound Allow rules of type MySQL/Aurora (3306). Specify the destinations as the database subnets.correct
    On the network ACLs for the database subnets, create an inbound Allow rule of type MySQL/Aurora (3306). Specify the source as the third web subnet.correct
    On the network ACLs for the database subnets, create an outbound Allow rule of type TCP with the ephemeral port range and the destination as the third web subnet.
    On the network ACLs for the database subnets, create an outbound Allow rule of type MySQL/Aurora (3306). Specify the destination as the third web subnet.

Question was not answered
21. A company is running an application on a fleet of Amazon EC2 instances behind an Application Load Balancer (ALB). The EC2 instances are launched by an Auto Scaling group and are automatically registered in a target group. A SysOps administrator must set up a notification to alert application owners when targets fail health checks.

What should the SysOps administrator do to meet these requirements?

    Create an Amazon CloudWatch alarm on the UnHealthyHostCount metric. Configure an action to send an Amazon Simple Notification Service (Amazon SNS) notification when the metric is greater than 0.correct
    Configure an Amazon EC2 Auto Scaling custom lifecycle action to send an Amazon Simple Notification Service (Amazon SNS) notification when an instance is in the Pending:Wait state.
    Update the Auto Scaling group. Configure an activity notification to send an Amazon Simple Notification Service (Amazon SNS) notification for the Unhealthy event type.
    Update the ALB health check to send an Amazon Simple Notification Service (Amazon SNS) notification when an instance is unhealthy.

Question was not answered
22. A company wants to build a solution for its business-critical Amazon RDS for MySQL database. The database requires high availability across different geographic locations. A SysOps administrator must build a solution to handle a disaster recovery (DR) scenario with the lowest recovery time objective

(RTO) and recovery point objective (RPO).

Which solution meets these requirements?

    Create automated snapshots of the database on a schedule. Copy the snapshots to the DR Region.
    Create a cross-Region read replica for the database.correct
    Create a Multi-AZ read replica for the database.
    Schedule AWS Lambda functions to create snapshots of the source database and to copy the snapshots to a DR Region.

Question was not answered
23. A SysOps administrator is using Amazon EC2 instances to host an application. The SysOps administrator needs to grant permissions for the application to access an Amazon DynamoDB table.

Which solution will meet this requirement?

    Create access keys to access the DynamoDB table. Assign the access keys to the EC2 instance profile.
    Create an EC2 key pair to access the DynamoDB table. Assign the key pair to the EC2 instance profile.
    Create an IAM user to access the DynamoDB table. Assign the IAM user to the EC2 instance profile.
    Create an IAM role to access the DynamoDB table. Assign the IAM role to the EC2 instance profile.correct

Question was not answered
24. A company has a web application with a database tier that consists of an Amazon EC2 instance that runs MySQL. A SysOps administrator needs to minimize potential data loss and the time that is required to recover in the event of a database failure.

What is the MOST operationally efficient solution that meets these requirements?

    Create an Amazon CloudWatch alarm for the StatusCheckFailed_System metric to invoke an AWS Lambda function that stops and starts the EC2 instance.
    Create an Amazon RDS for MySQL Multi-AZ DB instance. Use a MySQL native backup that is stored in Amazon S3 to restore the data to the new database. Update the connection string in the web application.
    Create an Amazon RDS for MySQL Single-AZ DB instance with a read replica. Use a MySQL native backup that is stored in Amazon S3 to restore the data to the new database. Update the connection string in the web application.
    Use Amazon Data Lifecycle Manager (Amazon DLM) to take a snapshot of the Amazon Elastic Block Store (Amazon EBS) volume every hour. In the event of an EC2 instance failure, restore the EBS volume from a snapshot.correct

Question was not answered
25. A company migrated an I/O intensive application to an Amazon EC2 general purpose instance. The EC2 instance has a single General Purpose SSD Amazon Elastic Block Store (Amazon EBS) volume attached.

Application users report that certain actions that require intensive reading and writing to the disk are taking much longer than normal or are failing completely. After reviewing the performance metrics of the EBS volume, a SysOps administrator notices that the VolumeQueueLength metric is consistently high during the same times in which the users are reporting issues. The SysOps administrator needs to resolve this problem to restore full performance to the application.

Which action will meet these requirements?

    Modify the instance type to be storage optimized.
    Modify the volume properties by deselecting Auto-Enable Volume 10.
    Modify the volume properties to increase the IOPcorrect
    Modify the instance to enable enhanced networking.

Question was not answered
26. A SysOps administrator is trying to set up an Amazon Route 53 domain name to route traffic to a website hosted on Amazon S3. The domain name of the website is www.anycompany.com and the S3 bucket name is anycompany-static. After the record set is set up in Route 53, the domain name www.anycompany.com does not seem to work, and the static website is not displayed in the browser.

Which of the following is a cause of this?

    The S3 bucket must be configured with Amazon CloudFront first.
    The Route 53 record set must have an IAM role that allows access to the S3 bucket.
    The Route 53 record set must be in the same region as the S3 bucket.
    The S3 bucket name must match the record set name in Route 53.correct

Question was not answered
27. An Amazon EC2 instance needs to be reachable from the internet.

The EC2 instance is in a subnet with the following route table:
"image"
Which entry must a SysOps administrator add to the route table to meet this requirement?

    A route for 0.0.0.0/0 that points to a NAT gateway
    A route for 0.0.0.0/0 that points to an egress-only internet gateway
    A route for 0.0.0.0/0 that points to an internet gatewaycorrect
    A route for 0.0.0.0/0 that points to an elastic network interface

Question was not answered
28. A SysOps administrator has enabled AWS CloudTrail in an AWS account. If CloudTrail is disabled, it must be re-enabled immediately.

What should the SysOps administrator do to meet these requirements WITHOUT writing custom code?

    Add the AWS account to AWS Organizations. Enable CloudTrail in the management account.
    Create an AWS Config rule that is invoked when CloudTrail configuration changes. Apply the AWS-ConfigureCloudTrailLogging automatic remediation action.
    Create an AWS Config rule that is invoked when CloudTrail configuration changes. Configure the rule to invoke an AWS Lambda function to enable CloudTrail.
    Create an Amazon EventBridge (Amazon CloudWatch Events) hourly rule with a schedule pattern to run an AWS Systems Manager Automation document to enable CloudTrail.correct

Question was not answered
29. A company has a stateless application that runs on four Amazon EC2 instances. The application requires tour instances at all times to support all traffic. A SysOps administrator must design a highly available, fault-tolerant architecture that continually supports all traffic if one Availability Zone

becomes unavailable.

Which configuration meets these requirements?

    Deploy two Auto Scaling groups in two Availability Zones with a minimum capacity of two instances in each group.
    Deploy an Auto Scaling group across two Availability Zones with a minimum capacity of four instances.
    Deploy an Auto Scaling group across three Availability Zones with a minimum capacity of four instances.correct
    Deploy an Auto Scaling group across three Availability Zones with a minimum capacity of six instances.

Question was not answered
30. A company's backend infrastructure contains an Amazon EC2 instance in a private subnet. The private subnet has a route to the internet through a NAT gateway in a public subnet. The instance must allow connectivity to a secure web server on the internet to retrieve data at regular intervals.

The client software times out with an error message that indicates that the client software could not establish the TCP connection.

What should a SysOps administrator do to resolve this error?

    Add an inbound rule to the security group for the EC2 instance with the following parameters:
    Type - HTTP, Source - 0.0.0.0/0.
    Add an inbound rule to the security group for the EC2 instance with the following parameters:
    Type - HTTPS, Source - 0.0.0.0/0.
    Add an outbound rule to the security group for the EC2 instance with the following parameters:
    Type - HTTP, Destination - 0.0.0.0/0.
    Add an outbound rule to the security group for the EC2 instance with the following parameters: Type - HTTPcorrect
    Destination - 0.0.0.0/0.

Question was not answered
31. A software development company has multiple developers who work on the same product. Each developer must have their own development environment, and these development environments must be identical. Each development environment consists of Amazon EC2 instances and an Amazon RDS DB instance. The development environments should be created only when necessary, and they must be terminated each night to minimize costs.

What is the MOST operationally efficient solution that meets these requirements?

    Provide developers with access to the same AWS CloudFormation template so that they can provision their development environment when necessary. Schedule a nightly cron job on each development instance to stop all running processes to reduce CPU utilization to nearly zero.
    Provide developers with access to the same AWS CloudFormation template so that they can provision their development environment when necessary. Schedule a nightly Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function to delete the AWS CloudFormation stacks.correct
    Provide developers with CLI commands so that they can provision their own development environment when necessary. Schedule a nightly Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function to terminate all EC2 instances and the DB instance.
    Provide developers with CLI commands so that they can provision their own development environment when necessary. Schedule a nightly Amazon EventBridge (Amazon CloudWatch Events) rule to cause AWS CloudFormation to delete all of the development environment resources.

Question was not answered
32. A company runs a stateless application that is hosted on an Amazon EC2 instance. Users are reporting performance issues. A SysOps administrator reviews the Amazon CloudWatch metrics for the application and notices that the instance's CPU utilization frequently reaches 90% during business hours.

What is the MOST operationally efficient solution that will improve the application's responsiveness?

    Configure CloudWatch logging on the EC2 instance. Configure a CloudWatch alarm for CPU utilization to alert the SysOps administrator when CPU utilization goes above 90%.
    Configure an AWS Client VPN connection to allow the application users to connect directly to the EC2 instance private IP address to reduce latency.
    Create an Auto Scaling group, and assign it to an Application Load Balancer. Configure a target tracking scaling policy that is based on the average CPU utilization of the Auto Scaling group.correct
    Create a CloudWatch alarm that activates when the EC2 instance's CPU utilization goes above
    80%. Configure the alarm to invoke an AWS Lambda function that vertically scales the instance.

Question was not answered
33. A company is testing Amazon Elasticsearch Service (Amazon ES) as a solution for analyzing system logs from a fleet of Amazon EC2 instances. During the test phase, the domain operates on a single-node cluster. A SysOps administrator needs to transition the test domain into a highly available production-grade deployment.

Which Amazon ES configuration should the SysOps administrator use to meet this requirement?

    Use a cluster of four data nodes across two AWS Regions. Deploy four dedicated master nodes in each Region.
    Use a cluster of six data nodes across three Availability Zones. Use three dedicated master nodes.correct
    Use a cluster of six data nodes across three Availability Zones. Use six dedicated master nodes.
    Use a cluster of eight data nodes across two Availability Zones. Deploy four master nodes in a failover AWS Region.

Question was not answered
34. A company recently acquired another corporation and all of that corporation's AWS accounts. A financial analyst needs the cost data from these accounts. A SysOps administrator uses Cost Explorer to generate cost and usage reports. The SysOps administrator notices that "No Tagkey" represents 20% of the monthly cost.

What should the SysOps administrator do to tag the "No Tagkey" resources?

    Add the accounts to AWS Organizations. Use a service control policy (SCP) to tag all the untagged resources.
    Use an AWS Config rule to find the untagged resources. Set the remediation action to terminate the resources.
    Use Cost Explorer to find and tag all the untagged resources.
    Use Tag Editor to find and taq all the untaqqed resources.correct

Question was not answered
Explanation:

"You can add tags to resources when you create the resource. You can use the resource's service console or API to add, change, or remove those tags one resource at a time. To add tags to―or edit or delete tags of―multiple resources at once, use Tag Editor. With Tag Editor, you search for the resources that you want to tag, and then manage tags for the resources in your search results." https://docs.aws.amazon.com/ARG/latest/userguide/tag-editor.html
35. A company is using Amazon Elastic File System (Amazon EFS) to share a file system among several Amazon EC2 instances. As usage increases, users report that file retrieval from the EFS file system is slower than normal.

Which action should a SysOps administrator take to improve the performance of the file system?

    Configure the file system for Provisioned Throughput.correct
    Enable encryption in transit on the file system.
    Identify any unused files in the file system, and remove the unused files.
    Resize the Amazon Elastic Block Store (Amazon EBS) volume of each of the EC2 instances.

Question was not answered
36. A SysOps administrator is helping a development team deploy an application to AWS Trie AWS CloudFormat on temp ate includes an Amazon Linux EC2 Instance an Amazon Aurora DB cluster and a hard coded database password that must be rotated every 90 days

What is the MOST secure way to manage the database password?

    Use the AWS SecretsManager Secret resource with the GenerateSecretString property to automatically generate a password Use the AWS SecretsManager RotationSchedule resource lo define a rotation schedule lor the password Configure the application to retrieve the secret from AWS Secrets Manager access the databasecorrect
    Use me AWS SecretsManager Secret resource with the SecretStrmg property Accept a password as a CloudFormation parameter Use the AllowedPatteen property of the CloudFormaton parameter to require e minimum length, uppercase and lowercase letters and special characters Configure me application to retrieve the secret from AWS Secrets Manager to access the database
    Use the AWS SSM Parameter resource Accept input as a Qoudformatton parameter to store the parameter as a secure sting Configure the application to retrieve the parameter from AWS Systems Manager Parameter Store to access the database
    Use the AWS SSM Parameter resource Accept input as a Cloudf ormetton parameter to store the parameter as a string Configure the application to retrieve the parameter from AWS Systems Manager Parameter Store to access the database

Question was not answered
37. An application team uses an Amazon Aurora MySQL DB cluster with one Aurora Replica. The application team notices that the application read performance degrades when user connections exceed 200. The number of user connections is typically consistent around 180. with occasional sudden increases above 200 connections. The application team wants the application to automatically scale as user demand increases or decreases.

Which solution will meet these requirements?

    Migrate to a new Aurora multi-master DB cluster. Modify the application database connection string.
    Modify the DB cluster by changing to serverless mode whenever user connections exceed 200.
    Create an auto scaling policy with a target metric of 195 Database Connectionscorrect
    Modify the DB cluster by increasing the Aurora Replica instance size.

Question was not answered
38. A company's SysOps administrator has created an Amazon EC2 instance with custom software that will be used as a template for all new EC2 instances across multiple AWS accounts. The Amazon Elastic Block Store (Amazon EBS) volumes that are attached to the EC2 instance are encrypted with AWS managed keys.

The SysOps administrator creates an Amazon Machine Image (AMI) of the custom EC2 instance and plans to share the AMI with the company's other AWS accounts. The company requires that all AMIs are encrypted with AWS Key Management Service (AWS KMS) keys and that only authorized AWS accounts can access the shared AMIs.

Which solution will securely share the AMI with the other AWS accounts?

    In the account where the AMI was created, create a customer master key (CMK). Modify the key policy to provide kms:DescribeKey, kms ReEncrypf, kms:CreateGrant, and kms:Decrypt permissions to the AWS accounts that the AMI will be shared with. Modify the AMI permissions to specify the AWS account numbers that the AMI will be shared with.
    In the account where the AMI was created, create a customer master key (CMK). Modify the key policy to provide kms:DescribeKey, kms:ReEncrypt*. kms:CreateGrant, and kms;Decrypt permissions to the AWS accounts that the AMI will be shared with. Create a copy of the AMcorrect
    and specify the CM
    Modify the permissions on the copied AMI to specify the AWS account numbers that the AMI will be shared with.
    In the account where the AMI was created, create a customer master key (CMK). Modify the key policy to provide kms:DescrlbeKey, kms:ReEncrypt kms:CreateGrant, and kms:Decrypt permissions to the AWS accounts that the AMI will be shared with. Create a copy of the AM
    and specify the CM
    Modify the permissions on the copied AMI to make it public.
    In the account where the AMI was created, modify the key policy of the AWS managed key to provide kms:DescnbeKey. kms:ReEncrypt kms:CreateGrant, and kms:Decrypt permissions to the AWS accounts that the AMI will be shared with. Modify the AMI permissions to specify the AWS account numbers that the AMI will be shared with.

Question was not answered
Explanation:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/sharingamis-explicit.html
39. A SysOps administrator is provisioning an Amazon Elastic File System (Amazon EFS) file system to provide shared storage across multiple Amazon EC2 instances. The instances all exist in the same VPC across multiple Availability Zones. There are two instances. In each Availability Zone. The SysOps administrator must make the file system accessible to each instance with the lowest possible latency.

Which solution will meet these requirements?

    Create a mount target for the EFS file system in the VP
    Use the mount target to mount the file system on each of the instances
    Create a mount target for the EFS file system in one Availability Zone of the VP
    Use the mount target to mount the file system on the instances in that Availability Zone. Share the directory with the other instances.correct
    Create a mount target for each instance. Use each mount target to mount the EFS file system on each respective instance.
    Create a mount target in each Availability Zone of the VPC Use the mount target to mount the EFS file system on the Instances in the respective Availability Zone.

Question was not answered
Explanation:

A mount target provides an IP address for an NFSv4 endpoint at which you can mount an Amazon EFS file system. You mount your file system using its Domain Name Service (DNS) name, which resolves to the IP address of the EFS mount target in the same Availability Zone as your EC2 instance. You can create one mount target in each Availability Zone in an AWS Region. If there are multiple subnets in an Availability Zone in your VPC, you create a mount target in one of the subnets. Then all EC2 instances in that Availability Zone share that mount target. https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html
40. A SysOps administrator has used AWS Cloud Formal ion to deploy a serverless application Into a production VPC. The application consists of an AWS Lambda function an Amazon DynamoDB table, and an Amazon API Gateway API. The SysOps administrator must delete the AWS Cloud Formation stack without deleting the DynamoDB table.

Which action should the SysOps administrator take before deleting the AWS Cloud Formation stack?

    Add a Retain deletion policy to the DynamoDB resource in the AWS CloudFormation stackcorrect
    Add a Snapshot deletion policy to the DynamoDB resource in the AWS CloudFormation stack.
    Enable termination protection on the AWS Cloud Formation stack.
    Update the application's IAM policy with a Deny statement for the dynamodb:DeleteTabie action.

Question was not answered
41. A SysOps administrator Is troubleshooting an AWS Cloud Formation template whereby multiple Amazon EC2 instances are being created.

The template is working In us-east-1. but it is failing In us-west-2 with the error code:

How should the administrator ensure that the AWS Cloud Formation template is working in every region?

    Copy the source region's Amazon Machine Image (AMI) to the destination region and assign it the same Icorrect
    Edit the AWS CloudFormatton template to specify the region code as part of the fully qualified AMI I
    Edit the AWS CloudFormatton template to offer a drop-down list of all AMIs to the user by using the aws :: EC2:: ami :: imageiD control.
    Modify the AWS CloudFormation template by including the AMI IDs in the "Mappings" section. Refer to the proper mapping within the template for the proper AMI I

Question was not answered
42. A company runs us Infrastructure on Amazon EC2 Instances that run In an Auto Scaling group. Recently, the company promoted faulty code to the entire EC2 fleet. This faulty code caused the Auto Scaling group to scale the instances before any of the application logs could be retrieved.

What should a SysOps administrator do to retain the application logs after instances are terminated?

A Configure an Auto Scaling lifecycle hook to create a snapshot of the ephemeral storage upon termination of the instances.

B. Create a new Amazon Machine Image (AMI) that has the Amazon CloudWatch agent installed and configured to send logs to Amazon CloudWatch Logs. Update the launch template to use the new AMI.

C. Create a new Amazon Machine Image (AMI) that has a custom script configured to send logs to AWS CloudTrail. Update the launch template to use the new AMI.

D. Install the Amazon CloudWatch agent on the Amazon Machine Image (AMI) that is defined in the launch template. Configure the CloudWatch agent to back up the logs to ephemeral storage.

    wrong

43. A company has a critical serverless application that uses multiple AWS Lambda functions. Each Lambda function generates 1 GB of log data daily in tts own Amazon CloudWatch Logs log group. The company's security team asks for a count of application errors, grouped by type, across all of the log groups.

What should a SysOps administrator do to meet this requirement?

    Perform a CloudWatch Logs Insights query that uses the stats command and count function.correct
    Perform a CloudWatch Logs search that uses the groupby keyword and count function.
    Perform an Amazon Athena query that uses the SELECT and GROUP BY keywords.
    Perform an Amazon RDS query that uses the SELECT and GROUP BY keywords.

Question was not answered
44. A company monitors its account activity using AWS CloudTrail. and is concerned that some log files are being tampered with after the logs have been delivered to the account's Amazon S3 bucket.

Moving forward, how can the SysOps administrator confirm that the log files have not been modified after being delivered to the S3 bucket?

    Stream the CloudTrail logs to Amazon CloudWatch Logs to store logs at a secondary location.
    Enable log file integrity validation and use digest files to verify the hash value of the log file.correct
    Replicate the S3 log bucket across regions, and encrypt log files with S3 managed keys.
    Enable S3 server access logging to track requests made to the log bucket for security audits.

Question was not answered
Explanation:

When you enable log file integrity validation, CloudTrail creates a hash for every log file that it delivers. Every hour, CloudTrail also creates and delivers a file that Reference the log files for the last hour and contains a hash of each. This file is called a digest file. CloudTrail signs each digest file using the private key of a public and private key pair. After delivery, you can use the public key to validate the digest file. CloudTrail uses different key pairs for each AWS region

https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-log-file-validation-intro.html
45. A team of On-call engineers frequently needs to connect to Amazon EC2 Instances In a private subnet to troubleshoot and run commands. The Instances use either the latest AWS-provided Windows Amazon Machine Images (AMIs) or Amazon Linux AMIs.

The team has an existing IAM role for authorization. A SysOps administrator must provide the team with access to the Instances by granting IAM permissions to this

Which solution will meet this requirement?

    Add a statement to the IAM role policy to allow the ssm:StartSession action on the instances. Instruct the team to use AWS Systems Manager Session Manager to connect to the Instances by using the assumed IAM role.correct
    Associate an Elastic IP address and a security group with each instance. Add the engineers' IP addresses to the security group inbound rules. Add a statement to the IAM role policy to allow the ec2:AuthoflzeSecurityGroupIngress action so that the team can connect to the Instances.
    Create a bastion host with an EC2 Instance, and associate the bastion host with the VP
    Add a statement to the IAM role policy to allow the ec2:CreateVpnConnection action on the bastion host. Instruct the team to use the bastion host endpoint to connect to the instances.
    D Create an internet-facing Network Load Balancer. Use two listeners. Forward port 22 to a target group of Linux instances. Forward port 3389 to a target group of Windows Instances. Add a statement to the IAM role policy to allow the ec2:CreateRoute action so that the team can connect to the Instances.

Question was not answered
46. A company has an AWS Cloud Formation template that creates an Amazon S3 bucket. A user authenticates to the corporate AWS account with their Active Directory credentials and attempts to deploy the Cloud Formation template. However, the stack creation fails.

Which factors could cause this failure? (Select TWO.)

    The user's IAM policy does not allow the cloudformation:CreateStack action.correct
    The user's IAM policy does not allow the cloudformation:CreateStackSet action.
    The user's IAM policy does not allow the s3:CreateBucket action.correct
    The user's IAM policy explicitly denies the s3:ListBucket action.
    The user's IAM policy explicitly denies the s3:PutObject action

Question was not answered
47. A company runs a web application on three Amazon EC2 instances behind an Application Load Balancer (ALB). The company notices that random periods of increased traffic cause a degradation in the application's performance. A SysOps administrator must scale the application to meet the increased traffic.

Which solution meets these requirements?

    Create an Amazon CloudWatch alarm to monitor application latency and increase the size of each EC2 instance If the desired threshold is reached.
    Create an Amazon EventBridge (Amazon CloudWatch Events) rule to monitor application latency and add an EC2 instance to the ALB if the desired threshold is reached.
    Deploy the application to an Auto Scaling group of EC2 instances with a target tracking scaling policy. Attach the ALB to the Auto Scaling group.correct
    Deploy the application to an Auto Scaling group of EC2 instances with a scheduled scaling policy. Attach the ALB to the Auto Scaling group.

Question was not answered
Explanation:

docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
48. A company has a new requirement stating that all resources In AWS must be tagged according to a set policy.

Which AWS service should be used to enforce and continually Identify all resources that are not in compliance with the policy?

    AWS CloudTrail
    Amazon Inspector
    AWS Configcorrect
    AWS Systems Manager

Question was not answered
49. A SysOps administrator is setting up an automated process to recover an Amazon EC2 instance In the event of an underlying hardware failure. The recovered instance must have the same private IP address and the same Elastic IP address that the original instance had. The SysOps team must receive an email notification when the recovery process is initiated.

Which solution will meet these requirements?

    Create an Amazon CloudWatch alarm for the EC2 instance, and specify the SiatusCheckFailedjnstance metric. Add an EC2 action to the alarm to recover the instance. Add an alarm notification to publish a message to an Amazon Simple Notification Service (Amazon SNS> topic. Subscribe the SysOps team email address to the SNS topic.
    Create an Amazon CloudWatch alarm for the EC2 Instance, and specify the StatusCheckFailed_System metric. Add an EC2 action to the alarm to recover the instance. Add an alarm notification to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the SysOps team email address to the SNS topic.correct
    Create an Auto Scaling group across three different subnets in the same Availability Zone with a minimum, maximum, and desired size of 1. Configure the Auto Seating group to use a launch template that specifies the private IP address and the Elastic IP address. Add an activity notification for the Auto Scaling group to send an email message to the SysOps team through Amazon Simple Email Service (Amazon SES).
    Create an Auto Scaling group across three Availability Zones with a minimum, maximum, and desired size of 1. Configure the Auto Scaling group to use a launch template that specifies the private IP address and the Elastic IP address. Add an activity notification for the Auto Scaling group to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the SysOps team email address to the SNS topic.

Question was not answered
Explanation:

You can create an Amazon CloudWatch alarm that monitors an Amazon EC2 instance and automatically recovers the instance if it becomes impaired due to an underlying hardware failure or a problem that requires AWS involvement to repair. Terminated instances cannot be recovered. A recovered instance is identical to the original instance, including the instance ID, private IP addresses, Elastic IP addresses, and all instance metadata. If the impaired instance has a public IPv4 address, the instance retains the public IPv4 address after recovery. If the impaired instance is in a placement group, the recovered instance runs in the placement group. When the StatusCheckFailed_System alarm is triggered, and the recover action is initiated, you will be notified by the Amazon SNS topic that you selected when you created the alarm and associated the recover action. https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-recover.html
50. A SysOps administrator must create a solution that immediately notifies software developers if an AWS Lambda function experiences an error.

Which solution will meet this requirement?

    Create an Amazon Simple Notification Service (Amazon SNS) topic with an email subscription for each developer. Create an Amazon CloudWatch alarm by using the Errors metric and the Lambda function name as a dimension. Configure the alarm to send a notification to the SNS topic when the alarm state reaches ALARcorrect
    Create an Amazon Simple Notification Service (Amazon SNS) topic with a mobile subscription for each developer. Create an Amazon EventBridge (Amazon CloudWatch Events) alarm by using LambdaError as the event pattern and the SNS topic name as a resource. Configure the alarm to send a notification to the SNS topic when the alarm state reaches ALAR
    Verify each developer email address in Amazon Simple Email Service (Amazon SES). Create an Amazon CloudWatch rule by using the LambdaError metric and developer email addresses as dimensions. Configure the rule to send an email through Amazon SES when the rule state reaches
    ALAR
    Verify each developer mobile phone in Amazon Simple Email Service {Amazon SES). Create an Amazon EventBridge (Amazon CloudWatch Events) rule by using Errors as the event pattern and the Lambda function name as a resource. Configure the rule to send a push notification through Amazon SES when the rule state reaches ALAR

Question was not answered
51. A SysOps administrator developed a Python script that uses the AWS SDK to conduct several maintenance tasks. The script needs to run automatically every night.

What is the MOST operationally efficient solution that meets this requirement?

    Convert the Python script to an AWS Lambda (unction. Use an Amazon EventBridge (Amazon
    CloudWatch Events) rule to invoke the function every night.correct
    Convert the Python script to an AWS Lambda function. Use AWS CloudTrail to invoke the function every night.
    Deploy the Python script to an Amazon EC2 Instance. Use Amazon EventBridge (Amazon CloudWatch Events) to schedule the instance to start and stop every night.
    Deploy the Python script to an Amazon EC2 instance. Use AWS Systems Manager to schedule the instance to start and stop every night.

Question was not answered
52. A SysOps administrator must create a solution that automatically shuts down any Amazon EC2 instances that have less than 10% average CPU utilization for 60 minutes or more.

Which solution will meet this requirement In the MOST operationally efficient manner?

    Implement a cron job on each EC2 instance to run once every 60 minutes and calculate the current CPU utilization. Initiate an instance shutdown If CPU utilization is less than 10%.
    Implement an Amazon CloudWatch alarm for each EC2 instance to monitor average CPU utilization. Set the period at 1 hour, and set the threshold at 10%. Configure an EC2 action on the alarm to stop the instance.correct
    Install the unified Amazon CloudWatch agent on each EC2 instance, and enable the Basic level predefined metric set. Log CPU utilization every 60 minutes, and initiate an instance shutdown if CPU utilization is less than 10%.
    Use AWS Systems Manager Run Command to get CPU utilization from each EC2 instance every 60 minutes. Initiate an instance shutdown if CPU utilization is less than 10%.

Question was not answered
Explanation:

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html
53. A company uses AWS Cloud Formation templates to deploy cloud infrastructure. An analysis of all the company's templates shows that the company has declared the same components in multiple templates. A SysOps administrator needs to create dedicated templates that have their own parameters and conditions for these common components.

Which solution will meet this requirement?

    Develop a CloudFormaiion change set.
    Develop CloudFormation macros.
    Develop CloudFormation nested stacks.correct
    Develop CloudFormation stack sets.

Question was not answered
54. A company has deployed AWS Security Hub and AWS Config in a newly implemented organization in AWS Organizations. A SysOps administrator must implement a solution to restrict all member accounts in the organization from deploying Amazon EC2 resources in the ap-southeast-2 Region. The solution must be implemented from a single point and must govern an current and future accounts. The use of root credentials also must be restricted in member accounts.

Which AWS feature should the SysOps administrator use to meet these requirements?

    AWS Config aggregator
    IAM user permissions boundaries
    AWS Organizations service control policies (SCPs)correct
    AWS Security Hub conformance packs

Question was not answered
55. A company has a new requirement stating that all resources in AWS must be tagged according to a set policy.

Which AWS service should be used to enforce and continually identify all resources that are not in compliance with the policy?

    AWS CloudTrail
    Amazon Inspector
    AWSConfigcorrect
    AWS Systems Manager

Question was not answered
56. A SysOps administrator has used AWS Cloud Formation to deploy a sereness application into a production VPC. The application consists of an AWS Lambda function, an Amazon DynamoOB table, and an Amazon API Gateway API. The SysOps administrator must delete the AWS Cloud Formation stack without deleting the DynamoOB table.

Which action should the SysOps administrator take before deleting the AWS Cloud Formation stack?

    Add a Retain deletion policy to the DynamoOB resource in the AWS CloudFormation stack.correct
    Add a Snapshot deletion policy to the DynamoOB resource In the AWS CloudFormation stack.
    Enable termination protection on the AWS Cloud Formation stack.
    Update the application's IAM policy with a Deny statement for the dynamodb: DeleteTabie action.

Question was not answered
57. A company has a critical serverless application that uses multiple AWS Lambda functions. Each Lambda function generates 1 GB of log data daily in its own Amazon CloudWatch Logs log group. The company's security team asks for a count of application errors, grouped by type, across all of the log groups.

What should a SysOps administrator do to meet this requirement?

    Perform a CloudWatch Logs Insights query that uses the stats command and count function.correct
    Perform a CloudWatch Logs search that uses the groupby keyword and count function.
    Perform an Amazon Athena query that uses the SELECT and GROUP BY keywords.
    Perform an Amazon RDS query that uses the SELECT and GROUP BY keywords.

Question was not answered
58. A SysOps administrator needs to give users the ability to upload objects to an Amazon S3 bucket. The SysOps administrator creates a presigned URL and provides the URL to a user, but the user cannot upload an object to the S3 bucket. The presigned URL has not expired, and no bucket policy is applied to the S3 bucket.

Which of the following could be the cause of this problem?

    The user has not properly configured the AWS CLI with their access key and secret access key.
    The SysOps administrator does not have the necessary permissions to upload the object to the S3 bucket.correct
    The SysOps administrator must apply a bucket policy to the S3 bucket to allow the user to upload the object.
    The object already has been uploaded through the use of the presigned URL, so the presigned URL is no longer valid.

Question was not answered
59. A SysOps administrator is responsible for a legacy. CPU-heavy application The application can only be scaled vertically Currently, the application is deployed on a single t2 large Amazon EC2 instance The system is showing 90% CPU usage and significant performance latency after a few minutes

What change should be made to alleviate the performance problem?

    Change the Amazon EBS volume to Provisioned lOPs
    Upgrade to a compute-optimized instancecorrect
    Add additional 12 large instances to the application
    Purchase Reserved Instances

Question was not answered
60. A company is tunning a website on Amazon EC2 instances that are in an Auto Scaling group When the website traffic increases, additional instances lake several minutes to become available because of a long-running user data script that installs software A SysOps administrator must decrease the time that is required (or new instances to become available

Which action should the SysOps administrator take to meet this requirement?

    Reduce the scaling thresholds so that instances are added before traffic increases
    Purchase Reserved Instances to cover 100% of the maximum capacity of the Auto Scaling group
    Update the Auto Scaling group to launch instances that have a storage optimized instance type
    Use EC2 Image Builder to prepare an Amazon Machine Image (AMI) that has pre-installed softwarecorrect

Question was not answered
Explanation:

automated way to update your image. Have a pipeline to update your image. When you boot from your AMI updates = scrits are already pre-installed, so no need to complete boot scripts in boot process. https://aws.amazon.com/image-builder/
61. A SysOps administrator is notified that an Amazon EC2 instance has stopped responding The AWS Management Console indicates that the system status checks are failing.

What should the administrator do first to resolve this issue?

    Reboot the EC2 instance so it can be launched on a new host
    Stop and then start the EC2 instance so that it can be launched on a new hostcorrect
    Terminate the EC2 instance and relaunch it
    View the AWS CloudTrail log to investigate what changed on the EC2 instance

Question was not answered
Explanation:

https://aws.amazon.com/premiumsupport/knowledge-center/ec2-windows-system-status-check-fail/
62. A SysOps administrator has enabled AWS CloudTrail in an AWS account If CloudTrail is disabled it must be re-enabled immediately What should the SysOps administrator do to meet these requirements WITHOUT writing custom code''

    Add the AWS account to AWS Organizations Enable CloudTrail in the management account
    Create an AWS Config rule that is invoked when CloudTrail configuration changes Apply the AWS-ConfigureCloudTrailLogging automatic remediation actioncorrect
    Create an AWS Config rule that is invoked when CloudTrail configuration changes Configure the rule to invoke an AWS Lambda function to enable CloudTrail
    Create an Amazon EventBridge (Amazon CloudWatch Events) hourly rule with a schedule pattern to run an AWS Systems Manager Automation document to enable CloudTrail

Question was not answered
63. A recent audit found that most resources belonging to the development team were in violation of patch compliance standards The resources were properly tagged.

Which service should be used to quickly remediate the issue and bring the resources back into compliance?

    AWS Config
    Amazon Inspector
    AWS Trusted Advisor
    AWS Systems Managercorrect

Question was not answered
64. An Amazon EC2 instance is running an application that uses Amazon Simple Queue Service (Amazon SQS} queues A SysOps administrator must ensure that the application can read, write, and delete messages from the SQS queues

Which solution will meet these requirements in the MOST secure manner?

    Create an IAM user with an IAM policy that allows the sqs SendMessage permission, the sqs ReceiveMessage permission, and the sqs DeleteMessage permission to the appropriate queues Embed the IAM user's credentials in the application's configuration
    Create an IAM user with an IAM policy that allows the sqs SendMessage permission, the sqs ReceiveMessage permission, and the sqs DeleteMessage permission to the appropriate queues Export the IAM user's access key and secret access key as environment variables on the EC2 instance
    Create and associate an IAM role that allows EC2 instances to call AWS services Attach an IAM policy to the role that allows sqs." permissions to the appropriate queues
    Create and associate an IAM role that allows EC2 instances to call AWS services Attach an IAM policy to the role that allows the sqs SendMessage permission, the sqs ReceiveMessage permission, and the sqs DeleteMessage permission to the appropriate queuescorrect

Question was not answered
65. A development team recently deployed a new version of a web application to production After the release, penetration testing revealed a cross-site scripting vulnerability that could expose user data

Which AWS service will mitigate this issue?

    AWS Shield Standard
    AWS WAFcorrect
    Elastic Load Balancing
    Amazon Cognito

Question was not answered
Explanation:

https://www.imperva.com/learn/application-security/cross-site-scripting-xss-attacks/
66. A company uses an AWS CloudFormation template to provision an Amazon EC2 instance and an Amazon RDS DB instance A SysOps administrator must update the template to ensure that the DB instance is created before the EC2 instance is launched

What should the SysOps administrator do to meet this requirement?

    Add a wait condition to the template Update the EC2 instance user data script to send a signal after the EC2 instance is started
    Add the DependsOn attribute to the EC2 instance resource, and provide the logical name of the RDS resourcecorrect
    Change the order of the resources in the template so that the RDS resource is listed before the EC2 instance resource
    Create multiple templates Use AWS CloudFormation StackSets to wait for one stack to complete before the second stack is created

Question was not answered
Explanation:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html

Syntax The DependsOn attribute can take a single string or list of strings. "DependsOn" : [ String, ... ] Example The following template contains an AWS::EC2::Instance resource with a DependsOn

attribute that specifies myDB, an AWS::RDS::DBInstance. When CloudFormation creates this stack, it first creates myDB, then creates Ec2Instance.
67. A company has an existing web application that runs on two Amazon EC2 instances behind an Application Load Balancer (ALB) across two Availability Zones The application uses an Amazon RDS Multi-AZ DB Instance Amazon Route 53 record sets route requests tor dynamic content to the load balancer and requests for static content to an Amazon S3 bucket Site visitors are reporting extremely long loading times.

Which actions should be taken to improve the performance of the website? (Select TWO )

    Add Amazon CloudFront caching for static contentcorrect
    Change the load balancer listener from HTTPS to TCP
    Enable Amazon Route 53 latency-based routing
    Implement Amazon EC2 Auto Scaling for the web serverscorrect
    Move the static content from Amazon S3 to the web servers

Question was not answered
68. A company is running an application on premises and wants to use AWS for data backup All of the data must be available locally. The backup application can write only to block-based storage that is compatible with the Portable Operating System Interface (POSIX)

Which backup solution will meet these requirements?

    Configure the backup software to use Amazon S3 as the target for the data backups
    Configure the backup software to use Amazon S3 Glacier as the target for the data backups
    Use AWS Storage Gateway, and configure it to use gateway-cached volumes
    Use AWS Storage Gateway, and configure it to use gateway-stored volumescorrect

Question was not answered
Explanation:

https://docs.aws.amazon.com/storagegateway/latest/userguide/StorageGatewayConcepts.html
69. An organization created an Amazon Elastic File System (Amazon EFS) volume with a file system ID of fs-85ba4Kc. and it is actively used by 10 Amazon EC2 hosts. The organization has become concerned that the file system is not encrypted

How can this be resolved?

    Enable encryption on each host's connection to the Amazon EFS volume Each connection must be recreated for encryption to take effect
    Enable encryption on the existing EFS volume by using the AWS Command Line Interface
    Enable encryption on each host's local drive Restart each host to encrypt the drive
    Enable encryption on a newly created volume and copy all data from the original volume Reconnect each host to the new volumecorrect

Question was not answered
Explanation:

https://docs.aws.amazon.com/efs/latest/ug/encryption.html

Amazon EFS supports two forms of encryption for file systems, encryption of data in transit and encryption at rest. You can enable encryption of data at rest when creating an Amazon EFS file system. You can enable encryption of data in transit when you mount the file system.
70. While setting up an AWS managed VPN connection, a SysOps administrator creates a customer gateway resource in AWS The customer gateway device resides in a data center with a NAT gateway in front of it

What address should be used to create the customer gateway resource?

    The private IP address of the customer gateway device
    The MAC address of the NAT device in front of the customer gateway device
    The public IP address of the customer gateway device
    The public IP address of the NAT device in front of the customer gateway devicecorrect

Question was not answered
71. An errant process is known to use an entire processor and run at 100% A SysOps administrator wants to automate restarting the instance once the problem occurs for more than 2 minutes

How can this be accomplished?

    Create an Amazon CloudWatch alarm for the Amazon EC2 instance with basic monitoring Enable an action to restart the instance
    Create a CloudWatch alarm for the EC2 instance with detailed monitoring Enable an action to restart the instancecorrect
    Create an AWS Lambda function to restart the EC2 instance triggered on a scheduled basis every 2 minutes
    Create a Lambda function to restart the EC2 instance, triggered by EC2 health checks

Question was not answered
72. A SysOps administrator notices a scale-up event for an Amazon EC2 Auto Scaling group Amazon CloudWatch shows a spike in the RequestCount metric for the associated Application Load Balancer The administrator would like to know the IP addresses for the source of the requests

Where can the administrator find this information?

    Auto Scaling logs
    AWS CloudTrail logs
    EC2 instance logs
    Elastic Load Balancer access logscorrect

Question was not answered
Explanation:

Elastic Load Balancing provides access logs that capture detailed information about requests sent to your load balancer. Each log contains information such as the time the request was received, the client's IP address, latencies, request paths, and server responses. You can use these access logs to analyze traffic patterns and troubleshoot issues.

https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-access-logs.html
73. An organization with a large IT department has decided to migrate to AWS With different job functions in the IT department it is not desirable to give all users access to all AWS resources Currently the organization handles access via LDAP group membership

What is the BEST method to allow access using current LDAP credentials?

    Create an AWS Directory Service Simple AD Replicate the on-premises LDAP directory to Simple AD
    Create a Lambda function to read LDAP groups and automate the creation of IAM users
    Use AWS CloudFormation to create IAM roles Deploy Direct Connect to allow access to the on-premises LDAP server
    Federate the LDAP directory with IAM using SAML Create different IAM roles to correspond to different LDAP groups to limit permissionscorrect

Question was not answered
74. An Amazon S3 Inventory report reveals that more than 1 million objects in an S3 bucket are not encrypted These objects must be encrypted, and all future objects must be encrypted at the time they are written

Which combination of actions should a SysOps administrator take to meet these requirements? (Select TWO)

    Create an AWS Config rule that runs evaluations against configuration changes to the S3 bucket When an unencrypted object is found run an AWS Systems Manager Automation document to encrypt the object in placecorrect
    Edit the properties of the S3 bucket to enable default server-side encryptioncorrect
    Filter the S3 Inventory report by using S3 Select to find all objects that are not encrypted Create an S3 Batch Operations job to copy each object in place with encryption enabledcorrect
    Filter the S3 Inventory report by using S3 Select to find all objects that are not encrypted Send each object name as a message to an Amazon Simple Queue Service (Amazon SQS) queue Use the SQS queue to invoke an AWS Lambda function to tag each object with a key of "Encryption" and a value of "SSE-KMS"
    Use S3 Event Notifications to invoke an AWS Lambda function on all new object-created events for the S3 bucket Configure the Lambda function to check whether the object is encrypted and to run an AWS Systems Manager Automation document to encrypt the object in place when an unencrypted object is found

Question was not answered
Explanation:

https://aws.amazon.com/blogs/storage/encrypting-objects-with-amazon-s3-batch-operations/
75. A company is using an AWS KMS customer master key (CMK) with imported key material The company Reference the CMK by its alias in the Java application to encrypt data The CMK must be rotated every 6 months

What is the process to rotate the key?

    Enable automatic key rotation for the CMK and specify a period of 6 months
    Create a new CMK with new imported material, and update the key alias to point to the new CMcorrect
    Delete the current key material, and import new material into the existing CMK
    Import a copy of the existing key material into a new CMK as a backup, and set the rotation schedule for 6 months

Question was not answered
76. A company is running a serverless application on AWS Lambda The application stores data in an Amazon RDS for MySQL DB instance Usage has steadily increased and recently there have been numerous "too many connections" errors when the Lambda function attempts to connect to the database The company already has configured the database to use the maximum max_connections value that is possible

What should a SysOps administrator do to resolve these errors'?

    Create a read replica of the database Use Amazon Route 53 to create a weighted DNS record that contains both databases
    Use Amazon RDS Proxy to create a proxy Update the connection string in the Lambda functioncorrect
    Increase the value in the max_connect_errors parameter in the parameter group that the database uses
    Update the Lambda function's reserved concurrency to a higher value

Question was not answered
Explanation:

https://aws.amazon.com/blogs/compute/using-amazon-rds-proxy-with-aws-lambda/

RDS Proxy acts as an intermediary between your application and an RDS database. RDS Proxy establishes and manages the necessary connection pools to your database so that your application creates fewer database connections. Your Lambda functions interact with RDS Proxy instead of your database instance. It handles the connection pooling necessary for scaling many simultaneous connections created by concurrent Lambda functions. This allows your Lambda applications to reuse existing connections, rather than creating new connections for every function invocation.

Check "Database proxy for Amazon RDS" section in the link to see how RDS proxy help Lambda handle huge connections to RDS MySQL https://aws.amazon.com/blogs/compute/using-amazon-rds-proxy-with-aws-lambda/
77. A company stores files on 50 Amazon S3 buckets in the same AWS Region The company wants to connect to the S3 buckets securely over a private connection from its Amazon EC2 instances. The company needs a solution that produces no additional cost

Which solution will meet these requirements?

    Create a gateway VPC endpoint lor each S3 bucket Attach the gateway VPC endpoints to each subnet inside the VPC
    Create an interface VPC endpoint (or each S3 bucket Attach the interface VPC endpoints to each subnet inside the VPC
    Create one gateway VPC endpoint for all the S3 buckets Add the gateway VPC endpoint to the VPC route tablecorrect
    Create one interface VPC endpoint for all the S3 buckets Add the interface VPC endpoint to the VPC route table

Question was not answered
78. A company uses AWS CloudFormation to deploy its application infrastructure Recently, a user accidentally changed a property of a database in a CloudFormation template and performed a stack update that caused an interruption to the application A SysOps administrator must determine how to modify the deployment process to allow the DevOps team to continue to deploy the infrastructure, but prevent against accidental modifications to specific resources.

Which solution will meet these requirements?

    Set up an AWS Config rule to alert based on changes to any CloudFormation stack An AWS Lambda function can then describe the stack to determine if any protected resources were modified and cancel the operation
    Set up an Amazon CloudWatch Events event with a rule to trigger based on any CloudFormation API call An AWS Lambda function can then describe the stack to determine if any protected resources were modified and cancel the operationcorrect
    Launch the CloudFormation templates using a stack policy with an explicit allow for all resources and an explicit deny of the protected resources with an action of Update
    Attach an IAM policy to the DevOps team role that prevents a CloudFormation stack from updating, with a condition based on the specific Amazon Resource Names (ARNs) of the protected resources

Question was not answered
79. A company's financial department needs to view the cost details of each project in an AWS account A SysOps administrator must perform the initial configuration that is required to view cost for each project in Cost Explorer

Which solution will meet this requirement?

    Activate cost allocation tags Add a project tag to the appropriate resourcescorrect
    Configure consolidated billing Create AWS Cost and Usage Reports
    Use AWS Budgets Create AWS Budgets reports
    Use cost categories to define custom groups that are based on AWS cost and usage dimensions

Question was not answered
80. A company is managing multiple AWS accounts in AWS Organizations The company is reviewing internal security of Its AWS environment The company's security administrator has their own AWS account and wants to review the VPC configuration of developer AWS accounts

Which solution will meet these requirements in the MOST secure manner?

    Create an IAM policy in each developer account that has read-only access related to VPC
    resources Assign the policy to an IAM user Share the user credentials with the security administrator
    Create an IAM policy in each developer account that has administrator access to all Amazon EC2 actions, including VPC actions Assign the policy to an IAM user Share the user credentials with the security administrator
    Create an IAM policy in each developer account that has administrator access related to VPC resources Assign the policy to a cross-account IAM role Ask the security administrator to assume the role from their account
    Create an IAM policy m each developer account that has read-only access related to VPC
    resources Assign the policy to a cross-account IAM role Ask the security administrator to assume the role from their accountcorrect

Question was not answered
81. An application runs on multiple Amazon EC2 instances in an Auto Scaling group The Auto Scaling group is configured to use the latest version of a launch template A SysOps administrator must devise a solution that centrally manages the application logs and retains the logs for no more than 90 days

Which solution will meet these requirements?

    Launch an Amazon Machine Image (AMI) that is preconfigured with the Amazon CloudWatch Logs agent to send logs to an Amazon S3 bucket Apply a 90-day S3 Lifecycle policy on the S3 bucket to expire the application logs
    Launch an Amazon Machine Image (AMI) that is preconfigured with the Amazon CloudWatch Logs agent to send logs to a log group Create an Amazon EventBridge (Amazon CloudWatch Events) scheduled rule to perform an instance refresh every 90 days
    Update the launch template user data to install and configure the Amazon CloudWatch Logs agent to send logs to a log group Configure the retention period on the log group to be 90 dayscorrect
    Update the launch template user data to install and configure the Amazon CloudWatch Logs agent to send logs to a log group Set the log rotation configuration of the EC2 instances to 90 days

Question was not answered
82. A company has a mobile app that uses Amazon S3 to store images The images are popular for a week, and then the number of access requests decreases over time The images must be highly available and must be immediately accessible upon request A SysOps administrator must reduce S3 storage costs for the company.

Which solution will meet these requirements MOST cost-effectively?

    Create an S3 Lifecycle policy to transition the images to S3 Glacier after 7 days
    Create an S3 Lifecycle policy to transition the images to S3 One Zone-Infrequent Access (S3 One Zone-IA) after 7 days
    Create an S3 Lifecycle policy to transition the images to S3 Standard after 7 days
    Create an S3 Lifecycle policy to transition the images to S3 Standard-Infrequent Access (S3 Standard-IA) after 7 dayscorrect

Question was not answered
83. A SysOps administrator receives notification that an application that is running on Amazon EC2 instances has failed to authenticate to an Amazon RDS database. To troubleshoot, the SysOps administrator needs to investigate AWS Secrets Manager password rotation

Which Amazon CloudWatch log will provide insight into the password rotation?

    AWS CloudTrail logs
    EC2 instance application logscorrect
    AWS Lambda function logs
    RDS database logs

Question was not answered
84. An AWS Lambda function is intermittently failing several times a day A SysOps administrator must find out how often this error has occurred in the last 7 days.

Which action will meet this requirement in the MOST operationally efficient manner?

    Use Amazon Athena to query the Amazon CloudWatch logs that are associated with the Lambda function
    Use Amazon Athena to query the AWS CloudTrail logs that are associated with the Lambda function
    Use Amazon CloudWatch Logs Insights to query the associated Lambda function logscorrect
    Use Amazon Elasticsearch Service (Amazon ES) to stream the Amazon CloudWatch logs for the Lambda function

Question was not answered
85. A company has an internal web application that runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group in a single Availability Zone. A SysOps administrator must make the application highly available.

Which action should the SysOps administrator take to meet this requirement?

    Increase the maximum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    Increase the minimum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    Update the Auto Scaling group to launch new instances in a second Availability Zone in the same AWS Region.correct
    Update the Auto Scaling group to launch new instances in an Availability Zone in a second AWS Region.

Question was not answered
Explanation:

"An Auto Scaling group can contain EC2 instances in one or more Availability Zones within the same Region. However, Auto Scaling groups cannot span multiple Regions". As stated in https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.htm
86. A SysOps administrator is building a process for sharing Amazon RDS database snapshots between different accounts associated with different business units within the same company. All data must be encrypted at rest.

How should the administrator implement this process?

    Write a script to download the encrypted snapshot, decrypt it using the AWS KMS encryption key used to encrypt the snapshot, then create a new volume in each account.
    Update the key policy to grant permission to the AWS KMS encryption key used to encrypt the snapshot with all relevant accounts, then share the snapshot with those accounts.correct
    Create an Amazon EC2 instance based on the snapshot, then save the instance's Amazon EBS volume as a snapshot and share it with the other accounts. Require each account owner to create a new volume from that snapshot and encrypt it.
    Create a new unencrypted RDS instance from the encrypted snapshot, connect to the instance using SSH/RD
    export the database contents into a file, then share this file with the other accounts.

Question was not answered
87. A SysOps administrator has an AWS CloudFormation template of the company's existing infrastructure in us-west-2. The administrator attempts to use the template to launch a new stack in eu-west-1, but the stack only partially deploys, receives an error message, and then rolls back.

Why would this template fail to deploy? (Select TWO.)

    The template referenced an IAM user that is not available in eu-west-1.correct
    The template referenced an Amazon Machine Image (AMI) that is not available in eu-west-1.correct
    The template did not have the proper level of permissions to deploy the resources.
    The template requested services that do not exist in eu-west-1.correct
    CloudFormation templates can be used only to update existing services.

Question was not answered
88. A development team recently deployed a new version of a web application to production. After the release, penetration testing revealed a cross-site scripting vulnerability that could expose user data.

Which AWS service will mitigate this issue?

    AWS Shield Standardcorrect
    AWS WAF
    Elastic Load Balancing
    Amazon Cognito

Question was not answered
89. A company is using an Amazon DynamoDB table for data. A SysOps administrator must configure replication of the table to another AWS Region for disaster recovery.

What should the SysOps administrator do to meet this requirement?

    Enable DynamoDB Accelerator (DAX).
    Enable DynamoDB Streams, and add a global secondary index (GSI).
    Enable DynamoDB Streams, and-add a global table Region.correct
    Enable point-in-time recovery.

Question was not answered
90. A company hosts a web portal on Amazon EC2 instances. The web portal uses an Elastic Load Balancer (ELB) and Amazon Route 53 for its public DNS service. The ELB and the EC2 instances are deployed by way of a single AWS CloudFormation stack in the us-east-1 Region. The web portal must be highly available across multiple Regions.

Which configuration will meet these requirements?

    Deploy a copy of the stack in the us-west-2 Region. Create a single start of authority (SOA) record in Route 53 that includes the IP address from each EL
    Configure the SOA record with health checks. Use the ELB in us-east-1 as the primary record and the ELB in us-west-2 as the secondary record.correct
    Deploy a copy of the stack in the us-west-2 Region. Create an additional A record in Route 53 that includes the ELB in us-west-2 as an alias target. Configure the A records with a failover routing policy and health checks. Use the ELB in us-east-1 as the primary record and the ELB in us-west-2 as the secondary record.
    Deploy a new group of EC2 instances in the us-west-2 Region. Associate the new EC2 instances with the existing ELB, and configure load balancer health checks on all EC2 instances. Configure the ELB to update Route 53 when EC2 instances in us-west-2 fail health checks.
    Deploy a new group of EC2 instances in the us-west-2 Region. Configure EC2 health checks on all EC2 instances in each Region. Configure a peering connection between the VPCs. Use the VPC in us-east-1 as the primary record and the VPC in us-west-2 as the secondary record.

Question was not answered
Explanation:

When you create a hosted zone, Route 53 automatically creates a name server (NS) record and a start of authority (SOA) record for the zone.

https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/migrate-dns-domain-in-use.html#migrate-dns-create-hosted-zone

https://en.wikipedia.org/wiki/SOA_record
91. A SysOps administrator must set up notifications for whenever combined billing exceeds a certain threshold for all AWS accounts within a company. The administrator has set up AWS Organizations and enabled Consolidated Billing.

Which additional steps must the administrator perform to set up the billing alerts?

    In the payer account: Enable billing alerts in the Billing and Cost Management console; publish an Amazon SNS message when the billing alert triggers.
    In each account: Enable billing alerts in the Billing and Cost Management console; set up a billing alarm in Amazon CloudWatch; publish an SNS message when the alarm triggers.
    In the payer account: Enable billing alerts in the Billing and Cost Management console; set up a billing alarm in the Billing and Cost Management console to publish an SNS message when the alarm triggers.
    In the payer account: Enable billing alerts in the Billing and Cost Management console; set up a billing alarm in Amazon CloudWatch; publish an SNS message when the alarm triggers.correct

Question was not answered
92. A company has multiple AWS Site-to-Site VPN connections between a VPC and its branch offices. The company manages an Amazon Elasticsearch Service (Amazon ES) domain that is configured with public access. The Amazon ES domain has an open domain access policy. A SysOps administrator needs to ensure that Amazon ES can be accessed only from the branch offices while preserving existing data.

Which solution will meet these requirements?

    Configure an identity-based access policy on Amazon E
    Add an allow statement to the policy that includes the Amazon Resource Name (ARN) for each branch office VPN connection.correct
    Configure an IP-based domain access policy on Amazon E
    Add an allow statement to the policy that includes the private IP CIDR blocks from each branch office network.
    Deploy a new Amazon ES domain in private subnets in a VPC, and import a snapshot from the old domain. Create a security group that allows inbound traffic from the branch office CIDR blocks.
    Reconfigure the Amazon ES domain in private subnets in a VP
    Create a security group that allows inbound traffic from the branch office CIDR blocks.

Question was not answered
93. A large company is using AWS Organizations to manage its multi-account AWS environment. According to company policy, all users should have read-level access to a particular Amazon S3 bucket in a central account. The S3 bucket data should not be available outside the organization. A SysOps administrator must set up the permissions and add a bucket policy to the S3 bucket.

Which parameters should be specified to accomplish this in the MOST efficient manner?

    Specify '*' as the principal and PrincipalOrgld as a condition.
    Specify all account numbers as the principal.
    Specify PrincipalOrgld as the principal.correct
    Specify the organization's management account as the principal.

Question was not answered
94. A SysOps administrator is troubleshooting connection timeouts to an Amazon EC2 instance that has a public IP address. The instance has a private IP address of 172.31.16.139. When the SysOps administrator tries to ping the instance's public IP address from the remote IP address 203.0.113.12, the response is "request timed out."

The flow logs contain the following information:

What is one cause of the problem?

    Inbound security group deny rule
    Outbound security group deny rule
    Network ACL inbound rules
    Network ACL outbound rulescorrect

Question was not answered
95. A company has multiple Amazon EC2 instances that run a resource-intensive application in a development environment. A SysOps administrator is implementing a solution to stop these EC2 instances when they are not in use.

Which solution will meet this requirement?

    Assess AWS CloudTrail logs to verify that there is no EC2 API activity. Invoke an AWS Lambda function to stop the EC2 instances.
    Create an Amazon CloudWatch alarm to stop the EC2 instances when the average CPU utilization is lower than 5% for a 30-minute period.correct
    Create an Amazon CloudWatch metric to stop the EC2 instances when the VolumeReadBytes metric is lower than 500 for a 30-minute period.
    Use AWS Config to invoke an AWS Lambda function to stop the EC2 instances based on resource
    configuration changes.

Question was not answered
Explanation:

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html#AddingStopActions
96. A SysOps administrator needs to configure a solution that will deliver digital content to a set of authorized users through Amazon CloudFront. Unauthorized users must be restricted from access.

Which solution will meet these requirements?

    Store the digital content in an Amazon S3 bucket that does not have public access blocked. Use signed URLs to access the S3 bucket through CloudFront.
    Store the digital content in an Amazon S3 bucket that has public access blocked. Use an origin access identity (OAI) to deliver the content through CloudFront. Restrict S3 bucket access with signed URLs in CloudFront.correct
    Store the digital content in an Amazon S3 bucket that has public access blocked. Use an origin access identity (OAI) to deliver the content through CloudFront. Enable field-level encryption.
    Store the digital content in an Amazon S3 bucket that does not have public access blocked. Use signed cookies for restricted delivery of the content through CloudFront.

Question was not answered
97. A company has attached the following policy to an IAM user:

Which of the following actions are allowed for the IAM user?

    Amazon RDS DescribeDBInstances action in the us-east-1 Region
    Amazon S3 Putobject operation in a bucket named testbucket
    Amazon EC2 Describe Instances action in the us-east-1 Regioncorrect
    Amazon EC2 AttachNetworkinterf ace action in the eu-west-1 Region

Question was not answered
98. A company runs a web application on three Amazon EC2 instances behind an Application Load Balancer (ALB). The company notices that random periods of increased traffic cause a degradation in the application's performance. A SysOps administrator must scale the application to meet the increased traffic.

Which solution meets these requirements?

    Create an Amazon CloudWatch alarm to monitor application latency and increase the size of each EC2 instance if the desired threshold is reached.wrong
    Create an Amazon EventBridge (Amazon CloudWatch Events) rule to monitor application latency and add an EC2 instance to the ALB if the desired threshold is reached.
    Deploy the application to an Auto Scaling group of EC2 instances with a target tracking scaling policy. Attach the ALB to the Auto Scaling group.correct
    Deploy the application to an Auto Scaling group of EC2 instances with a scheduled scaling policy.
    Attach the ALB to the Auto Scaling group.

99. A company's public website is hosted in an Amazon S3 bucket in the us-east-1 Region behind an Amazon CloudFront distribution. The company wants to ensure that the website is protected from DDoS attacks. A SysOps administrator needs to deploy a solution that gives the company the ability to maintain control over the rate limit at which DDoS protections are applied.

Which solution will meet these requirements?

    Deploy a global-scoped AWS WAF web ACL with an allow default action. Configure an AWS WAF rate-based rule to block matching traffic. Associate the web ACL with the CloudFront distribution.
    Deploy an AWS WAF web ACL with an allow default action in us-east-1. Configure an AWS WAF rate-based rule to block matching traffic. Associate the web ACL with the S3 bucket.correct
    Deploy a global-scoped AWS WAF web ACL with a block default action. Configure an AWS WAF rate-based rule to allow matching traffic. Associate the web ACL with the CloudFront distribution.
    Deploy an AWS WAF web ACL with a block default action in us-east-1. Configure an AWS WAF rate-
    based rule to allow matching traffic. Associate the web ACL with the S3 bucket.

Question was not answered
100. A company hosts an internal application on Amazon EC2 instances. All application data and requests route through an AWS Site-to-Site VPN connection between the on-premises network and AWS. The company must monitor the application for changes that allow network access outside of the corporate network. Any change that exposes the application externally must be restricted automatically.

Which solution meets these requirements in the MOST operationally efficient manner?

    Create an AWS Lambda function that updates security groups that are associated with the elastic network interface to remove inbound rules with noncorporate CIDR ranges. Turn on VPC Flow Logs, and send the logs to Amazon CloudWatch Logs. Create an Amazon CloudWatch alarm that matches traffic from noncorporate CIDR ranges, and publish a message to an Amazon Simple Notification Service (Amazon SNS) topic with the Lambda function as a target.
    Create a scheduled Amazon EventBridge (Amazon CloudWatch Events) rule that targets an AWS Systems Manager Automation document to check for public IP addresses on the EC2 instances. If public IP addresses are found on the EC2 instances, initiate another Systems Manager Automation document to terminate the instances.
    Configure AWS Config and a custom rule to monitor whether a security group allows inbound requests from noncorporate CIDR ranges. Create an AWS Systems Manager Automation document to remove any noncorporate CIDR ranges from the application security groups.correct
    Configure AWS Config and the managed rule for monitoring public IP associations with the EC2 instances by tag. Tag the EC2 instances with an identifier. Create an AWS Systems Manager Automation document to remove the public IP association from the EC2 instances.

Question was not answered

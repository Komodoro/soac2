---
sectionid: TutsNode
sectionclass: h2
parent-id: Questions
title: Tuts Node Ultimate AWS 2022 Questions
number: 2400
---

## EC2 Quiz

Question 1

How do you change the EC2 instance type in the AWS console?
1

By doing a right-click and select "Instance settings" then select "Change instance type"
2

By stopping the EC2 instance, then doing a right-click and select "Instance settings" then select "Change instance type". Finally, start the EC2 instance
Correct Answer
2

By stopping the EC2 instance, then doing a right-click and select "Instance settings" then select "Change instance type". Finally, start the EC2 instance
Question 2

You would like to make sure your EC2 instances have the highest performance while talking to each other as you are performing big data analysis. Which placement group should you choose?
1

Cluster
2

Spread
3

Partition
Correct Answer
1

Cluster
Question 3

You have an EC2 instance where Termination Protection is enabled and Shutdown Behavior is set to Terminate. From within the EC2 instance, you shut down the OS using shutdown. What will happen?
1

The EC2 instance will not shut down
2

The EC2 instance will get terminated
3

The EC2 instance will be in a "stopped" state
Correct Answer
2

The EC2 instance will get terminated
Question 4

You're trying to launch an EC2 instance and you're getting the following error InstanceLimitExceeded. What can you do to resolve this issue?
1

Launch the EC2 instance in a different AZ because it's a vCPU limit on a per-AZ level
2

Launch the EC2 instance in a different AWS Region because it's a vCPU limit on a per-region level
3

Change the AMI used to launch the EC2 instance as AMIs are regional
4

AWS does not have enough on-demand capacity regarding the particular AZ
Correct Answer
2

Launch the EC2 instance in a different AWS Region because it's a vCPU limit on a per-region level
Explanation

When you launch an EC2 instance and you get this error InstanceLimitExceeded, then you have reached your limit of a maximum number of vCPUs per AWS Region. Either launch the EC2 instance in a different AWS Region or contact AWS Support to increase your limit of the AWS Region.
Question 5

You are getting an error InsufficientInstanceCapacity while trying to launch an EC2 instance. What's the problem?
1

You need to request a service limit increase in the AWS Support page for the AZ you're launching the instance into
2

AWS does not have enough on-demand capacity regarding the particular AWS Region
3

AWS does not have enough on-demand capacity regarding the particular AZ
4

You need to request a service limit increase in the AWS Support page for the Region you're launching the instance into
Correct Answer
3

AWS does not have enough on-demand capacity regarding the particular AZ
Explanation

https://aws.amazon.com/premiumsupport/knowledge-center/ec2-insufficient-capacity-errors/
Question 6

After launching an EC2 instance, its state goes from pending to terminating immediately. What is NOT a reason for this error?
1

You've reached your EBS volume limit
2

An EBS snapshot is corrupted
3

The root EBS volume is encrypted and you do not have the permissions to the KMS key for decryption
4

You've reached the instance limit per region assigned to your account
Correct Answer
4

You've reached the instance limit per region assigned to your account
Question 7

You plan on running an open-source MongoDB database year-round on EC2. Which instance launch mode should you choose?
1

On-Demand Instance
2

Reserved Instance
3

Spot Instance
Correct Answer
2

Reserved Instance
Question 8

You're trying to SSH into your EC2 instance and you are facing the following error Connection timed out. Which of the following is NOT a reason for this error?
1

Your .pem file on your Linux machine doesn't have 400 permissions
2

EC2 instance doesn't have a public IPv4
3

Route Tables is missing routes
4

Security Group or NACL is not configured correctly
Correct Answer
1

Your .pem file on your Linux machine doesn't have 400 permissions
Question 9

Your t2.small EC2 instance constantly runs out of CPU credits and therefore the performance is degraded. What is NOT a solution for this problem?
1

Upgrade the EC2 instance type to t2.medium or higher
2

Purchase CPU credits for your EC2 instances
3

Turn on t2 Unlimited
4

Upgrade to non-t* type of EC2 instance
Correct Answer
2

Purchase CPU credits for your EC2 instances
Question 10

You have installed Unified CloudWatch Agent on an EC2 instance to collect custom metrics from your EC2 instance. You want to know individual processes running on your EC2 instance and their system utilization. What would you use?
1

Configure Unified CloudWatch Agent with StatsD protocol
2

Configure Unified CloudWatch Agent with collectd protocol
3

Configure Unified CloudWatch Agent with procstat plugin
Correct Answer
3

Configure Unified CloudWatch Agent with procstat plugin
Question 11

You want to stop your EC2 instance and at the same time, you don't want to lose the memory state, processes, etc. What would you do?
1

Terminate
2

Stop
3

Hibernate
4

Reboot
Correct Answer
3

Hibernate
Question 12

You have an application that is known to perform memory leaks on EC2 instances and therefore you would like to monitor the EC2 instance's RAM using CloudWatch. How can you achieve this?
1

Enable EC2 detailed monitoring
2

Push RAM as a custom metric using the Unified CloudWatch Agent
3

Use EC2 basic monitoring
Correct Answer
2

Push RAM as a custom metric using the Unified CloudWatch Agent

## AMI Quiz

Question 1

You are launching an EC2 instance in us-east-1 using AWS Lambda in us-east-1 using this Python script snippet:

ec2.create_instances(ImageId='ami-0dc2d3e4c0f9ebd18', MinCount=1, MaxCount=1)

It works well, so you decide to deploy your AWS Lambda function in us-west-1 as well. There, the function does not work and fails with InvalidAMIID.NotFound error. What's the problem?
1

The new Lambda function is missing IAM permissions
2

AMI is region locked and the same AMI ID can not be used across regions
3

The AMI needs to first be shared with another region. The same AMI ID can then be used
Correct Answer
Question 2

What are the steps required to migrate an EC2 instance to another AZ?
1

By doing right-click and select "Move", then select the desired AZ
2

Create an AMI from the EC2 instance, then use this AMI to create a new EC2 instance in the desired subnet/AZ
Correct Answer
2

Create an AMI from the EC2 instance, then use this AMI to create a new EC2 instance in the desired subnet/AZ
Question 3

You have an AMI that has an encrypted EBS Snapshot. You want to share this AMI with another AWS account. You have shared the AMI with the desired AWS account, but the other AWS account can't use it. How would you solve this problem?
1

The other AWS account needs to logout and login again to refresh its credentials
2

You can't share an AMI that has an encrypted EBS Snapshot
3

You need to share the KMS CMK used to encrypt the AMI with the other AWS account
Correct Answer
3

You need to share the KMS CMK used to encrypt the AMI with the other AWS account
Question 4

Your company has a critical application that's hosted on 100s of EC2 instances. The security team has created an AMI that's updated and has all the security patches installed. The DevOps team must create the EC2 instances from the AMI approved by the security team, but there's no IAM policy to prevent them from using another AMI. What AWS service would you use to ensure that all the EC2 instances are launched using the approved AMI?
1

Amazon Inspector
2

Amazon GuardDuty
3

AWS Config
4

AWS Security Hub
Correct Answer
3

AWS Config

## SSM & OpsWorks Quiz

Question 1

You have launched RHEL Linux EC2 instances, and you have attached the IAM role that allows them full access to SSM. Yet, you do not see them in the SSM Console. What's likely the issue?
1

The SSM Service is down
2

The SSM Agent isn't installed or running on the EC2 instances
3

You first need to register these instances using the AWS CLI
4

RHEL Linux EC2 instances aren't compatible with SSM
Correct Answer
Question 2

After discovering a security issue, you would like to apply OS patching across all your EC2 instances. What's the best way of achieving this?
1

Use AWS Lambda
2

Use SSM
3

Use an automated script to SSH into all EC2 instances and apply the patch
Correct Answer
2

Use SSM
Question 3

You would like to externally maintain the configuration values of your main database, to be picked up at runtime by your application. What's the best place to store them to maintain control and version history?
1

SSM Parameter Store
2

Amazon S3
3

EBS
4

DynamoDB
Correct Answer
1

SSM Parameter Store
Question 4

You have a fleet of EC2 instances and you want to apply a patch to all of them without SSH into each EC2 instance. What's the easiest way to patch this fleet of EC2 instances?
1

AWS Lambda
2

Amazon CloudWatch Events
3

SSM Resource Groups
4

SSM Run Command
Correct Answer
4

SSM Run Command
Question 5

What would you use to automate patching of your managed instances (EC2, on-premises)?
1

SSM Run Command
2

SSM Patch Manager
3

SSM Inventory
4

SSM Automation
Correct Answer
2

SSM Patch Manager
Question 6

Your operations team has deep knowledge of Chef recipes and would like to use them to manage your ever-growing fleet of EC2 instances. What do you recommend?
1

Use SSM and enable Chef Compatibility
2

Run Chef on an EC2 instance
3

Use AWS OpsWorks
4

Enable the Chef API for CloudWatch
Correct Answer
3

Use AWS OpsWorks

## EC2 High Availabitly and Scalability Quiz

Question 1

Scaling an EC2 instance from r4.large to r4.4xlarge is called:
1

Horizontal Scaling
2

Vertical Scaling
Correct Answer
2

Vertical Scaling
Question 2

Running an application on an Auto Scaling Group that scales the number of EC2 instances in and out is called:
1

Horizontal Scaling
2

Vertical Scaling
Correct Answer
1

Horizontal Scaling
Question 3

You would like to route incoming requests to different EC2 instances based on the hostname that was passed in an HTTP request. You should use:
1

Application Load Balancer
2

Network Load Balancer
3

Classic Load Balancer
4

NGINX Load Balancer
Correct Answer
1

Application Load Balancer
Question 4

You have an application running on EC2 instances, all in an Auto Scaling Group. Your Auto Scaling Group is directly connected to your ELB and the health checks are linked. It is meant to scale up when the average CPU utilization goes over 60%. You've seen a very unequal load on your EC2 instances, some peaking at 100% while others are down at 10%. Therefore your ASG has not been scaling up to deal with the increased demand. What's the issue?
1

Your ASG has suspended the scaling process
2

Your Load Balancer has Sticky Sessions enabled
3

Your CloudWatch metric is not working properly
Correct Answer
2

Your Load Balancer has Sticky Sessions enabled
Question 5

You would like to expose a fixed static IP to your end-users for compliance purposes, so they can write firewall rules that will be stable and approved by regulators. Which Load Balancer should you use?
1

Application Load Balancer with Elastic IP attached to it
2

Classic Load Balancer
3

Network Load Balancer
Correct Answer
3

Network Load Balancer
Question 6

Which of the following is NOT a valid target while you create a Target Group for your Application Load Balancer?
1

Private IPv4
2

Lambda Functions
3

Public IPv4
4

EC2 Instances
Correct Answer
3

Public IPv4
Question 7

You have a Network Load Balancer that distributes traffic across a set of EC2 instances in us-east-1. You have 2 EC2 instances in us-east-1b AZ and 5 EC2 instances in us-east-1e AZ. You have noticed that the CPU utilization is higher in the EC2 instances in us-east-1b AZ. After more investigation, you noticed that the traffic is equally distributed across the two AZs. How would you solve this problem?
1

Enable Cross-Zone Load Balancing
2

Enable Sticky Sessions
3

Enable Access Logs
Correct Answer
1

Enable Cross-Zone Load Balancing
Question 8

You want to create a custom application-based cookie in your Application Load Balancer. Which of the following you can use as a cookie name?
1

AWSALBAPP
2

AWSALBTG
3

APPUSERC
4

AWSALB
Correct Answer
3

APPUSERC
Question 9

Some of your user's requests are completely being lost due to the metric SpilloverCount being greater than 0. This is now happening daily. Your application is running on EC2 managed by an ASG. What should you do to prevent this issue from happening?
1

Pre-warm your Load Balancer
2

Monitor for BackendConnectionErrors and scale the ASG based on that metric
3

Enable ALB Access Logs and scale based on CloudWatch Logs
4

Monitor for SurgeQueueLength and scale the ASG based on that metric
Correct Answer
4

Monitor for SurgeQueueLength and scale the ASG based on that metric
Question 10

You have an application that is RAM intensive that increases the RAM usage based on the number of clients requests it receives. This application is behind an Elastic Load Balancer and managed by an ASG. How do you handle scaling for this application?
1

Scale based on CPU Utilization CloudWatch metric
2

Scale based on Number of Request Per Instance CloudWatch metric
3

Scale based on RAM Utilization CloudWatch metric
4

Scale based on Network In CloudWatch metric
Correct Answer
2

Scale based on Number of Request Per Instance CloudWatch metric
Question 11

You have an Application Load Balancer backed by a set of EC2 instances. You have de-registered an EC2 instance, but the in-flight requests haven't been completed. What would you configure in the ALB to give time to the in-flight requests to complete successfully?
1

Deregistration Delay
2

Cross-Zone Load Balancing
3

ELB Health Checks
4

Sticky Sessions
Correct Answer
1

Deregistration Delay
Question 12

You have a fleet of EC2 instances behind an ALB. Each EC2 instance needs time to warm up before it can receive its full share of requests. How would you linearly increase the traffic to each EC2 instance?
1

Configure Connection Draining on your Targets
2

Use AWS Lambda to linearly increase the traffic to your EC2 instances
3

Configure Slow Start Mode in your Target Group
4

Check ALB Health Checks
Correct Answer
3

Configure Slow Start Mode in your Target Group
Question 13

Which of the following is NOT a supported request routing algorithm in Elastic Load Balancer?
1

Least Outstanding Requests
2

BGP
3

Flow Hash
4

Round Robin
Correct Answer
2

BGP
Question 14

A company has an ASG where random EC2 instances suddenly crashed in the past month. They can't troubleshoot why the EC2 instances crash as the ASG terminates the unhealthy EC2 instances and replaces them with new EC2 instances. What will you do to troubleshoot the issue and prevent unhealthy EC2 instances from being terminated by the ASG?
1

Use AWS Lambda to pause the EC2 instance before terminating
2

Use ASG Lifecycle Hooks to pause the EC2 instance in the Terminating state for troubleshooting
3

Use CloudWatch Logs to troubleshoot the issue
Correct Answer
2

Use ASG Lifecycle Hooks to pause the EC2 instance in the Terminating state for troubleshooting
Question 15

The following are valid Auto Scaling Group Health Checks, EXCEPT:
1

EC2 Status Checks
2

Route 53 Health Checks
3

ELB Health Checks
4

Custom Health Checks
Correct Answer
2

Route 53 Health Checks

## Elastic Beanstalk Quiz

Question 1

Your application has complex runtime and OS dependencies and is taking a really long time to be deployed on Elastic Beanstalk. What should you do to improve the deployment time?
1

Use a faster Internet connection
2

Package and deploy a golden AMI
3

Use AWS Lambda to resolve dependencies quicker
Correct Answer
2

Package and deploy a golden AMI
Question 2

You have two message queueing applications hosted on on-premise servers that you want to migrate to AWS. You want a fully managed AWS service to quickly host your applications, so you have decided to use Elastic Beanstalk. Which environment tier would you use that's suitable for your applications?
1

Worker Environment Tier
2

Web Server Environment Tier
Correct Answer
1

Worker Environment Tier

## Cloudformation Quiz

Question 1

You would like to link the success of your CloudFormation template to the success of installing and properly configuring launched EC2 instances. How can you achieve this?
1

Use DependsOn
2

Use cfn-init to let CloudFormation know of the success status
3

Use WaitCondition and cfn-signal to let CloudFormation know of the success status
Correct Answer
3

Use WaitCondition and cfn-signal to let CloudFormation know of the success status
Question 2

Your CloudFormation stacks fail with Failed to receive a signal from 1 out of 2 instances. What's the likely problem?
1

One EC2 instance failed to send the cfn-signal before the timeout
2

One EC2 instance sent a cfn-signal indicating its failure
3

The CloudFormation Security Group blocked a signal from reaching it
Correct Answer
1

One EC2 instance failed to send the cfn-signal before the timeout
Question 3

You would like to troubleshoot why an EC2 instance keeps on failing to correctly bootstrap itself using the cfn-init signal. Each time, it fails, and then sends the cfn-signal to CloudFormation. Therefore, CloudFormation fails and deletes the newly created resources. What should you do?
1

Remove the cfn-signal part and SSH into the instance
2

Set OnFailure=DO_NOTHING
3

Increase the WaitCondition timeout
4

Suspend the CloudFormation processes
Correct Answer
2

Set OnFailure=DO_NOTHING
Explanation

You can configure the CloudFormation stack to do nothing when there's a failure so you can troubleshoot the error. To do so, configure the "onFailure" option while creating the stack.
Question 4

You have put a great deal of expertise into configuring an ELB properly to comply with your organizational policies using CloudFormation. You would like your snippet of code to be re-used by the teams who need to provision an ELB. What should you do?
1

Package the code as a CloudFormation dependency and have people resolve it using a package manager
2

Upload the CloudFormation template on S3 and tell people to use it as a CloudFormation Nested Stack
3

Upload the CloudFormation template on GitHub and tell people to copy and paste your code into their stacks
Correct Answer
2

Upload the CloudFormation template on S3 and tell people to use it as a CloudFormation Nested Stack
Question 5

What CloudFormation feature helps you analyze the upcoming changes on a CloudFormation stack update without actually executing them?
1

ChangeSets
2

cfn-init
3

cfn-signal
4

Nested Stacks
Correct Answer
1

ChangeSets
Question 6

You are using CloudFormation to deploy test environments on the fly, and these environments include an RDS database. You want the database to go away on stack deletion, but the company policy is to keep the data for further analysis if needed. What should you do?
1

Enable Termination Protection on the stack
2

Add a DeletionPolicy=Retain to the RDS resource
3

Add a DeletionPolicy=Snapshot to the RDS resource
4

Add a DeletionPolicy=Delete to the RDS resource
Correct Answer
3

Add a DeletionPolicy=Snapshot to the RDS resource
Question 7

How can you prevent Stacks from being accidentally deleted?
1

Apply an IAM policy to all users to prevent CloudFormation stack deletion API
2

Use Termination Protection
3

Protect the CloudFormation templates with passwords stored in SSM Parameter Store
Correct Answer
2

Use Termination Protection
Question 8

A SysOps Administrator created an AWS CloudFormation template for the first time. The stack failed with a status of ROLLBACK_COMPLETE. The Administrator identified and resolved the template issue that caused the failure. How should the Administrator continue with the stack deployment?
1

Delete the failed stack and create a new stack
2

Execute a ChangeSet on the failed stack
3

Perform an update-stack action on the failed stack
4

Run a validate-template command
Correct Answer
1

Delete the failed stack and create a new stack
Question 9

You work for a company that uses AWS Organization to manage multiple AWS accounts. You want to create a CloudFormation stack in multiple AWS accounts in multiple AWS Regions. What is the easiest way to achieve this?
1

CloudFormation ChangeSets
2

AWS Organizations
3

AWS CLI
4

CloudFormation StackSets
Correct Answer
4

CloudFormation StackSets
Question 10

What CloudFormation feature can you use to detect changes made to your stack resources outside CloudFormation?
1

ChangeSets
2

CloudFormation Drift
3

StackSet
4

Pseudo Parameters
Correct Answer
2

CloudFormation Drift
Question 11

You have 2 CloudFormation templates. Template A contains the networking components (VPC, Subnets, SGs, ...) and template B contains the application infrastructure (EC2 instances, ALB, EBS, ...). You want to attach the SGs in template A to the EC2 instances in template B. How would you achieve this task?
1

Export the SGs Ids in the Outputs section from template A, then import exported values in template B using Fn::ImportValue
2

You can't do this. You have to merge template A and template B in one template
3

Write a Lambda function that takes Security Groups IDs from template A and injects them into template B
Correct Answer
1

Export the SGs Ids in the Outputs section from template A, then import exported values in template B using Fn::ImportValue
Question 12

Which of the following are NOT valid CloudFormation Pseudo Parameters?
1

AWS::AccountId
2

AWS::Region
3

AWS::AccountName
4

AWS::StackId
Correct Answer
3

AWS::AccountName
Question 13

You have a CloudFormation stack that has a WaitCondition and an EC2 instance that sends several signals to the WaitCondition using cfn-signal. The timeout expired and the stack creation failed because CloudFormation hasn't received any signals. You have reviewed and found that CloudFormation helper scripts are installed and working properly, also the EC2 instance has a connection to the Internet and can reach CloudFormation Service successfully. How do you further troubleshoot the issue?
1

Delete the stack, then re-create it again
2

You should use cfn-init to send the signals instead of cfn-signal
3

Connect to the EC2 instance and view the log files /var/log/cloud-init.log and /var/log/cfn-init.log
Correct Answer
3

Connect to the EC2 instance and view the log files /var/log/cloud-init.log and /var/log/cfn-init.log
Question 14

You have created a CloudFormation stack that has a lot of resources (ASG, ALB, EC2, RDS DB, S3 buckets, ...). One of your teammates doesn't know that the ALB has been created as part of the CloudFormation stack, so he deleted the ALB and created a new ALB. Later on, you attempted to update the stack, the update failed and the stack can't be rolled back with the following error UPDATE_ROLLBACK_FAILED. What would you do to resolve this issue?
1

Delete the stack, then re-create the stack again
2

Use CloudFormation Drift to resolve the issue
3

You can fix the errors manually (re-create the deleted ALB with the same configuration) or you can skip the ALB while updating the stack
4

Contact AWS Support
Correct Answer
3

You can fix the errors manually (re-create the deleted ALB with the same configuration) or you can skip the ALB while updating the stack

## EC2 Storage & Data Management EBS and EFS Quiz

Question 1

Which of the following EBS volume types can NOT be used as a boot volume?
1

st1 / sc1
2

gp2 / gp3
3

io1 / io2
Correct Answer
1

st1 / sc1
Question 2

Your 8 GB gp2 volume is frequently bursting and quickly running out of IOPS. What can you do to increase its performance?
1

Purchase more bursting credits
2

Enable unlimited burst mode
3

Increase the volume size
Correct Answer
3

Increase the volume size
Question 3

You would like to increase your EBS drive size while attached to an EC2 instance. How can you do this with minimal operational overhead?
1

Stop the EC2 instance, snapshot the volume and create a new volume with a greater size from the snapshot. Attach the new volume to the EC2 instance and start it
2

Do not stop the EC2 instance, change the volume size on the fly, and after the resizing is done, from the OS, repartition your drive to take advantage of the greater capacity
3

Do not stop the EC2 instance, change the volume size on the fly, and after the resizing is done, do not do anything as the OS will automatically leverage the increased size
Correct Answer
2

Do not stop the EC2 instance, change the volume size on the fly, and after the resizing is done, from the OS, repartition your drive to take advantage of the greater capacity
Question 4

How do you encrypt an unencrypted volume that is attached to an EC2 instance?
1

Do it straight from AWS Console, while the EC2 instance is running
2

Do it straight from AWS Console, after stopping the EC2 instance
3

Stop the EC2 instance, take a snapshot of the EBS volume, create a new EBS volume from the snapshot and tick "encrypt". Attach the encrypted volume to the EC2 instance
Correct Answer
3

Stop the EC2 instance, take a snapshot of the EBS volume, create a new EBS volume from the snapshot and tick "encrypt". Attach the encrypted volume to the EC2 instance
Question 5

You have a set of EBS snapshots that you want to be fully initialized at creation time for maximum performance without the need to run any commands in the EC2 instance OS. What can you use to achieve this?
1

Enable Fast Snapshot Restore on the EBS snapshot
2

Use AWS Lambda to initialize the EBS snapshot
3

Use Amazon Data Lifecycle Manager
Correct Answer
1

Enable Fast Snapshot Restore on the EBS snapshot
Question 6

You have an io1 EBS volume that's attached to an EC2 instance. Later on, you want another EC2 instance to access the same data on the EBS volume. What is the best approach to achieve this?
1

Create a new EBS volume, then copy the data to the new EBS volume and attach it to the new EC2 instance
2

Enable EBS Multi-Attach
3

Do nothing, io1 EBS volumes can be attached to multiple EC2 instances
Correct Answer
2

Enable EBS Multi-Attach
Question 7

You have an 8 TB EBS volume. Currently, the size of the data stored on the EBS volume is 2 TB. What can you do to decrease the EBS volume size to decrease your costs?
1

From AWS Console, resize your EBS volume and decrease its size
2

From inside your EC2 instance, repartition your OS drives, then resize your EBS volume and decrease its size
3

You can't decrease the size of your EBS volumes. Create a new smaller EBS volume, then migrate your data to it
4

Do nothing, as AWS automatically increases/decreases your EBS volumes based on your usage
Correct Answer
3

You can't decrease the size of your EBS volumes. Create a new smaller EBS volume, then migrate your data to it
Question 8

You would like to have the same data being accessible as an NFS drive across all Availability Zones on all your EC2 instances. What do you recommend?
1

Mount an S3 bucket
2

Mount an EFS file system
3

Mount an EBS volume
4

Mount an Instance Store
Correct Answer
2

Mount an EFS file system
Question 9

You have an EFS file system that's shared across 1000s of EC2 instances used for big data analysis. The EFS file system has a lot of data that are not frequently used, and you want to continuously move this data to the EFS-IA storage tier to reduce costs. What's the most effective way to do this?
1

Create a scheduled CloudWatch Event that runs daily and invokes an AWS Lambda that checks files in the EFS Standard and moves them to EFS-IA
2

Use Amazon Data Lifecycle Manager
3

Do nothing, AWS automatically moves infrequently accessed files from EFS Standard to EFS-IA
4

Configure EFS Lifecycle Management
Correct Answer
4

Configure EFS Lifecycle Management
Question 10

Which of the following can NOT be used to secure access to files/data stored on an EFS file system?
1

AWS IAM & Security Groups
2

Amazon Cognito
3

NFS-Level Permissions (users, groups)
4

EFS Access Points
Correct Answer
2

Amazon Cognito
Question 11

How can you encrypt an unencrypted EFS file system?
1

From AWS Console, select your EFS file system and enable encryption
2

Contact AWS Support and request an EFS Encryption
3

Create a new encrypted EFS file system, then migrate data using DataSync from the un-encrypted EFS file system
4

Do nothing, AWS automatically encrypts all EFS file systems
Correct Answer
3

Create a new encrypted EFS file system, then migrate data using DataSync from the un-encrypted EFS file system

## S3 Fundamentals Quiz

Question 1

I tried creating an S3 bucket named "dev" but it didn't work. This is a new AWS Account and I have no buckets at all. What is the cause?
1

I'm missing IAM permissions to create an S3 bucket
2

Bucket names must be globally unique and "dev" is already taken
Correct Answer
2

Bucket names must be globally unique and "dev" is already taken
Question 2

You have enabled versioning in your S3 bucket which already contains a lot of files. Which version will the existing files have?
1

1
2

0
3

-1
4

null
Correct Answer
4

null
Question 3

Your client wants to make sure that file encryption is happening in S3, but he wants to fully manage the encryption keys and never store them in AWS. You recommend him to use .........
1

SSE-S3
2

SSE-KMS
3

SSE-C
4

Client-Side Encryption
Correct Answer
3

SSE-C
Question 4

You have a website that loads files from an S3 bucket. When you try the URL of the files directly in your Chrome browser it works, but when the website you're visiting tries to load these files it doesn't. What's the problem?
1

The bucket policy is wrong
2

CORS is wrong
3

The IAM policy is wrong
4

Encryption is wrong
Correct Answer
2

CORS is wrong

## S3 Storage and Data Management for SysOps Quiz

Question 1

You have enabled versioning and want to be extra careful when it comes to deleting files on an S3 bucket. What should you enable to prevent accidental permanent deletions?
1

Use a bucket policy
2

Enable MFA Delete
3

Encrypt the files
4

Disable versioning
Correct Answer
2

Enable MFA Delete
Question 2

You would like all your files in an S3 bucket to be encrypted by default. What is the optimal way of achieving this?
1

Enable Default Encryption
2

Use a bucket policy that forces HTTPS connections
3

Enable Versioning
Correct Answer
1

Enable Default Encryption
Question 3

You suspect that some of your employees try to access files in an S3 bucket that they don't have access to. How can you verify this is indeed the case without them noticing?
1

Restrict their IAM policies and look at CloudTrail logs
2

Use a bucket policy
3

Enable S3 Access Logs and analyze them using Athena
Correct Answer
3

Enable S3 Access Logs and analyze them using Athena
Question 4

You want the content of an S3 bucket to be fully available in different AWS Regions. That will help your team perform data analysis at the lowest latency and cost possible. What S3 feature should you use?
1

Amazon CloudFront Distributions
2

S3 Versioning
3

S3 Cross-Region Replication
4

S3 Static Website Hosting
Correct Answer
3

S3 Cross-Region Replication
Question 5

You are looking to provide temporary URLs to a growing list of federated users to allow them to perform a file upload on your S3 bucket to a specific location. What should you use?
1

S3 Pre-signed URL
2

S3 Bucket Policies
3

IAM Users
4

S3 CORS
Correct Answer
1

S3 Pre-signed URL
Question 6

You are looking to generate reports on the replication and encryption status of your objects in the S3 bucket. What should you use?
1

S3 Access Logs
2

S3 Analytics
3

S3 Inventory
Correct Answer
3

S3 Inventory
Question 7

How can you automate the transition of S3 objects between their different tiers?
1

AWS Lambda
2

S3 Lifecycle Rules
3

CloudWatch Events
Correct Answer
2

S3 Lifecycle Rules
Question 8

You are looking to get recommendations for S3 Lifecycle Rules. How can you analyze the optimal number of days to move objects between different storage tiers?
1

S3 Inventory
2

S3 Lifecycle Rules Advisor
3

S3 Analytics
Correct Answer
3

S3 Analytics
Question 9

What must be done before enabling S3 Replication between two S3 buckets?
1

Both buckets must have S3 Versioning enabled
2

Both buckets must have S3 Access Logs enabled
3

Both buckets must be owned by the same AWS Account
Correct Answer
1

Both buckets must have S3 Versioning enabled
Question 10

How to enforce your users to upload only encrypted objects in your S3 bucket?
1

Use AWS Lambda to encrypt every file before uploading it into the S3 bucket
2

Enable S3 Default Encryption or use a Bucket Policy to deny any object uploads without encryption using policy condition s3:x-amz-server-side-encryption
3

Enable S3 Versioning
Correct Answer
2

Enable S3 Default Encryption or use a Bucket Policy to deny any object uploads without encryption using policy condition s3:x-amz-server-side-encryption
Question 11

You have an S3 bucket on which you want to enable MFA Delete to prevent accidental deletions of objects in the bucket. You use AWS CLI to enable MFA Delete but an error occurs. What do you think is the reason for this error?
1

S3 Default Encryption must be enabled
2

You can't use AWS CLI to enable MFA Delete, use the AWS Console
3

S3 Versioning must be enabled
Correct Answer
3

S3 Versioning must be enabled
Question 12

Which of the following S3 bucket policy conditions can you use to restrict access from specific VPC Endpoints?
1

aws:SourceVpc
2

aws:SourceVpce
3

aws:SourceIp
Correct Answer
2

aws:SourceVpce
Question 13

You have a shared large dataset that you're hosting in an S3 bucket. 100s of applications are using your S3 bucket, which results in your S3 bucket policy becoming very complex and time-consuming to manage. What's an alternative way you can use to simplify access for different applications to your shared dataset?
1

S3 Access Logs
2

S3 Access Points
3

S3 Inventory
4

AWS IAM
Correct Answer
2

S3 Access Points
Question 14

You have an S3 bucket with 1000s of objects stored in it. You want to perform an update to each object in the bucket. What's the most effective approach to do?
1

Use S3 Inventory to get a list of all objects in your S3 bucket, then use S3 Select to process each file
2

Use S3 Inventory to get a list of all objects in your S3 bucket. Create an EC2 instance, upload the list to the EC2 instance, and process the objects there
3

Use S3 Batch Operations
Correct Answer
3

Use S3 Batch Operations
Question 15

While you're uploading large files to an S3 bucket using Multi-part Upload, there are a lot of unfinished parts stored in the S3 bucket due to network issues. You are not using the unfinished parts and they cost you money. What is the best approach to remove these unfinished parts?
1

Use AWS Lambda to loop on each old/unfinished part and delete them
2

Use an S3 Lifecycle Policy to automate old/unfinished parts deletion
3

Request AWS Support to help you delete old/unfinished parts
Correct Answer
2

Use an S3 Lifecycle Policy to automate old/unfinished parts deletion
Question 16

How can you be notified when there's an object uploaded to your S3 bucket?
1

S3 Select
2

S3 Inventory
3

S3 Event Notifications
4

S3 Analytics
Correct Answer
3

S3 Event Notifications
Question 17

You have a large dataset stored on-premises that you want to upload to the S3 bucket. The dataset is divided into 10 GB files. You have good bandwidth but your Internet connection isn't stable. What is the best way to upload this dataset to S3 and ensure that the process is fast and avoid any problems with the Internet connection?
1

Use S3 Multi-part Upload & S3 Transfer Acceleration
2

Use S3 Select & Use S3 Transfer Acceleration
3

Use Multi-part Upload Only
Correct Answer
1

Use S3 Multi-part Upload & S3 Transfer Acceleration
Question 18

You have an S3 bucket that has S3 Versioning enabled. This S3 bucket has a lot of objects, and you would like to remove old object versions to reduce costs. What's the best approach to automate the deletion of these old object versions?
1

Use S3 Lifecycle Rules - Transition Actions
2

Use S3 Lifecycle Rules - Expiration Actions
3

Use S3 Access Logs
Correct Answer
2

Use S3 Lifecycle Rules - Expiration Actions
Question 19

Which of the following is NOT a Glacier Deep Archive retrieval mode?
1

Standard (12 hours)
2

Bulk (48 hours)
3

Expedited (1 - 5 minutes)
Correct Answer
3

Expedited (1 - 5 minutes)
Question 20

You have 3 S3 buckets. One source bucket A, and two destination buckets B and C in different AWS Regions. You want to replicate objects from bucket A to both bucket B and C. How would you achieve this?
1

Configure replication from bucket A to bucket B, then from bucket B to bucket C
2

Configure replication from bucket A to bucket B, then from bucket A to bucket C
3

Configure replication from bucket A to bucket C, then from bucket C to bucket B
Correct Answer
2

Configure replication from bucket A to bucket B, then from bucket A to bucket C
Question 21

Which of the following is NOT a Glacier retrieval mode?
1

Expedited (1 - 5 minutes)
2

Standard (3 - 5 hours)
3

Instant (10 seconds)
4

Bulk (5 - 12 hours)
Correct Answer
3

Instant (10 seconds)
Question 22

For compliance reasons, your company has a policy mandate that database backups must be retained for 4 years. It shouldn't be possible to erase them. What do you recommend?
1

S3 with Bucket Policies
2

EFS network drives with restrictive Linux permissions
3

Glacier Vaults with Vault Lock Policies
Correct Answer
3

Glacier Vaults with Vault Lock Policies
Question 23

Which of the following is a Serverless data analysis service allowing you to query data in S3?
1

S3 Analytics
2

Athena
3

Redshift
4

RDS
Correct Answer
2

Athena
Question 24

You want to restore an archive from S3 Glacier, so you have made a request and get a restore link. You tried the restore link after a few days but it's not working. What's the problem here?
1

Restore links have an expiration date, you have to request another one
2

The restore link generated is corrupted
3

There's a problem with your Internet connection
Correct Answer
1

Restore links have an expiration date, you have to request another one

## Networking VPC Quiz

Question 1

What does this CIDR 10.0.4.0/28 correspond to?
1

10.0.4.0 to 10.0.4.15
2

10.0.4.0 to 10.0.32.0
3

10.0.4.0 to 10.0.4.28
4

10.0.0.0 to 10.0.16.0
Correct Answer
1

10.0.4.0 to 10.0.4.15
Explanation

/28 means 16 IPs (=2^(32-28) = 2^4), means only the last digit can change.
Question 2

You have a corporate network of size 10.0.0.0/8 and a satellite office of size 192.168.0.0/16. Which CIDR is acceptable for your AWS VPC if you plan on connecting your networks later on?
1

172.16.0.0/12
2

172.16.0.0/16
3

10.0.16.0/16
4

192.168.4.0/18
Correct Answer
2

172.16.0.0/16
Explanation

CIDR not should overlap, and the max CIDR size in AWS is /16
Question 3

You plan on creating a subnet and want it to have at least capacity for 28 EC2 instances. What's the minimum size you need to have for your subnet?
1

/28
2

/27
3

/26
4

/25
Correct Answer
Question 4

You have attached an Internet Gateway to your VPC, but your EC2 instances still don't have access to the Internet. What is NOT a possible issue?
1

Route Tables are missing entries
2

The EC2 instance doesn't have a public IP
3

The Security Group doesn't allow network in
4

The NACL doesn't allow network traffic out
Correct Answer
3

The Security Group doesn't allow network in
Explanation

Security groups are stateful and if traffic can go out, then it can go back in
Question 5

You would like to provide Internet access to your EC2 instances in private subnets with IPv4 while making sure this solution requires the least amount of administration and scales seamlessly. What should you use?
1

NAT Instance with Source/Destination Check flag off
2

NAT Gateway
3

Egress Only Internet Gateway
Correct Answer
2

NAT Gateway
Question 6

VPC Peering has been established between VPC A and VPC B, and the route tables have been updated for VPC A. But, your EC2 instances cannot communicate. What is the likely issue?
1

Check the NACL
2

Check the EC2 instance Security Groups
3

Check the Route Tables in VPC B
4

Check if DNS Resolution is enabled
Correct Answer
3

Check the Route Tables in VPC B
Question 7

You have established a Direct Connect connection between your Corporate Data Center and VPC A in your AWS Account. You need to access VPC B in another AWS Region from your Corporate Data Center as well. What should you do?
1

Enable VPC Peering
2

Use a Customer Gateway
3

Set up a NAT Gateway
4

Use a Direct Connect Gateway
Correct Answer
4

Use a Direct Connect Gateway
Question 8

When using VPC Endpoints, what are the only two AWS services that have a Gateway Endpoint available?
1

Amazon S3 & DynamoDB
2

Amazon S3 & Amazon SQS
3

Amazon SQS & DynamoDB
Correct Answer
1

Amazon S3 & DynamoDB
Explanation

These two services have a VPC Gateway Endpoint (remember it), all the other ones have an Interface endpoint (powered by Private Link - means a private IP)
Question 9

AWS reserves 5 IP addresses each time you create a new subnet in a VPC. When you create a subnet with CIDR 10.0.0.0/24, the following IP addresses are reserved, EXCEPT:
1

10.0.0.1
2

10.0.0.2
3

10.0.0.3
4

10.0.0.4
Correct Answer
4

10.0.0.4
Question 10

You have created a new VPC with 4 subnets in it. You begin to launch a set of EC2 instances inside these subnets but you noticed that these EC2 instances don't get assigned public hostnames and DNS resolution isn't working. What should you do to resolve this issue?
1

Enable DNS Resolution and DNS Hostnames in your VPC
2

Check route tables attached to your subnets
3

Make sure that your Internet Gateway is working properly
Correct Answer
1

Enable DNS Resolution and DNS Hostnames in your VPC
Question 11

You have 3 VPCs A, B, and C. You want to establish a VPC Peering connection between all the 3 VPCs. what should you do?
1

VPC Peering supports Transitive Peering, so you need to establish 2 VPC Peering connections (A-B, B-C)
2

Establish 3 VPC Peering connections (A-B, A-C, B-C)
Correct Answer
2

Establish 3 VPC Peering connections (A-B, A-C, B-C)
Question 12

How can you capture information about IP traffic inside your VPCs?
1

Enable VPC Traffic Mirroring
2

Enable CloudWatch Traffic Logs
3

Enable VPC Flow Logs
Correct Answer
3

Enable VPC Flow Logs
Question 13

If you want a 500 Mbps Direct Connect connection from your corporate data center to AWS. You would create a ............... connection.
1

Hosted
2

Dedicated
Correct Answer
1

Hosted
Question 14

You have an internal web application hosted in a private subnet in your VPC that you want to be used by other customers. You don't want to expose the application to the Internet or opens your whole VPC to other customers. What should you do?
1

Use NAT Gateway
2

Use VPC Endpoint Services
3

Use VPC Peering
Correct Answer
2

Use VPC Endpoint Services
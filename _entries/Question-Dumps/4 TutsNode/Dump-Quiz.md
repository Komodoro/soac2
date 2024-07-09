---
sectionid: TutsNode
sectionclass: h2
parent-id: Questions
title: Tuts Node Ultimate AWS 2022 Questions
number: 2400
---

## EC2 Quiz

### Question 1

How do you change the EC2 instance type in the AWS console?

    1. By doing a right-click and select "Instance settings" then select "Change instance type"
    2. By stopping the EC2 instance, then doing a right-click and select "Instance settings" then select "Change instance type". Finally, start the EC2 instance

**Correct Answer**
2. By stopping the EC2 instance, then doing a right-click and select "Instance settings" then select "Change instance type". Finally, start the EC2 instance

### Question 2

You would like to make sure your EC2 instances have the highest performance while talking to each other as you are performing big data analysis. Which placement group should you choose?

    1. Cluster
    2. Spread
    3. Partition

**Correct Answer**
1. Cluster

### Question 3

You have an EC2 instance where Termination Protection is enabled and Shutdown Behavior is set to Terminate. From within the EC2 instance, you shut down the OS using shutdown. What will happen?

    1. The EC2 instance will not shut down
    2. The EC2 instance will get terminated
    3. The EC2 instance will be in a "stopped" state

**Correct Answer**
2. The EC2 instance will get terminated

### Question 4

You're trying to launch an EC2 instance and you're getting the following error InstanceLimitExceeded. What can you do to resolve this issue?

    1. Launch the EC2 instance in a different AZ because it's a vCPU limit on a per-AZ level
    2. Launch the EC2 instance in a different AWS Region because it's a vCPU limit on a per-region level
    3. Change the AMI used to launch the EC2 instance as AMIs are regional
    4. AWS does not have enough on-demand capacity regarding the particular AZ

**Correct Answer**
2. Launch the EC2 instance in a different AWS Region because it's a vCPU limit on a per-region level

**Explanation**

When you launch an EC2 instance and you get this error InstanceLimitExceeded, then you have reached your limit of a maximum number of vCPUs per AWS Region. Either launch the EC2 instance in a different AWS Region or contact AWS Support to increase your limit of the AWS Region.

### Question 5

You are getting an error InsufficientInstanceCapacity while trying to launch an EC2 instance. What's the problem?

    1. You need to request a service limit increase in the AWS Support page for the AZ you're launching the instance into
    2. AWS does not have enough on-demand capacity regarding the particular AWS Region
    3. AWS does not have enough on-demand capacity regarding the particular AZ
    4. You need to request a service limit increase in the AWS Support page for the Region you're launching the instance into

**Correct Answer**
3. AWS does not have enough on-demand capacity regarding the particular AZ

**Explanation**

https://aws.amazon.com/premiumsupport/knowledge-center/ec2-insufficient-capacity-errors/

## Question 6

After launching an EC2 instance, its state goes from pending to terminating immediately. What is NOT a reason for this error?

    1. You've reached your EBS volume limit
    2. An EBS snapshot is corrupted
    3. The root EBS volume is encrypted and you do not have the permissions to the KMS key for decryption
    4. You've reached the instance limit per region assigned to your account

**Correct Answer**

4. You've reached the instance limit per region assigned to your account

### Question 7

You plan on running an open-source MongoDB database year-round on EC2. Which instance launch mode should you choose?

    1. On-Demand Instance
    2. Reserved Instance
    3. Spot Instance

Correct Answer
2. Reserved Instance

### Question 8

You're trying to SSH into your EC2 instance and you are facing the following error Connection timed out. Which of the following is NOT a reason for this error?

    1. Your .pem file on your Linux machine doesn't have 400 permissions
    2. EC2 instance doesn't have a public IPv4
    3. Route Tables is missing routes
    4. Security Group or NACL is not configured correctly

**Correct Answer**

1. Your .pem file on your Linux machine doesn't have 400 permissions

### Question 9

Your t2.small EC2 instance constantly runs out of CPU credits and therefore the performance is degraded. What is NOT a solution for this problem?

    1. Upgrade the EC2 instance type to t2.medium or higher
    2. Purchase CPU credits for your EC2 instances
    3. Turn on t2 Unlimited
    4. Upgrade to non-t* type of EC2 instance

**Correct Answer**

2. Purchase CPU credits for your EC2 instances

### Question 10

You have installed Unified CloudWatch Agent on an EC2 instance to collect custom metrics from your EC2 instance. You want to know individual processes running on your EC2 instance and their system utilization. What would you use?

    1. Configure Unified CloudWatch Agent with StatsD protocol
    2. Configure Unified CloudWatch Agent with collectd protocol
    3. Configure Unified CloudWatch Agent with procstat plugin

**Correct Answer**

3. Configure Unified CloudWatch Agent with procstat plugin

### Question 11

You want to stop your EC2 instance and at the same time, you don't want to lose the memory state, processes, etc. What would you do?

    1. Terminate
    2. Stop
    3. Hibernate
    4. Reboot

**Correct Answer**

3. Hibernate

### Question 12

You have an application that is known to perform memory leaks on EC2 instances and therefore you would like to monitor the EC2 instance's RAM using CloudWatch. How can you achieve this?

    1. Enable EC2 detailed monitoring
    2. Push RAM as a custom metric using the Unified CloudWatch Agent
    3. Use EC2 basic monitoring

**Correct Answer**

2. Push RAM as a custom metric using the Unified CloudWatch Agent

## AMI Quiz

### Question 1

You are launching an EC2 instance in us-east-1 using AWS Lambda in us-east-1 using this Python script snippet:

python:

    ec2.create_instances(ImageId='ami-0dc2d3e4c0f9ebd18', MinCount=1, MaxCount=1)

It works well, so you decide to deploy your AWS Lambda function in us-west-1 as well. There, the function does not work and fails with InvalidAMIID.NotFound error. What's the problem?

    1. The new Lambda function is missing IAM permissions
    2. AMI is region locked and the same AMI ID can not be used across regions
    3. The AMI needs to first be shared with another region. The same AMI ID can then be used

**Correct Answer**

2. AMI is region locked and the same AMI ID can not be used across regions

### Question 2

What are the steps required to migrate an EC2 instance to another AZ?

    1. By doing right-click and select "Move", then select the desired AZ
    2. Create an AMI from the EC2 instance, then use this AMI to create a new EC2 instance in the desired subnet/AZ

**Correct Answer**

2. Create an AMI from the EC2 instance, then use this AMI to create a new EC2 instance in the desired subnet/AZ

### Question 3

You have an AMI that has an encrypted EBS Snapshot. You want to share this AMI with another AWS account. You have shared the AMI with the desired AWS account, but the other AWS account can't use it. How would you solve this problem?

    1. The other AWS account needs to logout and login again to refresh its credentials
    2. You can't share an AMI that has an encrypted EBS Snapshot
    3. You need to share the KMS CMK used to encrypt the AMI with the other AWS account

**Correct Answer**

3. You need to share the KMS CMK used to encrypt the AMI with the other AWS account

### Question 4

Your company has a critical application that's hosted on 100s of EC2 instances. The security team has created an AMI that's updated and has all the security patches installed. The DevOps team must create the EC2 instances from the AMI approved by the security team, but there's no IAM policy to prevent them from using another AMI. What AWS service would you use to ensure that all the EC2 instances are launched using the approved AMI?

    1. Amazon Inspector
    2. Amazon GuardDuty
    3. AWS Config
    4. AWS Security Hub

**Correct Answer**

3. AWS Config

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

## CloudFormation Quiz

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

## Advanced Storage Section

Question 1

You need to move hundreds of Terabytes into Amazon S3, then process the data using a fleet of EC2 instances. You have a 1 Gbit/s broadband. You would like to move the data faster and possibly processing it while in transit. What do you recommend?
1

Use your network
2

Use AWS Data Migration
3

Use Snowball Edge
Correct Answer
Question 2

You want to expose virtually infinite storage for your tape backups. You want to keep the same software you're using and want an iSCSI compatible interface. What do you use?
1

AWS Snowball
2

AWS Storage Gateway - File Gateway
3

AWS Storage Gateway - Volume Gateway
4

AWS Storage Gateway - Tape Gateway
Correct Answer
4

AWS Storage Gateway - Tape Gateway
Question 3

You have hundreds of Terabytes that you want to migrate to AWS S3 as soon as possible. You tried to use your network bandwidth and it will take around 3 weeks to complete the upload process. What's the recommended approach to use in this situation?
1

AWS Snowball Edge
2

AWS Storage Gateway - Volume Gateway
3

S3 Multi-part Upload
4

AWS Data Migration Service
Correct Answer
1

AWS Snowball Edge
Question 4

You have a large dataset stored in S3 that you want to access from on-premises servers using the NFS or SMB protocol. Also, you want to authenticate access to these files through on-premise Microsoft AD. What would you use?
1

AWS Storage Gateway - Volume Gateway
2

AWS Storage Gateway - File Gateway
3

AWS Storage Gateway - Tape Gateway
4

AWS Data Migration Service
Correct Answer
2

AWS Storage Gateway - File Gateway
Question 5

You're having issues activating your Storage Gateway VM. You have checked that the time is correct and that the Storage Gateway VM is synchronizing its time with an NTP server, but it's still not working. What else you can check to resolve this issue?
1

Ensure that the Storage Gateway VM has port 80 opened
2

Ensure that the Storage Gateway VM has enough local storage
Correct Answer
1

Ensure that the Storage Gateway VM has port 80 opened
Question 6

You're planning to migrate your company's infrastructure from on-premises to AWS Cloud. You have an on-premises Microsoft Windows File Server that you want to migrate. What is the most suitable AWS service you can use?
1

AWS Storage Gateway - File Gateway
2

Amazon FSx for Windows (File Server)
3

AWS Managed Microsoft AD
Correct Answer
2

Amazon FSx for Windows (File Server)
Question 7

You're migrating your on-premise data hosted on Windows File Server to AWS. You want a highly available and durable AWS service that's in case of an AZ failure there's no impact on your data. What should you choose?
1

Amazon S3
2

Two FSx for Windows with Single-AZ with DFRS replication set-up
3

FSx for Windows with Multi-AZ
4

Amazon RDS
Correct Answer
3

FSx for Windows with Multi-AZ

## CloudFront

Question 1

You have a static website hosted on an S3 Bucket. You have created a CloudFront Distribution that points to your S3 Bucket to better serve your requests and improve performance. After a while, you noticed that users can still access your website directly from the S3 Bucket. You want to enforce users to access the website only through CloudFront. How would you achieve that?
1

Send an email to your clients and tell them to not use the S3 endpoint
2

Configure your CloudFront Distribution and create an Origin Access Identity, then update your S3 Bucket Policy to only accept requests from your CloudFront Distribution OAI user
3

Use S3 Access Points to redirect clients to CloudFront
Correct Answer
2

Configure your CloudFront Distribution and create an Origin Access Identity, then update your S3 Bucket Policy to only accept requests from your CloudFront Distribution OAI user
Question 2

You have a CloudFront Distribution that serves your website hosted on a fleet of EC2 instances behind an Application Load Balancer. All your clients are from the United States, but you found that some malicious requests come from other countries. What's the easiest and most cost-effective way to allow users from the US and block other countries?
1

Use NACLs and Security Groups to block certain countries
2

Create an AWS WAF and associate it with your CloudFront Distribution, then configure AWS WAF to block all countries except the US
3

Use CloudFront Geo Restriction
Correct Answer
3

Use CloudFront Geo Restriction
Question 3

You are looking to analyze the global traffic patterns of your website that is hosted in S3 and distributed by CloudFront. What should you use?
1

CloudFront Access Logs with Athena
2

CloudFront Trails with Athena
3

S3 Access Logs with Athena
Correct Answer
1

CloudFront Access Logs with Athena
Question 4

Amazon CloudFront generates a set of reports about your CloudFront Distribution activity. Which of the following is NOT a valid report?
1

Access Logs Report
2

Cache Statistics Report
3

Popular Objects Report
4

Top Referrers Report
Correct Answer
1

Access Logs Report
Question 5

You have a React Single Page Application hosted on an S3 Bucket and served through CloudFront Distribution. You have made an update to your React application and pushed it to S3, but the old version is still cached at CloudFront, and clients still see the old version. You want the new update to be propagated immediately. What would you do?
1

Delete and create a new CloudFront Distribution
2

Use CloudFront Invalidation
3

Tell your clients to remove cache from their browsers or use Incognito Mode
Correct Answer
2

Use CloudFront Invalidation
Question 6

When creating a new CloudFront Distribution, what provides the most caching efficiency while making sure users get Cache Behavior based on the "color" attribute in a cookie?
1

HTTP Methods
2

Headers
3

Cookies
4

Query String Parameters
Correct Answer
3

Cookies

## Databases for SysOps

Question 1

You manage many RDS DB instances and you want to be notified of when there's a change in DB instance state, DB Parameter Groups, DB Security Groups, DB Snapshots, etc. What should you use?
1

CloudWatch Events
2

RDS Events & Event subscriptions
3

Amazon EventBridge
Correct Answer
2

RDS Events & Event subscriptions
Question 2

You have a MySQL RDS DB encrypted using a KMS CMK. You have taken a manual snapshot that you want to share with another AWS Account. You have shared the encrypted DB snapshot but the other account can't access the DB snapshot. What are you missing here?
1

You have to share the KMS CMK used to encrypt the DB snapshot with the other AWS Account
2

You shared the snapshot with an incorrect AWS Account
3

You can't share an encrypted DB snapshot
Correct Answer
1

You have to share the KMS CMK used to encrypt the DB snapshot with the other AWS Account
Question 3

A company has an application that's composed of API Gateway, a set of Lambda functions, and a PostgreSQL RDS DB instance. The PostgreSQL RDS DB instance is hosted in a private subnet and the Lambda functions are also given access to run inside a VPC so they can access the database. As your traffic grows, you start getting TooManyConnections errors from your PostgreSQL RDS DB instance. What's the best way to resolve this error?
1

Restart the PostgreSQL RDS DB instance
2

Contact AWS Support and request increase your AWS Lambda limit
3

Place an RDS Proxy before the PostgreSQL RDS DB instance
Correct Answer
3

Place an RDS Proxy before the PostgreSQL RDS DB instance
Explanation

RDS Proxy handles cleaning up idle connections and managing connection pools, instead of manually handle it in your Lambda functions and at the RDS database side.
Question 4

You have migrated the MySQL database from on-premises to RDS. You have a lot of applications and developers interacting with your database. Each developer has an IAM user in the company's AWS account. What's a suitable approach to give access to developers to the MySQL RDS DB instance instead of creating a DB user for each one?
1

Enable IAM Database Authentication
2

Use Amazon Cognito
3

By default IAM users have access to your RDS database
Correct Answer
1

Enable IAM Database Authentication
Question 5

You have an un-encrypted RDS DB instance and you want to create Read Replicas. Can you configure the RDS Read Replicas to be encrypted?
1

Yes
2

No
Correct Answer
2

No
Question 6

For your RDS database, you can have up to ....... Read Replicas.
1

3
2

7
3

5
Correct Answer
3

5
Question 7

You have an application that stores its data in an RDS database. You're expecting your application to receive a large number of writes in the next 24 hours. You have enabled Storage Auto Scaling for your RDS database so your RDS database storage can handle a large number of writes. Your RDS database has increased storage at 1 P.M, but when it tries to scale again at 3 P.M it fails. What do you expect the reason for this?
1

You can only scale up your RDS storage once within 24 hours
2

You can only scale up your RDS storage once within 6 hours
3

You can only scale up your RDS storage once within 48 hours
Correct Answer
2

You can only scale up your RDS storage once within 6 hours
Question 8

One analytics application is currently performing its queries against your main production database. These queries slow down the database which impacts the main user experience. What should you do to improve the situation?
1

Add Read Replicas
2

Enable Multi-AZ
3

Run the analytics queries at night
4

Increase the RDS instance size
Correct Answer
1

Add Read Replicas
Question 9

You want to enforce SSL connections to your PostgreSQL RDS database. What should you do?
1

Configure your Security Group
2

Configure Parameter Groups
3

Setup a proxy in front of your database and provide SSL termination
Correct Answer
2

Configure Parameter Groups
Question 10

Sometimes, your RDS database experiences failures and you would like to automatically recover it in case these failures happen. What should you use?
1

Use Network Load Balancer in front of RDS
2

Add Read Replicas
3

Enable Multi-AZ
Correct Answer
3

Enable Multi-AZ
Question 11

Your RDS backups are impacting your production database when they run. What can you do to improve the performance of your production database when backups are taken?
1

Enable Multi-AZ
2

Add Read Replicas
3

Configure backups to be asynchronous and use lower I/O
Correct Answer
1

Enable Multi-AZ
Question 12

What option of the Performance Insights dashboard should you use to figure out which SQL queries are affecting the most to the performance of your database?
1

Waits
2

Users
3

SQL Statements
4

Hosts
Correct Answer
3

SQL Statements
Question 13

You have an Aurora DB Cluster and Aurora Read Replicas keep on coming up as you have enabled Autoscaling. Your developers are complaining they cannot keep track of all the Read Replicas endpoints and their applications therefore do not use them. What do you recommend?
1

Create an AWS Lambda cron job that leverages the RDS API to update SSM Parameter Store with a full connection string
2

Use an Aurora Reader Endpoint
3

Disable Auto Scaling
Correct Answer
2

Use an Aurora Reader Endpoint
Question 14

An Aurora DB Cluster has 5 Read Replicas. Two db.r3.xlarge instances, two db.r3.4xlarge instances, and one db.r4.16xlarge. All the Read Replicas have the same priority tier Tier 0. When there's a failover in the DB Cluster which Read Replica will be promoted?
1

db.r4.16xlarge
2

db.r3.xlarge
3

db.r3.4xlarge
Correct Answer
1

db.r4.16xlarge
Question 15

You have a production Aurora DB Cluster. You want to create a test environment that uses the same data in this prod DB Cluster. What is the most cost-effective way to do this?
1

Create a manual snapshot of the production DB Cluster, then use this snapshot to create a new DB cluster
2

Create a new DB Cluster and uses AWS Database Migration Service (DMS) to migrate data from the production DB Cluster
3

Use Aurora Database Cloning to create a new DB Cluster (clone) of the production DB Cluster
Correct Answer
3

Use Aurora Database Cloning to create a new DB Cluster (clone) of the production DB Cluster
Question 16

What is Aurora Feature that enables you to rewind the DB Cluster back and forth in time without creating a new DB Cluster?
1

Aurora Database Cloning
2

Aurora Serverless
3

Aurora Backtracking
4

Aurora Backup and Restore
Correct Answer
3

Aurora Backtracking
Question 17

How many Aurora Read Replicas can you have in a single Aurora DB Cluster?
1

15
2

5
3

10
Correct Answer
1

15
Question 18

You have an Aurora DB Cluster where the automatic backup is enabled with a retention period of 10 days. You're using this Aurora DB Cluster for testing purposes, so you want to disable automatic backups to reduce costs. What should you do?
1

Use AWS CLI as this can't be done from AWS Console
2

Take a snapshot from your Aurora DB Cluster, terminate the old DB Cluster, then create a new DB Cluster with Automatic Backups disabled
3

You can't disable Aurora DB Cluster Automatic Backups
Correct Answer
3

You can't disable Aurora DB Cluster Automatic Backups
Question 19

You have an ElastiCache Redis Cluster that serves a popular application. You have noticed that there are a large number of requests that go to the database because a large number of items are removed from the cache before they expire. To solve the problem you scaled up your ElastiCache Redis Cluster to a larger node type to increase memory. What should you do to be notified of this issue if it happens again?
1

Create a CloudWatch Alarm based on the Evictions metric
2

Create a CloudWatch Alarm based on the CPUUtilization metric
3

Create a CloudWatch Alarm based on the SwapUsage metric
Correct Answer
1

Create a CloudWatch Alarm based on the Evictions metric
Question 20

What is the maximum number of Read Replicas you can add in an ElastiCache Redis Cluster with Cluster-Mode Disabled?
1

15
2

10
3

5
Correct Answer
3

5
Question 21

A type of ElastiCache Redis Scaling that you can do while still serving requests during the scaling process?
1

Online Scaling
2

Offline Scaling
Correct Answer
1

Online Scaling
Question 22

Your application is hosted on a fleet of EC2 instances trying to connect to your ElasticCache Memcached Cluster and you often add and remove nodes. What's the best way of making sure your EC2 instances correctly connect to them?
1

Create a CloudWatch Events that trigger an AWS Lambda which retrieves the list of cache nodes endpoints and update the text file
2

Create a CloudWatch Events that trigger an SNS topic notify you when there's a change in the cache nodes
3

Use Memcached Auto Discovery
Correct Answer
3

Use Memcached Auto Discovery

## Monitoring Auditing and Performance

Question 1

You have an RDS DB instance that's configured to push its database logs to CloudWatch. You want to create a CloudWatch alarm if there's an Error found in the logs. How would you do that?
1

Create a CloudWatch Logs Metric Filter that filter the logs for the keyword Error, then create a CloudWatch Alarm based on that Metric Filter
2

Create a scheduled CloudWatch Event that triggers an AWS Lambda every 1 hour, scans the logs, and notify you through SNS topic
3

Create an AWS Config Rule that monitors Error in your database logs and notify you through SNS topic
Correct Answer
1

Create a CloudWatch Logs Metric Filter that filter the logs for the keyword Error, then create a CloudWatch Alarm based on that Metric Filter
Question 2

How would you monitor your EC2 instance memory usage in CloudWatch?
1

Enable EC2 Detailed Monitoring
2

Use Unified CloudWatch Agent to push memory usage as a custom metric to CloudWatch
3

By default, the EC2 instance pushes memory usage to CloudWatch
Correct Answer
2

Use Unified CloudWatch Agent to push memory usage as a custom metric to CloudWatch
Question 3

You would like to evaluate the compliance of your resource's configurations over time. Which AWS service will you choose?
1

Amazon CloudWatch
2

AWS CloudTrail
3

AWS Config
Correct Answer
3

AWS Config
Question 4

Someone changed the configuration of a resource and made it non-compliant. Which AWS service can you use to find out who made the change?
1

Amazon CloudWatch
2

AWS CloudTrail
3

AWS Config
Correct Answer
2

AWS CloudTrail
Question 5

You have made a configuration change and would like to evaluate the impact of it on the performance of your application. Which AWS service do you use?
1

Amazon CloudWatch
2

AWS CloudTrail
3

AWS Config
Correct Answer
1

Amazon CloudWatch
Question 6

You would like to test out a complex CloudWatch Alarm that responds to a globally increased traffic on your application. You are in a test environment. How can you test out this alarm in a cost-effective manner and efficiently?
1

Setup a global EC2 fleet and increase the request rate to your application until you reach the Alarm state
2

Use the set-alarm-state CLI command
3

Change the alarm thresholds temporarily
Correct Answer
2

Use the set-alarm-state CLI command
Question 7

You would like to ensure that over time, none of your EC2 instances expose port 84 as it is known to have vulnerabilities with the OS you are using. What can you do to monitor this?
1

CloudWatch Metrics
2

CloudTrail Trails
3

AWS Config Rules
4

Create an AWS Lambda cron job
Correct Answer
3

AWS Config Rules
Question 8

You have enabled AWS Config to monitor Security Groups if there's unrestricted SSH access to any of your EC2 instances. What AWS Config feature you can use to automatically re-configure your Security Groups to the correct state?
1

AWS Config Remediations
2

AWS Config Rules
3

AWS Config Notifications
Correct Answer
1

AWS Config Remediations
Question 9

How do you ensure that the CloudTrail logs stored in the S3 bucket haven't been modified or deleted by other users?
1

Use CloudTrail Insights
2

Use CloudTrail Log File Integrity Validation
3

Use CloudTrail Events
Correct Answer
2

Use CloudTrail Log File Integrity Validation
Question 10

You have CloudTrail enabled for your AWS Account in all AWS Regions. What should you use to detect unusual activity in your AWS Account?
1

CloudTrail Events
2

CloudTrail Log File Integrity Validation
3

CloudTrail Insights
Correct Answer
3

CloudTrail Insights
Question 11

Which AWS services help you to be notified when your service quotas thresholds are approaching?
1

AWS GuardDuty & AWS CloudTrail
2

AWS Service Quota & AWS Trusted Advisor
3

AWS Config & CloudWatch Alarms
Correct Answer
2

AWS Service Quota & AWS Trusted Advisor

## AWS Account Management

Question 1

You're using AWS Service Catalog to make it easy for your users to provision AWS resources. You have created a portfolio and a set of products. How should you standardize tags across provisioned products?
1

AWS Organization - Tag Policies
2

AWS Service Catalog - TagOptions Library
3

AWS Resource Groups & Tag Editor
Correct Answer
2

AWS Service Catalog - TagOptions Library
Question 2

What can you use to standardize tags across resources in all AWS Accounts inside your AWS Organization?
1

AWS Organization - Tag Policies
2

AWS Service Catalog - TagOptions Library
3

AWS Resource Groups & Tag Editor
Correct Answer
1

AWS Organization - Tag Policies
Question 3

You manage a set of AWS Accounts using AWS Organization which has Consolidated Billing feature enabled and Reserved Instance Discount Sharing turned on. You have an AWS Account that purchased a set of reserved EC2 instances that the owner doesn't want to share with the AWS Organization. What should you do?
1

This can't be done as the AWS Account is already part of the AWS Organization
2

Remove the AWS Account from the AWS Organization, turn off sharing, then add to the AWS Organization again
3

Disable Reserved Instance Discount Sharing at the AWS account level
Correct Answer
3

Disable Reserved Instance Discount Sharing at the AWS account level
Question 4

You have 5 AWS Accounts that you manage using AWS Organizations. You want to restrict access to certain AWS services in each account. How should you do that?
1

Using AWS Organizations SCP
2

Using IAM Roles
3

Using AWS Config
Correct Answer
1

Using AWS Organizations SCP
Question 5

You want to be notified in your company's Slack channel when there's a scheduled AWS maintenance on EC2 that affects your EC2 instances. What should you do?
1

From AWS Personal Health Dashboard, select Notifications Tab, then select your Slack channel as your Notifications Destination
2

Create a CloudWatch Event that will be triggered by AWS Personal Health, then select your Slack channel as a target for your CW Event
3

Create a CloudWatch Event triggered by AWS Personal Health and then create a Lambda function as a target for your CW Event. Use this Lambda function to send a message to your Slack channel
Correct Answer
3

Create a CloudWatch Event triggered by AWS Personal Health and then create a Lambda function as a target for your CW Event. Use this Lambda function to send a message to your Slack channel
Question 6

AWS EC2 experiences an outage and you would like to get a list of all your resources that are affected. What should you use?
1

AWS Organizations
2

AWS Service Health Dashboard
3

AWS Personal Health Dashboard
4

AWS Budgets
Correct Answer
3

AWS Personal Health Dashboard
Question 7

Before going ahead with an AWS service, your manager asks you to find out if Amazon ElasticSearch Service in ap-northeast-1 has had outages over the past year. Where can you find this information?
1

AWS Advisor
2

AWS Service Health Dashboard
3

AWS Personal Health Dashboard
4

AWS Config
Correct Answer
2

AWS Service Health Dashboard
Question 8

You have strong regulatory requirements to only allow fully audited AWS Services in production. You still want to allow your teams to experiment in a development environment while services are being audited. How can you best set this up?
1

Create an AWS Organization and create two Prod and Dev OUs, then Apply an SCP on the Prod OU
2

Provide the Dev team with a completely independent AWS account
3

Apply a global IAM policy on your Prod account
4

Create an AWS Config Rule
Correct Answer
1

Create an AWS Organization and create two Prod and Dev OUs, then Apply an SCP on the Prod OU
Question 9

Your data scientists need a self-service portal to provision their big data analysis environments. They are not AWS experts and would like something simple yet controlled. What do you advise?
1

Buy them the AWS CloudFormation Master Class Course
2

Setup an AWS Organization OU for your data scientists and give them a monthly allowance where they can create anything they want
3

Create a Service Catalog for your data scientists in which you upload products they should have access to
Correct Answer
3

Create a Service Catalog for your data scientists in which you upload products they should have access to
Question 10

For accounting reasons, you need to separate costs into categories in AWS, such as Environment. How do you achieve this?
1

Ask for a monthly AWS Data Export and run an Excel macro to aggregate your costs
2

Use Cost Allocation Tags
3

Use Billing Tags
4

Create multiple AWS accounts
Correct Answer
2

Use Cost Allocation Tags
Question 11

You need recommendations for the types of reserved EC2 instances you should buy to optimize your AWS costs. You also want to have access to a report detailing how utilized your reserved EC2 instances are. What do you recommend?
1

Setup a billing alarm
2

Use AWS Config
3

Use AWS Cost Explorer
4

Use AWS Budgets
Correct Answer
3

Use AWS Cost Explorer
Question 12

What should you use to be notified when your AWS usage costs exceed a certain threshold?
1

AWS Budgets
2

AWS Cost Explorer
3

AWS Cost Allocation Tags
Correct Answer
1

AWS Budgets
Question 13

You want to analyze your AWS resource usage and costs so you can take decisions to decrease costs. Your analytics team wants this data each day so they can run queries on it. What should you use?
1

Use AWS Cost Explorer
2

Use AWS Cost and Usage Reports service and configure it to deliver reports daily to an S3 bucket
3

Use AWS Cost Allocation Tags
Correct Answer
2

Use AWS Cost and Usage Reports service and configure it to deliver reports daily to an S3 bucket
Question 14

Which AWS service helps you improve performance and reduce costs by using Machine Learning to analyze your resources' configurations and their utilization?
1

AWS Trusted Advisor
2

AWS Cost Explorer
3

AWS Compute Optimizer
Correct Answer
3

AWS Compute Optimizer

## Disaster Recovery

Question 1

You have an un-encrypted EFS filesystem that contains a lot of data. You want to encrypt this EFS filesystem, so you created a new encrypted EFS filesystem and want to migrate data to it. Which AWS service should you use?
1

AWS Snowball
2

AWS DataSync
3

AWS Database Migration Service (AWS DMS)
Correct Answer
2

AWS DataSync
Question 2

What's the best approach to automate/manage cross-regions backups for AWS RDS DB instances?
1

CloudWatch Scheduled Event with AWS Lambda
2

EC2 Instance with Cron job
3

AWS Backup
Correct Answer
3

AWS Backup

## Security and Compliance for SysOps

Question 1

You would like to use a dedicated hardware module to manage your encryption keys and have full control over them. What do you recommend?
1

AWS KMS
2

AWS CloudHSM
3

AWS GuardDuty
Correct Answer
2

AWS CloudHSM
Question 2

When you enable Automatic Rotation on your KMS CMK, the backing key is rotated every .........
1

1 year
2

3 years
3

6 months
Correct Answer
1

1 year
Question 3

You've created a Customer-managed CMK in KMS that you use to encrypt both S3 buckets and EBS snapshots. Your company policy mandates that your encryption keys be rotated every 3 months. What should you do?
1

Use AWS Managed Keys as they're automatically rotated by AWS every 3 months
2

Re-configure your KMS CMK and enable Automatic Rotation, in the "Period" select 3 months
3

Rotate the KMS CMK manually. Create a new KMS CMK and use Key Aliases to reference the new KMS CMK. Keep the old KMS CMK so you can decrypt the old data
Correct Answer
3

Rotate the KMS CMK manually. Create a new KMS CMK and use Key Aliases to reference the new KMS CMK. Keep the old KMS CMK so you can decrypt the old data
Question 4

What should you use to control access to your KMS CMKs?
1

KMS IAM Policy
2

KMS Key Policies
3

AWS GuardDuty
4

KMS Access Control List (KMS ACL)
Correct Answer
2

KMS Key Policies
Question 5

Which AWS Service analyzes your AWS account and gives recommendations for cost optimization, performance, security, fault tolerance, and service limits?
1

AWS Cost and Usage Reports
2

AWS Security Hub
3

AWS Trusted Advisor
4

AWS GuardDuty
Correct Answer
3

AWS Trusted Advisor
Question 6

AWS GuardDuty scans the following data, EXCEPT:
1

DNS Logs
2

VPC Flow Logs
3

CloudTrail Logs
4

CloudWatch Logs
Correct Answer
4

CloudWatch Logs
Question 7

Which of the following AWS Services are you prohibited to run security assessments against?
1

Route 53
2

EC2
3

RDS
4

API Gateway
Correct Answer
1

Route 53
Question 8

You have a website hosted on a fleet of EC2 instances fronted by an Application Load Balancer. What you should use to protect your website from common web application attacks (e.g., SQL Injection)?
1

AWS Shield
2

AWS Security Hub
3

AWS WAF
4

AWS GuardDuty
Correct Answer
3

AWS WAF
Question 9

According to AWS Shared Responsibility Model, what are you responsible for in RDS?
1

Security Group Rules
2

OS Patching
3

Database Patching
4

Underlying Hardware Security
Correct Answer
1

Security Group Rules
Question 10

Your user-facing website is a high-risk target for DDoS attacks and you would like to get 24/7 support in case they happen and AWS bill reimbursement for the incurred costs during the attack. What AWS service should you use?
1

AWS WAF
2

AWS Shield Advanced
3

AWS Shield Standard
4

AWS DDoS OpsTeam
Correct Answer
2

AWS Shield Advanced
Question 11

You would like to analyze OS vulnerabilities from within your EC2 instances. You need these analyses to occur weekly and provide you with concrete recommendations in case vulnerabilities are found. Which AWS service should you use?
1

AWS Trusted Advisor
2

AWS Config
3

Amazon Inspector
4

AWS GuardDuty
Correct Answer
3

Amazon Inspector
Question 12

Your development team tends to commit their AWS credentials in public repositories and is afraid of misuse of your AWS account. Which AWS service can notify you of suspicious account activity?
1

Amazon Inspector
2

AWS GuardDuty
3

AWS Trusted Advisor
4

AWS Enhanced Protection
Correct Answer
2

AWS GuardDuty
Question 13

To support an ongoing audit, you need to provide auditors with documents that prove that AWS has achieved certain compliance. How can you do this?
1

Contact AWS Support
2

AWS GuardDuty
3

Amazon Inspector
4

AWS Artifact
Correct Answer
4

AWS Artifact
Question 14

AWS Certificate Manager helps you easily provision, manage, and deploy SSL/TLS certificates. It's integrated with the following AWS services EXCEPT:
1

EC2
2

Elastic Load Balancer
3

CloudFront
4

API Gateway
Correct Answer
1

EC2
Question 15

What is the most suitable solution for storing RDS DB passwords which also provides you automatic rotation?
1

AWS SSM Parameter Store
2

AWS KMS
3

AWS Secrets Manager
Correct Answer
3

AWS Secrets Manager

## Identity

Question 1

During an IT audit, it has been highlighted that some of your users do not have MFA enabled. Where can you obtain a report giving you details about which users do not have MFA enabled?
1

STS
2

AWS IAM Credential Report
3

AWS Trusted Advisor
4

AWS GuardDuty
Correct Answer
2

AWS IAM Credential Report
Question 2

You have a mobile application and you would like to give your users access to their own personal space in Amazon S3. How do you achieve that?
1

Generate IAM user credentials for each of your application's users
2

Use a bucket policy to make your bucket public
3

Use Amazon Cognito Identity Federation
4

Use SAML Identity Federation
Correct Answer
3

Use Amazon Cognito Identity Federation
Question 3

How to find the AWS resources that are accessible from outside your AWS Account?
1

Using IAM Access Advisor
2

Using IAM Credentials Report
3

Using IAM Access Analyzer
Correct Answer
3

Using IAM Access Analyzer
Question 4

You want to provide unauthenticated guess access to your web application developed and hosted using AWS Amplify. What should you use?
1

Amazon Cognito User Pools
2

Amazon Cognito Identity Pools
3

AWS IAM Users
Correct Answer
2

Amazon Cognito Identity Pools

## Networking - Route 53

Question 1

You have purchased "mycoolcompany.com" on Route 53 Registrar and would like for it to point to "lb1-1234.us-east-2.elb.amazonaws.com". Which Route 53 record type is IMPOSSIBLE to set up for this?
1

CNAME
2

ALIAS
Correct Answer
1

CNAME
Question 2

You have deployed a new Elastic Beanstalk environment and would like to direct 5% of your production traffic to this new environment, to monitor for CloudWatch metrics and ensuring no issues exist. Which Route 53 routing policy allows you to do so?
1

Simple
2

Weighted
3

Failover
4

Latency
Correct Answer
2

Weighted
Question 3

After updating a Route 53 record to point "myapp.mydomain.com" from an old Load Balancer to a new load balancer, it looks like the users are still redirected to the old load balancer. You are wondering why ...
1

Because of the Alias record!
2

Because of the CNAME record!
3

Because of the TTL!
4

Because of the health checks!
Correct Answer
3

Because of the TTL!
Question 4

You want your users to get the best possible user experience, minimizing the response time from your servers to your users. Which Route 53 routing policy should help?
1

Multi-Value
2

Weighted
3

Geolocation
4

Latency
Correct Answer
4

Latency
Question 5

You have a legal requirement that people in any country but France should not be able to access your website. Which Route 53 routing policy helps you in achieving this?
1

Latency
2

Geolocation
3

Multi-Value
4

Simple
Correct Answer
2

Geolocation
Question 6

You have purchased a domain on GoDaddy and would like to use it with Route 53. What should you do?
1

Request for a domain transfer
2

Create a private hosted zone and update the 3rd party registrar NS records to use Route 53 name servers
3

Create a public hosted zone and update Route 53 NS records to use 3rd party registrar name servers
4

Create a public hosted zone and update the 3rd party registrar NS records to use Route 53 name servers
Correct Answer
4

Create a public hosted zone and update the 3rd party registrar NS records to use Route 53 name servers
Question 7

You have purchased "mycoolcompany.com" from Route 53 Registrar. Also, you have created an S3 bucket "mycoolapplication" and uploaded your static website to the S3 bucket, then enabled Static Website Hosting. You're trying to create an APEX Alias Route 53 record to point to your S3 bucket but you can't. What are you missing here?
1

Your S3 bucket must be the same name as your Route 53 record "mycoolcompany.com"
2

Nothing, just refresh the AWS Console, and all good!
3

You can't create an APEX Alias record for the S3 bucket with Static Website Hosting enabled
Correct Answer
1

Your S3 bucket must be the same name as your Route 53 record "mycoolcompany.com"


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

## 22 Other Services

Question 1

How can you restrict access to your Amazon ElasticSearch domain to your company's CIDR block?
1

Using IAM Policies
2

Using IP-Based Policies
3

Using AWS Shield
4

Using AWS WAF
Correct Answer
2

Using IP-Based Policies
Question 2

Which of the following are NOT a supported Kibana Authentication type in your Amazon ElasticSearch domain?
1

IAM Users and Roles
2

HTTP Basic Authentication
3

SAML
4

Amazon Cognito
Correct Answer
1

IAM Users and Roles
Question 3

What is the best way to find errors, exceptions, and request behavior in your AWS serverless application?
1

AWS Security Hub
2

AWS Amplify
3

AWS X-Ray
4

CloudWatch Logs
Correct Answer
3

AWS X-Ray



## Practice Test Stephane Maarek

Instructions

About this practice exam:
- questions order and response orders are randomized
- you can only review the answer after finishing the exam due to how Udemy works
- it consists of 65 questions, the duration is 130 minutes, the passing score is 720

======

In case of an issue with a question:
- ask a question in the Q&A
- please take a screenshot of the question (because they're randomized) and attach it
- we will get back to you as soon as possible and fix the issue

Good luck, and happy learning!


### Question 1

* A media company runs its business on Amazon EC2 instances backed by Amazon S3 storage. The company is apprehensive about the consistent increase in costs incurred from S3 buckets. The company wants to make some decisions regarding data retention, storage, and deletion based on S3 usage and cost reports. As a SysOps Administrator, you have been hired to develop a solution to track the costs incurred by each S3 bucket in the AWS account.

How will you configure this requirement?
    
    1. Configure AWS Budgets to see the cost against each S3 bucket in the AWS account

    2. Use AWS Simple Monthly Calculator to check the cost against each S3 bucket in your AWS account

    3. Use AWS Trusted Advisor's rich set of best practice checks to configure cost utilization for individual S3 buckets. Trusted Advisor also provides recommendations based on the findings derived from analyzing your AWS cloud architecture

    4. Add a common tag to each bucket. Activate the tag as a cost allocation tag. Use the AWS Cost Explorer to create a cost report for the tag

**Correct Answer**
    4. Add a common tag to each bucket. Activate the tag as a cost allocation tag. Use the AWS Cost Explorer to create a cost report for the tag

**Explanation**


**Correct option:**
~~~
Add a common tag to each bucket. Activate the tag as a cost allocation tag. Use the AWS Cost Explorer to create a cost report for the tag

Before you begin, your AWS Identity and Access Management (IAM) policy must have permission to: Access the Billing and Cost Management console, Perform the actions s3:GetBucketTagging and s3:PutBucketTagging.

Start by adding a common tag to each bucket. Activate the tag as a cost allocation tag. Use the AWS Cost Explorer to create a cost report for the tag. After you create the cost report, you can use it to review the cost of each bucket that has the cost allocation tag that you created.

You can set up a daily or hourly AWS Cost and Usage report to get more Amazon S3 billing details. However, these reports won't show you who made requests to your buckets. To get more information on certain Amazon S3 billing items, you must enable logging ahead of time. Then, you'll have logs that contain Amazon S3 request details.
~~~
**Incorrect options:**
~~~
Configure AWS Budgets to see the cost against each S3 bucket in the AWS account - AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount. You can also use AWS Budgets to set reservation utilization or coverage targets and receive alerts when your metrics drop below the threshold you define. It cannot showcase the cost of each S3 bucket.

Use AWS Simple Monthly Calculator to check the cost against each S3 bucket in your AWS account - The AWS Simple Monthly Calculator is an easy-to-use online tool that enables you to estimate the monthly cost of AWS services for your use case based on your expected usage. This useful tool helps estimate the cost of resources, but the current use case is not about estimations but being able to understand which bucket is incurring the maximum cost.

Use AWS Trusted Advisor's rich set of best practice checks to configure cost utilization for individual S3 buckets. Trusted Advisor also provides recommendations based on the findings derived from analyzing your AWS cloud architecture - AWS Trusted Advisor offers a rich set of best practice checks and recommendations across five categories. For Amazon S3 buckets, Trusted Advisor offers checks the following -

1) Checks buckets in Amazon S3 that have open access permissions 2) Checks the logging configuration of Amazon S3 buckets- whether it is enabled and for what duration 3) Checks for Amazon S3 buckets that do not have versioning enabled.

Trusted Advisor cannot however generate reports for costs incurred on S3 buckets.

References:

https://aws.amazon.com/premiumsupport/knowledge-center/s3-find-bucket-cost/

https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/

https://aws.amazon.com/getting-started/hands-on/control-your-costs-free-tier-budgets/

~~~

### Question 2

* A startup uses Amazon S3 buckets for storing their customer data. The company has defined different retention periods for different objects present in their Amazon S3 buckets, based on the compliance requirements. But, the retention rules do not seem to work as expected.

Which of the following points are important to remember when configuring retention periods for objects in Amazon S3 buckets (Select two)?

**Multi Select**


    1. When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version

    2. You cannot place a retention period on an object version through a bucket default setting

    3. When you use bucket default settings, you specify a Retain Until Date for the object version

    4. Different versions of a single object can have different retention modes and periods

    5. The bucket default settings will override any explicit retention mode or period you request on an object version


**Correct Answer**
1. When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version
4. Different versions of a single object can have different retention modes and periods

**Explanation**

Correct options:
~~~
When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version - You can place a retention period on an object version either explicitly or through a bucket default setting. When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version. Amazon S3 stores the Retain Until Date setting in the object version's metadata and protects the object version until the retention period expires.

Different versions of a single object can have different retention modes and periods - Like all other Object Lock settings, retention periods apply to individual object versions. Different versions of a single object can have different retention modes and periods.

For example, suppose that you have an object that is 15 days into a 30-day retention period, and you PUT an object into Amazon S3 with the same name and a 60-day retention period. In this case, your PUT succeeds, and Amazon S3 creates a new version of the object with a 60-day retention period. The older version maintains its original retention period and becomes deletable in 15 days.
~~~
Incorrect options:
~~~
You cannot place a retention period on an object version through a bucket default setting - You can place a retention period on an object version either explicitly or through a bucket default setting.

When you use bucket default settings, you specify a Retain Until Date for the object version - When you use bucket default settings, you don't specify a Retain Until Date. Instead, you specify a duration, in either days or years, for which every object version placed in the bucket should be protected.

The bucket default settings will override any explicit retention mode or period you request on an object version - If your request to place an object version in a bucket contains an explicit retention mode and period, those settings override any bucket default settings for that object version.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock-overview.html
~~~

### Question 3

* After a developer had mistakenly shutdown a test instance, the Team Lead has decided to configure termination protection on all the instances. As a systems administrator, you have been tasked to review the termination policy and check its viability for the given requirements.

Which of the following choices are correct about Amazon EC2 instance's termination policy (Select two)?

**Multi Select**
    
    1. The DisableApiTermination attribute prevents you from terminating an instance by initiating shutdown from the instance
    
    2. The DisableApiTermination attribute does not prevent you from terminating an instance by initiating shutdown from Amazon EC2 console
    
    3. You can't enable termination protection for Spot Instances
    
    4. To prevent instances that are part of an Auto Scaling group from terminating on scale in, use instance protection
    
    5. The DisableApiTermination attribute prevents Amazon EC2 Auto Scaling from terminating an instance

**Correct Answer**

3. You can't enable termination protection for Spot Instances
4. To prevent instances that are part of an Auto Scaling group from terminating on scale in, use instance protection


**Explanation**

Correct options:
~~~
You can't enable termination protection for Spot Instances - You can't enable termination protection for Spot Instances—a Spot Instance is terminated when the Spot price exceeds the amount you're willing to pay for Spot Instances. However, you can prepare your application to handle Spot Instance interruptions.

To prevent instances that are part of an Auto Scaling group from terminating on scale in, use instance protection - The DisableApiTermination attribute does not prevent Amazon EC2 Auto Scaling from terminating an instance. For instances in an Auto Scaling group, use the following Amazon EC2 Auto Scaling features instead of Amazon EC2 termination protection:

    - To prevent instances that are part of an Auto Scaling group from terminating on scale in, use instance protection.

    - To prevent Amazon EC2 Auto Scaling from terminating unhealthy instances, suspend the ReplaceUnhealthy process.

    - To specify which instances Amazon EC2 Auto Scaling should terminate first, choose a termination policy.
~~~

Incorrect options:
~~~
The DisableApiTermination attribute prevents you from terminating an instance by initiating shutdown from the instance - This is false. The DisableApiTermination attribute does not prevent you from terminating an instance by initiating shutdown from the instance

The DisableApiTermination attribute does not prevent you from terminating an instance by initiating shutdown from Amazon EC2 console - By default, you can terminate your instance using the Amazon EC2 console, command line interface, or API. To prevent your instance from being accidentally terminated using Amazon EC2, you can enable termination protection for the instance.

The DisableApiTermination attribute prevents Amazon EC2 Auto Scaling from terminating an instance - The DisableApiTermination attribute does not prevent Amazon EC2 Auto Scaling from terminating an instance.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/terminating-instances.html#Using_ChangingDisableAPITermination
~~~

### Question 4

A company is moving their on-premises technology infrastructure to AWS Cloud. Compliance rules and regulatory guidelines mandate the company to use its own software that needs socket level configurations. As the company is new to AWS Cloud, they have reached out to you for guidance on this requirement.

As an AWS Certified SysOps Administrator, which option will you suggest for the given requirement?
    
    1. Opt for On-Demand instances that are highly available and require no prior planning
    
    2. Opt for Reserved Instances that allow you to plan and help install the necessary software
    
    3. Opt for Amazon EC2 Dedicated Host
    
    4. Opt for Amazon EC2 Dedicated Instance
Correct Answer
3

Opt for Amazon EC2 Dedicated Host
Explanation

Correct option:

Opt for Amazon EC2 Dedicated Host

An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing per-socket, per-core, or per-VM software licenses, including Windows Server, Microsoft SQL Server, SUSE, and Linux Enterprise Server. Hence, is the right choice for the current requirement.

Differences between Dedicated Hosts and Dedicated Instances: via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html

Incorrect options:

Opt for Amazon EC2 Dedicated Instance - Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at a hardware level, even if those accounts are linked to a single payer account. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances.

Opt for On-Demand instances that are highly available and require no prior planning

Opt for Reserved Instances that allow you to plan and help install the necessary software

You cannot install your own software that needs socket level programming on On-Demand or Reserved Instances.

References:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html

Question 5

Security and Compliance is a Shared Responsibility between AWS and the customer. As part of this Shared Responsibility, the customer is also responsible for securing the resources that he has procured under his AWS account.

Which of the following is the responsibility of the customer?
1

For Amazon S3 service, managing the operating system and platform is customer responsibility
2

AWS is responsible for patching and fixing flaws within the infrastructure, for patching the guest Operating Systems and applications of the customers
3

AWS is responsible for training their customers and their employees as part of Customer Specific training
4

For Amazon EC2 service, managing guest operating system (including updates and security patches), application software and Security Groups is the responsibility of the customer
Correct Answer
4

For Amazon EC2 service, managing guest operating system (including updates and security patches), application software and Security Groups is the responsibility of the customer
Explanation

Correct option:

For Amazon EC2 service, managing guest operating system (including updates and security patches), application software and Security Groups is the responsibility of the customer

Customer responsibility will be determined by the AWS Cloud services that a customer selects. This determines the amount of configuration work the customer must perform as part of their security responsibilities. For example, a service such as Amazon Elastic Compute Cloud (Amazon EC2) is categorized as Infrastructure as a Service (IaaS) and, as such, requires the customer to perform all of the necessary security configuration and management tasks. Customers that deploy an Amazon EC2 instance are responsible for the management of the guest operating system (including updates and security patches), any application software or utilities installed by the customer on the instances, and the configuration of the AWS-provided firewall (called a security group) on each instance.

AWS Shared Responsibility Model: via - https://aws.amazon.com/compliance/shared-responsibility-model/

Incorrect options:

For Amazon S3 service, managing the operating system and platform is customer responsibility - For abstracted services, such as Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data. Customers are responsible for managing their data (including encryption options), classifying their assets, and using IAM tools to apply the appropriate permissions.

AWS is responsible for patching and fixing flaws within the infrastructure, for patching the guest Operating Systems and applications of the customers - As part of Patch management, AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.

AWS is responsible for training their customers and their employees as part of Customer Specific training - As part of Awareness & Training, AWS trains AWS employees, but a customer must train their own employees.

Reference:

https://aws.amazon.com/compliance/shared-responsibility-model/

Question 6

As a SysOps Administrator, you have been tasked to generate a report on all API calls made for Elastic Load Balancer from the AWS Management Console.

Which feature/service will you use to fetch this data?
1

CloudWatch metrics
2

Load Balancer Access logs
3

CloudTrail logs
4

Load Balancer Request tracing
Correct Answer
3

CloudTrail logs
Explanation

Correct option:

CloudTrail logs - Elastic Load Balancing is integrated with AWS CloudTrail, a service that provides a record of actions taken by a user, role, or an AWS service in Elastic Load Balancing. CloudTrail captures all API calls for Elastic Load Balancing as events. The calls captured include calls from the AWS Management Console and code calls to the Elastic Load Balancing API operations. If you create a trail, you can enable continuous delivery of CloudTrail events to an Amazon S3 bucket, including events for Elastic Load Balancing. If you don't configure a trail, you can still view the most recent events in the CloudTrail console in Event history. Using the information collected by CloudTrail, you can determine the request that was made to Elastic Load Balancing, the IP address from which the request was made, who made the request, when it was made, and additional details.

Incorrect options:

CloudWatch metrics - You can use Amazon CloudWatch to retrieve statistics about data points for your load balancers and targets as an ordered set of time-series data, known as metrics. You can use these metrics to verify that your system is performing as expected.

Load Balancer Access logs - You can use access logs to capture detailed information about the requests made to your load balancer and store them as log files in Amazon S3. You can use these access logs to analyze traffic patterns and to troubleshoot issues with your targets.

Load Balancer Request tracing - You can use request tracing to track HTTP requests. The load balancer adds a header with a trace identifier to each request it receives.

Reference:

https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudtrail-logs.html

Question 7

A Systems Administrator has just configured an internet facing Load Balancer for traffic distribution across the EC2 instances placed in different Availability Zones. The clients, however, are unable to connect to the Load Balancer.

What is the most plausible reason for this issue?
1

It is an internal server error
2

A security group or network ACL is not allowing traffic from the client
3

The target returned the error code of 200 indicating an error on the server side
4

The target was incorrectly configured as a Lambda function and not an EC2 instance
Correct Answer
2

A security group or network ACL is not allowing traffic from the client
Explanation

Correct option:

A security group or network ACL is not allowing traffic from the client

If the load balancer is not responding to client requests, check for the following issues:

    Your internet-facing load balancer may be attached to a private subnet - You must specify public subnets for your load balancer. A public subnet has a route to the Internet Gateway for your virtual private cloud (VPC).

    A security group or network ACL does not allow traffic - The security group for the load balancer and any network ACLs for the load balancer subnets must allow inbound traffic from the clients and outbound traffic to the clients on the listener ports.

Incorrect options:

It is an internal server error - HTTP 500 is the error code for internal server error, generated by Load Balancer and sent back to the requesting client. But, in the given use case, the client is unable to connect to the Load Balancer itself.

The target returned the error code of 200 indicating an error on the server side - By default, the success code is 200. So, returning an HTTP 200 indicates a successful message.

The target was incorrectly configured as a Lambda function and not an EC2 instance - An ELB can be configured to have a Lambda Function as its target. This should not result in any access issues or errors.

Reference:

https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-troubleshooting.html

Question 8

A Systems Administrator is configuring an Application Load Balancer (ALB) that fronts Amazon EC2 instances.

Which of the following options would you identify as correct for configuring the ALB? (Select two)
Multi Select
1

The targets of a target group in an ALB should all belong to the same Availability Zone
2

Before you start using your Application Load Balancer, you must add one or more listeners
3

A target can be registered with only one target group at any given time
4

When you create a listener, you define actions and conditions for the default rule
5

You configure target groups of an ALB by attaching them to the listeners
Correct Answer
2

Before you start using your Application Load Balancer, you must add one or more listeners
5

You configure target groups of an ALB by attaching them to the listeners
Explanation

Correct options:

Before you start using your Application Load Balancer, you must add one or more listeners - A listener checks for connection requests from clients, using the protocol and port that you configure. The rules that you define for a listener determine how the load balancer routes requests to its registered targets. Each rule consists of a priority, one or more actions, and one or more conditions. When the conditions for a rule are met, then its actions are performed. You must define a default rule for each listener, and you can optionally define additional rules.

You configure target groups of an ALB by attaching them to the listeners - Each target group is used to route requests to one or more registered targets. When you create each listener rule, you specify a target group and conditions. When a rule condition is met, traffic is forwarded to the corresponding target group. You can create different target groups for different types of requests.

Load Balancer basic components: via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html

Incorrect options:

The targets of a target group in an ALB should all belong to the same Availability Zone - A load balancer serves as the single point of contact for clients. The load balancer distributes incoming application traffic across multiple targets, such as EC2 instances, in multiple Availability Zones. This increases the availability of your application.

A target can be registered with only one target group at any given time - Each target group routes requests to one or more registered targets, such as EC2 instances, using the protocol and port number that you specify. You can register a target with multiple target groups.

When you create a listener, you define actions and conditions for the default rule - When you create a listener, you define actions for the default rule. Default rules can't have conditions. If the conditions for none of a listener's rules are met, then the action for the default rule is performed.

Reference:

https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html

Question 9

A company wants to migrate a part of its on-premises infrastructure to AWS Cloud. As a starting point, the company is looking at moving their daily workflow files to AWS Cloud, such that the files are accessible from the on-premises systems as well as AWS Cloud. To reduce the management overhead, the company wants a fully managed service.

Which service/tool is the right choice for this requirement?
1

File Gateway of AWS Storage Gateway
2

Volume Gateway of AWS Storage Gateway
3

Amazon Simple Storage Service (Amazon S3)
4

Amazon Elastic Block Store (Amazon EBS)
Correct Answer
1

File Gateway of AWS Storage Gateway
Explanation

Correct option:

File Gateway of AWS Storage Gateway - AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. Storage Gateway provides a standard set of storage protocols such as iSCSI, SMB, and NFS, which allow you to use AWS storage without rewriting your existing applications. It provides low-latency performance by caching frequently accessed data on-premises, while storing data securely and durably in Amazon cloud storage services. Storage Gateway optimizes data transfer to AWS by sending only changed data and compressing data.

File Gateway presents a file-based interface to Amazon S3, which appears as a network file share. It enables you to store and retrieve Amazon S3 objects through standard file storage protocols. File Gateway allows your existing file-based applications or devices to use secure and durable cloud storage without needing to be modified. With S3 File Gateway, your configured S3 buckets will be available as Network File System (NFS) mount points or Server Message Block (SMB) file shares. Your applications read and write files and directories over NFS or SMB, interfacing to the gateway as a file server. In turn, the gateway translates these file operations into object requests on your S3 buckets.

Incorrect options:

Volume Gateway of AWS Storage Gateway - Volume Gateway provides an iSCSI target, which enables you to create block storage volumes and mount them as iSCSI devices from your on-premises or EC2 application servers. The Volume Gateway runs in either a cached or stored mode. Volume Gateway cannot be used for file storage.

Amazon Simple Storage Service (Amazon S3) - Amazon S3 is object storage built to store and retrieve any amount of data from anywhere. Amazon S3 provides a simple web service interface that you can use to store and retrieve any amount of data, at any time, from anywhere. Using this service, you can easily build applications that make use of cloud-native storage. The given use case needs a hybrid storage facility since the data will be accessed from the on-premises servers and applications on AWS Cloud. Hence, S3 is not the right choice.

Amazon Elastic Block Store (Amazon EBS) - Amazon Elastic Block Store (EBS) is an easy-to-use, high-performance, block-storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale. A broad range of workloads, such as relational and non-relational databases, enterprise applications, containerized applications, big data analytics engines, file systems, and media workflows are widely deployed on Amazon EBS. The given use case needs a hybrid storage facility since the data will be accessed from the on-premises servers and applications on AWS Cloud. Hence, EBS is not the right choice.

Reference:

https://aws.amazon.com/storagegateway/

Question 10

A SysOps Administrator was asked to enable versioning on an Amazon S3 bucket after a few objects were accidentally deleted by the development team.

Which of the following represent valid scenarios when a developer deletes an object in the versioning-enabled bucket? (Select two)
Multi Select
1

A delete marker is set on the deleted object, but the actual object is not deleted
2

GET requests can retrieve delete marker objects
3

A delete marker has a key, version ID and Access Control List (ACL) associated with it
4

GET requests do not retrieve delete marker objects
5

The delete marker has the same data associated with it, as the actual object
Correct Answer
1

A delete marker is set on the deleted object, but the actual object is not deleted
4

GET requests do not retrieve delete marker objects
Explanation

Correct options:

A delete marker is set on the deleted object, but the actual object is not deleted - A delete marker in Amazon S3 is a placeholder (or marker) for a versioned object that was named in a simple DELETE request. Because the object is in a versioning-enabled bucket, the object is not deleted. But the delete marker makes Amazon S3 behave as if it is deleted. A delete marker has a key name (or key) and version ID like any other object. It does not have data associated with it. It is not associated with an access control list (ACL) value.

GET requests do not retrieve delete marker objects - The only way to list delete markers (and other versions of an object) is by using the versions subresource in a GET Bucket versions request. A simple GET does not retrieve delete marker objects.

What Delete Markers are: via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/DeleteMarker.html

Incorrect options:

GET requests can retrieve delete marker objects

A delete marker has a key, version ID and Access Control List (ACL) associated with it

The delete marker has the same data associated with it, as the actual object

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/userguide/DeleteMarker.html

Question 11

An analytics company generates reports for various client applications, some of which have critical data. As per the company's compliance guidelines, data has to be encrypted during data exchange, for all channels of communication. An Amazon S3 bucket is configured as a website endpoint and this is now being added as a custom origin for CloudFront.

How will you secure this channel, as per the company's requirements?
1

Configure CloudFront that mandates viewers to use HTTPS to request objects from S3. Configure S3 bucket to support HTTPS communication only. This will force CloudFront to use HTTPS for communication between CloudFront and S3
2

Configure CloudFront to mandate viewers to use HTTPS to request objects from S3. However, CloudFront and S3 will use HTTP to communicate with each other
3

Communication between CloudFront and Amazon S3 is always on HTTP protocol since the network used for communication is internal to AWS and is inherently secure
4

CloudFront always forwards requests to S3 by using the protocol that viewers used to submit the requests. So, we only need to configure CloudFront to mandate the use of HTTPS for users
Correct Answer
2

Configure CloudFront to mandate viewers to use HTTPS to request objects from S3. However, CloudFront and S3 will use HTTP to communicate with each other
Explanation

Correct option:

Configure CloudFront to mandate viewers to use HTTPS to request objects from S3. CloudFront and S3 will use HTTP to communicate with each other

If your Amazon S3 bucket is configured as a website endpoint, you can't configure CloudFront to use HTTPS to communicate with your origin because Amazon S3 doesn't support HTTPS connections in that configuration.

HTTPS for Communication Between CloudFront and Your Amazon S3 Origin: via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https-cloudfront-to-s3-origin.html

Incorrect options:

Configure CloudFront that mandates viewers to use HTTPS to request objects from S3. Configure S3 bucket to support HTTPS communication only. This will force CloudFront to use HTTPS for communication between CloudFront and S3 - As discussed above, HTTPS between CloudFront and Amazon S3 is not supported when the S3 bucket is configured as a website endpoint.

Communication between CloudFront and Amazon S3 is always on HTTP protocol since the network used for communication is internal to AWS and is inherently secure - When your origin is an Amazon S3 bucket, your options for using HTTPS for communications with CloudFront depend on how you're using the bucket. If your Amazon S3 bucket is configured as a website endpoint, you can't configure CloudFront to use HTTPS to communicate with your origin.

When your origin is an Amazon S3 bucket that supports HTTPS communication, CloudFront always forwards requests to S3 by using the protocol that viewers used to submit the requests.

CloudFront always forwards requests to S3 by using the protocol that viewers used to submit the requests. So, we only need to configure CloudFront to mandate the use of HTTPS for users - This option has been added as a distractor. As mentioned earlier, if your Amazon S3 bucket is configured as a website endpoint, you can't configure CloudFront to use HTTPS while communicating with S3.

Reference:

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https-cloudfront-to-s3-origin.html

Question 12

A junior developer is tasked with creating necessary configurations for AWS CloudFormation that is extensively used in a project. After declaring the necessary stack policy, the developer realized that the users still do not have access to stack resources. The stack policy created by the developer looks like so:

{
  "Statement" : [
    {
      "Effect" : "Allow",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "*"
    },
    {
      "Effect" : "Deny",
      "Action" : "Update:*",
      "Principal": "*",
      "Resource" : "LogicalResourceId/ProductionDatabase"
    }
  ]
}

Why are the users unable to access the stack resources even after giving access permissions to all?
1

A stack policy applies only during stack updates, it doesn't provide access controls. The developer needs to provide access through IAM policies
2

The stack policy is invalid and hence the users are not granted any permissions. The developer needs to fix the syntactical errors in the policy
3

Stack policies do not allow wildcard character value (*) for the Principal element of the policy
4

Stack policies are associated with a particular IAM role or an IAM user. Hence, they only work for the users you have explicitly attached the policy to
Correct Answer
1

A stack policy applies only during stack updates, it doesn't provide access controls. The developer needs to provide access through IAM policies
Explanation

Correct option:

A stack policy applies only during stack updates, it doesn't provide access controls. The developer needs to provide access through IAM policies - When you create a stack, all update actions are allowed on all resources. By default, anyone with stack update permissions can update all of the resources in the stack. You can prevent stack resources from being unintentionally updated or deleted during a stack update by using a stack policy. A stack policy is a JSON document that defines the update actions that can be performed on designated resources.

After you set a stack policy, all of the resources in the stack are protected by default. To allow updates on specific resources, you specify an explicit Allow statement for those resources in your stack policy. You can define only one stack policy per stack, but, you can protect multiple resources within a single policy.

A stack policy applies only during stack updates. It doesn't provide access controls like an AWS Identity and Access Management (IAM) policy. Use a stack policy only as a fail-safe mechanism to prevent accidental updates to specific stack resources. To control access to AWS resources or actions, use IAM.

Incorrect options:

The stack policy is invalid and hence the users are not granted any permissions. The developer needs to fix the syntactical errors in the policy - This statement is incorrect and given only as a distractor.

Stack policies do not allow wildcard character value (*) for the Principal element of the policy - The Principal element specifies the entity that the policy applies to. This element is required while creating a policy but supports only the wildcard (*), which means that the policy applies to all principals.

Stack policies are associated with a particular IAM role or an IAM user. Hence, they only work for the users you have explicitly attached the policy to - A stack policy applies to all AWS CloudFormation users who attempt to update the stack. You can't associate different stack policies with different users.

Reference:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/protect-stack-resources.html

Question 13

A large IT company uses several AWS accounts for the different lines of business. Quite often, the systems administrator is faced with the problem of sharing Customer Master Keys (CMKs) across multiple AWS accounts for accessing AWS resources spread across these accounts.

How will you implement a solution to address this issue?
1

The key policy for the CMK must give the external account (or users and roles in the external account) permission to use the CMK. IAM policies in the external account must delegate the key policy permissions to its users and roles
2

Use AWS KMS service-linked roles to share access across AWS accounts
3

AWS Owned CMK can be used across AWS accounts. Configure an AWS Owned CMK and use it across accounts that need to share the key material
4

Declare a key policy for the CMK to give the external account permission to use the CMK. This key policy should be embedded with the first request of every transaction
Correct Answer
1

The key policy for the CMK must give the external account (or users and roles in the external account) permission to use the CMK. IAM policies in the external account must delegate the key policy permissions to its users and roles
Explanation

Correct option:

The key policy for the CMK must give the external account (or users and roles in the external account) permission to use the CMK. IAM policies in the external account must delegate the key policy permissions to its users and roles

You can allow IAM users or roles in one AWS account to use a customer master key (CMK) in a different AWS account. You can add these permissions when you create the CMK or change the permissions for an existing CMK.

To permit the usage of a CMK to users and roles in another account, you must use two different types of policies:

    The key policy for the CMK must give the external account (or users and roles in the external account) permission to use the CMK. The key policy is in the account that owns the CMK.

    IAM policies in the external account must delegate the key policy permissions to its users and roles. These policies are set in the external account and give permissions to users and roles in that account.

Incorrect options:

AWS Owned CMK can be used across AWS accounts. Configure an AWS Owned CMK and use it across accounts that need to share the key material - AWS owned CMKs are a collection of CMKs that an AWS service owns and manages for use in multiple AWS accounts. However, you cannot view, use, track, or audit them

Use AWS KMS service-linked roles to share access across AWS accounts - AWS Key Management Service uses AWS Identity and Access Management (IAM) service-linked roles. A service-linked role is a unique type of IAM role that is linked directly to AWS KMS. The service-linked roles are defined by AWS KMS and include all the permissions that the service requires to call other AWS services on your behalf. You cannot use AWS KMS service-linked roles to share access across AWS accounts.

Declare a key policy for the CMK to give the external account permission to use the CMK. This key policy should be embedded with the first request of every transaction - Key policy can not be directly shared across accounts.

References:

https://docs.aws.amazon.com/kms/latest/developerguide/key-policy-modifying-external-accounts.html

https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#aws-owned-cmk

Question 14

An e-commerce company is running its server infrastructure on Amazon EC2 instance store-backed instances. For better performance, the company has decided to move their applications to another Amazon EC2 instance store-backed instance with a different instance type.

How will you configure a solution for this requirement?
1

You can't resize an instance store-backed instance. Instead, you choose a new compatible instance and move your application to the new instance
2

You can't resize an instance store-backed instance. Instead, configure an EBS volume to be the root device for the instance and migrate using the EBS volume
3

Create an image of your instance, and then launch a new instance from this image with the instance type that you need. Take any Elastic IP address that you've associated with your original instance and associate it with the new instance for uninterrupted service to your application
4

Create an image of your instance, and then launch a new instance from this image with the instance type that you need. Any public IP address associated with the instance can be moved with the instance for uninterrupted access of services
Correct Answer
3

Create an image of your instance, and then launch a new instance from this image with the instance type that you need. Take any Elastic IP address that you've associated with your original instance and associate it with the new instance for uninterrupted service to your application
Explanation

Correct option:

Create an image of your instance, and then launch a new instance from this image with the instance type that you need. Take any Elastic IP address that you've associated with your original instance and associate it with the new instance for uninterrupted service to your application

When you want to move your application from one instance store-backed instance to an instance store-backed instance with a different instance type, you must migrate it by creating an image from your instance, and then launching a new instance from this image with the instance type that you need. To ensure that your users can continue to use the applications that you're hosting on your instance uninterrupted, you must take any Elastic IP address that you've associated with your original instance and associate it with the new instance. Then you can terminate the original instance.

Complete steps to migrate an instance store-backed instance: via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-resize.html

Incorrect options:

You can't resize an instance store-backed instance. Instead, you choose a new compatible instance and move your application to the new instance - An instance store-backed EC2 instance can be resized, as explained above.

You can't resize an instance store-backed instance. Instead, configure an EBS volume to be the root device for the instance and migrate using the EBS volume - This statement is incorrect.

Create an image of your instance, and then launch a new instance from this image with the instance type that you need. Any public IP address associated with the instance can be moved with the instance for uninterrupted access of services - Public IP addresses are released when an instance is changed. You need an Elastic IP to keep the service uninterrupted for users since these can be moved across instances.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-resize.html

Question 15

A developer is tasked with cleaning up obsolete resources. When he tried to delete an AWS CloudFormation stack, the stack deletion process returned without any error or a success message. The stack was not deleted either.

What is the reason for this behavior and how will you fix it?
1

The AWS user who initiated the stack deletion does not have enough permissions
2

Some resources must be empty before they can be deleted. Such resources will not be deleted if they are not empty and stack deletion fails without any error
3

If you attempt to delete a stack with termination protection enabled, the deletion fails and the stack - including its status - remains unchanged
4

Dependent resources should be deleted first, before deleting the rest of the resources in the stack. If this order is not followed, then stack deletion fails without an error
Correct Answer
3

If you attempt to delete a stack with termination protection enabled, the deletion fails and the stack - including its status - remains unchanged
Explanation

Correct option:

If you attempt to delete a stack with termination protection enabled, the deletion fails and the stack - including its status - remains unchanged

You cannot delete stacks that have termination protection enabled. If you attempt to delete a stack with termination protection enabled, the deletion fails and the stack - including its status - remains unchanged. Disable termination protection on the stack, then perform the delete operation again.

This includes nested stacks whose root stacks have termination protection enabled. Disable termination protection on the root stack, then perform the delete operation again. It is strongly recommended that you do not delete nested stacks directly, but only delete them as part of deleting the root stack and all its resources.

Complete steps for Stack deletion: via - https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-delete-stack.html

Incorrect options:

The AWS user who initiated the stack deletion does not have enough permissions - If the user does not have enough permissions to delete the stack, an error explaining the same is displayed and the stack will be in the DELETE_FAILED state.

Some resources must be empty before they can be deleted. Such resources will not be deleted if they are not empty and stack deletion fails without any error - Some resources must be empty before they can be deleted. For example, you must delete all objects in an Amazon S3 bucket or remove all instances in an Amazon EC2 security group before you can delete the bucket or security group. Otherwise, stack deletion fails and the stack will be in the DELETE_FAILED state.

Dependent resources should be deleted first, before deleting the rest of the resources in the stack. If this order is not followed, then stack deletion fails without an error - Any error during stack deletion will result in the stack being in the DELETE_FAILED state.

Reference:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting.html

Question 16

An organization that started as a single AWS account, gradually moved to a multi-account setup. The organization also has multiple AWS environments in each account, that were being managed at the account level. Backups are a big part of this management task. The organization is looking at moving to a centralized backup management process that consolidates and automates Cross-Region backup tasks across AWS accounts.

Which of the solutions below is the right choice for this requirement?
1

Configure AWS Systems Manager Maintenance Windows to schedule backup tasks as per company's policies. Tag the resources to help identify them by the AWS environment they run in. Amazon CloudWatch dashboards hosted by Systems Manager to get an overall view of the status of all resources under the AWS account
2

Use Amazon EventBridge to create a workflow for scheduled backup of all AWS resources under an account. Amazon S3 lifecycle policies, Amazon EC2 instance backups, and Amazon RDS backups can be used to create the events for the EventBridge. The same workflow can be scheduled to work on production and non-production environments, based on the tags created
3

Create a backup plan in AWS Backup. Assign tags to resources based on the environment ( Production, Development, Testing). Create one backup policy for production environments and one backup policy for non-production environments. Schedule the backup plan based on the organization's backup policies
4

Use Amazon Data Lifecycle Manager to manage creation, deletion, and managing of all the AWS resources under an account. Tag all the resources that need to be backed up and use lifecycle policies to customize the backup management to cater to the needs of the organization
Correct Answer
3

Create a backup plan in AWS Backup. Assign tags to resources based on the environment ( Production, Development, Testing). Create one backup policy for production environments and one backup policy for non-production environments. Schedule the backup plan based on the organization's backup policies
Explanation

Correct option:

Create a backup plan in AWS Backup. Assign tags to resources based on the environment ( Production, Development, Testing). Create one backup policy for production environments and one backup policy for non-production environments. Schedule the backup plan based on the organization's backup policies

AWS Backup is a fully managed and cost-effective backup service that simplifies and automates data backup across AWS services including Amazon EBS, Amazon EC2, Amazon RDS, Amazon Aurora, Amazon DynamoDB, Amazon EFS, and AWS Storage Gateway. In addition, AWS Backup leverages AWS Organizations to implement and maintain a central view of backup policy across resources in a multi-account AWS environment. Customers simply tag and associate their AWS resources with backup policies managed by AWS Backup for Cross-Region data replication.

The following post shows how to centrally manage backup tasks across AWS accounts in your organization by deploying backup policies with AWS Backup.

Example AWS Backup Architecture: via - https://aws.amazon.com/blogs/storage/centralized-cross-account-management-with-cross-region-copy-using-aws-backup/

Incorrect options:

Configure AWS Systems Manager Maintenance Windows to schedule backup tasks as per the company's policies. Tag the resources to help identify them by the AWS environment they run in. Amazon CloudWatch dashboards hosted by Systems Manager to get an overall view of the status of all resources under the AWS account

AWS Systems Manager Maintenance Windows let you define a schedule for when to perform potentially disruptive actions on your instances such as patching an operating system, updating drivers, or installing software or patches. Although a useful service, it is not suited for the given requirements.

Use Amazon EventBridge to create a workflow for scheduled backup of all AWS resources under an account. Amazon S3 lifecycle policies, Amazon EC2 instance backups, and Amazon RDS backups can be used to create the events for the EventBridge. The same workflow can be scheduled to work on production and non-production environments, based on the tags created - Amazon EventBridge is a serverless event bus that makes it easy to connect applications together using data from your own applications, integrated Software-as-a-Service (SaaS) applications, and AWS services. It is possible to build a backup solution using EventBridge, but it will not be an optimized one, since AWS offers services with better features for centrally managing backups.

Use Amazon Data Lifecycle Manager to manage creation, deletion and managing of all the AWS resources under an account. Tag all the resources that need to be backed up and use lifecycle policies to customize the backup management to cater to the needs of the organization - DLM provides a simple way to manage the lifecycle of EBS resources, such as volume snapshots. You should use DLM when you want to automate the creation, retention, and deletion of EBS snapshots.

References:

https://aws.amazon.com/blogs/storage/centralized-cross-account-management-with-cross-region-copy-using-aws-backup/

https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-maintenance.html

https://aws.amazon.com/eventbridge/

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html

Question 17

The development team at an IT company is looking at moving its web applications to Amazon EC2 instances. The team is weighing its options for EBS volumes and instance store-backed instances for these applications with varied workloads.

Which of the following would you identify as correct regarding instance store and EBS volumes? (Select three)
Multi Select
1

Use separate Amazon EBS volumes for the operating system and your data, even though root volume persistence feature is available
2

Data stored in the instance store is preserved when you stop or terminate your instance. However, data is lost when you hibernate the instance. Configure EBS volumes or have a backup plan to avoid using critical data to this behavior
3

EBS snapshots only capture data that has been written to your Amazon EBS volume, which might exclude any data that has been locally cached by your application or operating system
4

By default, data on a non-root EBS volume is preserved even if the instance is shutdown or terminated
5

EBS encryption does not support boot volumes
6

Snapshots of EBS volumes, stored on Amazon S3, can be accessed using Amazon S3 APIs
Correct Answer
1

Use separate Amazon EBS volumes for the operating system and your data, even though root volume persistence feature is available
3

EBS snapshots only capture data that has been written to your Amazon EBS volume, which might exclude any data that has been locally cached by your application or operating system
4

By default, data on a non-root EBS volume is preserved even if the instance is shutdown or terminated
Explanation

Correct options:

Use separate Amazon EBS volumes for the operating system and your data, even though root volume persistence feature is available

As a best practice, AWS recommends the use of separate Amazon EBS volumes for the operating system and your data. This ensures that the volume with your data persists even after instance termination or any issues to the operating system.

EBS snapshots only capture data that has been written to your Amazon EBS volume, which might exclude any data that has been locally cached by your application or operating system

Snapshots only capture data that has been written to your Amazon EBS volume, which might exclude any data that has been locally cached by your application or OS. To ensure consistent snapshots on volumes attached to an instance, AWS recommends detaching the volume cleanly, issuing the snapshot command, and then reattaching the volume. For Amazon EBS volumes that serve as root devices, AWS recommends shutting down the machine to take a clean snapshot.

By default, data on a non-root EBS volume is preserved even if the instance is shutdown or terminated

By default, when you attach a non-root EBS volume to an instance, its DeleteOnTermination attribute is set to false. Therefore, the default is to preserve these volumes. After the instance terminates, you can take a snapshot of the preserved volume or attach it to another instance. You must delete a volume to avoid incurring further charges.

Incorrect options:

Data stored in the instance store is preserved when you stop or terminate your instance. However, data is lost when you hibernate the instance. Configure EBS volumes or have a backup plan to avoid using critical data to this behavior - Data stored in instance store is lost when you stop, hibernate or terminate the instance.

EBS encryption does not support boot volumes - EBS volumes used as root devices can be encrypted without any issue.

Snapshots of EBS volumes, stored on Amazon S3, can be accessed using Amazon S3 APIs - This is incorrect. Snapshots are only available through the Amazon EC2 API.

References:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-best-practices.html

https://aws.amazon.com/ebs/faqs/

Question 18

A retail company has complex AWS VPC architecture that is getting difficult to maintain. The company has decided to configure VPC flow logs to track the network traffic to analyze various traffic flow scenarios. The systems administration team has configured VPC flow logs for one of the VPCs, but it's not able to see any logs. After initial analysis, the team has been able to track the error. It says Access error and the administrator of the team wants to change the IAM Role defined in the flow log definition.

What is the correct way of configuration a solution for this issue so that the VPC flow logs can be operational?
1

The error indicates that the IAM role does not have a trust relationship with the flow logs service. Change the trust relationship from flow log configuration
2

The flow log is still in the process of being created. It sometimes takes almost 10 minutes to start the logs
3

The error indicates IAM role is not correctly configured. After you've created a flow log, you cannot change its configuration. Instead, you need to delete the flow log and create a new one with the required configuration
4

The error indicates an internal error has occurred in the flow logs service. Raise a service request with AWS
Correct Answer
3

The error indicates IAM role is not correctly configured. After you've created a flow log, you cannot change its configuration. Instead, you need to delete the flow log and create a new one with the required configuration
Explanation

Correct option:

The error indicates the IAM role is not correctly configured. After you've created a flow log, you cannot change its configuration. Instead, you need to delete the flow log and create a new one with the required configuration

Access error can be caused by one of the following reasons:

    The IAM role for your flow log does not have sufficient permissions to publish flow log records to the CloudWatch log group

    The IAM role does not have a trust relationship with the flow logs service

    The trust relationship does not specify the flow logs service as the principal

After you've created a flow log, you cannot change its configuration or the flow log record format. For example, you can't associate a different IAM role with the flow log or add or remove fields in the flow log record. Instead, you can delete the flow log and create a new one with the required configuration.

Incorrect options:

The error indicates that the IAM role does not have a trust relationship with the flow logs service. Change the trust relationship from flow log configuration - As discussed above, the VPC flow log configuration cannot be changed once created.

The flow log is still in the process of being created. It sometimes takes almost 10 minutes to start the logs - This scenario is possible when you have just configured the flow logs. However, the status of the flow logs will not be in an error state.

The error indicates an internal error has occurred in the flow logs service. Raise a service request with AWS - This is a made-up option, given only as a distractor.

References:

https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs-troubleshooting.html

https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html#flow-log-records

Question 19

A data analytics company runs its technology operations on AWS Cloud using different VPC configurations for each of its applications. A systems administrator wants to configure the Network Access Control List (ACL) and Security Group (SG) of VPC1 to allow access for AWS resources in VPC2.

Which is the best way of configuring this requirement?
1

Network ACLs and Security Groups share a parent-child relationship. If resources in VPC2 are given inbound and outbound permissions on Network ACLs of VPC1, the resources will get necessary permissions on the associated security groups too
2

By default, Security Groups allow outbound traffic. Hence, only the inbound traffic configuration of the security groups have to be changed to allow requests from resources in VPC2 to access instances in VPC1. If the subnet is not associated with any Network ACL, you will not need any configuration changes
3

Based on the inbound and outbound traffic configurations on Network ACL of VPC1, you can create a similar deny rules on Security Groups of the instances in VPC1 to deny all traffic, other than the one originating from resources in VPC2
4

The Security Groups of instances on VPC1 should be configured to allow inbound traffic from resources in VPC2. By default, Network ACLs allow all inbound and outbound traffic. So, a default Network ACLs on VPC1 will not need any configuration changes
Correct Answer
4

The Security Groups of instances on VPC1 should be configured to allow inbound traffic from resources in VPC2. By default, Network ACLs allow all inbound and outbound traffic. So, a default Network ACLs on VPC1 will not need any configuration changes
Explanation

Correct option:

The Security Groups of instances on VPC1 should be configured to allow inbound traffic from resources in VPC2. By default, Network ACLs allow all inbound and outbound traffic. So, a default Network ACLs on VPC1 will not need any configuration changes - A security group acts as a virtual firewall for your instance to control inbound and outbound traffic. Security groups act at the instance level, not the subnet level. Therefore, each instance in a subnet in your VPC can be assigned to a different set of security groups.

A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups in order to add an additional layer of security to your VPC.

Security groups are stateful — if you send a request from your instance, the response traffic for that request is allowed to flow in regardless of inbound security group rules. Responses to allowed inbound traffic are allowed to flow out, regardless of outbound rules.

Network ACLs are stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).

Incorrect options:

Network ACLs and Security Groups share a parent-child relationship. If resources in VPC2 are given inbound and outbound permissions on Network ACLs of VPC1, the resources will get necessary permissions on the associated security groups too - This is an incorrect statement. Security Groups act at the instance level and Network ACLs are at the subnet level. They are different levels of security provided by AWS and do not form any hierarchy.

By default, Security Groups allow outbound traffic. Hence, only the inbound traffic configuration of the security groups have to be changed to allow requests from resources in VPC2 to access instances in VPC1. If the subnet is not associated with any Network ACL, you will not need any configuration changes - Each subnet in your VPC must be associated with a network ACL. If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with the default network ACL. Hence, a subnet will always have a network ACL associated with it.

Based on the inbound and outbound traffic configurations on Network ACL of VPC1, you can create similar deny rules on Security Groups of the instances in VPC1 to deny all traffic, other than the one originating from resources in VPC2 - Security Groups and Network ACLs are mutually exclusive and do not share permissions. Also, Security Groups can only be used to specify allow rules, and not deny rules.

References:

https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html

Question 20

A banking service uses Amazon EC2 instances and Amazon RDS databases to run its core business functionalities. The Chief Technology Officer (CTO) of the company has requested granular OS level metrics from the database service for benchmarking.

As a SysOps Administrator, how will you provide this information?
1

Enable Enhanced Monitoring for your RDS DB instance
2

Subscribe to Amazon RDS events to be notified when changes occur with a DB instance and its connected resources
3

Subscribe to CloudWatch metrics that track CPU utilization of the instances the RDS is hosted on
4

Enable Performance Insights to expand on the existing Amazon RDS monitoring features to illustrate your database's performance
Correct Answer
1

Enable Enhanced Monitoring for your RDS DB instance
Explanation

Correct option:

Enable Enhanced Monitoring for your RDS DB instance - Amazon RDS provides metrics in real time for the operating system (OS) that your DB instance runs on. You can view the metrics for your DB instance using the console. Also, you can consume the Enhanced Monitoring JSON output from Amazon CloudWatch Logs in a monitoring system of your choice.

By default, Enhanced Monitoring metrics are stored for 30 days in the CloudWatch Logs, which are different from typical CloudWatch metrics. Enhanced Monitoring for RDS provides the following OS metrics: 1.Free Memory 2.Active Memory 3.Swap Free 4.Processes Running 5.File System Used

You can use these metrics to understand the environment's performance, and these metrics are ingested by Amazon CloudWatch Logs as log entries. You can use CloudWatch to create alarms based on metrics. These alarms run actions, and you can publish these metrics from within your infrastructure, device, or application into CloudWatch as a custom metric. By using Enhanced Monitoring and CloudWatch together, you can automate tasks by creating a custom metric for the CloudWatch Logs RDS ingested date from the Enhanced Monitoring metrics. Enhanced Monitoring metrics are useful when you want to see how different processes or threads on a DB instance use the CPU.

Incorrect options:

Subscribe to Amazon RDS events to be notified when changes occur with a DB instance and its connected resources - Subscribe to Amazon RDS events to be notified when changes occur with a DB instance, DB snapshot, DB parameter group, or DB security group. Amazon RDS uses the Amazon Simple Notification Service (Amazon SNS) to provide notification when an Amazon RDS event occurs. This option is not relevant for the given use-case.

Subscribe to CloudWatch metrics that track CPU utilization of the instances the RDS is hosted on - CloudWatch gathers metrics about CPU utilization from the hypervisor for a DB instance, and Enhanced Monitoring gathers its metrics from an agent on the instance. As a result, you might find differences between the measurements, because the hypervisor layer performs a small amount of work. The differences can be greater if your DB instances use smaller instance classes because then there are likely more virtual machines (VMs) that are managed by the hypervisor layer on a single physical instance. Enhanced Monitoring metrics are useful when you want to see how different processes or threads on a DB instance use the CPU.

Enable Performance Insights to expand on the existing Amazon RDS monitoring features to illustrate your database's performance - Performance Insights collects metric data from the database engine to monitor the actual load on a database. Performance Insights will not help in gathering granular OS level metrics.

Reference:

https://aws.amazon.com/premiumsupport/knowledge-center/custom-cloudwatch-metrics-rds/

Question 21

Your application has complex runtime and OS dependencies and is taking a long time to be deployed on Elastic Beanstalk. You cannot sacrifice application availability.

What should you do to improve the deployment time? (Select two)
Multi Select
1

Create a Golden AMI with your application
2

Create a new beanstalk environment for each application and apply blue/green deployment patterns
3

Use rolling with additional batch
4

Upgrade the EC2 instance type
5

Use all at once deployment pattern
Correct Answer
1

Create a Golden AMI with your application
2

Create a new beanstalk environment for each application and apply blue/green deployment patterns
Explanation

Correct options:

Create a Golden AMI with your application

A Golden AMI is an AMI that you standardize through configuration, consistent security patching, and hardening. It also contains agents you approve for logging, security, performance monitoring, etc. For the given use-case, you can have the complex runtime and OS dependencies already setup via the golden AMI.

Golden AMI Pipeline: via - https://aws.amazon.com/blogs/awsmarketplace/announcing-the-golden-ami-pipeline/

Create a new beanstalk environment for each application and apply blue/green deployment patterns

Elastic Beanstalk provides several deployment policies and settings.

via - https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deploy-existing-version.html

Since AWS Elastic Beanstalk performs an in-place update when you update your application versions, your application can become unavailable to users for a short period of time. You can avoid this downtime by performing a blue/green deployment, where you deploy the new version to a separate environment, and then swap CNAMEs of the two environments to redirect traffic to the new version instantly.

via - https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.CNAMESwap.html

A blue/green deployment is also required when you want to update an environment to an incompatible platform version.

Incorrect options:

Use rolling with additional batch - With the rolling update, your application is deployed to your environment one batch of instances at a time. Most bandwidth is retained throughout the deployment. This also avoids downtime and minimizes reduced availability, at a cost of a longer deployment time. Since the use-case mandates a short deployment time, this option is ruled out.

Upgrade the EC2 instance type - An upgraded instance type may only marginally improve the deployment time.

Use all at once deployment pattern - With all at once deployment, Elastic Beanstalk deploys the new application version to each instance. Then, the web proxy or application server might need to restart. As a result, your application might be unavailable to users (or have low availability) for a short time. Since the use-case mandates high availability, this option is ruled out.

References:

https://aws.amazon.com/blogs/awsmarketplace/announcing-the-golden-ami-pipeline/

https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.CNAMESwap.html

https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deploy-existing-version.html

Question 22

You are deploying an application and use the cfn-init and cfn-signal script to ensure the application is properly deployed before signaling to CloudFormation the success of your stack deployment. Right now, every time you deploy, CloudFormation completes successfully, even though the instance is still executing the cfn-init script.

As a SysOps Administrator, which of the following would you identify as the root cause behind the issue?
1

You forgot the Wait Condition
2

You did not disable Rollbacks
3

You forgot to include the cfn-signal command in your user data
4

You forgot to include a deletion policy
Correct Answer
1

You forgot the Wait Condition
Explanation

Correct option:

You forgot the Wait Condition

The cfn-init helper script reads template metadata from the AWS::CloudFormation::Init key and acts accordingly to:

Fetch and parse metadata from AWS CloudFormation

Install packages

Write files to disk

Enable/disable and start/stop services

The cfn-signal helper script signals AWS CloudFormation to indicate whether Amazon EC2 instances have been successfully created or updated. If you install and configure software applications on instances, you can signal AWS CloudFormation when those software applications are ready.

You can use the wait condition handle to make AWS CloudFormation pause the creation of a stack and wait for a signal before it continues to create the stack. For example, you might want to download and configure applications on an Amazon EC2 instance before considering the creation of that Amazon EC2 instance complete.

AWS CloudFormation creates a wait condition just like any other resource. When AWS CloudFormation creates a wait condition, it reports the wait condition’s status as CREATE_IN_PROGRESS and waits until it receives the requisite number of success signals or the wait condition’s timeout period has expired. If AWS CloudFormation receives the requisite number of success signals before the time out period expires, it continues creating the stack; otherwise, it sets the wait condition’s status to CREATE_FAILED and rolls the stack back.

Incorrect options:

You did not disable Rollbacks - Enabling/disabling rollbacks has no impact on the ability to track the status of the cfn-init script.

You forgot to include the cfn-signal command in your user data - This is a distractor as the cfn-signal command is managed via CloudFormation and not via the user data.

You forgot to include a deletion policy - This is again a distractor as a deletion policy has nothing to do with tracking the status of the cfn-init script.

References:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-helper-scripts-reference.html

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-waitcondition.html

Question 23

As part of the best practices for DevOps, all your infrastructure is deployed using CloudFormation. This includes EBS volumes. When the CloudFormation stacks are deleted, it is mandatory to keep a snapshot of the EBS volumes for backup and compliance purposes.

How can you achieve this using CloudFormation?
1

Enable termination protection
2

Use cfn helper scripts and Wait Conditions upon stack deletion
3

Use DeletionPolicy=Snapshot
4

Reference the EBS volume as a stack output
Correct Answer
3

Use DeletionPolicy=Snapshot
Explanation

Correct option:

Use DeletionPolicy=Snapshot

To control how AWS CloudFormation handles the EBS volume when the stack is deleted, set a deletion policy for your volume. You can choose to retain the volume, to delete the volume, or to create a snapshot of the volume.

Here is the sample YAML:

NewVolume:
  Type: AWS::EC2::Volume
  Properties:
    Size: 100
    Encrypted: true
    AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
    Tags:
      - Key: MyTag
        Value: TagValue
  DeletionPolicy: Snapshot

via - https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html

Incorrect options:

Enable termination protection - You can prevent a stack from being accidentally deleted by enabling termination protection on the stack. If a user attempts to delete a stack with termination protection enabled, the deletion fails and the stack--including its status--remains unchanged. You can enable termination protection on a stack when you create it. Termination protection on stacks is disabled by default. You can set termination protection on a stack with any status except DELETE_IN_PROGRESS or DELETE_COMPLETE.

Use cfn helper scripts and Wait Conditions upon stack deletion - The cfn helper scripts such as cfn-init, cfn-signal, etc help in installing packages or to indicate whether Amazon EC2 instances have been successfully created or updated. You cannot use these scripts to mandatorily keep a snapshot of the EBS volume.

Reference the EBS volume as a stack output - The optional Outputs section for a CloudFormation stack declares output values that you can import into other stacks (to create cross-stack references), return in response (to describe stack calls), or view on the AWS CloudFormation console. You should note that a stack that is referenced by another stack cannot be deleted and it cannot modify or remove the exported value. Just by referencing the EBS volume as a stack output, you will not be able to enforce the snapshot of the EBS volume.

References:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html

https://aws.amazon.com/blogs/aws/aws-cloudformation-update-yaml-cross-stack-references-simplified-substitution/

Question 24

You are provisioning an internal full LAMP stack using CloudFormation, and the EC2 instance gets configured automatically using the cfn helper scripts, such as cfn-init and cfn-signal. The stack creation fails as CloudFormation fails to receive a signal from your EC2 instance.

What are the possible reasons for this? (Select two)
Multi Select
1

The subnet where the application is deployed does not have a network route to the CloudFormation service through a NAT Gateway or Internet Gateway
2

The EC2 instance does not have a proper IAM role allowing to signal the success to CloudFormation
3

The cfn-signal script does not get executed before the timeout of the wait condition
4

AWS is experiencing an Insufficient Capacity for the instance type you requested
5

The cfn-init script failed
Correct Answer
1

The subnet where the application is deployed does not have a network route to the CloudFormation service through a NAT Gateway or Internet Gateway
3

The cfn-signal script does not get executed before the timeout of the wait condition
Explanation

Correct options:

The subnet where the application is deployed does not have a network route to the CloudFormation service through a NAT Gateway or Internet Gateway - As the use-case mentions an internal full LAMP stack, this implies that the stack is to be deployed in a private subnet. Now this private subnet must have a network route to the CloudFormation service through a NAT Gateway or Internet Gateway.

You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.

An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It, therefore, imposes no availability risks or bandwidth constraints on your network traffic. Internet Gateways must be deployed in a public subnet and the corresponding entry should be added in the route table.

The cfn-signal script does not get executed before the timeout of the wait condition

The Timeout property determines how long AWS CloudFormation waits for the requisite number of success signals. Timeout is a minimum-bound property, meaning the timeout occurs no sooner than the time you specify, but can occur shortly thereafter. The maximum time that you can specify is 43200 seconds (12 hours ). For the given scenario, the stack creation can fail as CloudFormation may fail to receive a signal from your EC2 instance if the Timeout property is set to a low value.

Incorrect options:

The EC2 instance does not have a proper IAM role allowing to signal the success to CloudFormation - You do not need an IAM role to use cfn-signal.

AWS is experiencing an Insufficient Capacity for the instance type you requested - In case of Insufficient Capacity, the instance would have not been created and the CloudFormation stack would have failed altogether.

The cfn-init script failed - The cfn-init script failure should still be followed by the cfn-signal script, which would have sent a signal to CloudFormation nonetheless.

References:

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-comparison.html

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-waitcondition.html

Question 25

You are developing a new CloudFormation stack and writing some very complex cfn-init code. The code fails and you would like to debug why. When reading the documentation, you see all the logs are in the file /var/cfn/cfn-init-output.log and will give you more information as to why the instance provisioning is failing. But you realize that you can't gain access to this file as the CloudFormation stack always terminates the EC2 instance when the creation fails.

What can you do to access these logs files, while not changing the way your EC2 instance works and ensuring you can debug your instance over 24 hours?
1

Install the CloudWatch logs agent, create a new IAM role and assign it to the EC2 instance, and send the logs directly to CloudWatch Logs
2

Set OnFailure=DO_NOTHING
3

Increase the Wait Timeout to 2 hours
4

Enable VPC Flow Logs and intercept the cfn-init log file
Correct Answer
2

Set OnFailure=DO_NOTHING
Explanation

Correct option:

Set OnFailure=DO_NOTHING

You can use the OnFailure property of the CloudFormation CreateStack call for this use-case. The OnFailure property determines what action will be taken if stack creation fails. This must be one of DO_NOTHING, ROLLBACK, or DELETE. You can specify either OnFailure or DisableRollback, but not both.

Using the OnFailure property, you can prevent the termination of the EC2 instances created by the CloudFormation stack.

Incorrect options:

Install the CloudWatch logs agent, create a new IAM role and assign it to the EC2 instance, and send the logs directly to CloudWatch Logs

Enable VPC Flow Logs and intercept the cfn-init log file

As the use-case mentions that there should be no changes done to the EC2 instance, so both these options are ruled out since these involve installing or configuring additional software.

Increase the Wait Timeout to 2 hours - The wait timeout works with cfn-signal, however, the given issue is related to cfn-init wherein some underlying code is failing. Therefore increasing wait timeout is not a valid solution for this scenario.

References:

https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html

https://aws.amazon.com/premiumsupport/knowledge-center/cloudformation-prevent-rollback-failure/

Question 26

Your gp2 drive of 8TB is reaching its peak performance of 10,000 IOPS while being almost fully utilized.

How can you increase the performance while keeping the costs at the same level?
1

Convert the gp2 drive to io1 and increase the PIOPS
2

Create two 4 TB gp2 drives and mount them in RAID 0 on the EC2 instance
3

Create two 4 TB gp2 drives and mount them in RAID 1 on the EC2 instance
4

Enable burst mode on the gp2 drive
Correct Answer
2

Create two 4 TB gp2 drives and mount them in RAID 0 on the EC2 instance
Explanation

Correct option:

Create two 4 TB gp2 drives and mount them in RAID 0 on the EC2 instance

With Amazon EBS, you can use any of the standard RAID configurations that you can use with a traditional bare metal server, as long as that particular RAID configuration is supported by the operating system for your instance. This is because all RAID is accomplished at the software level.

For greater I/O performance than you can achieve with a single volume, RAID 0 can stripe multiple volumes together; for on-instance redundancy, RAID 1 can mirror two volumes together. So for the given use-case, to increase the performance, you should use RAID 0.

via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/raid-config.html

Incorrect options:

Convert the gp2 drive to io1 and increase the PIOPS - Changing the gp2 drive to io1 entails more costs as the pricing is $0.10 per GB-month of provisioned storage for gp2 and $0.125 per GB-month of provisioned storage for io1. So this option is ruled out.

Create two 4 TB gp2 drives and mount them in RAID 1 on the EC2 instance - You should use RAID 1 when fault tolerance is more important than I/O performance.

Enable burst mode on the gp2 drive - gp2 volumes can burst to 3,000 IOPS for extended periods of time. This option is a distractor as you do not need to enable the burst mode for gp2 volumes as it's available by default.

via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html

References:

https://aws.amazon.com/ebs/pricing/

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/raid-config.html

https://aws.amazon.com/blogs/database/understanding-burst-vs-baseline-performance-with-amazon-rds-and-gp2/

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html

Question 27

Which of the following services allows for an in-place switch from unencrypted to encrypted without impacting existing operations?
1

S3
2

RDS
3

EBS
4

EFS
Correct Answer
1

S3
Explanation

Correct options:

S3

Amazon S3 default encryption provides a way to set the default encryption behavior for an S3 bucket. You can set default encryption on a bucket so that all new objects are encrypted when they are stored in the bucket. The objects are encrypted using server-side encryption with either Amazon S3-managed keys (SSE-S3) or customer master keys (CMKs) stored in AWS Key Management Service (AWS KMS). When you use server-side encryption, Amazon S3 encrypts an object before saving it to disk and decrypts it when you download the objects.

There is no change to the encryption of the objects that existed in the bucket before default encryption was enabled.

So for the given use-case, you can continue to use the same S3 buckets without impacting operations.

Incorrect options:

RDS - You can only enable encryption for an Amazon RDS DB instance when you create it, not after the DB instance is created.

However, because you can encrypt a copy of an unencrypted snapshot, you can effectively add encryption to an unencrypted DB instance. That is, you can create a snapshot of your DB instance, and then create an encrypted copy of that snapshot. You can then restore a DB instance from the encrypted snapshot, and thus you have an encrypted copy of your original DB instance.

EBS - There is no direct way to encrypt an existing unencrypted volume or snapshot, you can encrypt them by creating either a volume or a snapshot. If you enabled encryption by default, Amazon EBS encrypts the resulting new volume or snapshot using your default key for EBS encryption.

EFS - You can enable encryption of data at rest when creating an Amazon EFS file system. Once the file system is created, you cannot modify the file system to be unencrypted or vice-versa.

References:

https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html

Question 28

How can you enforce encryption on all the files uploaded into your example S3 bucket?
1

Using the "Default Encryption" setting in AWS S3
2

Use the following S3 bucket policy:

{
    "Statement":[
        {
            "Action": "s3:*",
            "Effect":"Deny",
            "Principal": "*",
            "Resource":"arn:aws:s3:::bucketname/*",
            "Condition":{
                "Bool":
                { "aws:SecureTransport": false }
            }
        }
    ]
}

3

Use the following S3 bucket policy:

{
    "Statement":[
        {
            "Action": "s3:*",
            "Effect":"Deny",
            "Principal": "*",
            "Resource":"arn:aws:s3:::bucketname/*",
            "Condition":{
                "Bool":
                { "aws:SecureTransport": true }
            }
        }
    ]
}

4

Use an encrypted CloudFront distribution in front of your S3 bucket
Correct Answer
1

Using the "Default Encryption" setting in AWS S3
Explanation

Correct option:

Using the "Default Encryption" setting in AWS S3

Amazon S3 default encryption provides a way to set the default encryption behavior for an S3 bucket. You can set default encryption on a bucket so that all new objects are encrypted when they are stored in the bucket. The objects are encrypted using server-side encryption with either Amazon S3-managed keys (SSE-S3) or customer master keys (CMKs) stored in AWS Key Management Service (AWS KMS).

When you use server-side encryption, Amazon S3 encrypts an object before saving it to disk and decrypts it when you download the objects.

Incorrect options:

Use the following S3 bucket policy:

{
    "Statement":[
        {
            "Action": "s3:*",
            "Effect":"Deny",
            "Principal": "*",
            "Resource":"arn:aws:s3:::bucketname/*",
            "Condition":{
                "Bool":
                { "aws:SecureTransport": false }
            }
        }
    ]
}

The above bucket policy only denies access to HTTP requests for any action on the S3 bucket bucketname. It cannot help enforce SSE-S3 encryption on S3. So it's not the right fit for the given use-case.

Use the following S3 bucket policy:

{
    "Statement":[
        {
            "Action": "s3:*",
            "Effect":"Deny",
            "Principal": "*",
            "Resource":"arn:aws:s3:::bucketname/*",
            "Condition":{
                "Bool":
                { "aws:SecureTransport": true }
            }
        }
    ]
}

The above bucket policy only denies access to HTTPS requests for any action on the S3 bucket bucketname. It cannot help enforce SSE-S3 encryption on S3. So it's not the right fit for the given use-case.

Use an encrypted CloudFront distribution in front of your S3 bucket - This option is a distractor as you cannot enforce SSE-S3 encryption on S3 by using in-transit or at-rest encryption for CloudFront.

References:

https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html

https://aws.amazon.com/blogs/security/how-to-prevent-uploads-of-unencrypted-objects-to-amazon-s3/

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/data-protection-summary.html

Question 29

You are in S3 and have deleted all the files in it. As you can see, the bucket is empty:

You have tried to delete the bucket afterward and it fails with an error saying the bucket is not empty.

What's the issue?
1

S3 is eventually consistent. Wait two minutes and retry, it will work then
2

S3 versioning is enabled and delete markers are still present in the bucket
3

An S3 bucket policy is set up and it prevents bucket deletion
4

Some files are in Glacier
Correct Answer
2

S3 versioning is enabled and delete markers are still present in the bucket
Explanation

Correct option:

S3 versioning is enabled and delete markers are still present in the bucket

S3 Versioning is a means of keeping multiple variants of an object in the same bucket. You can use versioning to preserve, retrieve, and restore every version of every object stored in your Amazon S3 bucket. With versioning, you can easily recover from both unintended user actions and application failures. When you enable versioning for a bucket, if Amazon S3 receives multiple write requests for the same object simultaneously, it stores all of the objects.

If you overwrite an object, it results in a new object version in the bucket. You can always restore the previous version.

If you delete an object, instead of removing it permanently, Amazon S3 inserts a delete marker, which becomes the current object version.

So for the given use-case, as delete markers are still present in the bucket, therefore you get the error saying the bucket is not empty.

Incorrect options:

S3 is eventually consistent. Wait two minutes and retry, it will work then - This is a made-up option. Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions.

An S3 bucket policy is set up and it prevents bucket deletion - You could set up a bucket policy to prevent bucket deletion, but it would not present an error that says the bucket is not empty.

Some files are in Glacier - You store your data in Amazon S3 Glacier as archives. Archives may be further grouped into vaults. So files are not stored in buckets for Glacier. So while deleting, you will not get an error that says the bucket is not empty.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html

https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html#ConsistencyModel

https://aws.amazon.com/glacier/faqs/

Question 30

After enabling S3 MFA-Delete, for which actions do you need MFA? (Select two)
Multi Select
1

Permanently delete an object version
2

Suspending versioning
3

Enabling Versioning
4

Listing deleted versions
5

Uploading a new object version
Correct Answer
1

Permanently delete an object version
2

Suspending versioning
Explanation

Correct options:

Permanently delete an object version

Suspending versioning

You may add another layer of security by configuring a bucket to enable MFA (multi-factor authentication) Delete, which requires additional authentication for either of the following operations:

Change the versioning state of your bucket

Permanently delete an object version

MFA Delete requires two forms of authentication together:

Your security credentials

The concatenation of a valid serial number, a space, and the six-digit code displayed on an approved authentication device

If a bucket's versioning configuration is MFA Delete–enabled, the bucket owner must include the x-amz-mfa request header in requests to permanently delete an object version or change the versioning state of the bucket. Requests that include x-amz-mfa must use HTTPS.

Incorrect options:

Enabling Versioning - You do not need MFA to enable versioning for a bucket.

Listing deleted versions - You do not need MFA to list deleted versions.

Uploading a new object version - You do not need MFA to upload a new object version.

References:

https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html#MultiFactorAuthenticationDelete

Question 31

How should MFA-Delete be enabled on an S3 bucket?
1

Using the root account and the AWS Console
2

Using the root account and the AWS CLI
3

Using an admin IAM user and the AWS Console
4

Using an admin IAM user and the AWS CLI
Correct Answer
2

Using the root account and the AWS CLI
Explanation

Correct option:

Using the root account and the AWS CLI

MFA Delete represents another layer of security wherein you can configure a bucket to enable MFA (multi-factor authentication) Delete, which requires additional authentication for either of the following operations:

Change the versioning state of your bucket

Permanently delete an object version

You should note that only the bucket owner (root account) can enable MFA Delete only via the AWS CLI. However, the bucket owner, the AWS account that created the bucket (root account), and all authorized IAM users can enable versioning.

via - https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html#MultiFactorAuthenticationDelete

Incorrect options:

Using the root account and the AWS Console

Using an admin IAM user and the AWS Console

Using an admin IAM user and the AWS CLI

These three options contradict the explanation above, so these options are incorrect.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html#MultiFactorAuthenticationDelete

Question 32

You suspect some of your employees try to access files in S3 that they don't have access to.

How can you verify this is indeed the case without them noticing?
1

Restrict their IAM policies and look at CloudTrail logs
2

Enable S3 Access Logs and analyze them using Athena
3

Use a bucket policy
4

Use AWS Config to define compliance rules on these users
Correct Answer
2

Enable S3 Access Logs and analyze them using Athena
Explanation

Correct option:

Enable S3 Access Logs and analyze them using Athena

By default, Amazon Simple Storage Service (Amazon S3) doesn't collect server access logs. When you enable logging, Amazon S3 delivers access logs for a source bucket to a target bucket that you choose. The target bucket must be in the same AWS Region as the source bucket and must not have a default retention period configuration.

Server access logging provides detailed records for the requests that are made to an S3 bucket. Server access logs are useful for many applications. For example, access log information can be useful in security and access audits. It can also help you learn about your customer base and understand your Amazon S3 bill. Each access log record provides details about a single access request, such as the requester, bucket name, request time, request action, response status, and an error code, if relevant.

Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to set up or manage, and customers pay only for the queries they run. You can use Athena to process logs, perform ad-hoc analysis, and run interactive queries.

For the given use-case, you can enable S3 access logs and then use Athena to analyze the access patterns for specific employees.

Incorrect options:

Restrict their IAM policies and look at CloudTrail logs - Restricting their IAM policies would deny access to S3 which is to be avoided per the use-case.

Use a bucket policy - You cannot use a bucket policy to log S3 access information

Use AWS Config to define compliance rules on these users - AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. With Config, you can review changes in configurations and relationships between AWS resources, dive into detailed resource configuration histories, and determine your overall compliance against the configurations specified in your internal guidelines. You can use Config to answer questions such as - "What did my AWS resource look like at xyz point in time?". You cannot use AWS Config to log S3 access information.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerLogs.html

Question 33

As a service provider, you generate a daily report that you need to share with your dynamically changing list of over 10,000 customers. These reports sit in S3, and you would like to automate sharing the reports with them so they can have on-demand access upon their identity being proven.

You plan to use Cognito, API Gateway and AWS Lambda to address this use-case. On the S3 side, what should you do?
1

Provide each of your customers an AWS user and tell them to use the CLI
2

Generate pre-signed URLs for your reports
3

Create a bucket policy so that the S3 files are only accessible from CloudFront and force SSL mutual authentication there
4

Make the S3 bucket public and password protect each S3 file. Share the password with each customer
Correct Answer
2

Generate pre-signed URLs for your reports
Explanation

Correct option:

Generate pre-signed URLs for your reports

A presigned URL gives you access to the object identified in the URL, provided that the creator of the presigned URL has permissions to access that object.

All objects by default are private. Only the object owner has permission to access these objects. However, the object owner can optionally share objects with others by creating a presigned URL, using their own security credentials, to grant time-limited permission to download the objects.

When you create a presigned URL for your object, you must provide your security credentials, specify a bucket name, an object key, specify the HTTP method (GET to download the object) and expiration date and time. The presigned URLs are valid only for the specified duration.

Anyone who receives the presigned URL can then access the object. For example, if you have a video in your bucket and both the bucket and the object are private, you can share the video with others by generating a presigned URL.

Incorrect options:

Provide each of your customers an AWS user and tell them to use the CLI - This is not practicable considering that there are 10,000 customers.

Create a bucket policy so that the S3 files are only accessible from CloudFront and force SSL mutual authentication there - Mutual Transport Layer Security (TLS) authentication is supported for Amazon API Gateway and not for CloudFront. This is a new method for client-to-server authentication that can be used with API Gateway’s existing authorization options.

Make the S3 bucket public and password protect each S3 file. Share the password with each customer - This is a distractor as there is no way to password protect files on S3.

Reference:

https://docs.aws.amazon.com/AmazonS3/latest/dev/ShareObjectPreSignedURL.html

Question 34

In order to improve the read performance of the files stored in S3, you have decided to deploy it using CloudFront. As part of this deployment, you would like to ensure that only CloudFront is allowed to access the S3 bucket files.

How can you achieve that?
1

Using an Origin Access Identity and a bucket policy
2

Attaching an IAM role to CloudFront and defining a bucket policy to only allow this role
3

Encrypt all your files using a KMS key that only CloudFront can access
4

Attaching a security group to S3 and CloudFront and only allow incoming traffic from CloudFront using the security group rules
Correct Answer
1

Using an Origin Access Identity and a bucket policy
Explanation

Correct option:

Using an Origin Access Identity and a bucket policy

To restrict access to content that you serve from Amazon S3 buckets, you need to follow these steps:

Create a special CloudFront user called an origin access identity (OAI) and associate it with your distribution.

Configure your S3 bucket permissions so that CloudFront can use the OAI to access the files in your bucket and serve them to your users. Make sure that users can’t use a direct URL to the S3 bucket to access a file there.

via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html

After you take these steps, users can only access your files through CloudFront, not directly from the S3 bucket.

Incorrect options:

Attaching an IAM role to CloudFront and defining a bucket policy to only allow this role - This is a distractor as you cannot associate an IAM role to CloudFront.

Encrypt all your files using a KMS key that only CloudFront can access - Although you could enable SSE-KMS on S3 and serve content using CloudFront by using Lambda@Edge, but this solution does not address the given use-case. You can ensure that only CloudFront is allowed to access the S3 bucket files by using Origin Access Identity and a bucket policy.

via - https://aws.amazon.com/blogs/networking-and-content-delivery/serving-sse-kms-encrypted-content-from-s3-using-cloudfront/

Attaching a security group to S3 and CloudFront and only allow incoming traffic from CloudFront using the security group rules - This is a distractor as you cannot attach a security group to S3 or CloudFront.

References:

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html

https://aws.amazon.com/blogs/networking-and-content-delivery/serving-sse-kms-encrypted-content-from-s3-using-cloudfront/

Question 35

You distribute a monthly raw data extract of your public forum's discussions that is about 10TB each month. Currently, the archive is distributed through an EFS drive, that is mounted on all your EC2 instances. Customers retrieve the file through the load balancer you have. This solution is costing you a lot of money and forces you to tremendously scale on the 1st of each month as people all try to retrieve the file at the same time.

What can you do to improve the situation?
1

Enable static file caching on the ALB
2

Store the files in S3 and distribute them using a CloudFront distribution instead
3

Store the files on instance stores instead, so you don't need to use EFS anymore
4

Enable enhanced networking between EC2 and ALB
Correct Answer
2

Store the files in S3 and distribute them using a CloudFront distribution instead
Explanation

Correct option:

Store the files in S3 and distribute them using a CloudFront distribution instead

S3 is more cost-effective than EFS. For example, per GB storage cost for S3 is $0.023/month whereas per GB storage cost for EFS is $0.3/month. Further, storing your static content with S3 provides a lot of advantages. But to help optimize your application’s performance and security while effectively managing cost, AWS recommends that you also set up Amazon CloudFront to work with your S3 bucket to serve and protect the content. CloudFront is a content delivery network (CDN) service that delivers static and dynamic web content, video streams, and APIs around the world, securely and at scale. By design, delivering data out of CloudFront can be more cost-effective than delivering it from S3 directly to your users.

Incorrect options:

Enable static file caching on the ALB - This is a distractor as there is no such thing as static file caching on the ALB.

Store the files on instance stores instead, so you don't need to use EFS anymore - You cannot use Instance Stores since they are physically attached to their own EC2 instances. Instance Store is not a shared storage like EFS, so this option is ruled out.

Enable enhanced networking between EC2 and ALB - Enhanced networking uses single root I/O virtualization (SR-IOV) to provide high-performance networking capabilities on supported EC2 instance types. SR-IOV is a method of device virtualization that provides higher I/O performance and lower CPU utilization when compared to traditional virtualized network interfaces. There is no such thing as enhanced networking between EC2 and ALB.

References:

https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/enhanced-networking.html

Question 36

Your website is hosted on S3 and exposed through a CloudFront distribution and some users are said to experience a lot of 501 errors.

How can you analyze these errors and come up with a solution?
1

Analyze the CloudFront access logs using Athena
2

Analyze the CloudFront access logs using Inspector
3

Enable S3 access logs and analyze using Athena
4

Enable S3 access logs and analyze using Inspector
Correct Answer
1

Analyze the CloudFront access logs using Athena
Explanation

Correct option:

Analyze the CloudFront access logs using Athena

You can configure CloudFront to create log files that contain detailed information about every user request that CloudFront receives. These are called standard logs, also known as access logs. These standard logs are available for both web and RTMP distributions. If you enable standard logs, you can also specify the Amazon S3 bucket that you want CloudFront to save files in.

via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/AccessLogs.html

AWS recommends that you use the logs to understand the nature of the requests for your content, not as a complete accounting of all requests. CloudFront delivers access logs on a best-effort basis. The log entry for a particular request might be delivered long after the request was actually processed and, in rare cases, a log entry might not be delivered at all. When a log entry is omitted from access logs, the number of entries in the access logs won't match the usage that appears in the AWS usage and billing reports.

Incorrect options:

Analyze the CloudFront access logs using Inspector

Enable S3 access logs and analyze using Inspector

Amazon Inspector is an automated security assessment service that helps you test the network accessibility of your Amazon EC2 instances and the security state of your applications running on the instances.

Inspector cannot be used to analyze CloudFront access logs or S3 access logs, so both these options are incorrect.

Enable S3 access logs and analyze using Athena - The S3 access logs will not provide details about the user IP and other crucial information, as the requests are proxied through CloudFront. Additionally, results are cached in CloudFront and the S3 access logs won't contain a lot of information, so this option is incorrect.

Reference:

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/AccessLogs.html

Question 37

You host a forum for law questions and per your country's law, you must store all the archives of conversations (about 1 TB) every week for 7 years. These archives must not be tampered with in any way, and you must prove you have set enough controls around your data protection.

What should you do?
1

Store the archives in S3 and set up a bucket policy, enable versioning and MFA-Delete
2

Store the archives in Glacier and set up a Vault Lock Policy for WORM access
3

Store the archives in EBS and use Linux file system protection on the files
4

Store the archives in AWS Artifact and enable compliance monitoring
Correct Answer
2

Store the archives in Glacier and set up a Vault Lock Policy for WORM access
Explanation

Correct option:

Store the archives in Glacier and set up a Vault Lock Policy for WORM access

You store your data in Amazon S3 Glacier as archives. Archives may be further grouped into vaults.

S3 Glacier Vault Lock allows you to easily deploy and enforce compliance controls for individual S3 Glacier vaults with a vault lock policy. You can specify controls such as “write once read many” (WORM) in a vault lock policy and lock the policy from future edits. Once locked, the policy can no longer be changed.

For the given use-case, as you need to ensure that the archives are not tampered, so you need to store the archives in Glacier and set up a Vault Lock Policy for WORM access.

via - https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html

Incorrect options:

Store the archives in S3 and set up a bucket policy, enable versioning and MFA-Delete - Even if you store the archives in a versioned S3 bucket, someone could overwrite the archive and create a new version of it so it does not strictly meet the requirements of the given use-case wherein an existing object mutates into a new version. MFA-Delete would only protect against permanent delete of any object.

Store the archives in EBS and use Linux file system protection on the files Linux file system protection would not be able to enforce compliance controls for the archives in EFS.

Store the archives in AWS Artifact and enable compliance monitoring - AWS Artifact is a self-service audit artifact retrieval portal that provides our customers with on-demand access to AWS’ compliance documentation and AWS agreements. You cannot use AWS Artifact to enforce compliance controls for the archives.

Reference:

https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html

Question 38

Your data center generates tens of terabytes of data daily and has a cumulative historic data volume of 5PB. The data center is running short of storage as well as bandwidth infrastructure to store or transfer this data. Later you would like to analyze this data using Redshift or Athena, however, first you must clean it using a proprietary process running on EC2.

What's the optimal way of moving this data to the cloud?
1

Use S3 transfer acceleration
2

Use Snowball Edge
3

Use Volume Gateway
4

Use AWS Data Migration
Correct Answer
2

Use Snowball Edge
Explanation

Correct option:

Use Snowball Edge

AWS Snowball, a part of the AWS Snow Family, is a data migration and edge computing device that comes in two options. Snowball Edge Storage Optimized devices provide both block storage and Amazon S3-compatible object storage, and 40 vCPUs. They are well suited for local storage and large scale data transfer. Snowball Edge Compute Optimized devices provide 52 vCPUs, block and object storage, and an optional GPU for use cases like advanced machine learning and full-motion video analysis in disconnected environments.

Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 TB of usable HDD storage, 40 vCPUs, 1 TB of SATA SSD storage, and up to 40 Gb network connectivity to address large scale data transfer and pre-processing use cases.

For the given use-case, you can use multiple Snowball Edge devices to migrate the entire data to AWS Cloud.

Exam Alert:

The original Snowball devices were transitioned out of service and Snowball Edge Storage Optimized are now the primary devices used for data transfer. You may see the Snowball device on the exam, just remember that the original Snowball device had 80TB of storage space.

Incorrect options:

Use S3 transfer acceleration - Amazon S3 Transfer Acceleration can speed up content transfers to and from Amazon S3 by as much as 50-500% for long-distance transfer of larger objects. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path. As the data center does not have sufficient bandwidth infrastructure, so this option is ruled out.

Use Volume Gateway - You can configure the AWS Storage Gateway service as a Volume Gateway to present cloud-based iSCSI block storage volumes to your on-premises applications. The Volume Gateway provides either a local cache or full volumes on-premises while also storing full copies of your volumes in the AWS cloud. Volume Gateway also provides Amazon EBS Snapshots of your data for backup, disaster recovery, and migration. It's easy to get started with the Volume Gateway: Deploy it as a virtual machine or hardware appliance, give it local disk resources, connect it to your applications, and start using your hybrid cloud storage for block data. As the data center does not have sufficient bandwidth infrastructure, so this option is ruled out.

How Storage Gateway Works: via - https://aws.amazon.com/storagegateway/

Use AWS Data Migration - AWS Database Migration Service helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. The AWS Database Migration Service can migrate your data to and from the most widely used commercial and open-source databases. As the data center does not have sufficient bandwidth infrastructure, so this option is ruled out.

References:

https://aws.amazon.com/snowball/

https://aws.amazon.com/dms/

https://aws.amazon.com/storagegateway/

Question 39

You have tape backup processes and you would like to start migrating to the cloud to leverage the S3 storage capacity while keeping the same processes and iSCSI-compatible backup software you purchased a 10-year license for.

What do you recommend your company should be using?
1

File Gateway
2

Volume Gateway
3

Tape Gateway
4

Snowball
Correct Answer
3

Tape Gateway
Explanation

Correct option:

Tape Gateway

Tape Gateway enables you to replace using physical tapes on-premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway supports all leading backup applications and caches virtual tapes on-premises for low-latency data access. Tape Gateway encrypts data between the gateway and AWS for secure data transfer and compresses data and transitions virtual tapes between Amazon S3 and Amazon S3 Glacier, or Amazon S3 Glacier Deep Archive, to minimize storage costs.

How Storage Gateway Works: via - https://aws.amazon.com/storagegateway/

How Tape Gateway Works: via - https://aws.amazon.com/storagegateway/vtl/

Incorrect options:

File Gateway - File Gateway provides a seamless way to connect to the cloud in order to store application data files and backup images as durable objects in Amazon S3 cloud storage. File Gateway offers SMB or NFS-based access to data in Amazon S3 with local caching. It can be used for on-premises applications, and for Amazon EC2-based applications that need file protocol access to S3 object storage.

File Gateway cannot be used to facilitate tape backup processes.

Volume Gateway - You can configure the AWS Storage Gateway service as a Volume Gateway to present cloud-based iSCSI block storage volumes to your on-premises applications. The Volume Gateway provides either a local cache or full volumes on-premises while also storing full copies of your volumes in the AWS cloud. Volume Gateway also provides Amazon EBS Snapshots of your data for backup, disaster recovery, and migration. It's easy to get started with the Volume Gateway: Deploy it as a virtual machine or hardware appliance, give it local disk resources, connect it to your applications, and start using your hybrid cloud storage for block data.

Volume Gateway cannot be used to facilitate tape backup processes.

Snowball - AWS Snowball, a part of the AWS Snow Family, is a data migration and edge computing device that comes in two options. Snowball Edge Storage Optimized devices provide both block storage and Amazon S3-compatible object storage, and 40 vCPUs. They are well suited for local storage and large scale data transfer. Snowball Edge Compute Optimized devices provide 52 vCPUs, block and object storage, and an optional GPU for use cases like advanced machine learning and full-motion video analysis in disconnected environments.

Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 TB of usable HDD storage, 40 vCPUs, 1 TB of SATA SSD storage, and up to 40 Gb network connectivity to address large scale data transfer and pre-processing use cases.

Snowball cannot be used to facilitate tape backup processes.

References:

https://aws.amazon.com/storagegateway/vtl/

https://aws.amazon.com/storagegateway/

https://aws.amazon.com/snowball/

Question 40

You would like to replace your on-premise NFS v3 drive with something that will leverage the huge capacity of Amazon S3. You would like to ensure files that are commonly used are locally cached on-premises.

What should you use?
1

EFS
2

File Gateway
3

EBS Drives
4

Volume Gateway
Correct Answer
2

File Gateway
Explanation

Correct option:

File Gateway - File Gateway provides a seamless way to connect to the cloud in order to store application data files and backup images as durable objects in Amazon S3 cloud storage. File Gateway offers SMB or NFS-based access to data in Amazon S3 with local caching. It can be used for on-premises applications, and for Amazon EC2-based applications that need file protocol access to S3 object storage.

How Storage Gateway Works: via - https://aws.amazon.com/storagegateway/

How File Gateway Works: via - https://aws.amazon.com/storagegateway/file/

Incorrect options:

EFS - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics (such as strong consistency and file locking), and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon S3 is an object storage service. EFS cannot leverage S3 for storage.

EBS Drives - Amazon Elastic Block Store (EBS) is an easy to use, high-performance, block-storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale. A broad range of workloads, such as relational and non-relational databases, enterprise applications, containerized applications, big data analytics engines, file systems, and media workflows are widely deployed on Amazon EBS. EBS cannot leverage S3 for storage.

Volume Gateway - You can configure the AWS Storage Gateway service as a Volume Gateway to present cloud-based iSCSI block storage volumes to your on-premises applications. The Volume Gateway provides either a local cache or full volumes on-premises while also storing full copies of your volumes in the AWS cloud. Volume Gateway also provides Amazon EBS Snapshots of your data for backup, disaster recovery, and migration. It's easy to get started with the Volume Gateway: Deploy it as a virtual machine or hardware appliance, give it local disk resources, connect it to your applications, and start using your hybrid cloud storage for block data. Since Volume Gateway represents cloud-backed iSCSI block storage, so it cannot be used to replace an on-premise NFS v3 drive, so this option is incorrect.

How Volume Gateway Works: via - https://aws.amazon.com/storagegateway/volume/

References:

https://aws.amazon.com/storagegateway/file/

https://aws.amazon.com/storagegateway/volume/

https://aws.amazon.com/storagegateway/

Question 41

You just released a new mobile game and users have the chance to interact with each other. In order to publish a profile picture, your company has made the architectural decision to have users directly upload their images into a designated S3 bucket.

How can you provide write access to the mobile application users effectively?
1

Create an AWS Lambda function that will create an IAM User for each new user, and store their API keys in the mobile app database
2

Create one IAM user and publish the access keys as part of the mobile application
3

Federate the users with SAML so they can use Single Sign-On (SSO) to access S3
4

Federate the users with Cognito so they can assume a role to access S3
Correct Answer
4

Federate the users with Cognito so they can assume a role to access S3
Explanation

Correct option:

Federate the users with Cognito so they can assume a role to access S3

Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0. Application-specific user authentication can be provided via a Cognito User Pool and then users can access AWS services such as S3 using a Cognito Identity Pool. Here Cognito is the best technology choice for managing mobile user accounts.

via - https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-integrating-user-pools-with-identity-pools.html

Amazon Cognito Features: via - https://aws.amazon.com/cognito/details/

Exam Alert:

Please review the following note to understand the differences between Cognito User Pools and Cognito Identity Pools: via - https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html

Incorrect options:

Create an AWS Lambda function that will create an IAM User for each new user, and store their API keys in the mobile app database - Creating an IAM user for each new user of the mobile phone is not practicable, so this option is ruled out.

Create one IAM user and publish the access keys as part of the mobile application - This is a security bad-practice. You should not expose the IAM user access keys via a third-party application. The best solution is to use Cognito user pool for authentication and then access AWS services using an identity pool.

Federate the users with SAML so they can use Single Sign-On (SSO) to access S3 - The scenario does not mention that the users belong to a specific organization, therefore you cannot use SAML to facilitate SSO to access S3.

via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html

References:

https://aws.amazon.com/cognito/details/

https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html

https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html

https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-integrating-user-pools-with-identity-pools.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html

Question 42

Your home-cooking website stores its recipes and comments from users in a Multi-AZ RDS database, which is located in a private subnet. As of yesterday, it seems that your users are unable to access the website and see an error message "512 - Cannot connect to the database".

What could be the reason why the website cannot connect to the database anymore? (Select three)
Multi Select
1

DB Security Group inbound rules have changed
2

Network ACL inbound rules have changed
3

Security Group outbound rules have changed
4

Network ACL outbound rules have changed
5

The primary database's private IP has changed
6

A read replica has been created recently
Correct Answer
1

DB Security Group inbound rules have changed
2

Network ACL inbound rules have changed
4

Network ACL outbound rules have changed
Explanation

Correct options:

DB Security Group inbound rules have changed

A security group acts as a virtual firewall that controls the traffic for one or more instances. When you launch an instance, you can specify one or more security groups; otherwise, we use the default security group. You can add rules to each security group that allows traffic to or from its associated instances. You can modify the rules for a security group at any time; the new rules are automatically applied to all instances that are associated with the security group. When we decide whether to allow traffic to reach an instance, we evaluate all the rules from all the security groups that are associated with the instance.

The following are the characteristics of security group rules:

By default, security groups allow all outbound traffic.

Security group rules are always permissive; you can't create rules that deny access.

Security groups are stateful

For the given use-case, if the DB Security Group inbound rules have changed, then the website may not be able to connect to the database.

Network ACL inbound rules have changed

Network ACL outbound rules have changed

A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups in order to add an additional layer of security to your VPC.

The following are the basic things that you need to know about network ACLs:

The default NACL allows all inbound and outbound IPv4 traffic and, if applicable, IPv6 traffic.

You can create a custom network ACL and associate it with a subnet. By default, each custom network ACL denies all inbound and outbound traffic until you add rules.

Each subnet in your VPC must be associated with a network ACL. If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with the default network ACL.

You can associate a network ACL with multiple subnets. However, a subnet can be associated with only one network ACL at a time. When you associate a network ACL with a subnet, the previous association is removed.

A network ACL contains a numbered list of rules. AWS evaluates the rules in order, starting with the lowest numbered rule, to determine whether traffic is allowed in or out of any subnet associated with the network ACL. The highest number that you can use for a rule is 32766. AWS recommends that you start by creating rules in increments (for example, increments of 10 or 100) so that you can insert new rules where you need to later on.

A network ACL has separate inbound and outbound rules, and each rule can either allow or deny traffic.

Network ACLs are stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).

For the given use-case, if the inbound or the outbound NACL rules have changed, then the website may not be able to connect to the database.

Incorrect options:

Security Group outbound rules have changed - Since security groups are stateful so incoming connections can send a reply back to, regardless of any outbound rules, so this option is incorrect.

The primary database's private IP has changed - The private IP associated with an RDS database can change due to things such as multi-AZ failover, so you should use the DNS endpoint to connect to the database. Even if the private IP of the database changes, the DNS endpoint would not change on its own. So this option is incorrect.

A read replica has been created recently - Adding a read replica does not change the primary database's DNS name, so this option is ruled out.

References:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html

Question 43

The Big Data team at an insurance company is performing a nightly ETL on top of your production RDS database to compute a view and then extract it into their data lake in Amazon S3. This query has been performing reasonably well in your website's infancy but now that it has grown in popularity, the query is running for a much longer period and affects the user experience while they browse your website.

How can you improve the situation in the short and long term?
1

Enable RDS Multi-AZ
2

Create an RDS Read Replica for the ETL team
3

Upgrade the RDS instance type
4

Use Athena to query RDS
Correct Answer
2

Create an RDS Read Replica for the ETL team
Explanation

Correct option:

Create an RDS Read Replica for the ETL team

Amazon RDS Read Replicas provide enhanced performance and durability for RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. For the MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server database engines, Amazon RDS creates a second DB instance using a snapshot of the source DB instance. It then uses the engines' native asynchronous replication to update the read replica whenever there is a change to the source DB instance.

For the given use-case, you can use one or more read replicas for the given source DB instance as the source for the ETL process to populate the data lake on S3.

via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html

Incorrect options:

Enable RDS Multi-AZ - Amazon RDS Multi-AZ deployments provide enhanced availability and durability for RDS database (DB) instances, making them a natural fit for production database workloads. When you provision a Multi-AZ DB Instance, Amazon RDS automatically creates a primary DB Instance and synchronously replicates the data to a standby instance in a different Availability Zone (AZ). You cannot use Multi-AZ to improve the ETL process as it cannot use the standby instance as a source for the ETL process.

Exam Alert:

Please review the key differences between Read Replicas and Multi-AZ: via - https://aws.amazon.com/rds/features/multi-az/

Upgrade the RDS instance type - Upgrade the RDS instance type may help a little bit, but the problem will resurface as traffic increases further. A better solution is to use the Read Replica as the source for the ETL process to populate the data lake on S3.

Use Athena to query RDS - Although Athena can query data from RDS by using its federated query feature, however, the problem would persist as the entire ETL load will fall on the main database. A better solution is to use the Read Replica as the source for the ETL process to populate the data lake on S3.

References:

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html

https://aws.amazon.com/rds/features/multi-az/

https://aws.amazon.com/blogs/big-data/query-any-data-source-with-amazon-athenas-new-federated-query/

Question 44

Your RDS database sometimes can become unresponsive, failing health checks and you need your application to fail-over automatically and safely without losing any committed transactions.

Which options would you choose?
1

Create an RDS read replica in the same region and an AWS lambda function to promote that replica as the main database when the main RDS database is down
2

Enable RDS Multi-AZ
3

Create an RDS read replica in a different region and an AWS lambda function to promote that replica as the main database when the main RDS database is down
4

Setup a CloudWatch alarm for DB RAM going over 90% and reboot the database then
Correct Answer
2

Enable RDS Multi-AZ
Explanation

Correct option:

Enable RDS Multi-AZ

RDS provides high availability and failover support for DB instances using Multi-AZ deployments. In a Multi-AZ deployment, RDS automatically provisions and maintains a synchronous standby replica in a different Availability Zone.

The failover happens only in the following conditions:

The primary DB instance fails

An Availability Zone outage

The DB instance server type is changed

The operating system of the DB instance is undergoing software patching.

A manual failover of the DB instance can be initiated using Reboot with failover.

via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html

Incorrect options:

Create an RDS read replica in the same region and an AWS lambda function to promote that replica as the main database when the main RDS database is down

Create an RDS read replica in a different region and an AWS lambda function to promote that replica as the main database when the main RDS database is down

RDS Read Replicas provide enhanced performance and durability for RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. Whether you create the Read Replica in the same AWS Region or a different Region from the primary DB, you cannot use it for building a High Availability solution that also transparently switches to the standby by maintaining the same DB endpoint. Using AWS Lambda to promote the Read Replica as the main database when the primary RDS database is down, would cause the DB endpoint to change.

Therefore, both of these options are incorrect.

Exam Alert:

Please review the key differences between Read Replicas and Multi-AZ: via - https://aws.amazon.com/rds/features/multi-az/

Setup a CloudWatch alarm for DB RAM going over 90% and reboot the database then - This is akin to applying a band-aid. As the root cause persists, as soon as the DB instance is up and running, you will face the DB performance issues again.

References:

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html

https://aws.amazon.com/rds/features/multi-az/

Question 45

You have a production Postgres RDS database and a custom rule in AWS Config has been set up and shows that some connections established to your database are not encrypted.

How can you ensure all connections to RDS are encrypted?
1

Edit the security group rules
2

Review the DB parameter groups
3

Enable SSL connections from the RDS Console
4

Patch the database with the SSL/TLS Postgres Addon
Correct Answer
2

Review the DB parameter groups
Explanation

Correct option:

Review the DB parameter groups

You can allow only SSL connections to your RDS for PostgreSQL database instance by enabling the rds.force_ssl parameter ("0" by default) through the parameter groups page on the RDS Console or through the CLI.

via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.SSL

Incorrect options:

Edit the security group rules - Security group can be used to allow connections based on certain inbound rules from selected sources. However, you need to use parameter groups to enforce SSL.

Enable SSL connections from the RDS Console - This is a made-up option and has been added as a distractor.

Patch the database with the SSL/TLS Postgres Addon - You cannot install patches on RDS databases as these are completely managed by AWS, so this option is incorrect.

Reference:

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.SSL

Question 46

A retail company has realized that their Amazon EBS volume backed EC2 instance is consistently over-utilized and needs an upgrade. A developer has connected with you to understand the key parameters to be considered when changing the instance type.

As a SysOps Administrator, which of the following would you identify as correct regarding the instance types for the given use-case? (Select three)
Multi Select
1

Resizing of an instance is only possible if the root device for your instance is an EBS volume
2

The new instance retains its public, private IPv4 addresses, any Elastic IP addresses, and any IPv6 addresses that were associated with the old instance
3

You must stop your Amazon EBS–backed instance before you can change its instance type. AWS moves the instance to new hardware; however, the instance ID does not change
4

If your instance is in an Auto Scaling group, the Amazon EC2 Auto Scaling service marks the stopped instance as unhealthy, and may terminate it and launch a replacement instance
5

There is no downtime on the instance if you choose an instance of a compatible type since AWS starts the new instance and shifts the applications from current instance
6

Resizing of an instance is possible if the root device is either EBS volume or an instance store volume. However, instance store volumes taking longer to start on the new instance, since cache data is lost on these instances
Correct Answer
1

Resizing of an instance is only possible if the root device for your instance is an EBS volume
3

You must stop your Amazon EBS–backed instance before you can change its instance type. AWS moves the instance to new hardware; however, the instance ID does not change
4

If your instance is in an Auto Scaling group, the Amazon EC2 Auto Scaling service marks the stopped instance as unhealthy, and may terminate it and launch a replacement instance
Explanation

Correct options:

Resizing of an instance is only possible if the root device for your instance is an EBS volume - If the root device for your instance is an EBS volume, you can change the size of the instance simply by changing its instance type, which is known as resizing it. If the root device for your instance is an instance store volume, you must migrate your application to a new instance with the instance type that you need.

You must stop your Amazon EBS–backed instance before you can change its instance type. AWS moves the instance to new hardware; however, the instance ID does not change - You must stop your Amazon EBS–backed instance before you can change its instance type. When you stop and start an instance, AWS moves the instance to new hardware; however, the instance ID does not change.

If your instance is in an Auto Scaling group, the Amazon EC2 Auto Scaling service marks the stopped instance as unhealthy, and may terminate it and launch a replacement instance - If your instance is in an Auto Scaling group, the Amazon EC2 Auto Scaling service marks the stopped instance as unhealthy, and may terminate it and launch a replacement instance. To prevent this, you can suspend the scaling processes for the group while you're resizing your instance.

Incorrect options:

The new instance retains its public, private IPv4 addresses, any Elastic IP addresses, and any IPv6 addresses that were associated with the old instance - If your instance has a public IPv4 address, AWS releases the address and gives it a new public IPv4 address. The instance retains its private IPv4 addresses, any Elastic IP addresses, and any IPv6 addresses.

There is no downtime on the instance if you choose an instance of a compatible type since AWS starts the new instance and shifts the applications from current instance - AWS suggests that you plan for downtime while your instance is stopped. Stopping and resizing an instance may take a few minutes, and restarting your instance may take a variable amount of time depending on your application's startup scripts.

Resizing of an instance is possible if the root device is either EBS volume or an instance store volume. However, instance store volumes taking longer to start on the new instance, since cache data is lost on these instances - As discussed above, resizing of an instance is possible only if the root device for the instance is an EBS volume.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-resize.html

Question 47

A large IT company manages several projects on AWS Cloud and has decided to use AWS X-Ray to trace application workflows. The company uses a plethora of AWS services like API Gateway, Amazon EC2 instances, Amazon S3 storage service, Elastic Load Balancers and AWS Lambda functions.

Which of the following should the company keep in mind while using AWS X-Ray for the AWS services they use?
1

Application Load balancers do not send data to X-Ray
2

AWS X-Ray does not integrate with Amazon S3 and you need to use CloudTrail for tracking requests on S3
3

AWS X-Ray cannot be used to trace your AWS Lambda functions since they are not integrated
4

You cannot use X-Ray to trace or analyze user requests to your Amazon API Gateway APIs
Correct Answer
1

Application Load balancers do not send data to X-Ray
Explanation

Correct option:

Application Load balancers do not send data to X-Ray - Elastic Load Balancing application load balancers add a trace ID to incoming HTTP requests in a header named X-Amzn-Trace-Id. Load balancers do not send data to X-Ray and do not appear as a node on your service map.

Incorrect options:

AWS X-Ray does not integrate with Amazon S3 and you need to use CloudTrail for tracking requests on S3 - AWS X-Ray integrates with Amazon S3 to trace upstream requests to update your application's S3 buckets.

AWS X-Ray cannot be used to trace your AWS Lambda functions since they are not integrated - You can use AWS X-Ray to trace your AWS Lambda functions. Lambda runs the X-Ray daemon and records a segment with details about the function invocation and execution.

You cannot use X-Ray to trace or analyze user requests to your Amazon API Gateway APIs - You can use X-Ray to trace and analyze user requests as they travel through your Amazon API Gateway APIs to the underlying services. API Gateway supports X-Ray tracing for all API Gateway endpoint types: Regional, edge-optimized, and private. You can use X-Ray with Amazon API Gateway in all AWS Regions where X-Ray is available.

Reference:

https://docs.aws.amazon.com/xray/latest/devguide/xray-services-elb.html

Question 48

A systems administrator has configured Amazon EC2 instances in an Auto Scaling Group (ASG) for two separate development teams. However, only one configuration has CloudWatch agent installed on the instances, whereas the other one does not have it. The administrator has not manually installed the agents on either group of instances.

Which of the following would you identify as a root-cause behind this issue?
1

CloudWatch agent can be configured to be loaded on the EC2 instances while configuring the ASG. The developer could have unintentionally checked this flag on one of the ASGs he created
2

The architecture of the InstanceType mentioned in your launch configuration does not match the image architecture. So, the ASG was created with errors, resulting in skipping CloudWatch agent. A thorough check is needed for such ASGs, more services could have been skipped
3

If your AMI contains a CloudWatch agent, it’s automatically installed on EC2 instances when you create an EC2 Auto Scaling group. The developer needs to choose the AMI that has CloudWatch agent pre-configured on it
4

The instance architecture might not have been compatible with the AMI chosen. The incompatibility results in various errors, one of which is, some of the AWS services will not be installed as expected
Correct Answer
3

If your AMI contains a CloudWatch agent, it’s automatically installed on EC2 instances when you create an EC2 Auto Scaling group. The developer needs to choose the AMI that has CloudWatch agent pre-configured on it
Explanation

Correct option:

If your AMI contains a CloudWatch agent, it’s automatically installed on EC2 instances when you create an EC2 Auto Scaling group. The developer needs to choose the AMI that has CloudWatch agent pre-configured on it

If your AMI contains a CloudWatch agent, it’s automatically installed on EC2 instances when you create an EC2 Auto Scaling group. With the stock Amazon Linux AMI, you need to install it (AWS recommends to install via yum).

Incorrect options:

CloudWatch agent can be configured to be loaded on the EC2 instances while configuring the ASG. The developer could have unintentionally checked this flag on one of the ASGs he created - This is incorrect and added only as a distractor.

The architecture of the InstanceType mentioned in your launch configuration does not match the image architecture. So, the ASG was created with errors, resulting in skipping CloudWatch agent. A thorough check is needed for such ASGs, more services could have been skipped - This is incorrect. Either the ASG is created successfully or fails completely. Partial installation of services will not take place.

The instance architecture might not have been compatible with the AMI chosen. The incompatibility results in various errors, one of which is, some of the AWS services will not be installed as expected - If there are compatibility issues, the ASG will not be able to spin up instances, and throws an error that explains the compatibility error.

Reference:

https://aws.amazon.com/ec2/autoscaling/faqs/

Question 49

An automobile company manages its AWS resource creation and maintenance process through AWS CloudFormation. The company has successfully used CloudFormation so far, and wishes to continue using the service. However, while moving to CloudFormation, the company only moved critical resources and left out the other resources to be managed manually. To leverage the ease of creation and maintenance that CloudFormation offers, the company wants to move rest of the resources to CloudFormation.

Which of the following options is the recommended way to configure this requirement?
1

Use Parameters section of CloudFormation template to input the required resources
2

You can bring an existing resource into AWS CloudFormation management using resource import
3

You can use Mappings part of CloudFormation template to input the needed resources
4

Drift detection is the mechanism by which you add resources to the stack of Cloudformation resources already created
Correct Answer
2

You can bring an existing resource into AWS CloudFormation management using resource import
Explanation

Correct option:

You can bring an existing resource into AWS CloudFormation management using resource import

If you created an AWS resource outside of AWS CloudFormation management, you can bring this existing resource into AWS CloudFormation management using resource import. You can manage your resources using AWS CloudFormation regardless of where they were created without having to delete and re-create them as part of a stack.

During an import operation, you create a change set that imports your existing resources into a stack or creates a new stack from your existing resources. You provide the following during import.

    A template that describes the entire stack, including both the original stack resources and the resources you're importing. Each resource to import must have a DeletionPolicy attribute.

    Identifiers for the resources to import. You provide two values to identify each target resource.

a) An identifier property. This is a resource property that can be used to identify each resource type. For example, an AWS::S3::Bucket resource can be identified using its BucketName.

b) An identifier value. This is the target resource's actual property value. For example, the actual value for the BucketName property might be MyS3Bucket.

Incorrect options:

Use Parameters section of CloudFormation template to input the required resources - Parameters are a way to provide inputs to your AWS CloudFormation template. They are useful when you want to reuse your templates. Some inputs can not be determined ahead of time. They aren't useful for importing resources into CloudFormation.

You can use Mappings part of CloudFormation template to input the needed resources - Mappings are fixed variables within your CloudFormation Template. They’re very handy to differentiate between different environments (dev vs prod), regions (AWS regions), AMI types, etc. They aren't useful for importing resources into CloudFormation.

Drift detection is the mechanism by which you add resources to the stack of Cloudformation resources already created - Performing a drift detection operation on a stack determines whether the stack has drifted from its expected template configuration, and returns detailed information about the drift status of each resource in the stack that supports drift detection. It is not useful for importing resources into CloudFormation.

Reference:

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html

Question 50

As a SysOps Administrator, you have been asked to fix the network performance issues for a fleet of Amazon EC2 instances of a company.

Which of the following use-cases represents the right fit for using enhanced networking?
1

To reach speeds up to 2,500 Gbps between EC2 instances
2

To support throughput near or exceeding 20K packets per second (PPS) on the VIF driver
3

To configure multi-attach for an EBS volume that can be attached to a maximum of 16 EC2 instances in a single Availability Zone
4

To configure Direct Connect to reach speeds up to 25 Gbps between EC2 instances
Correct Answer
2

To support throughput near or exceeding 20K packets per second (PPS) on the VIF driver
Explanation

Correct option:

To support throughput near or exceeding 20K packets per second (PPS) on the VIF driver - Enhanced networking uses single root I/O virtualization (SR-IOV) to provide high-performance networking capabilities on supported instance types. SR-IOV is a method of device virtualization that provides higher I/O performance and lower CPU utilization when compared to traditional virtualized network interfaces. Enhanced networking provides higher bandwidth, higher packet per second (PPS) performance, and consistently lower inter-instance latencies. There is no additional charge for using enhanced networking.

Consider using enhanced networking for the following scenarios:

    If your packets-per-second rate reaches its ceiling, consider moving to enhanced networking. If your rate reaches its ceiling, you've likely reached the upper thresholds of the virtual network interface driver.

    If your throughput is near or exceeding 20K packets per second (PPS) on the VIF driver, it's a best practice to use enhanced networking.

All current generation instance types support enhanced networking, except for T2 instances.

Incorrect options:

To reach speeds up to 2,500 Gbps between EC2 instances - If you need to reach speeds up to 25 Gbps between instances, launch instances in a cluster placement group along with ENA compatible instances. If you need to reach speeds up to 10 Gbps between instances, launch your instances into a cluster placement group with the enhanced networking instance type. This option has been added as a distractor, as it is not possible to support speeds up to 2,500 Gbps between EC2 instances.

To configure multi-attach for an EBS volume that can be attached to a maximum of 16 EC2 instances in a single Availability Zone - An EBS (io1 or io2) volume, when configured with the new Multi-Attach option, can be attached to a maximum of 16 EC2 instances in a single Availability Zone. Additionally, each Nitro-based EC2 instance can support the attachment of multiple Multi-Attach enabled EBS volumes. Multi-Attach capability makes it easier to achieve higher availability for applications that provide write-ordering to maintain storage consistency. You do not need to use enhanced networking to configure this option.

To configure Direct Connect to reach speeds up to 25 Gbps between EC2 instances - AWS Direct Connect is a networking service that provides an alternative to using the internet to connect your on-premises resources to AWS Cloud. In many circumstances, private network connections can reduce costs, increase bandwidth, and provide a more consistent network experience than internet-based connections. You cannot use enhanced networking to configure Direct Connect to reach speeds up to 25 Gbps between EC2 instances.

References:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/enhanced-networking.html

https://aws.amazon.com/premiumsupport/knowledge-center/enable-configure-enhanced-networking/

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html

Question 51

As SysOps Administrator, you have created two configuration files for CloudWatch Agent configuration. The first configuration file collects a set of metrics and logs from all servers and the second configuration file collects metrics from certain applications. You have given the same name to both the files but stored these files in different file paths.

What is the outcome when the CloudWatch Agent is started with the first configuration file and then the second configuration file is appended to it?
1

Second configuration file parameters are added to the Agent already running with the first configuration file parameters
2

Two different Agents are started with different configurations, collecting the metrics and logs listed in either of the configuration files
3

The append command overwrites the information from the first configuration file instead of appending to it
4

A CloudWatch Agent can have only one configuration file and all required parameters are defined in this file alone
Correct Answer
3

The append command overwrites the information from the first configuration file instead of appending to it
Explanation

Correct option:

The append command overwrites the information from the first configuration file instead of appending to it

You can set up the CloudWatch agent to use multiple configuration files. For example, you can use a common configuration file that collects a set of metrics and logs that you always want to collect from all servers in your infrastructure. You can then use additional configuration files that collect metrics from certain applications or in certain situations.

To set this up, first create the configuration files that you want to use. Any configuration files that will be used together on the same server must have different file names. You can store the configuration files on servers or in Parameter Store.

Start the CloudWatch agent using the fetch-config option and specify the first configuration file. To append the second configuration file to the running agent, use the same command but with the append-config option. All metrics and logs listed in either configuration file are collected.

Any configuration files appended to the configuration must have different file names from each other and from the initial configuration file. If you use append-config with a configuration file with the same file name as a configuration file that the agent is already using, the append command overwrites the information from the first configuration file instead of appending to it. This is true even if the two configuration files with the same file name are on different file paths.

Incorrect options:

Second configuration file parameters are added to the Agent already running with the first configuration file parameters

Two different Agents are started with different configurations, collecting the metrics and logs listed in either of the configuration files

A CloudWatch Agent can have only one configuration file and all required parameters are defined in this file alone

These three options contradict the explanation provided above, so these options are incorrect.

Reference:

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Agent-common-scenarios.html

Question 52

A SysOps administrator has deployed multiple applications on a fleet of Amazon EC2 instances.

What is the right way to configure scheduled events for these EC2 instances?
1

Use CloudWatch Alarm to configure scheduled events on Amazon EC2 instances
2

Use Amazon EventBridge to configure scheduled events on Amazon EC2 instances
3

Use CloudWatch Agent to configure scheduled events on Amazon EC2 instances
4

Scheduled events are managed by AWS, you cannot configure scheduled events for your instances
Correct Answer
4

Scheduled events are managed by AWS, you cannot configure scheduled events for your instances
Explanation

Correct option:

Scheduled events are managed by AWS, you cannot configure scheduled events for your instances - AWS can schedule events for your instances, such as a reboot, stop/start, or retirement. These events do not occur frequently. If one of your instances will be affected by a scheduled event, AWS sends an email to the email address that's associated with your AWS account before the scheduled event. The email provides details about the event, including the start and end date. Depending on the event, you might be able to take action to control the timing of the event. AWS also sends an AWS Health event, which you can monitor and manage using Amazon CloudWatch Events.

Scheduled events are managed by AWS; you cannot schedule events for your instances. You can view the events scheduled by AWS, customize scheduled event notifications to include or remove tags from the email notification, perform actions when an instance is scheduled to reboot, retire, or stop.

Incorrect options:

Use CloudWatch Alarm to configure scheduled events on Amazon EC2 instances - CloudWatch alarms can be used to watch a single metric over a time period you specify, and perform one or more actions based on the value of the metric relative to a given threshold over a number of time periods. The action is a notification sent to an Amazon Simple Notification Service (Amazon SNS) topic or Amazon EC2 Auto Scaling policy. CloudWatch Alarm cannot be used to configure scheduled events on Amazon EC2 instances.

Use Amazon EventBridge to configure scheduled events on Amazon EC2 instances - Amazon EventBridge helps automate your AWS services and respond automatically to system events. Events from AWS services are delivered to EventBridge in near real-time, and you can specify automated actions to take when an event matches a rule you write. EventBridge cannot be used to configure scheduled events on Amazon EC2 instances.

Use CloudWatch Agent to configure scheduled events on Amazon EC2 instances - CloudWatch Agent helps collect logs and system-level metrics from both hosts and guests on your EC2 instances and on-premises servers. CloudWatch Agent cannot be used to configure scheduled events on Amazon EC2 instances.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitoring-instances-status-check_sched.html

Question 53

A systems administrator is configuring Amazon EC2 status check alarm to publish a notification to an SNS topic when the instance fails either the instance check or system status check.

Which CloudWatch metric is the right choice for this configuration?
1

StatusCheckFailed
2

CombinedStatusCheckFailed
3

StatusCheckFailed_Instance
4

StatusCheckFailed_System
Correct Answer
1

StatusCheckFailed
Explanation

Correct option:

StatusCheckFailed - The AWS/EC2 namespace includes a few status check metrics. By default, status check metrics are available at a 1-minute frequency at no charge. For a newly-launched instance, status check metric data is only available after the instance has completed the initialization state (within a few minutes of the instance entering the running state).

StatusCheckFailed - Reports whether the instance has passed both the instance status check and the system status check in the last minute. This metric can be either 0 (passed) or 1 (failed). By default, this metric is available at a 1-minute frequency at no charge.

List of EC2 status check metrics: via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics

Incorrect options:

CombinedStatusCheckFailed - This is a made-up option, given only as a distractor.

`StatusCheckFailed_Instance - Reports whether the instance has passed the instance status check in the last minute. This metric can be either 0 (passed) or 1 (failed).

StatusCheckFailed_System - Reports whether the instance has passed the system status check in the last minute. This metric can be either 0 (passed) or 1 (failed).

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html#status-check-metrics

Question 54

As a SysOps Administrator, you have been asked to calculate the total network usage for all the EC2 instances of a company and determine which instance used the most bandwidth within a date range.

Which Amazon CloudWatch metric(s) will help you get the needed data?
1

DataTransfer-Out-Bytes
2

NetworkIn and NetworkOut
3

DiskReadBytes and DiskWriteBytes
4

NetworkTotalBytes
Correct Answer
2

NetworkIn and NetworkOut
Explanation

Correct option:

NetworkIn and NetworkOut - You can determine which instance is causing high network usage using the Amazon CloudWatch NetworkIn and NetworkOut metrics. You can aggregate the data points from these metrics to calculate the network usage for your instance.

NetworkIn - The number of bytes received by the instance on all network interfaces. This metric identifies the volume of incoming network traffic to a single instance.

The number reported is the number of bytes received during the period. If you are using basic (five-minute) monitoring and the statistic is Sum, you can divide this number by 300 to find Bytes/second. If you have detailed (one-minute) monitoring and the statistic is Sum, divide it by 60. Units of this metric are Bytes.

NetworkOut - The number of bytes sent out by the instance on all network interfaces. This metric identifies the volume of outgoing network traffic from a single instance.

The number reported is the number of bytes sent during the period. If you are using basic (five-minute) monitoring and the statistic is Sum, you can divide this number by 300 to find Bytes/second. If you have detailed (one-minute) monitoring and the statistic is Sum, divide it by 60. Units of this metric are Bytes.

Incorrect options:

DataTransfer-Out-Bytes - DataTransfer-Out-Bytes metric is used in AWS Cost Explorer reports and is not useful for the current scenario.

DiskReadBytes and DiskWriteBytes - DiskReadBytes is the bytes read from all instance store volumes available to the instance. This metric is used to determine the volume of the data the application reads from the hard disk of the instance. This can be used to determine the speed of the application.

DiskWriteBytes is the bytes written to all instance store volumes available to the instance. This metric is used to determine the volume of the data the application writes onto the hard disk of the instance. This can be used to determine the speed of the application.

NetworkTotalBytes - This is a made-up option, given only as a distractor.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html

Question 55

A team noticed that it has accidentally deleted the AMI of Amazon EC2 instances belonging to the test environment. The team had configured backups via EBS snapshots for these instances.

Which of the following options would you suggest to recover/rebuild the accidentally deleted AMI? (Select two)
Multi Select
1

AWS Support retains backups of AMIs. Write to the support team to get help for recovering the lost AMI
2

Create a new AMI from Amazon EBS snapshots that were created as backups
3

Create a new AMI from Amazon EC2 instances that were launched before the deletion of AMI
4

Recover the AMI from the current Amazon EC2 instances that were launched before the deletion of AMI
5

Recover the AMI from Amazon EBS snapshots that were created as backups before the deletion of AMI
Correct Answer
2

Create a new AMI from Amazon EBS snapshots that were created as backups
3

Create a new AMI from Amazon EC2 instances that were launched before the deletion of AMI
Explanation

Correct options:

Create a new AMI from Amazon EBS snapshots that were created as backups

Create a new AMI from Amazon EC2 instances that were launched before the deletion of AMI

It isn't possible to restore or recover a deleted or deregistered AMI. However, you can create a new, identical AMI using one of the following:

    Amazon Elastic Block Store (Amazon EBS) snapshots that were created as backups: When you delete or deregister an Amazon EBS-backed AMI, any snapshots created for the volume of the instance during the AMI creation process are retained. If you accidentally delete the AMI, you can launch an identical AMI using one of the retained snapshots.

    Amazon Elastic Compute Cloud (Amazon EC2) instances that were launched from the deleted AMI: If you deleted the AMI and the snapshots are also deleted, then you can recover the AMI from any existing EC2 instances launched using the deleted AMI. Unless you have selected the No reboot option on the instance, performing this step will reboot the instance.

Incorrect options:

AWS Support retains backups of AMIs. Write to the support team to get help for recovering the lost AMI - For security and privacy reasons, AWS Support doesn't have visibility or access to customer data. If you don't have backups of your deleted AMI, AWS Support can't recover it for you.

Recover the AMI from the current Amazon EC2 instances that were launched before the deletion of AMI

Recover the AMI from Amazon EBS snapshots that were created as backups before the deletion of AMI

As discussed above, it is not possible to restore or recover a deleted or deregistered AMI. The only option is to create a new, identical AMI as discussed above.

Reference:

https://aws.amazon.com/premiumsupport/knowledge-center/recover-ami-accidentally-deleted-ec2/

Question 56

A team needs to create an AMI from their Amazon EC2 instances for use in another environment.

What is the right way to create an application-consistent AMI from existing EC2 instances?
1

Create the AMI with No reboot option enabled
2

Create an EBS-backed AMI for application consistency
3

Create the AMI by disabling the No reboot option
4

Create the AMI with Delete on termination enabled
Correct Answer
3

Create the AMI by disabling the No reboot option
Explanation

Correct option:

Create the AMI by disabling the No reboot option - On the Create image page, No reboot flag is present. The default functionality is, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. When No reboot option is selected, the instance is not shut down while creating the AMI. This option is not selected by default.

If you select No reboot, the AMI will be crash-consistent (all the volumes are snapshotted at the same time), but not application-consistent (all the operating system buffers are not flushed to disk before the snapshots are created).

Incorrect options:

Create the AMI with No reboot option enabled - If the No reboot flag is selected, the instance is not shutdown while creating an AMI. This implies, the Operating System buffers are not flushed before creating an AMI, so data integrity could be an issue with AMIs created in this way. Such AMIs are crash-consistent but not application-consistent.

Create an EBS-backed AMI for application consistency - When you create a new instance from an EBS-backed AMI, you are using persistent storage. No reboot flag should still be unchecked to ensure that everything on the instance is stopped and in a consistent state during the creation process.

Create the AMI with Delete on termination enabled - If you select Delete on termination, when you terminate the instance created from this AMI, the EBS volume is deleted. If you clear Delete on termination, when you terminate the instance, the EBS volume is not deleted. This option has been added as a distractor.

Reference:

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami-ebs.html

Question 57

An organization has multiple AWS accounts to manage different lines of business. A user from the Finance account has to access reports stored in Amazon S3 buckets of two other AWS accounts (belonging to the HR and Audit departments) and copy these reports back to the S3 bucket in the Finance account. The user has requested the necessary permissions from the systems administrator to perform this task.

As a SysOps Administrator, how will you configure a solution for this requirement?
1

Create resource-based policies in the HR, Audit accounts that will allow the requester from the Finance account to access the respective S3 buckets
2

Create resource-level permissions in the HR, Audit accounts to allow access to respective S3 buckets for the user in the Finance account
3

Create identity-based IAM policy in the Finance account that allows the user to make a request to the S3 buckets in the HR and Audit accounts. Also, create resource-based IAM policies in the HR, Audit accounts that will allow the requester from the Finance account to access the respective S3 buckets
4

Create IAM roles in the HR, Audit accounts, which can be assumed by the user from the Finance account when the user needs to access the S3 buckets of the accounts
Correct Answer
3

Create identity-based IAM policy in the Finance account that allows the user to make a request to the S3 buckets in the HR and Audit accounts. Also, create resource-based IAM policies in the HR, Audit accounts that will allow the requester from the Finance account to access the respective S3 buckets
Explanation

Correct option:

Create identity-based IAM policy in the Finance account that allows the user to make a request to the S3 buckets in the HR and Audit accounts. Also, create resource-based IAM policies in the HR, Audit accounts that will allow the requester from the Finance account to access the respective S3 buckets

Identity-based policies are attached to an IAM user, group, or role. These policies let you specify what that identity can do (its permissions).

Resource-based policies are attached to a resource. For example, you can attach resource-based policies to Amazon S3 buckets, Amazon SQS queues, and AWS Key Management Service encryption keys.

Identity-based policies and resource-based policies are both permissions policies and are evaluated together. For a request to which only permissions policies apply, AWS first checks all policies for a Deny. If one exists, then the request is denied. Then AWS checks for each Allow. If at least one policy statement allows the action in the request, the request is allowed. It doesn't matter whether the Allow is in the identity-based policy or the resource-based policy.

For requests made from one account to another, the requester in Account A must have an identity-based policy that allows them to make a request to the resource in Account B. Also, the resource-based policy in Account B must allow the requester in Account A to access the resource. There must be policies in both accounts that allow the operation, otherwise, the request fails.

Comparing IAM policies: via - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_identity-vs-resource.html

Incorrect options:

Create resource-based policies in the HR, Audit accounts that will allow the requester from the Finance account to access the respective S3 buckets - Creating resource-based policy alone will be sufficient when the request is made within a single AWS account.

Create resource-level permissions in the HR, Audit accounts to allow access to respective S3 buckets for the user in the Finance account - Resource-based policies differ from resource-level permissions. You can attach resource-based policies directly to a resource, as described in this topic. Resource-level permissions refer to the ability to use ARNs to specify individual resources in a policy. Resource-based policies are supported only by some AWS services.

Create IAM roles in the HR, Audit accounts, which can be assumed by the user from the Finance account when the user needs to access the S3 buckets of the accounts - Cross-account access with a resource-based policy has some advantages over cross-account access with a role. With a resource that is accessed through a resource-based policy, the principal still works in the trusted account and does not have to give up his or her permissions to receive the role permissions. In other words, the principal continues to have access to resources in the trusted account at the same time as he or she has access to the resource in the trusting account. This is useful for tasks such as copying information to or from the shared resource in the other account.

We chose resource-based policy, so the user from the Finance account will continue to have access to resources in his own account while also getting permissions on resources from other accounts.

References:

https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_identity-vs-resource.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_compare-resource-policies.html

Question 58

A retail company wants to get out of the business of owning and maintaining its own IT infrastructure. As part of this digital transformation, the company wants to archive about 5PB of data in its on-premises data center to durable long term storage.

As a SysOps Administrator, what is your recommendation to migrate this data in the MOST cost-optimal way?
1

Transfer the on-premises data into multiple Snowball Edge Storage Optimized devices. Copy the Snowball Edge data into AWS Glacier
2

Setup AWS direct connect between the on-premises data center and AWS Cloud. Use this connection to transfer the data into AWS Glacier
3

Setup Site-to-Site VPN connection between the on-premises data center and AWS Cloud. Use this connection to transfer the data into AWS Glacier
4

Transfer the on-premises data into multiple Snowball Edge Storage Optimized devices. Copy the Snowball Edge data into Amazon S3 and create a lifecycle policy to transition the data into AWS Glacier
Correct Answer
4

Transfer the on-premises data into multiple Snowball Edge Storage Optimized devices. Copy the Snowball Edge data into Amazon S3 and create a lifecycle policy to transition the data into AWS Glacier
Explanation

Correct option:

Transfer the on-premises data into multiple Snowball Edge Storage Optimized devices. Copy the Snowball Edge data into Amazon S3 and create a lifecycle policy to transition the data into AWS Glacier

Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 TB of usable HDD storage, 40 vCPUs, 1 TB of SATA SSD storage, and up to 40 Gb network connectivity to address large scale data transfer and pre-processing use cases. The data stored on the Snowball Edge device can be copied into the S3 bucket and later transitioned into AWS Glacier via a lifecycle policy. You can't directly copy data from Snowball Edge devices into AWS Glacier.

Incorrect options:

Transfer the on-premises data into multiple Snowball Edge Storage Optimized devices. Copy the Snowball Edge data into AWS Glacier - As mentioned earlier, you can't directly copy data from Snowball Edge devices into AWS Glacier. Hence, this option is incorrect.

Setup AWS direct connect between the on-premises data center and AWS Cloud. Use this connection to transfer the data into AWS Glacier - AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations. Using industry-standard 802.1q VLANs, this dedicated connection can be partitioned into multiple virtual interfaces. Direct Connect involves significant monetary investment and takes more than a month to set up, therefore it's not the correct fit for this use-case where just a one-time data transfer has to be done.

Setup Site-to-Site VPN connection between the on-premises data center and AWS Cloud. Use this connection to transfer the data into AWS Glacier - AWS Site-to-Site VPN enables you to securely connect your on-premises network or branch office site to your Amazon Virtual Private Cloud (Amazon VPC). VPN Connections are a good solution if you have an immediate need, and have low to modest bandwidth requirements. Because of the high data volume for the given use-case, Site-to-Site VPN is not the correct choice.

Reference:

https://aws.amazon.com/snowball/

Question 59

The Chief Technology Officer (CTO) of a healthcare company realized that he does not have access to an Amazon S3 bucket present in the company's own AWS account. The CTO is the root user for the AWS account and has created other AWS users using the root user account.

What is the reason for this behavior and how can you fix this?
1

If an IAM user, with full access to IAM and Amazon S3, assigns a bucket policy to an Amazon S3 bucket and doesn't specify the AWS account root user as a principal, the root user is denied access to that bucket
2

Root user always has access to all the resources of the account. The Amazon S3 bucket could be from another AWS account and the S3 bucket has been shared with the root user and hence appears in his list of S3 buckets
3

An Amazon S3 bucket policy that specifies a wildcard (*) in the principal element, sometimes is declared void by AWS to avoid the risk of complete public exposure. Such S3 buckets policies are in invalid status and have random behavior
4

Root user has access to all the resources in his AWS account. Contact AWS support to resolve the access issue
Correct Answer
1

If an IAM user, with full access to IAM and Amazon S3, assigns a bucket policy to an Amazon S3 bucket and doesn't specify the AWS account root user as a principal, the root user is denied access to that bucket
Explanation

Correct option:

If an IAM user, with full access to IAM and Amazon S3, assigns a bucket policy to an Amazon S3 bucket and doesn't specify the AWS account root user as a principal, the root user is denied access to that bucket

Sometimes, you might have an IAM user with full access to IAM and Amazon S3. If the IAM user assigns a bucket policy to an Amazon S3 bucket and doesn't specify the AWS account root user as a principal, the root user is denied access to that bucket. However, as the root user, you can still access the bucket. To do that, modify the bucket policy to allow root user access from the Amazon S3 console or the AWS CLI. Use the following principal, replacing 123456789012 with the ID of the AWS account.

"Principal": { "AWS": "arn:aws:iam::123456789012:root" }

Incorrect options:

Root user always has access to all the resources of the account. The Amazon S3 bucket could be from another AWS account and the S3 bucket has been shared with the root user and hence appears in his list of S3 buckets

An Amazon S3 bucket policy that specifies a wildcard (*) in the principal element, sometimes is declared void by AWS to avoid the risk of complete public exposure. Such S3 buckets policies are in invalid status and have random behavior

Root user has access to all the resources in his AWS account. Contact AWS support to resolve the access issue

These three options contradict the explanation above, so these options are incorrect.

Reference:

https://docs.aws.amazon.com/IAM/latest/UserGuide/troubleshoot_iam-s3.html

Question 60

The development team at a retail company manages the deployment and scaling of their web application through AWS Elastic Beanstalk. After configuring the Elastic Beanstalk environment, the team has realized that Beanstalk is not handling the scaling activities the way they expected. This has impacted the application's ability to respond to the variations in traffic.

How should the environment be configured to get the best of Beanstalk's auto-scaling capabilities?
1

The IAM Role attached to the Auto Scaling group might not have enough permissions to scale instances on-demand
2

The Auto Scaling group in your Elastic Beanstalk environment uses the number of logged-in users, as the criteria to trigger auto-scaling action. These alarms must be configured based on the parameters appropriate for your application
3

By default, Auto Scaling group created from Beanstalk uses Elastic Load Balancing health checks. Configure the Beanstalk to use Amazon EC2 status checks
4

The Auto Scaling group in your Elastic Beanstalk environment uses two default Amazon CloudWatch alarms to trigger scaling operations. These alarms must be configured based on the parameters appropriate for your application
Correct Answer
4

The Auto Scaling group in your Elastic Beanstalk environment uses two default Amazon CloudWatch alarms to trigger scaling operations. These alarms must be configured based on the parameters appropriate for your application
Explanation

Correct option:

The Auto Scaling group in your Elastic Beanstalk environment uses two default Amazon CloudWatch alarms to trigger scaling operations. These alarms must be configured based on the parameters appropriate for your application

The Auto Scaling group in your Elastic Beanstalk environment uses two Amazon CloudWatch alarms to trigger scaling operations. Default Auto Scaling triggers are configured to scale when the average outbound network traffic (NetworkOut) from each instance is higher than 6 MB or lower than 2 MB over a period of five minutes.

For more efficient Amazon EC2 Auto Scaling, configure triggers that are appropriate for your application, instance type, and service requirements. You can scale based on several statistics including latency, disk I/O, CPU utilization, and request count.

Incorrect options:

The IAM Role attached to the Auto Scaling group might not have enough permissions to scale instances on-demand - The Auto Scaling group will not be able to spin up Amazon EC2 instances if the IAM Role associated with Beanstalk does not have enough permissions. Since the current use-case talks about scaling not happening at the expected rate, this should not be the issue.

By default, Auto Scaling group created from Beanstalk uses Elastic Load Balancing health checks. Configure the Beanstalk to use Amazon EC2 status checks - This statement is incorrect. By default, Auto Scaling group created from Beanstalk uses Amazon EC2 status checks.

The Auto Scaling group in your Elastic Beanstalk environment uses the number of logged-in users, as the criteria to trigger auto-scaling action. These alarms must be configured based on the parameters appropriate for your application - The default scaling criteria has already been discussed above (and it is not the number of logged-in users).

Reference:

https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.alarms.html

Question 61

A company initially used a manual process to create and manage different IAM roles needed for the organization. As the company expanded and lines of business grew, different AWS accounts were created to manage the AWS resources as well as the users. The manual process has resulted in errors with IAM roles getting created with insufficient permissions. The company is looking at automating the process of creating and managing the necessary IAM roles for multiple AWS accounts. The company already uses AWS Organizations to manage multiple AWS accounts.

As a SysOps Administrator, can you suggest an effective way to automate this process?
1

Create CloudFormation templates and reuse them to create necessary IAM roles in each of the AWS accounts
2

Use CloudFormation StackSets with AWS Organizations to deploy and manage IAM roles to multiple AWS accounts simultaneously
3

Use AWS Directory Service with AWS Organizations to automatically associate necessary IAM roles with the Microsoft Active Directory users
4

Use AWS Resource Access Manager that integrates with AWS Organizations to deploy and manage shared resources across AWS accounts
Correct Answer
2

Use CloudFormation StackSets with AWS Organizations to deploy and manage IAM roles to multiple AWS accounts simultaneously
Explanation

Correct option:

Use CloudFormation StackSets with AWS Organizations to deploy and manage IAM roles to multiple AWS accounts simultaneously

CloudFormation StackSets allow you to roll out CloudFormation stacks over multiple AWS accounts and in multiple Regions with just a couple of clicks. When AWS launched StackSets, grouping accounts was primarily for billing purposes. Since the launch of AWS Organizations, you can centrally manage multiple AWS accounts across diverse business needs including billing, access control, compliance, security and resource sharing.

You can now centrally orchestrate any AWS CloudFormation enabled service across multiple AWS accounts and regions. For example, you can deploy your centralized AWS Identity and Access Management (IAM) roles, provision Amazon Elastic Compute Cloud (EC2) instances or AWS Lambda functions across AWS Regions and accounts in your organization. CloudFormation StackSets simplify the configuration of cross-accounts permissions and allow for automatic creation and deletion of resources when accounts are joining or are removed from your Organization.

You can get started by enabling data sharing between CloudFormation and Organizations from the StackSets console. Once done, you will be able to use StackSets in the Organizations master account to deploy stacks to all accounts in your organization or in specific organizational units (OUs). A new service managed permission model is available with these StackSets. Choosing Service managed permissions allows StackSets to automatically configure the necessary IAM permissions required to deploy your stack to the accounts in your organization.

How to use AWS CloudFormation StackSets for Multiple Accounts in an AWS Organization: via - https://aws.amazon.com/blogs/aws/new-use-aws-cloudformation-stacksets-for-multiple-accounts-in-an-aws-organization/

Incorrect options:

Create CloudFormation templates and reuse them to create necessary IAM roles in each of the AWS accounts - CloudFormation templates can ease the current manual process that the company is using. However, it's not a completely automated process that the company needs.

Use AWS Directory Service with AWS Organizations to automatically associate necessary IAM roles with the Microsoft Active Directory users - AWS Directory Service for Microsoft Active Directory, or AWS Managed Microsoft AD, lets you run Microsoft Active Directory (AD) as a managed service. AWS Directory Service makes it easy to set up and run directories in the AWS Cloud or connect your AWS resources with an existing on-premises Microsoft Active Directory. It is not meant for the automatic creation of IAM roles across AWS accounts.

Use AWS Resource Access Manager that integrates with AWS Organizations to deploy and manage shared resources across AWS accounts - AWS Resource Access Manager (AWS RAM) enables you to share specified AWS resources that you own with other AWS accounts. It's a centralized service that provides a consistent experience for sharing different types of AWS resources across multiple accounts. This service enables you to share resources across AWS accounts. It's not meant for re-creating the same resource definitions in different AWS accounts.

References:

https://aws.amazon.com/blogs/aws/new-use-aws-cloudformation-stacksets-for-multiple-accounts-in-an-aws-organization/

https://docs.aws.amazon.com/organizations/latest/userguide/services-that-can-integrate-ram.html

Question 62

An e-commerce company uses AWS Elastic Beanstalk to create test environments comprising of an Amazon EC2 instance and an RDS instance whenever a new product or line-of-service is launched. The company is currently testing one such environment but wants to decouple the database from the environment to run some analysis and reports later in another environment. Since testing is in progress for a high-stakes product, the company wants to avoid downtime and database sync issues.

As a SysOps Administrator, which solution will you recommend to the company?
1

Since it is a test environment, take a snapshot of the database and terminate the current environment. Create a new one without attaching an RDS instance directly to it (from the snapshot)
2

Use an Elastic Beanstalk Immutable deployment to make the entire architecture completely reliable. You can terminate the first environment whenever you are confident of the second environment working correctly
3

Use an Elastic Beanstalk blue (environment A)/green (environment B) deployment to decouple the RDS DB instance from environment A. Create a new Elastic Beanstalk environment (environment B) with the necessary information to connect to the decoupled RDS DB instance
4

Decoupling an RDS instance that is part of a running Elastic Beanstalk environment is not currently supported by AWS. You will need to terminate the current environment after taking the snapshot of the database and create a new one with RDS configured outside the environment
Correct Answer
3

Use an Elastic Beanstalk blue (environment A)/green (environment B) deployment to decouple the RDS DB instance from environment A. Create a new Elastic Beanstalk environment (environment B) with the necessary information to connect to the decoupled RDS DB instance
Explanation

Correct option:

Use an Elastic Beanstalk blue (environment A)/green (environment B) deployment to decouple the RDS DB instance from environment A. Create a new Elastic Beanstalk environment (environment B) with the necessary information to connect to the decouple RDS DB instance - Attaching an RDS DB instance to an Elastic Beanstalk environment is ideal for development and testing environments. However, it's not recommended for production environments because the lifecycle of the database instance is tied to the lifecycle of your application environment. If you terminate the environment, then you lose your data because the RDS DB instance is deleted by the environment.

Since the current use case mentions not having downtime on the database, we can follow these steps for resolution: 1. Use an Elastic Beanstalk blue (environment A)/green (environment B) deployment to decouple an RDS DB instance from environment A. Create an RDS DB snapshot and enable Deletion protection on the DB instance to Safeguard your RDS DB instance from deletion. 2. Create a new Elastic Beanstalk environment (environment B) with the necessary information to connect to the RDS DB instance. Your new Elastic Beanstalk environment (environment B) must not include an RDS DB instance in the same Elastic Beanstalk application.

Step-by-step instructions to configure the above solution: via - https://aws.amazon.com/premiumsupport/knowledge-center/decouple-rds-from-beanstalk/

Incorrect options:

Since it is a test environment, take a snapshot of the database and terminate the current environment. Create a new one without attaching an RDS instance directly to it (from the snapshot) - It is mentioned in the problem statement that the company is looking at a solution with no downtime. Hence, this is an incorrect option.

Use an Elastic Beanstalk Immutable deployment to make the entire architecture completely reliable. You can terminate the first environment whenever you are confident of the second environment working correctly - Immutable deployments perform an immutable update to launch a full set of new instances running the new version of the application in a separate Auto Scaling group, alongside the instances running the old version. Immutable deployments can prevent issues caused by partially completed rolling deployments. If the new instances don't pass health checks, Elastic Beanstalk terminates them, leaving the original instances untouched. This solution is an over-kill for the test environment, even if the company is looking at a no-downtime option.

Decoupling an RDS instance that is part of a running Elastic Beanstalk environment is not currently supported by AWS. You will need to terminate the current environment after taking the snapshot of the database and create a new one with RDS configured outside the environment - This is a made-up option and given only as a distractor.

References:

https://aws.amazon.com/premiumsupport/knowledge-center/decouple-rds-from-beanstalk/

https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.rolling-version-deploy.html

Question 63

An IT company runs its server infrastructure on Amazon EC2 instances configured in an Auto Scaling Group (ASG) fronted by an Elastic Load Balancer (ELB). For ease of deployment and flexibility in scaling, this AWS architecture is maintained via an Elastic Beanstalk environment. The Technology Lead of a project has requested to automate the replacement of unhealthy Amazon EC2 instances in the Elastic Beanstalk environment.

How will you configure a solution for this requirement?
1

To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from EC2 to ELB by using a configuration file of your Beanstalk environment
2

Modify the Auto Scaling Group from Amazon EC2 console directly to change the health check type to ELB
3

To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from ELB to EC2 by using a configuration file of your Beanstalk environment
4

Modify the Auto Scaling Group from Amazon EC2 console directly to change the health check type to EC2
Correct Answer
1

To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from EC2 to ELB by using a configuration file of your Beanstalk environment
Explanation

Correct option:

To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from EC2 to ELB by using a configuration file of your Beanstalk environment

By default, the health check configuration of your Auto Scaling group is set as an EC2 type that performs a status check of EC2 instances. To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from EC2 to ELB by using a configuration file.

The following are some important points to remember:

    Status checks cover only an EC2 instance's health, and not the health of your application, server, or any Docker containers running on the instance.

    If your application crashes, the load balancer removes the unhealthy instances from its target. However, your Auto Scaling group doesn't automatically replace the unhealthy instances marked by the load balancer.

    By changing the health check type of your Auto Scaling group from EC2 to ELB, you enable the Auto Scaling group to automatically replace the unhealthy instances when the health check fails.

Complete list of steps to configure the above: via - https://aws.amazon.com/premiumsupport/knowledge-center/elastic-beanstalk-instance-automation/

Incorrect options:

To automate the replacement of unhealthy EC2 instances, you must change the health check type of your instance's Auto Scaling group from ELB to EC2 by using a configuration file of your Beanstalk environment - As mentioned earlier, the health check type of your instance's Auto Scaling group should be changed from EC2 to ELB.

Modify the Auto Scaling Group from Amazon EC2 console directly to change the health check type to ELB

Modify the Auto Scaling Group from Amazon EC2 console directly to change the health check type to EC2

You should configure your Amazon EC2 instances in an Elastic Beanstalk environment by using Elastic Beanstalk configuration files (.ebextensions). Configuration changes made to your Elastic Beanstalk environment won't persist if you use the following configuration methods:

    Configuring an Elastic Beanstalk resource directly from the console of a specific AWS service.

    Installing a package, creating a file, or running a command directly from your Amazon EC2 instance.

Both these options contradict the above explanation and therefore these two options are incorrect.

Reference:

https://aws.amazon.com/premiumsupport/knowledge-center/elastic-beanstalk-configuration-files/

Question 64

An e-commerce company runs its web application on Amazon EC2 instances backed by Amazon Elastic Block Store (Amazon EBS) volumes. An Amazon S3 bucket is used for storing sharable data. A developer has attached an Amazon EBS to an Amazon EC2 instance, but it’s still in the "attaching" state after 10-15 minutes.

As a SysOps Administrator, what solution will you suggest to fix this issue with the EBS volume?
1

Check that the device name you specified when you attempted to attach the EBS volume isn't already in use. Attempt to attach the volume to the instance, again, but use a different device name
2

The EBS volume could be encrypted and the custom KMS key used to encrypt the snapshot is missing. The custom KMS key needs to be added to the volume configuration
3

Each EBS volume receives an initial I/O credit balance, an error in accumulating the credit balance can stop the volume from attaching properly to the instance. Restart the instance to fix the error
4

The attaching status indicates that the underlying hardware related to your EBS volume has failed. This issue cannot be fixed. Raise a service request on AWS and request for a new volume. You are not charged for volumes that are in error state
Correct Answer
1

Check that the device name you specified when you attempted to attach the EBS volume isn't already in use. Attempt to attach the volume to the instance, again, but use a different device name
Explanation

Correct option:

Check that the device name you specified when you attempted to attach the EBS volume isn't already in use. Attempt to attach the volume to the instance, again, but use a different device name

Check that the device name you specified when you attempted to attach the EBS volume isn't already in use. If the specified device name is already being used by the block device driver of the EC2 instance, the operation fails.

When attaching an EBS volume to an Amazon EC2 instance, you can specify a device name for the volume (by default, one is filled in for you). The block device driver of the EC2 instance mounts the volume and assigns a name. The volume name can be different from the name that you assign.

If you specify a device name that's not in use by Amazon EC2, but is used by the block device driver within the EC2 instance, the attachment of the Amazon EBS volume fails. Instead, the EBS volume is stuck in the attaching state. This is usually due to one of the following reasons:

    The block device driver is remapping the specified device name: On an HVM EC2 instance, /dev/sda1 remaps to /dev/xvda. If you attempt to attach a secondary Amazon EBS volume to /dev/xvda, the secondary EBS volume can't successfully attach to the instance. This can cause the EBS volume to be stuck in the attaching state.

    The block device driver didn't release the device name: If a user has initiated a forced detach of an Amazon EBS volume, the block device driver of the Amazon EC2 instance might not immediately release the device name for reuse. Attempting to use that device name when attaching a volume causes the volume to be stuck in the attaching state. You must either choose a different device name or reboot the instance.

You can resolve most issues with volumes stuck in the attaching state by following these steps: Force detach the volume and attempt to attach the volume to the instance, again, but use a different device name. The instance must be in running state for this to work.

If the above does not solve the problem, you can reboot the instance or stop and start the instance to migrate it to new underlying hardware. Keep in mind that instance store data is lost when you stop and start an instance.

Incorrect options:

The EBS volume could be encrypted and the custom KMS key used to encrypt the snapshot is missing. The custom KMS key needs to be added to the volume configuration - A missing KMS key will not lead to attaching state of the volume.

Each EBS volume receives an initial I/O credit balance, an error in accumulating the credit balance can stop the volume from attaching properly to the instance. Restart the instance to fix the error - This is a made-up option and has been added as a distractor.

The attaching status indicates that the underlying hardware related to your EBS volume has failed. This issue cannot be fixed. Raise a service request on AWS and request for a new volume. You are not charged for volumes that are in error state - When the underlying hardware related to your EBS volume has failed, the EBS volume will have a status of error. The data associated with the volume is unrecoverable and Amazon EBS processes the volume as lost. AWS doesn't bill for volumes with a status of error.

References:

https://aws.amazon.com/premiumsupport/knowledge-center/ebs-stuck-attaching/

https://docs.amazonaws.cn/en_us/AWSEC2/latest/WindowsGuide/ebs-volume-types.html

Question 65

A hospitality company runs their applications on its on-premises infrastructure but stores the critical customer data on AWS Cloud using AWS Storage Gateway. At a recent audit, the company has been asked if the customer data is secure while in-transit and at rest in the Cloud.

What is the correct answer to the auditor's question? And what should the company change to meet the security requirements?
1

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. File and Volume Gateway data stored on Amazon S3 is encrypted. Tape Gateway data cannot be encrypted at-rest
2

AWS Storage Gateway uses IPsec to encrypt data that is transferred between your gateway appliance and AWS storage. File and Volume Gateway data stored on Amazon S3 is encrypted. Tape Gateway data cannot be encrypted at-rest
3

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. By default, Storage Gateway uses Amazon S3-Managed Encryption Keys to server-side encrypt all data it stores in Amazon S3
4

AWS Storage Gateway uses IPsec to encrypt data that is transferred between your gateway appliance and AWS storage. All three Gateway types store data in encrypted form at-rest
Correct Answer
3

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. By default, Storage Gateway uses Amazon S3-Managed Encryption Keys to server-side encrypt all data it stores in Amazon S3
Explanation

Correct option:

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. By default, Storage Gateway uses Amazon S3-Managed Encryption Keys to server-side encrypt all data it stores in Amazon S3

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. By default, Storage Gateway uses Amazon S3-Managed Encryption Keys (SSE-S3) to server-side encrypt all data it stores in Amazon S3. You have an option to use the Storage Gateway API to configure your gateway to encrypt data stored in the cloud using server-side encryption with AWS Key Management Service (SSE-KMS) customer master keys (CMKs).

File, Volume and Tape Gateway data is stored in Amazon S3 buckets by AWS Storage Gateway. Tape Gateway supports backing data to Amazon S3 Glacier apart from the standard storage.

Encrypting a file share: For a file share, you can configure your gateway to encrypt your objects with AWS KMS–managed keys by using SSE-KMS.

Encrypting a volume: For cached and stored volumes, you can configure your gateway to encrypt volume data stored in the cloud with AWS KMS–managed keys by using the Storage Gateway API.

Encrypting a tape: For a virtual tape, you can configure your gateway to encrypt tape data stored in the cloud with AWS KMS–managed keys by using the Storage Gateway API.

Incorrect options:

AWS Storage Gateway uses IPsec to encrypt data that is transferred between your gateway appliance and AWS storage. File and Volume Gateway data stored on Amazon S3 is encrypted. Tape Gateway data cannot be encrypted at-rest

AWS Storage Gateway uses IPsec to encrypt data that is transferred between your gateway appliance and AWS storage. All three Gateway types store data in encrypted form at-rest

There is no such thing as using IPSec for encrypting in-transit data between your gateway appliance and AWS storage. You need to use SSL/TLS for this. So both these options are incorrect.

AWS Storage Gateway uses SSL/TLS (Secure Socket Layers/Transport Layer Security) to encrypt data that is transferred between your gateway appliance and AWS storage. File and Volume Gateway data stored on Amazon S3 is encrypted. Tape Gateway data cannot be encrypted at-rest - For a virtual tape, you can configure your gateway to encrypt tape data stored in the cloud with AWS KMS–managed keys by using the Storage Gateway API. So this option is incorrect.

Reference:

https://docs.aws.amazon.com/storagegateway/latest/userguide/encryption.html


---
sectionid: 3Dumps
sectionclass: h2
parent-id: Questions
title: Official Practice Question Set
number: 2300
---

## Official Practice Question Set AWS Certified SysOps Administrator - Associate

### Q 1

* A company uses an AWS CloudFormation stack to create an Auto Scaling group of Amazon EC2 instances. The company needs to address a security vulnerability in the Amazon Machine Image (AMI) that the EC2 instances use. The company needs to update to the latest operating system to address the security concerns. The company's application runs on the EC2 instances and must stay online at all times. At least one EC2 instance must stay operational during the change operation.

A SysOps administrator is updating the AMI ID in the CloudFormation template.

How can the SysOps administrator apply the AMI update to meet these requirements?

    A. Use a direct update of the stack

    B. run a change set for the stack

    C. use the autoscalingrollingupdate policy

    D. use the autoscalingreplaing update policy

**Correct Answer: C**

### Q 2

* A company's customers report that they are receiving HTTP 404 errors on the company's website. The company's infrastructure includes several Amazon EC2 instances. The logs are sent from each instance to a consolidated log group in Amazon CloudWatch Logs. A SysOps administrator needs to create a notification to indicate when the HTTP 404 errors pass a certain threshold.

Which steps are required to meet this requirement? (Select TWO.)

    A - Configure a log stream with log file compression

Incorrect. Compression is not necessary to monitor the HTTP 404 errors.

For more information about log compression in CloudWatch Logs, see Collect metrics, logs, and traces with the CloudWatch agent.

    B Configure CloudWatch Logs Insights to generate metrics on HTTP 404 erros

Incorrect. With CloudWatch Logs Insights, you can search and analyze your log file data. CloudWatch Logs Insights does not generate CloudWatch metrics natively.

For more information about CloudWatch Logs Insights, see Analyzing log data with CloudWatch Logs Insights.

    C Create metric filters with a filter pattern that identifies the http 404 errors.

Correct. You can create a count of 404 errors and exclude other 4xx errors with a filter pattern on 404 errors.

For more information about CloudWatch Logs filters, see Creating metrics from log events using filters.

    D Create an Amazon CloudWatch alarm based on the count of HTTP 404 errors.

Correct. You can set an alarm to notify operators when the 404 filter metric exceeds a threshold.

For more information about CloudWatch alarms, see Using Amazon CloudWatch alarms.

    E Create an Amazon EventBridge event based on the CloudWatch Logs Insights threshold.

Incorrect. With CloudWatch Logs Insights, you can search and analyze your log file data. CloudWatch Logs Insights does not generate EventBridge events.

For more information about CloudWatch Logs Insights, see Analyzing log data with CloudWatch Logs Insights.

**Correct Answer: C & D**

### Q 3

* A SysOps administrator sets up Traffic Mirroring on an Amazon EC2 instance. The SysOps administrator examines the logs from the traffic mirror and discovers that a number of packets have been truncated.

What should the SysOps administrator do to resolve this problem?

A Trace the truncated packets before they enter the AWS network

B Increase the maximum transmission unit (MTU) size for the mirror source

C Increase the maximum transmission unit (MTU) size for the mirror target (<- this)

D Use a Nitro instance type for the EC2 instance that is being mirrored

**Correct Answer: C**

* Explanation 

A. Incorrect. Truncated packets are dropped when the packets enter the AWS network and are not captured by the mirror target.

For more information about truncated packets, see Traffic mirror target concepts.

B. Incorrect. The packets are truncated because the source sent a larger packet than the mirror target can read. The increase of MTU size for the mirror source would not fix this issue.

For more information about truncated packets, see Traffic mirror target concepts.

C. Correct. Traffic Mirroring provides the ability to create a copy of a packet flow to examine the contents of a packet. This feature is useful for threat monitoring, content inspection, and troubleshooting.

A packet is truncated to the MTU value when both of the following are true:

    The traffic mirror target is a standalone instance.
    The traffic packet size from the mirror source is greater than the MTU size for the traffic mirror target.

For more information about Traffic Mirroring, see What is Traffic Mirroring?

For more information about truncated packets, see Traffic mirror target concepts.

D. Incorrect. Traffic Mirroring is available on current generations of EC2 instances as well as on Nitro instances. The source instance is sending mirrored traffic according to the logs. Therefore, the source instance is compatible with Traffic Mirroring.

For more information about Traffic Mirroring compatible instance types, see Amazon VPC Traffic Mirroring is now supported on select non-Nitro instance types.

### Q 4

* A company created a new application that uses a Spot Fleet for a variety of instance families across multiple Availability Zones.

What should a SysOps administrator do to ensure that the Spot Fleet is configured for cost optimization?

    A Apply Spot pricing and Reserved Instances purchasing to the same instances

    B Ensure instance capacity by specifying the desired target capacity. Specify how much of that capacity must be On-Demand Instances

    C Use the lowestPrice allocation strategy in combination with the InstancePoolsToUseCount paramter in the Spot Fleet request

    D Launch instances uo to the Spot Fleet target capacity or the maximum acceptable payment ammount.

**Correct Answer: C**

* Explanation:

A - Incorrect. Instances can be launched either as Spot Instances or as Reserved Instances, but not as both.

For more information about Reserved Instances, see Reserved Instances.

B - Incorrect. The request for On-Demand capacity in a Spot Fleet request ensures that there is always instance capacity. However, the question asks for a solution that focuses on cost optimization and not instance capacity.

C - Correct. With this solution, a Spot Fleet automatically deploys the lowest price combination of instance types and Availability Zones based on the current Spot price across the number of Spot pools specified. You can use this combination to avoid the most expensive Spot Instances.

For more information about Spot Instance allocation strategies, see Spot Fleet configuration strategies.

D - Incorrect. This solution is the default behavior of a Spot Fleet. A Spot Fleet stops the launch of instances when it has reached the target capacity or the maximum amount a user will pay. This solution improves the likelihood of getting Spot Instances, but it does not optimize the cost.


### Q 5

* A SysOps administrator needs to deploy a duplicate AWS development environment into a new AWS Region. The environment will be periodically redeployed as part of the maintenance process. The SysOps administrator deploys the current working template into the new Region. The template's Amazon EC2 instances fail to deploy, and AWS CloudFormation automatically rolls back the deployment.

After reviewing the logs, the SysOps administrator discovers that the EC2 instances are not deploying because of an Amazon Machine Image (AMI) ID value that is not valid in the new Region. The SysOps administrator must correct the CloudFormation template so that the instances deploy correctly.

What should the SysOps administrator do to meet this requirement with the LEAST operational overhead?


    A Create a template that is specific to each Region
    
    B Create a Mappings section in the template to reference the correct AMI ID value for both Regions (<- this)
    
    C Remove the EC2 instances from the template. Manually deploy the EC2 instances.
    
    D Create a parameter field that requests the AMI ID value. Pass the AMI ID value to the resource section for EC2 deployment.

**Correct Answer: B**

* Explanation:

A - Incorrect. The creation and maintenance of a template that is specific to each Region would require additional work. Additionally, changes that are made to one template would not be reflected in infrastructure in other Regions.

B - Correct. The optional Mappings section matches a key to a corresponding set of named values. For example, if you set values based on a Region, you can create a mapping that uses the Region name as a key. This mapping contains the values you want to specify for each specific Region.

For more information about the Mappings section in CloudFormation, see Mappings.

C - Incorrect. This solution is not automated and would not minimize operational overhead. This solution is a manual process that the SysOps administrator would have to perform.

D - Incorrect. This solution would require additional work every time the template is launched. The SysOps administrator would have to look up the correct AMI ID and enter it into the parameter field before the template could deploy.

For more information about parameters in CloudFormation, see Parameters.

### Q 6

* A SysOps administrator needs to block malicious traffic that is reaching a company's web servers. The malicious traffic is distributed over many IP addresses. The malicious traffic consists of a significantly higher number of connections than the company typically receives from legitimate users. The SysOps administrator needs to protect the web servers by using a solution that maximizes operational efficiency.

Which solution meets these requirements?

    A Create a security group for the web servers. Add deny rules for malicious sources
    
    B Set the network ACL for the subnet that is assigned to the web servers. Add deny rules for the malicious sources.
    
    C Use Amazon CloudFront to cache all pages and remove the traffic from the web servers
    
    D Place the web servers behind AWS WAF. Establish the rate limit to create a deny list (<- this)

**Correct Answer: D**

* Explanation

A - Incorrect. Security groups allow specific IP address ranges. Security groups block any traffic that is not specifically allowed. It is not possible to deny specific IP address ranges with security groups.

For more information about security groups, see Control traffic to your AWS resources using security groups.

B - Incorrect. This solution would require extra operational effort to establish and maintain the deny rules.

For more information about network ACLs, see Control traffic to subnets using network ACLs.

C - Incorrect. It is not reasonable to expect all contents to be cacheable.

For more information about CloudFront, see What is Amazon CloudFront?.

D - Correct. AWS WAF is a web application firewall that helps protect web applications or APIs against common web exploits that can affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by offering you the ability to create security rules that block common attack patterns, such as SQL injection or cross-site scripting. You also can create rules that filter out specific traffic patterns that you define.

For more information about filtering IP addresses to protect your applications, see Working with IP match conditions.


### Q 7

* A photo sharing site delivers content worldwide from a library on Amazon S3 by using Amazon CloudFront. Some users try to access photos that do not exist. Other users try to access photos that the users are not authorized to view.

Which Amazon CloudWatch metric should a SysOps administrator monitor to better understand the extent of this issue?

    A GetRequest S3 metric
    
    B 4xx ErrorRate CloudFront metric
    
    C 5xxErrorRate CloudFront metric
    
    D PostRequests S3 metric

**Correct Answer: B**

A - Incorrect. The GetRequests metric shows access activity. The GetRequests metric does not show errors.

For more information about S3 metrics in CloudWatch, see Metrics and dimensions.

B - Correct. The 4xx errors include errors for objects that do not exist. These errors include 404 and 403 errors for objects that users are unauthorized to view. The 4xx errors are front-end errors that pertain to access to the object.

For more information about HTTP error codes, see List of Error Codes.

For more information about S3 metrics in CloudWatch, see Metrics and dimensions.

C - Incorrect. The 5xx errors are server-side errors, not access or authorization errors.

For more information about HTTP error codes, see List of Error Codes.

For more information about S3 metrics in CloudWatch, see Metrics and dimensions.

D - Incorrect. The PostRequests metric shows access activity. The PostRequests metric does not show errors.

For more information about S3 metrics in CloudWatch, see Metrics and dimensions.


### Q 8

* A company uses Amazon CloudFront to speed up the distribution of static and dynamic web content to users. Users are spread across different geographical regions around the world. The company wants to reduce the resource consumption on the content source servers.

Which solution will reduce the load on the origin?

    A Use Lambda@Edge
    
    B Use CloudFront Origin Shield
    
    C Configure custom headers
    
    D AWS Shield Advanced

**Correct Answer: B**

* Explanation

A - Incorrect. You can use Lambda@Edge to run code at global AWS edge locations without the need to provision or manage servers. However, Lambda@Edge would not speed up the distribution of content.

For more information about Lambda@Edge, see Using AWS Lambda with CloudFront Lambda@Edge.

B - Correct. Origin Shield is an additional layer in the CloudFront caching infrastructure that helps minimize an origin’s load, improve its availability, and reduce its operating costs. CloudFront provides a reduced load on the origin because requests that CloudFront can serve from the cache do not go to the origin.

For more information about Origin Shield, see Using Amazon CloudFront Origin Shield.

C - Incorrect. Custom headers validate that requests to an origin were sent from CloudFront. You can use custom headers to direct traffic, but custom headers do not reduce the load on a single origin.

For more information about custom headers, see Adding custom headers to origin requests.

D - Incorrect. Shield Advanced is a managed DDoS protection service for applications that run on AWS. Shield Advanced does not help reduce the burden of the origin servers.

For more information about Shield Advanced, see AWS Shield FAQs.


### Q 9

* A company is preparing to launch a new website. The website runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The company launched the instances by using a custom Amazon Machine Image (AMI) from an EC2 instance that runs without problems in a different VPC in the same AWS Region.

After deployment of the new EC2 instances, external testing failed to connect to the website by using HTTPS. The website is reachable by using SSH through a bastion host instance that runs in the same VPC.

Which steps should a SysOps administrator take to find the problem? (Select TWO.)

    A Ensure that the security group that is assigned to the instances is open to port 443 from the ALB's security group. (<- this)
    
    B Ensure that the ALB is assigned to a subnet with 0.0.0.0/0 routed to an internet gateway (<- this)
    
    C Ensure that the instances have a public IP address or an Elastic IP address that is assigned to each instance's elastic network interface.
    
    D Ensure that the instances are located in a subnet with 0.0.0.0/0 access routed to an internet gateway.
    
    E Ensure that both the system status and instance reachability checks for the instances are succeeding.

**Correct Answer: A & B**

A - Correct. The ALB must have port 443 open on its assigned security groups if the external user wants to connect over HTTPS. The instance's security group also must be open to port 443 to complete the connection. The subnets that include the ALB must have access to the internet gateway.

For more information about how to troubleshoot network connectivity, see How do I troubleshoot instance connection timeout errors in Amazon VPC?

For more information about security groups, see Control traffic to your AWS resources using security groups.

For more information about subnets and route tables, see VPCs and subnets.

B - Correct. The ALB must have port 443 open on its assigned security groups if the external user wants to connect over HTTPS. The instance's security group also must be open to port 443 to complete the connection. The subnets that include the ALB must have access to the internet gateway, ensuring the route table associated to the subnet allows all traffic to the internet gateway will allow external users to connect.

For more information about how to troubleshoot network connectivity, see How do I troubleshoot instance connection timeout errors in Amazon VPC?

For more information about security groups, see Control traffic to your AWS resources using security groups.

For more information about subnets and route tables, see VPCs and subnets.

C - Incorrect. Because the instances are behind an ALB, external users are not connecting directly to the instances by using a public IP address or an Elastic IP address. The ALB will direct traffic to the instances by using private—or internal—IP addresses.

D - Incorrect. Because the instances are behind an ALB, external users are not connecting directly to the instances. Therefore, there is no need for the instances to route through an internet gateway. The ALB will direct traffic to the instances by using private—or internal—IP addresses.

E - Incorrect. The instances are reachable by using private access through an SSH bastion host. This indicates that they are operational.


### Q 10

* A company has a key management service in its on-premises data center. The key management service uses an RSA asymmetric encryption algorithm. The company needs to integrate its system with a highly available, secure service in AWS to replace the on-premises service. The keys must be stored in dedicated hardware security modules that are validated by a third party. The company must control these hardware security modules.

Which solution will meet these requirements?

    A Import the current keys from the on-premises environmet into an AWS CloudHSM cluster. (<- this)
    
    B Revoke the current keys. Generate new asymmetric keys in AWS Key Management Service (AWS KMS).
    
    C Generate a customer key from AWS Key Management Service (AWS KMS). Import the key into the on-premises environment.
    
    D Launch an Amazon EC2 instance. Install an application that generates RSA keys. Import the existing keys into the application.

**Correct Answer: A**

* Explanation

A - Correct. With CloudHSM, you can manage your own encryption keys by using FIPS 140-2 Level 3 validated hardware security modules (HSMs). While AWS manages the HSM appliance, CloudHSM does not have access to your keys. You control and manage your own keys. You can cluster together CloudHSM devices for a highly available environment.

For more information about CloudHSM clusters, see AWS CloudHSM Clusters.

B - Incorrect. AWS KMS does not allow the storage of asymmetric keys in a dedicated environment under your control.
For more information about AWS KMS and asymmetric keys, see AWS Key Management Service supports asymmetric keys.

C - Incorrect. AWS KMS supports asymmetric keys. However, you cannot store the asymmetric keys in a dedicated environment under your control.

For more information about AWS KMS, see What is AWS Key Management Service?

D - Incorrect. A single EC2 instance does not meet the requirements for high availability.

For more information about EC2 instances, see Amazon EC2.


### Q 11

* A company's disaster recovery policy states that Amazon Elastic Block Store (Amazon EBS) snapshots must be created daily. The EBS snapshots must be retained for 6 months and then must be deleted. A SysOps administrator must automate this process.

Which solution will meet these requirements with the LEAST operational overhead?

    
    A Use Amazon EventBridge rules for AWS config.
    
    B Use Amazon Data Lifecycle Manager (Amazon DLM)
    
    C Use an Amazon S3 Lifecyle rule.
    
    D Use AWS CodePipeline to create snapshots. Use an AWS CloudFormation template to retain and delete snapshots.

**Correct Answer: B**

* Explanation

A - Incorrect. AWS Config and EventBridge are governance tools that assess, audit, evaluate, and remediate the configurations of AWS resources. However, AWS Config and EventBridge cannot automate the removal of EBS snapshots.

For more information about AWS Config, see What is AWS Config?

For more information about EventBridge, see What is Amazon EventBridge?

B - Correct. Amazon DLM can automate the creation, retention, and deletion of EBS snapshots and EBS-backed Amazon Machine Images (AMIs).

For more information about Amazon DLM, see Amazon Data Lifecycle Manager.

C - Incorrect. S3 Lifecycle rules define actions for Amazon S3 to take during an object's lifetime. EBS snapshots are stored in Amazon S3. However, the EBS snapshots are not accessible through standard S3 APIs. The S3 Lifecycle rules cannot access EBS snapshots.

For more information about S3 Lifecycle rules, see Managing your storage lifecycle.

For more information about the deletion of EBS snapshots, see Delete an Amazon EBS snapshot.

D - Incorrect. CodePipeline is a continuous integration and continuous delivery (CI/CD) tool. CloudFormation automates the creation of AWS resource stacks. However, CodePipeline and CloudFormation cannot automate the removal of EBS snapshots.

For more information about CodePipeline, see What is AWS CodePipeline?

For more information about CloudFormation, see What is AWS CloudFormation?


### Q 12

* A company maintains its AWS accounts with AWS Organizations and uses AWS Firewall Manager. The company wants to change the administrator account of Firewall Manager to a different account within the organization.

What should a SysOps administrator do to accomplish this task?

    
    A Remove the current administrator account from the organization that administers the firewall. Add the new administrator to the organization that administers the firewall.
    
    B Modify the service control policy (SCP) to deny access to Firewall Manager on the current account. Modify the SCP to allow access to Firewall Manager on the new administrator account.
    
    C Use the AWS Systems Manager console with the Organizations Maintenance account to switch Firewall Manager from the original administrator account to the new Firewall Manager administrator account number.
    
    D Log in to the current Firewall administrator account. Use the revoke feature of Firewall Manager. Sign in to the AWS Managemenet Console by using the Organizations management. Enter the new Firewall Manager administrator account number.

**Correct Answer: D**

* Explanation

A - Incorrect. You use the Firewall Manager console to remove the original Firewall Manager administrator account and to add the new Firewall Manager administrator account.

For more information about Firewall Manager, see AWS Firewall Manager.

For more information about Firewall Manager and Organizations, see AWS Firewall Manager and AWS Organizations.

B - Incorrect. SCPs allow or deny access to services from Organizations member accounts. SCPs do not control which account is the administrator account for Firewall Manager.

For more information about Firewall Manager, see AWS Firewall Manager.

For more information about Firewall Manager and Organizations, see AWS Firewall Manager and AWS Organizations.

C - Incorrect. This modification cannot be performed in the Systems Manager console.

For more information about how to change the Firewall Manager administrator account, see Changing the default administrator account.

For more information about Firewall Manager and Organizations, see AWS Firewall Manager and AWS Organizations.

D - Correct. You can designate only one account in an organization as a Firewall Manager administrator account. To create a new Firewall Manager administrator account, you must revoke the original administrator account first.

For more information about how to change the Firewall Manager administrator account, see Changing the default administrator account.

For more information about Firewall Manager and Organizations, see AWS Firewall Manager and AWS Organizations.


### Q 13

* A SysOps administrator needs to monitor a fleet of Amazon EC2 Linux instances by using Amazon CloudWatch. The SysOps administrator must not install any agents.

Which metrics can the SysOps administrator use CloudWatch to measure? (Select TWO.)


    
    A CPU utilization.
    
    B Memory utilization.
    
    C Network packets in. 
    
    D Network packets dropped.
    
    E CPU ready time.

**Correct Answer: A & C**

* Explanation

A - Correct. CloudWatch collects data about the performance of EC2 instances. CPUUtilization is one of the metrics that CloudWatch collects without the CloudWatch agent. With the agent, additional metrics are available.

For more information about CloudWatch metrics, see List the available CloudWatch metrics for your instances.

For more information about the CloudWatch agent, see Collect metrics, logs, and traces with the CloudWatch agent.

B - Incorrect. CloudWatch collects data about the performance of EC2 instances. However, the CloudWatch agent must be installed for CloudWatch to collect metrics about the memory utilization of an instance.

For more information about how to use CloudWatch metrics, see Using Amazon CloudWatch metrics.

For more information about the CloudWatch agent, see Collect metrics, logs, and traces with the CloudWatch agent.

C - Correct. CloudWatch collects data about the performance of EC2 instances. NetworkPacketsIn is one of the metrics that CloudWatch collects without the CloudWatch agent. With the agent, additional metrics are available.

For more information about CloudWatch metrics, see List the available CloudWatch metrics for your instances.

For more information about the CloudWatch agent, see Collect metrics, logs, and traces with the CloudWatch agent.

D - Incorrect. CloudWatch collects data about the performance of EC2 instances. However, metrics about network packet loss are not directly available from CloudWatch and would require you to install an additional tool on the instances.

For more information about how to use CloudWatch metrics, see Use Amazon CloudWatch metrics.

E - Incorrect. CloudWatch collects data about the performance of EC2 instances. CPU ready time is not a collectable metric available from CloudWatch.

For more information about how to use CloudWatch metrics, see Use Amazon CloudWatch metrics.


### Q 14

* A company is hosting a service-oriented architecture across multiple Amazon EC2 instances. Each instance hosts a different application. The services read and write messages to Amazon Simple Queue Service (Amazon SQS) queues for cross-service communication. The company uses Amazon CloudWatch for monitoring.

The company has configured a CloudWatch alarm to alert system operators when the value of the ApproximateNumberOfMessagesVisible metric is more than 50. A system operator just received an alert that the alarm has entered the ALARM state.

What could be the cause of the alarm?


    
    A The visibility timeout for the SQS queue is set to a value that is too long in duration.
    
    B the applications that are receiving the messages from the SQS queue are purging the messages from the queue after processing the messages.
    
    C the delivery delay for the SQS queue is set to a value that is too long in duration
    
    D The applications that are receiving the messages from the SQS queue are not deleting the mssages from the queue after processing them.

**Correct Answer: D**

A - Incorrect. A duration that is too long for the visibility timeout would reduce the value that is tracked by the ApproximateNumberOfMessagesVisible metric. Therefore, it would not cause the issue of the ApproximateNumberOfMessagesVisible value being too high.

For more information about visibility timeout, see Amazon SQS visibility timeout.

B - Incorrect. A purge of the SQS queue would delete all messages in the queue. Therefore, the queue would not form a backlog.

For more information about how to purge SQS queues, see Purging messages from an Amazon SQS queue (console).

C - Incorrect. A duration that is too long for the delivery delay would not cause the SQS queue to form a backlog. It would artificially reduce the number of visible messages in the queue.

For more information about the delivery delay parameter for Amazon SQS, see Amazon SQS delay queues.

D - Correct. Amazon SQS does not automatically delete a message after retrieving it, in case the message was not received. To delete a message, send a separate request that acknowledges a message has been successfully received and processed. A message must be received before it can be deleted.

If you fail to delete a message after successfully processing it, the message would be placed back into the queue even though the message already has been processed. This process eventually could cause a backlog of messages in the queue because no message is ever deleted from the queue.

For more information about SQS queues, see Receive and delete a message (console).


### Q 15

* A company has deployed a new application that runs on Amazon EC2 instances. The company’s security team wants the application team to verify that all common vulnerabilities and exposures are addressed regularly throughout the application's life span.

How can the application team meet this requirement?


    
    A Perform regular assessments with Amazon Inspector.
    
    B Perform regular assessments with AWS Trusted Advisor.
    
    C Integrate the AWS Health Dashboard with Amazon EventBridge events to get security notifications.
    
    D Grant the security team access to AWS Artifact.

**Correct Answer: A**

* Explanation

A - Correct. Amazon Inspector discovers potential security issues by using security rules to analyze AWS resources. Amazon Inspector also integrates with AWS Security Hub to provide a view of your security posture across multiple AWS accounts.

For more information about Amazon Inspector, see Amazon Inspector Classic Assessment Templates and Assessment Runs.

B - Incorrect. Trusted Advisor provides recommendations that help you follow AWS best practices. Trusted Advisor does not check for vulnerabilities on the instance itself.

For more information about Trusted Advisor, see AWS Trusted Advisor.

C - Incorrect. AWS Health Dashboard provides visibility into both public events and account-specific events. These events can be upcoming maintenance issues for a service in a Region or account-specific events, such as a deprecated resource in your account. However, AWS Health Dashboard does not check for vulnerabilities and exposures.

For more information about AWS Health Dashboard, see AWS Health Dashboard.

For more information about AWS Health Dashboard integration with Amazon EventBridge, see Monitoring AWS Health Events with Amazon EventBridge.

D - Incorrect. AWS Artifact provides access to compliance documentation. AWS Artifact does not check for vulnerabilities and exposures.

For more information about AWS Artifact, see AWS Artifact.


### Q 16

* An IT director needs a monthly breakdown of cloud computing expenditures for each department in a company. The company uses AWS Organizations to manage the AWS accounts and has multiple AWS accounts in each organization.

Which combination of steps will provide this financial information? (Select TWO.)
    
    A Use AWS Systems Manager Fleet Manager to identify resources that are not tagged in each account. Apply a tag that is named Department to any untagged resources.
    
    B Activate a cost allocation tag that is named Department in the AWS Billing and Cost Management console in the Organizations management account. Use a tag policy to a mandate a Department tag on new resources.
    
    C Use the AWS Resource Groups Tag Editor to identify resources that are not tagged in each account. Apply a tag that is named Department to any untagged resources.
    
    D Activate a cost allocation tag that is named Department within the AWS Billing and Cost Management console in each account in the organization.
    
    E Create an AWS Config rule across all accounts in the organization to mark resources that lack a Department tag as noncompliant.

**Correct Answer: B & C**

* Explanation

A - Incorrect. Fleet Manager helps you remotely view the performance of your fleet of servers that run on AWS. Fleet Manager will not help identify resources that are not tagged in each account.

For more information about Fleet Manager, see AWS Systems Manager Fleet Manager.

B - Correct. You must activate a tag in the Billing and Cost Management console before viewing the expense by cost allocation tag. You should mandate the use of tags to ensure that the resources are tagged correctly.

For more information about tag policies, see Tag policies.

C - Correct. With Resource Groups, you can create, maintain, and view a collection of resources that share common tags. Tag Editor manages tags across services and AWS Regions. Tag Editor can perform a global search and can edit a large number of tags at one time.

For more information about resource groups and tagging, see Using Tag Editor.

D - Incorrect. Cost allocation tags are managed at the management account level, not separately on each AWS account.

For more information about tagging Organizations resources, see Tagging AWS Organizations resources.

E - Incorrect. AWS Config rules can identify resources that are noncompliant, but AWS Config rules do not tag the resources. Even if you tag resources as noncompliant, this step does not provide any financial information. Therefore, you cannot receive financial reporting as required by the scenario.

For more information about AWS Config rules, see Tagging Your AWS Config Resources.


### Q 17

* A SysOps administrator must ensure that AWS CloudFormation deployment changes are properly tracked for governance.

Which AWS service should the SysOps administrator use to meet this requirement?

    
    A AWS Artifact
    
    B AWS Config
    
    C Amazon Inspector
    
    D AWS Trusted Advisor

**Correct Answer: B**

* Explanation

A - Incorrect. AWS Artifact keeps compliance-related reports and agreements. AWS Artifact does not track CloudFormation changes.

For more information about AWS Artifact, see What is AWS Artifact?

B - Correct. AWS Config can track changes to CloudFormation stacks. A CloudFormation stack is a collection of AWS resources that you can manage as a single unit. With AWS Config, you can review the historical configuration of your CloudFormation stacks and review all changes that occurred to them.

For more information about how AWS Config can track changes to CloudFormation deployments, see cloudformation-stack-drift-detection-check.

C - Incorrect. Amazon Inspector is used for security compliance of instances and applications, but it does not track CloudFormation changes.

For more information about Amazon Inspector, see What is Amazon Inspector?.

D - Incorrect. Trusted Advisor provides real-time guidance to help users follow AWS best practices to provision their resources. However, Trusted Advisor does not provide guidance about CloudFormation deployments.

For more information about Trusted Advisor, see AWS Trusted Advisor.


### Q 18

* A company is running a website that stores data in an Amazon RDS for MySQL DB instance. The company expects the data that is stored in the database to grow significantly during the next 6 months.

A SysOps administrator can see that the DB instance will run out of storage space in that time period. The current DB instance uses General Purpose SSD (gp2) volumes for storage.

Which action can the SysOps administrator take to scale the storage for the DB instance?


    A Launch an RDS read replica

    B Enable storage autoscaling for the DB instance.

    C Turn on Multi-AZ feature for the DB instance

    D Change the DB instance storage type to standard magnetic

**Correct Answer: B**

A - Incorrect. An RDS read replica will not scale the storage for the DB instance. RDS read replicas offload read requests for data.

For more information about RDS read replicas, see Working with DB instance read replicas.

B - Correct. With RDS storage autoscaling, you can set the desired maximum storage limit. Autoscaling will manage the storage size. RDS storage autoscaling monitors actual storage consumption and then scales capacity automatically when actual utilization approaches the provisioned storage capacity.

For more information about storage autoscaling, see Managing capacity automatically with Amazon RDS storage autoscaling.

C - Incorrect. A Multi-AZ deployment for the DB instance will launch another DB instance in another subnet to make the database highly available. This deployment does not scale the storage.

For more information about Multi-AZ deployments, see Configuring and managing a Multi-AZ deployment.

D - Incorrect. A change in the type of storage could affect performance, but it will not scale the amount of data that can be stored on the DB instance.

For more information about RDS storage options, see Amazon RDS DB instance storage.


### Q 19

* A company has an application that runs on a fleet of Amazon EC2 instances that run Microsoft Windows. The company needs to apply patches to the operating system each month. The company uses AWS Systems Manager Patch Manager to apply the patches on a schedule. When the fleet is being patched, users of the application report delayed service responses.

What should the company do to MINIMIZE the impact on users during patch deployment?


    
    A Change the number of instances patched at any one time to 100%
    
    B Create a snapshot of each instance in the fleet by using a Systems Manager Automation runbook before the start of the patch process.
    
    C Configure the maintenance window to patch 10% of the instances in the patch group at a time.
    
    D Create a patched Amazon Machine Image (AMI). Configure the maintenance windows option to deploy the patched AMI on only 10% of the fleet at a time.

**Correct Answer: C**

* Explanation:

A - Incorrect. With this approach, all the instances are patched at the same time. If a reboot is necessary, all the instances will reboot at the same time. This solution would have a greater impact on the users.

For more information about how to apply rate controls during patching, see Creating a maintenance window for patching (console).

B - Incorrect. The creation of a snapshot is a good safeguard. However, a snapshot does not reduce the risk of an outage while patches are applied.

For more information about snapshots, see Amazon EC2 backup and recovery with snapshots and AMIs.

C - Correct. A rate control concurrency of 10% ensures that only 1 out of 10 instances will get patched at a time. This process will leave enough capacity to run most workloads without interruption. You can set rate control as an absolute number or a percentage.

For more information about how to apply rate controls during patching, see Creating a maintenance window for patching (console).

D - Incorrect. Patch Manager applies patches. Patch Manager does not deploy AMIs.

For more information about AMIs, see Instances and AMIs.


### Q 20

* A SysOps administrator attached the following IAM policy to a developer's IAM user account:

~~~
```
{

    "Version": "2012-10-17",

    "Statement": {

        "Effect": "Allow",

        "Action": "dynamodb:GetItem",

        "Resource": "*",

        "Condition": {

            "DateGreaterThan": {

                "aws:CurrentTime": "2020-07-01T00:00:00Z"

            },

            "DateLessThan": {

                "aws:CurrentTime": "2020-12-31T23:59:59Z"

            },

            "StringEquals": {

                "aws:SourceVpc": "vpc-111bbb22"

            }

        }

    }

}
```
~~~

Which permission will the developer have for using GetItem?


    
    A Access is allowed on or between July 1, 2020, and December 21, 2020 (UTC), and if the request is initiated from vpc-111bbb22
    
    B Access is allowed on or between July 1, 2020, and December 21, 2020 (UTC), or if the request is initiated from vpc-111bbb22
    
    C Access is allowed on or between July 1, 2020, and December 21, 2020 (UTC), and if the request uses a VPC endpoint in vpc-111bbb22
    
    D Access is allowed on or between July 1, 2020, and December 21, 2020 (UTC), or if the request uses a VPC endpoint in vpc-111bbb22

**Correct Answer: A**

* Explanation

A - Correct. This IAM policy includes multiple conditions. One condition allows access to actions based on date and time. Another condition requires the API call to originate from a specific VPC. This policy grants the permissions necessary to complete this action from the AWS API or AWS CLI only.

For more information about how to create a condition with multiple keys or values, see Conditions with multiple context keys or values.

B - Incorrect. Multiple conditions all need to evaluate as true for the condition block to match. This response incorrectly states that one or the other of the conditions cause the IAM policy to meet the condition.

C - Incorrect. The aws:SourceVpc condition is related to the VPC from where the API call initiates.

D - Incorrect. The aws:SourceVpc condition is related to the VPC from where the API call initiates. Additionally, multiple conditions all need to evaluate as true for the condition block to match.
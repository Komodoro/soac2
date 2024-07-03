---
sectionid: Dump231012023
sectionclass: h2
parent-id: Questions
title: Dump 2 - Exam Topics - 31-01-2023
number: 3200
---

### Question #1 

* A company is planning to run a global marketing application in the AWS Cloud. The application will feature videos that can be viewed by users. The company must ensure that all users can view these videos with low latency.
Which AWS service should the company use to meet this requirement?

A. AWS Auto Scaling

B. Amazon Kinesis Video Streams

C. Elastic Load Balancing

D. Amazon CloudFront 

**Correct Answer: D**

### Question #2

* Which pillar of the AWS Well-Architected Framework refers to the ability of a system to recover from infrastructure or service disruptions and dynamically acquire computing resources to meet demand?

A. Security

B. Reliability

C. Performance efficiency

D. Cost optimization

**Correct Answer: B**

### Question #3

* Which of the following are benefits of migrating to the AWS Cloud? (Choose two.)

A. Operational resilience

B. Discounts for products on Amazon.com

C. Business agility

D. Business excellence

E. Increased staff retention

**Correct Answer: A, C**

### Question #4

* A company is planning to replace its physical on-premises compute servers with AWS serverless compute services. The company wants to be able to take advantage of advanced technologies quickly after the migration.
Which pillar of the AWS Well-Architected Framework does this plan represent?


A. Security

B. Performance efficiency

C. Operational excellence

D. Reliability

**Correct Answer: B**


### Question #5

* A large company has multiple departments. Each department has its own AWS account. Each department has purchased Amazon EC2 Reserved Instances.
Some departments do not use all the Reserved Instances that they purchased, and other departments need more Reserved Instances than they purchased.
The company needs to manage the AWS accounts for all the departments so that the departments can share the Reserved Instances.
Which AWS service or tool should the company use to meet these requirements?

A. AWS Systems Manager

B. Cost Explorer

C. AWS Trusted Advisor

D. AWS Organizations 

**Correct Examtopic Answer: B**

**Correct Community Answer: D**

* Explanation: https://aws.amazon.com/ru/organizations/ 

It has to be D because the cost explorer is for managing the "AWS COST & USAGE", while the AWS organization is for managing the "ACCOUNTS".

AWS Organizations
When your account is managed by AWS Organizations, you can take advantage of that to share resources more easily. With or without Organizations, a user can share with individual accounts. However, if your account is in an organization, then you can share with individual accounts, or with all accounts in the organization or in an OU without having to enumerate each account.

https://docs.aws.amazon.com/ram/latest/userguide/getting-started-sharing.html#getting-started-sharing-orgs


### Question #6

* Which component of the AWS global infrastructure is made up of one or more discrete data centers that have redundant power, networking, and connectivity?

A. AWS Region

B. Availability Zone

C. Edge location

D. AWS Outposts

**Correct Answer: B**

### Question #7

* Which duties are the responsibility of a company that is using AWS Lambda? (Choose two.)

A. Security inside of code

B. Selection of CPU resources

C. Patching of operating system

D. Writing and updating of code

E. Security of underlying infrastructure

**Correct Answer: A, D**

### Question #8

* Which AWS services or features provide disaster recovery solutions for Amazon EC2 instances? (Choose two.)


A. EC2 Reserved Instances

B. EC2 Amazon Machine Images (AMIs)

C. Amazon Elastic Block Store (Amazon EBS) snapshots

D. AWS Shield

E. Amazon GuardDuty

**Correct Answer: B, C**

### Question #9

* A company is migrating to the AWS Cloud instead of running its infrastructure on premises.
Which of the following are advantages of this migration? (Choose two.)

A. Elimination of the need to perform security auditing

B. Increased global reach and agility

C. Ability to deploy globally in minutes

D. Elimination of the cost of IT staff members

E. Redundancy by default for all compute services

**Correct Examtopics Answer: B, D**

**Correct Community Answer: B, C**

* Explanation:

The six advantages of cloud computing are:

•	Trade upfront expense for variable expense.

•	Benefit from massive economies of scale.

•	Stop guessing capacity.

•	Increase speed and agility.   Yes B

•	Stop spending money running and maintaining data centers.

•	Go global in minutes.  YES C

Additional reference to support the answers B, C.
Refer to: https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html

Adding to the fact that it must be ***B & C*** the correct answers, at the end of the day you'll still need someone to manage your IT workloads in the cloud, you can't just fire them all even if C is already part of the B to some extent, where AWS always a money saver on IT Staff spending.

### Question 10

* A user is comparing purchase options for an application that runs on Amazon EC2 and Amazon RDS. The application cannot sustain any interruption. The application experiences a predictable amount of usage, including some seasonal spikes that last only a few weeks at a time. It is not possible to modify the application.
Which purchase option meets these requirements MOST cost-effectively?


A. Review the AWS Marketplace and buy Partial Upfront Reserved Instances to cover the predicted and seasonal load.

B. Buy Reserved Instances for the predicted amount of usage throughout the year. Allow any seasonal usage to run on Spot Instances.

C. Buy Reserved Instances for the predicted amount of usage throughout the year. Allow any seasonal usage to run at an On-Demand rate.

D. Buy Reserved Instances to cover all potential usage that results from the seasonal usage.

**Correct Examtopics Answer: B**

**Correct Community Answer: C**

* Explanation: C is the correct answer, the question explicitly mentioned that "The application cannot sustain any interruption"  of which Spot Instances are ideal for workloads with flexible start and end times, or that can withstand interruptions.  Ideally we want pricing that doesn't allow interruption in this case it will be On-Demand.

### Question #11

* A company wants to review its monthly costs of using Amazon EC2 and Amazon RDS for the past year.
Which AWS service or tool provides this information?

A. AWS Trusted Advisor

B. Cost Explorer

C. Amazon Forecast

D. Amazon CloudWatch

**Correct Answer: B**

### Question #12

* A company wants to migrate a critical application to AWS. The application has a short runtime. The application is invoked by changes in data or by shifts in system state. The company needs a compute solution that maximizes operational efficiency and minimizes the cost of running the application.
Which AWS solution should the company use to meet these requirements?

A. Amazon EC2 On-Demand Instances

B. AWS Lambda

C. Amazon EC2 Reserved Instances

D. Amazon EC2 Spot Instances

**Correct Answer: B**

### Question #13

* Which AWS service or feature allows users to connect with and deploy AWS services programmatically?

A. AWS Management Console

B. AWS Cloud9

C. AWS CodePipeline

D. AWS software development kits (SDKs) 

**Correct Answer: D**

### Question #14

* A company plans to create a data lake that uses Amazon S3.
Which factor will have the MOST effect on cost?


A. The selection of S3 storage tiers

B. Charges to transfer existing data into Amazon S3

C. The addition of S3 bucket policies

D. S3 ingest fees for each request

**Correct Answer: A**

### Question #15

* A company is launching an ecommerce application that must always be available. The application will run on Amazon EC2 instances continuously for the next
12 months.
What is the MOST cost-effective instance purchasing option that meets these requirements?


A. Spot Instances

B. Savings Plans

C. Dedicated Hosts

D. On-Demand Instances

**Correct Answer: B**

### Question #16

* Which AWS service or feature can a company use to determine which business unit is using specific AWS resources?


A. Cost allocation tags

B. Key pairs

C. Amazon Inspector

D. AWS Trusted Advisor

**Correct Answer: A**

### Question #17

* A company wants to migrate its workloads to AWS, but it lacks expertise in AWS Cloud computing.
Which AWS service or feature will help the company with its migration?


A. AWS Trusted Advisor

B. AWS Consulting Partners

C. AWS Artifacts

D. AWS Managed Services 

**Correct Answer: D**

* Explanation: Altough you still need expertise to use managed services. An APN Consulting Partner helps an AWS customer implement and manage an AWS cloud deployment. These types of partners include system integrators, managed services providers, and other consultancies and agencies. An APN Technology Partner provides software tools and services that are hosted on or integrated with AWS. They help customers design, architect, build, migrate, and manage workloads and applications on Amazon Web Services. 

https://d1.awsstatic.com/partner-network/APN_Consulting-Benefits_Brochure-Digital.pdf

The question, mentions that the company "lacks expertise". This means that the answer should be something that provides that. By choosing D we are "trying" to remove the need of that expertise, even tough is arguable because you still need some degree of expertise to do use managed services. AWS Consulting Partners is a service that is provided by Amazon. In this case is not a cloud service but is a service where Amazon is working constantly to provide a vetted list of Partners that provide good expertise. Being what mostly makes sense the answer being B.

But answer may be indeed D. Look into this video https://www.youtube.com/watch?v=OCK8GCImWZw&t=98 starting from 10:49. Also agree with fryderyk comment i.e " A case study from AWS website seems to support the idea that it's the Managed Services: https://aws.amazon.com/solutions/case-studies/origin-energy-case-study/ "

Being B more of a feature then a service, like it says in question it may be B also. Maybe its both.


### uestion #18 
* Which AWS service or tool should a company use to centrally request and track service limit increases?

A. AWS Config

B. Service Quotas Most Voted

C. AWS Service Catalog

D. AWS Budgets

**Correct Answer: B**

### Question #19

* Which documentation does AWS Artifact provide?


A. Amazon EC2 terms and conditions

B. AWS ISO certifications

C. A history of a company's AWS spending

D. A list of previous-generation Amazon EC2 instance types

**Correct Answer: B**

### Question #20

* Which task requires using AWS account root user credentials?

A. Viewing billing information

B. Changing the AWS Support plan

C. Starting and stopping Amazon EC2 instances

D. Opening an AWS Support case

**Correct Answer: B**

### Question #21 Topic 1

* A company needs to simultaneously process hundreds of requests from different users.
Which combination of AWS services should the company use to build an operationally efficient solution?


A. Amazon Simple Queue Service (Amazon SQS) and AWS Lambda

B. AWS Data Pipeline and Amazon EC2

C. Amazon Kinesis and Amazon Athena

D. AWS Amplify and AWS AppSync

**Correct Examtopic Answer: B** <- This is wrong obviously

**Correct Community Answer: A**

### Question #22

* What is the scope of a VPC within the AWS network?

A. A VPC can span all Availability Zones globally.

B. A VPC must span at least two subnets in each AWS Region.

C. A VPC must span at least two edge locations in each AWS Region.

D. A VPC can span all Availability Zones within an AWS Region. 

**Correct Answer: D**

### Question #23

* Which of the following are components of an AWS Site-to-Site VPN connection? (Choose two.)


A. AWS Storage Gateway

B. Virtual private gateway

C. NAT gateway

D. Customer gateway

E. Internet gateway

**Correct Answer: B, D**

### Question #24

* A company needs to establish a connection between two VPCs. The VPCs are located in two different AWS Regions. The company wants to use the existing infrastructure of the VPCs for this connection.
Which AWS service or feature can be used to establish this connection?


A. AWS Client VPN

B. VPC peering

C. AWS Direct Connect

D. VPC endpoints

**Correct Answer: B**

Reference: https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html

### Question #25

* According to the AWS shared responsibility model, what responsibility does a customer have when using Amazon RDS to host a database?


A. Manage connections to the database

B. Install Microsoft SQL Server

C. Design encryption-at-rest strategies

D. Apply minor database patches

**Correct Answer: A**

### Question #26

* What are some advantages of using Amazon EC2 instances to host applications in the AWS Cloud instead of on premises? (Choose two.)


A. EC2 includes operating system patch management.

B. EC2 integrates with Amazon VPC, AWS CloudTrail, and AWS Identity and Access Management (IAM).

C. EC2 has a 100% service level agreement (SLA).

D. EC2 has a flexible, pay-as-you-go pricing model.

E. EC2 has automatic storage cost optimization. 

**Correct Answer: D, E**

### Question #27 

* A user needs to determine whether an Amazon EC2 instance's security groups were modified in the last month.
How can the user see if a change was made?


A. Use Amazon EC2 to see if the security group was changed.

B. Use AWS Identity and Access Management (IAM) to see which user or role changed the security group.

C. Use AWS CloudTrail to see if the security group was changed.

D. Use Amazon CloudWatch to see if the security group was changed.

**Correct Answer: C**

### Question #28

Which AWS service will help protect applications running on AWS from DDoS attacks?


A. Amazon GuardDuty

B. AWS WAF

C. AWS Shield

D. Amazon Inspector

**Correct Answer: C**

### Question #29

* Which AWS service or feature acts as a firewall for Amazon EC2 instances?


A. Network ACL

B. Elastic network interface

C. Amazon VPC

D. Security group 

**Correct Answer: D**

### Question #30

* How does the AWS Cloud pricing model differ from the traditional on-premises storage pricing model?


A. AWS resources do not incur costs

B. There are no infrastructure operating costs 

C. There are no upfront cost commitments

D. There are no software licensing costs

**Correct ExamTopic Answer: B** - because in AWS you pay for storage, compute, etc. You don't pay for infra ops directly. On the other hand you can make commitments with saving plans or reserved instances. (but: the question is specific to Storage.. there are no upfront commitments (savings plan etc apply to ec2 instances only))

**Correct Community Answer: C** - No Capex, Only Opex. No upfront or capital expenditure. But On premise or AWS will have operational expenditure (OpEx), and the same is managed/covered by the fees you pay for AWS. - the question is specific to Storage.. there are no upfront commitments (savings plan etc apply to ec2 instances only)

* Explanation:  CapEx vs. OpEx: An Overview

There are a variety of costs and expenses which companies have to pay in order to continue running their businesses. These costs can be one-off or they can be recurring, and it can often be challenging to keep up with all of these expenses. But how are they able to keep track of all of them?

One way is to divide them up into different categories—the most common of which are capital expenditures (CapEx) and operating expenses (OpEx). Capital expenditures are major purchases that a company makes, which are used over the long term. Operating expenses, on the other hand, are the day-to-day expenses that a company incurs to keep its business running. 

### Question #31

* A company has a single Amazon EC2 instance. The company wants to adopt a highly available architecture.
What can the company do to meet this requirement?


A. Scale vertically to a larger EC2 instance size.

B. Scale horizontally across multiple Availability Zones.

C. Purchase an EC2 Dedicated Instance.

D. Change the EC2 instance family to a compute optimized instance.

**Correct Answer: B**

### Question #32

* A company's on-premises application deployment cycle was 3-4 weeks. After migrating to the AWS Cloud, the company can deploy the application in 2-3 days.
Which benefit has this company experienced by moving to the AWS Cloud?


A. Elasticity

B. Flexibility

C. Agility

D. Resilience

**Correct Examtopics Answer: A**

**Correct Community Answer: C**

* Explanation: Answer is C. This is the definition of agility as per AWS : Increase speed and agility – In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower. Elasticity basically means scaling up/down when needed since they are talking about Application not hosts, so it should be Agility not Elasticity. - https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html

### Question #33

* Which of the following are included in AWS Enterprise Support? (Choose two.)


A. AWS technical account manager (TAM)

B. AWS partner-led support

C. AWS Professional Services

D. Support of third-party software integration to AWS

E. 5-minute response time for critical issues

**Correct Answer: A, D**

https://i.ytimg.com/vi/0LQcq_zyNmg/maxresdefault.jpg

Explanation: 

* Guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components.) https://aws.amazon.com/premiumsupport/plans/enterprise/
* The word integration in option D seems confusing. Since AWS does provide third-party application support, D seems like the correct choice along with A
https://aws.amazon.com/premiumsupport/third-party-applications/
* Not E, because it's  it's 15min not 5 min (it's a "*< 15 mins*")

### Question #34

* A global media company uses AWS Organizations to manage multiple AWS accounts.
Which AWS service or feature can the company use to limit the access to AWS services for member accounts?


A. AWS Identity and Access Management (IAM)

B. Service control policies (SCPs)

C. Organizational units (OUs)

D. Access control lists (ACLs)

**Correct Examtopic Answer: C**

**Correct Community Answer: B**

* *Explanation*: Must be B (SCPs)

https://aws.amazon.com/blogs/industries/best-practices-for-aws-organizations-service-control-policies-in-a-multi-account-environment/#:~:text=One%20of%20the%20features%20from,each%20member%20account%20can%20access.

* ***One of the features from AWS Organizations is SCPs, which helps you specify the maximum permissions for member accounts in the organization. ***

### Question #35

* A company wants to limit its employees' AWS access to a portfolio of predefined AWS resources.
Which AWS solution should the company use to meet this requirement?


A. AWS Config

B. AWS software development kits (SDKs)

C. AWS Service Catalog

D. AWS AppSync

**Correct Answer: C**

### Question #36

* An online company was running a workload on premises and was struggling to launch new products and features. After migrating the workload to AWS, the company can quickly launch products and features and can scale its infrastructure as required.
Which AWS Cloud value proposition does this scenario describe?


A. Business agility

B. High availability

C. Security

D. Centralized auditing

**Correct Answer: A**

### Question #37

* Which of the following are advantages of the AWS Cloud? (Choose two.)


A. AWS management of user-owned infrastructure

B. Ability to quickly change required capacity

C. High economies of scale

D. Increased deployment time to market

E. Increased fixed expenses

**Correct Answer: B, C**

### Question #38

* AWS has the ability to achieve lower pay-as-you-go pricing by aggregating usage across hundreds of thousands of users.
This describes which advantage of the AWS Cloud?

A. Launch globally in minutes

B. Increase speed and agility

C. High economies of scale

D. No guessing about compute capacity

**Correct Answer: C**

### Question #39

* A company has a database server that is always running. The company hosts the server on Amazon EC2 instances. The instance sizes are suitable for the workload. The workload will run for 1 year.
Which EC2 instance purchasing option will meet these requirements MOST cost-effectively?


A. Standard Reserved Instances

B. On-Demand Instances

C. Spot Instances

D. Convertible Reserved Instances

**Correct Answer: A**

### Question #40

* A company is developing a mobile app that needs a high-performance NoSQL database.
Which AWS services could the company use for this database? (Choose two.)


A. Amazon Aurora

B. Amazon RDS

C. Amazon Redshift

D. Amazon DocumentDB (with MongoDB compatibility)

E. Amazon DynamoDB 

**Correct Examtopics Answer: B, E**

**Correct Community  Answer: D, E**

Explanation: RDS is a SQL based DB. So it has to be D and E.

### Question #41

* Which tasks are the responsibility of AWS, according to the AWS shared responsibility model? (Choose two.)


A. Patch the Amazon EC2 guest operating system.

B. Upgrade the firmware of the network infrastructure.

C. Apply password rotation for IAM users.

D. Maintain the physical security of edge locations.

E. Maintain least privilege access to the root user account.

**Correct Answer: B, D**

### Question #42

* Which of the following are features of network ACLs as they are used in the AWS Cloud? (Choose two.)


A. They are stateless.

B. They are stateful.

C. They evaluate all rules before allowing traffic.

D. They process rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic.

E. They operate at the instance level.

**Correct Answer: A, D**

### Question #43

A company has designed its AWS Cloud infrastructure to run its workloads effectively. The company also has protocols in place to continuously improve supporting processes.
Which pillar of the AWS Well-Architected Framework does this scenario represent?


A. Security

B. Performance efficiency

C. Cost optimization

D. Operational excellence 

**Correct Answer: D**

### Question #44

* Which AWS service or feature can be used to create a private connection between an on-premises workload and an AWS Cloud workload?


A. Amazon Route 53

B. Amazon Macie

C. AWS Direct Connect

D. AWS PrivateLink

**Correct Examtopic Answer: D** <- This time the guy from the site is right IMHO.

**Correct Community Answer: C**

* Explanation: It has to be D. Because: Its a workload and not a network connection. "AWS Direct Connect allows to create a private, dedicated network connection from on-premises data center to your VPC, but it does not create a direct private connection between a specific on-premises application and an AWS Cloud service. Direct Connect is a network-level connection, it allows you to connect your on-premises network to your VPC, but it does not provide a direct, application-level connection between your on-premises application and an AWS Cloud service. To create a private connection between a specific on-premises application and an AWS Cloud service, you can use VPC endpoint services (such as PrivateLink) to access the service over an Amazon VPC endpoint, rather than over external network infrastructure. This provides increased security and performance by eliminating the need to traverse external networks." - https://aws.amazon.com/privatelink/

AWS PrivateLink provides private connectivity between virtual private clouds (VPCs), supported AWS services, and your on-premises networks without exposing your traffic to the public internet. Interface VPC endpoints, powered by PrivateLink, connect you to services hosted by AWS Partners and supported solutions available in AWS Marketplace.

Private Connection may be the keyword along with workload on-premises.

For Direct Conn4ect to be private needs the Sitelink: With AWS Direct Connect SiteLink, you can send data between AWS Direct Connect locations to create private network connections between the offices and data centers in your global network. It's a feature from AWS Direct Connect (DX) - https://aws.amazon.com/blogs/networking-and-content-delivery/introducing-aws-direct-connect-sitelink/



### Question #45

* A company needs to graphically visualize AWS billing and usage over time. The company also needs information about its AWS monthly costs.
Which AWS Billing and Cost Management tool provides this data in a graphical format?


A. AWS Bills

B. Cost Explorer

C. AWS Cost and Usage Report

D. AWS Budgets

**Correct Answer: B**

### Question #46

* A company wants to run production workloads on AWS. The company needs concierge service, a designated AWS technical account manager (TAM), and technical support that is available 24 hours a day, 7 days a week.
Which AWS Support plan will meet these requirements?


A. AWS Basic Support

B. AWS Enterprise Support

C. AWS Business Support

D. AWS Developer Support

**Correct Answer: B**

### Question #47

* Which architecture design principle describes the need to isolate failures between dependent components in the AWS Cloud?


A. Use a monolithic design.

B. Design for automation.

C. Design for single points of failure.

D. Loosely couple components.

**Correct Answer: D**

### Question #48

* Which AWS services are managed database services? (Choose two.)


A. Amazon Elastic Block Store (Amazon EBS)

B. Amazon S3

C. Amazon RDS

D. Amazon Elastic File System (Amazon EFS)

E. Amazon DynamoDB 

**Correct Answer: C, E**

* Explanation: A , B & D are Storage Services.. and  C & E are Database Services. KEYWORD here is DATABASE


### Question #49

* A company is using the AWS Free Tier for several AWS services for an application.
What will happen if the Free Tier usage period expires or if the application use exceeds the Free Tier usage limits?


A. The company will be charged the standard pay-as-you-go service rates for the usage that exceeds the Free Tier usage.

B. AWS Support will contact the company to set up standard service charges.

C. The company will be charged for the services it consumed during the Free Tier period, plus additional charges for service consumption after the Free Tier period.

D. The company's AWS account will be frozen and can be restarted after a payment plan is established.

**Correct Answer: A**

### Question #50

* A company recently deployed an Amazon RDS instance in its VPC. The company needs to implement a stateful firewall to limit traffic to the private corporate network.
Which AWS service or feature should the company use to limit network traffic directly to its RDS instance?


A. Network ACLs

B. Security groups

C. AWS WAF

D. Amazon GuardDuty

**Correct Examtopic Answer: C**

**Correct Community Answer: B**

* Explanation: 

**It has to be B.** Again, same old topic; the keyword here is STATEFUL:

- stateless: Netwrok ACL

- stateful: security group

* AWS WAF is a web application firewall that lets you monitor the HTTP(S) requests that are forwarded to your protected web application resources. You can protect the following resource types:

- Amazon CloudFront distribution

- Amazon API Gateway REST API

- Application Load Balancer

- AWS AppSync GraphQL API

- Amazon Cognito user pool

* "Security groups are stateful". Hence sec group is the right answer. 

- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules.html

- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html

WAF is for internet and web application/services. Hence not the answer.

### Question #51

* Which AWS service uses machine learning to help discover, monitor, and protect sensitive data that is stored in Amazon S3 buckets?


A. AWS Shield

B. Amazon Macie

C. AWS Network Firewall

D. Amazon Cognito

**Correct Answer: B**

### Question #52

* A company wants to improve the overall availability and performance of its applications that are hosted on AWS.
Which AWS service should the company use?


A. Amazon Connect

B. Amazon Lightsail

C. AWS Global Accelerator

D. AWS Storage Gateway

**Correct Answer: C**

### Question #53

* Which AWS service or feature identifies whether an Amazon S3 bucket or an IAM role has been shared with an external entity?


A. AWS Service Catalog

B. AWS Systems Manager

C. AWS IAM Access Analyzer

D. AWS Organizations

**Correct Answer: C**

### Question #54

* A company does not want to rely on elaborate forecasting to determine its usage of compute resources. Instead, the company wants to pay only for the resources that it uses. The company also needs the ability to increase or decrease its resource usage to meet business requirements.
Which pillar of the AWS Well-Architected Framework aligns with these requirements?

A. Operational excellence
B. Security
C. Reliability
D. Cost optimization 

**Correct Answer: D**

### Question #55

* A company wants to launch its workload on AWS and requires the system to automatically recover from failure.
Which pillar of the AWS Well-Architected Framework includes this requirement?


A. Cost optimization

B. Operational excellence

C. Performance efficiency

D. Reliability 

**Correct Answer: D**

### Question #56

* A large enterprise with multiple VPCs in several AWS Regions around the world needs to connect and centrally manage network connectivity between its VPCs.
Which AWS service or feature meets these requirements?


A. AWS Direct Connect

B. AWS Transit Gateway

C. AWS Site-to-Site VPN

D. VPC endpoints

**Correct Answer: B**

### Question #57

* Which AWS service supports the creation of visual reports from AWS Cost and Usage Report data?

A. Amazon Athena

B. Amazon QuickSight

C. Amazon CloudWatch

D. AWS Organizations

**Correct ExamTopics Answer: A**

**Correct Community Answer: B**

Explanation: **The answer is B** Quicksight for sure. https://aws.amazon.com/premiumsupport/knowledge-center/quicksight-cost-usage-report/ | Keyword here is visual report. Enabling Athena allows you to query the data not visualize it. 

Quicksight ~ MS PowerBI / Tableau. Answer is Quicksight. Athena can also read from the S3 bucket in which CUR data is stored but there is no report visulalization capability in Athena. You can create a simple tabular report in Athena. - https://docs.aws.amazon.com/cur/latest/userguide/cur-query-athena.html

"For Enable report data integration for, select whether you want to enable your Cost and Usage Reports to integrate with Amazon Athena, Amazon Redshift, or Amazon QuickSight. The report is compressed in the following formats:
- Athena: parquet format
- Amazon Redshift or Amazon QuickSight: .gz compression"

https://docs.aws.amazon.com/cur/latest/userguide/cur-create.html


### Question #58

* Which AWS service should be used to monitor Amazon EC2 instances for CPU and network utilization?


A. Amazon Inspector

B. AWS CloudTrail

C. Amazon CloudWatch

D. AWS Config

**Correct Answer: C**

### Question #59

* A company is preparing to launch a new web store that is expected to receive high traffic for an upcoming event. The web store runs only on AWS, and the company has an AWS Enterprise Support plan.
Which AWS resource will provide guidance about how the company should scale its architecture and operational support during the event?


A. AWS Abuse team

B. The designated AWS technical account manager (TAM)

C. AWS infrastructure event management

D. AWS Professional Services

**Correct Examtopic Answer: B**

**Correct Community Answer: C**

* Explanation: Its an ***event*** as the documentation states: https://aws.amazon.com/premiumsupport/programs/iem/ | AWS Infrastructure Event Management (IEM) offers architecture and scaling guidance and operational support during the preparation and execution of planned events, such as shopping holidays, product launches, and migrations. For these events, AWS Infrastructure Event Management will help you assess operational readiness, identify and mitigate risks, and execute your event confidently with AWS experts by your side. The program is included in the Enterprise Support plan and is available to Business Support customers for an additional fee.

The correct answer should be C. 

Altough: As per the https://aws.amazon.com/premiumsupport/plans/enterprise/. Enterprise support plan is having AWS IEM covered under TAM.

And a Technical Account Manager (TAM) is your designated technical point of contact who helps you onboard, provides advocacy and guidance to help plan and build solutions using best practices, coordinates access to subject matter experts, assists with case management, presents insights and recommendations on your AWS spend, workload optimization, and event management, and proactively keeps your AWS environment healthy. Here it is mentioned TAM helps you in event management as well so if you have Enterprise support. So it's a weird one. **Majority of the Community goes with C**

### Question #60

* A user wants to deploy a service to the AWS Cloud by using infrastructure-as-code (IaC) principles.
Which AWS service can be used to meet this requirement?


A. AWS Systems Manager

B. AWS CloudFormation

C. AWS CodeCommit

D. AWS Config

**Correct Answer: B**

### Question #61

* A company that has multiple business units wants to centrally manage and govern its AWS Cloud environments. The company wants to automate the creation of
AWS accounts, apply service control policies (SCPs), and simplify billing processes.
Which AWS service or tool should the company use to meet these requirements?


A. AWS Organizations

B. Cost Explorer

C. AWS Budgets

D. AWS Trusted Advisor

**Correct Answer: A**

### Question #62

* Which IT controls do AWS and the customer share, according to the AWS shared responsibility model? (Choose two.)


A. Physical and environmental controls

B. Patch management

C. Cloud awareness and training

D. Zone security

E. Application data encryption

**Correct Answer: B, C**

### Question #63

* A company is launching an application in the AWS Cloud. The application will use Amazon S3 storage. A large team of researchers will have shared access to the data. The company must be able to recover data that is accidentally overwritten or deleted.
Which S3 feature should the company turn on to meet this requirement?


A. Server access logging

B. S3 Versioning

C. S3 Lifecycle rules

D. Encryption in transit and at rest

**Correct Answer: B**


### Question #64

* A manufacturing company has a critical application that runs at a remote site that has a slow internet connection. The company wants to migrate the workload to
AWS. The application is sensitive to latency and interruptions in connectivity. The company wants a solution that can host this application with minimum latency.
Which AWS service or feature should the company use to meet these requirements?


A. Availability Zones

B. AWS Local Zones

C. AWS Wavelength

D. AWS Outposts 

**Correct Examtopic and 51% of Community Answer: B**

**Correct 49% of Community Answer: D**

* Explanation: AWS Outposts is designed for workloads that need to remain on-premises due to latency requirements, where customers want that workload to run seamlessly with the rest of their other workloads in AWS. 

AWS Local Zones are a new type of AWS infrastructure designed to run workloads that require single-digit millisecond latency, like video rendering and graphics intensive, virtual desktop applications. Not every customer wants to operate their own on-premises data center, while others may be interested in getting rid of their local data center entirely. Local Zones allow customers to gain all the benefits of having compute and storage resources closer to end-users, without the need to own and operate their own data center infrastructure.

(D) AWS Outposts could be the best fit here. Since the client is migrating only the workloads on AWS while (B) AWS Local Zone wants to get rid of hosting its on-prem data center.

But although outposts would mostly solve it, the text states: "A manufacturing company has a critical application that runs at a remote site that has a slow internet connection". The slow internet connection is the problem, doing Outpost won't fix this. Local Zone will. Since both Outposts and Local Zones fit a customer’s use case and requirements, then Local Zones will be the preferred choice.

AWS Local Zones are designed to bring the power of AWS to select geographic locations closer to users and customers, providing low-latency access to services. This service allows customers to run compute and storage resources in an on-premises environment, while still using the same APIs and management tools as the rest of their AWS infrastructure. This could be a good solution for a manufacturing company that wants to host a critical application with minimal latency.

**The answer is B** and not D. We use AWS outposts when we want to use local AWS Services in on-premises data centres, but the question here specifically mentions that they want to migrate their workload into the cloud. Therefore, we can AWS outposts to place your resources closer to end users.


### Question #65

* A company wants to migrate its applications from its on-premises data center to a VPC in the AWS Cloud. These applications will need to access on-premises resources.
Which actions will meet these requirements? (Choose two.)


A. Use AWS Service Catalog to identify a list of on-premises resources that can be migrated.

B. Create a VPN connection between an on-premises device and a virtual private gateway in the VPC.

C. Use an Amazon CloudFront distribution and configure it to accelerate content delivery close to the on-premises resources.

D. Set up an AWS Direct Connect connection between the on-premises data center and AWS.

E. Use Amazon CloudFront to restrict access to static web content provided through the on-premises web servers.

**Correct Examtopics Answer: A, D**

**Correct Examtopics Answer: B, D**

Explanation: **It has to be B and D** because: https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-direct-connect-vpn.html

Can't be A: Regarding Service Catalog (SC), 'This helps you achieve consistent governance and meet your compliance requirements, while enabling users to quickly deploy only the approved IT services they need (link below).' The question never said anything about requiring the services SC provides. The customer may benefit from SC but it's not needed to meet their requirements. https://aws.amazon.com/servicecatalog/?aws-service-catalog.sort-by=item.additionalFields.createdDate&aws-service-catalog.sort-order=desc


### Question #66

* A company wants to use the AWS Cloud to provide secure access to desktop applications that are running in a fully managed environment.
Which AWS service should the company use to meet this requirement?


A. Amazon S3

B. Amazon AppStream 2.0

C. AWS AppSync

D. AWS Outposts

**Correct Examtopics Answer: A** (doesn't make any sense)

**Correct Community Answer: B**

* Explanation: **Answer has to be B.** AppStream 2.0 is a fully managed application streaming service that provides users instant access to their desktop applications from anywhere. https://aws.amazon.com/pm/appstream2/?trk=11ff099d-a664-4cc9-bb3f-ef7173e10b69&sc_channel=ps&s_kwcid=AL!4422!3!593877466233!e!!g!!aws%20appstream&ef_id=Cj0KCQjwk5ibBhDqARIsACzmgLQeX468vkRfgjdpLagjFH7clBYYketIOiDbBWGSVGCmsvdX_U2Urj4aArQBEALw_wcB:G:s&s_kwcid=AL!4422!3!593877466233!e!!g!!aws%20appstream

Secure, reliable, and scalable access to applications and non-persistent desktops from any location

* ***Note:*** Appstream is not listed on the exam guide. I see a lot of questions that are using services that are not on the exam guide. Are they even relevant? 
I guess they want to see if you know the rest of answers (that they actually are in the exam guide) are not valid options. It has no sense, I would write a note in the comment section of the question if this is asked.

### Question #67

* A company wants to implement threat detection on its AWS infrastructure. However, the company does not want to deploy additional software.
Which AWS service should the company use to meet these requirements?


A. Amazon VPC

B. Amazon EC2

C. Amazon GuardDuty

D. AWS Direct Connect

**Correct Answer: C**

### Question #68

* Which AWS service uses edge locations?


A. Amazon Aurora

B. AWS Global Accelerator

C. Amazon Connect

D. AWS Outposts

**Correct Answer: B**

* Explanation: https://aws.amazon.com/global-accelerator/ 

### Question #69

* A company needs to install an application in a Docker container.
Which AWS service eliminates the need to provision and manage the container hosts?


A. AWS Fargate

B. Amazon FSx for Windows File Server

C. Amazon Elastic Container Service (Amazon ECS)

D. Amazon EC2

**Correct Examtopic Answer: C** <- this would be correct if you didn't need to have the instances running to host the containers.

**Correct Community Answer: A** <- Fargate eliminates the need to provision and manage the container hosts. 

* Explanation:  **Answer must be A**

https://aws.amazon.com/ecs/
Optimize your time with AWS Fargate serverless compute for containers, which eliminates the need to configure and manage control plane, nodes, and instances.

https://aws.amazon.com/fargate/
Deploy and manage your applications, not infrastructure. Fargate removes the operational overhead of scaling, patching, securing, and managing servers.

It eliminates the need to provision and MANAGE the container hosts.
ECS is a container orchestration service that allows you to run, stop, and MANAGE Docker containers on a cluster of EC2 instances


### Question #70

* Which AWS service or feature checks access policies and offers actionable recommendations to help users set secure and functional policies?


A. AWS Systems Manager

B. AWS IAM Access Analyzer

C. AWS Trusted Advisor

D. Amazon GuardDuty

**Correct Answer: B**

---
sectionid: introduction
sectionclass: h1
title: Course Overview
number: 1000
---
Course overview

Welcome to the AWS Sysops Administrator Assossiate Question Page - For the exam code SOA-C02.

# Exam Essentials

## AWS Fundamentals

### Know how to create an AWS account and secure the root user. 
The exam validates your ability to implement
security controls to meet compliance requirements.
Understanding how to operate the IAM service and
securing the AWS root account user are essential practices
for this exam objective. This includes setting robust
password policies, enabling MFA for users, and managing
policies.

### Understand how to use the AWS Management Console and CLI. 
Another important skill validated by the exam is
performing operations by using the AWS Management
Console and the AWS CLI. Experiment with the AWS CLI
and observe the results using the management console. It
will provide you with visibility and familiarity with basic
commands, options, and parsing results. Keep in mind that
the exam may have one or more exam lab components
where a scenario made of a set of tasks to perform will be
requested. You may be expected to perform the tasks using
the AWS Management Console or AWS CLI.

### Be familiar with the AWS Personal Health Dashboard. 
Identifying, classifying, and remediatingincidents is an essential part of your role as a SysOps
administrator. Understand how to obtain and respond to
AWS service degradation, scheduled changes, or resourceimpacting issues by leveraging the AWS Health API and the
AWS Personal Health Dashboard.

### Understand the AWS global infrastructure and all components. 
Implementing high availability and resilient environments will demand that you differentiate between
the use of a single availability zone and multi-AZ
deployments for a variety of services. Understanding the
AWS global infrastructure and all components is critical for
such implementation types.

### Understand the purpose and function of as many AWS services as possible, starting with those listed in the exam guide. 
The easiest type of questions in the
certification exam are those that challenge you to
remember the name of a service, what the service does,
and under what use case you choose the service as
compared to a different solution. Navigate to the
certification exam guide appendix and make a note of all
the services listed as being in scope. For each of those
services, try to remember what they do, their anatomy, and
how to use them. As of this writing, there are over 65
services and features that might be covered on the exam.
The certification exam guide appendix also shows a list of
out-of-scope services and features. While the exam will
probably not include complex scenarios that will test deep
knowledge of out-of-scope services, it is important that you
at least recognize the name and function of all services
listed even if you are yet to learn how to operate them.

## Account Creation, Security and Compliance

### Know the shared responsibility model. 
The shared responsibility model is fundamental to everything in AWS
security. Understand how the line of responsibility shifts as
you move from unmanaged services like EC2 to managed
services such as RDS or S3.

### Recognize that everything is an API. 
This fact drives IAM policies but also helps explain the role of services like
AWS Organizations and AWS Control Tower and their
ability to provide guardrails and service control policies
based on API actions.

### Remember authentication vs. authorization. 
Recall which services serve which function.

### Know Directory Services use cases. 
There are three
directory services and each has a different use case. You
will be expected to be able to select the best service for a
customer's use case.

### Know IAM policies well. 
Because everything is an API and policies define authorization based on APIs, you will
find policies everywhere. Recognize the different types of policies and where they are used.

### Understand the common tasks in IAM. 
Be prepared to do common tasks in IAM, such as enabling and managing
multifactor authentication, setting the password policy, and
running a credential report. This list is not exhaustive, but
just a reminder not to forget to review the simple and
common tasks of a systems administrator.

## AWS Cost Management

Understand the importance of implementing AWS
cost allocation tags. AWS cost allocation tags provide
extended visibility and reporting across AWS Budgets, Cost
and Usage Reports, and Cost Explorer in customizable tags
such as cost center, project name, or even departmental
identification. This can provide a starting point for cost
optimization automation tasks.

Understand how to export AWS Cost and Usage
Reports. Properly storing and reviewing AWS Cost and
Usage reports provides valuable insight into prior cost
optimization initiatives and AWS cost history. Some
organizations will be required to meet compliance or
regulatory needs and must store AWS Cost and Usage
reports for archival purposes. This process is accomplished
by storing AWS Cost and Usage Reports in an Amazon S3
bucket and disabling the overwrite feature.

Understand how to create AWS Budget notifications
and actions. AWS Budget notifications provide advanced
warning of potential cost overages. This advanced warning
provides an opportunity to automate preventive measures
to avoid costly overages.

Understand how to identify and remediate unused
resources using AWS Cost Explorer. AWS Cost
Explorer can help identify underused or unused services
using custom filters and dimensions. The built-in AWS Cost
Explorer reports allow a breakdown of the top five cost-
accruing AWS Services and analysis of Reserved Instance
utilization.

Understand AWS managed service opportunities to
reduce cost. AWS Managed services provide a simplified
administration and configuration of commonly used
building blocks like containers, databases, and storage.
These managed services can reduce IT administration
overhead and reduce overall administrative costs.

Understand when to use Savings Plans. Savings Plans
are a flexible pricing model used to lower prices of services
utilized under the Compute, EC2 Instance, and SageMaker
Savings Plans. AWS Cost Explorer provides
recommendations for which Savings Plans will realize the
biggest savings.

## Automated Security Services and Compliance

Understand how to review Trusted Advisor security
checks. Trusted Advisor offers several security checks
and guidance for an AWS account. It offers basic security
checks for IAM Use, MFA on Root Account, Security
Groups – Specific Ports Unrestricted, and Amazon S3
Bucket Permissions. Understand that Business and
Enterprise support unlocks additional security checks,
which assist an organization in reporting or automating
security best practices.

Understand Security Hub findings and reports.
Security Hub provides a centralized management and
reporting location for security findings in an AWS account.
Security Hub enables further automation and management
of security findings by integrating with other AWS services
like GuardDuty, Macie, AWS WAF, and Shield. Automation
using EventBridge and Security Hub is important when
creating automated remediation actions based on findings
from any source.

Understand GuardDuty threat detection findings.
GuardDuty provides analysis of threats for any VPC flow
log, DNS log, or CloudTrail network activity. Any threats
identified within a GuardDuty-monitored region is available
as a finding in the GuardDuty console. GuardDuty provides
findings for EC2 resources, S3 resources, and IAM
resources, as well as Kubernetes resources within an
account. You can review findings for GuardDuty in the
GuardDuty console, Security Hub, or the AWS CLI, or by
using API operations.

Be able to review findings in Inspector. Inspector
offers findings for vulnerabilities discovered within your
web applications hosted in the AWS Cloud. Inspector offers
findings for package vulnerability types and network
reachability types. You can review findings using the
Inspector console and dashboard, or in AWS Security Hub,
or by exporting the findings to CSV or JSON format for use
with other applications.

Understand how to implement encryption at rest
using AWS KMS. Key Management Service offers the
creation and management of symmetric and asymmetric
keys to encrypt data stored within AWS at rest. Understand
how AWS KMS keys are rotated, managed, and used with
envelope encryption to securely store data in AWS services
like S3, and how AWS KMS is used to encrypt EBS volumes
to protect data at rest.

Know how to implement encryption in transit using
AWS Certificate Manager. The AWS Certificate
Manager (ACM) service lets you create and manage
certificates to protect data in transit. Understand how ACM
integrates with CloudFront, Elastic Load Balancing, and
when to use private certificates within an infrastructure.
Know how to enforce a data classification scheme
with Macie. The Macie service offers pattern detection
and analysis of data stored in S3 to identify and classify PII.
Know how to review Macie findings and create data
discovery jobs to enforce data classification in S3 buckets.
Understand how to securely store secrets using
Secrets Manager. The Secrets Manager service tightly
integrates with several AWS services. Understand how to
create, store, and rotate secrets for use with RDS,
DocumentDB, and Redshift clusters. Understand which
secrets you can automatically rotate and how to access
secrets using CloudFormation.

Be able to configure AWS network protection services
using AWS Shield. Shield offers DDoS protection for
AWS resources and edge locations. Know how to enable
Shield Advanced and review findings from Shield to
mitigate and reduce DDoS attacks.

Understand how to configure AWS network protection
services using AWS WAF. AWS WAF provides protection
for web applications running in the AWS Cloud.
Understand how to create and apply AWS WAF ACLs, rules,
and rule groups. Know when to use AWS-managed rule
groups and when to create custom rule groups, and how to
review findings and apply remediation using Firewall
Manager for out-of-compliance rule groups.

## Compute

Know what to monitor. Be sure to have basic hands-on
knowledge of all the many monitoring and optimization
tools such as Cost Explorer, Compute Optimizer, and, of
course, CloudWatch. Don't neglect basics like monitoring
tab resources such as EC2 and ELB. For each compute
type, be sure you know what metrics are important. Know
basic versus detailed monitoring.

Know how and when to optimize compute pricing.
Savings plans and Spot instances are very important
mechanisms for reducing and managing cost and
availability. Know the capabilities and limitations of
Compute Optimizer.

Be familiar with EC2 enhanced capabilities. The best
way to learn is to go through the setup screens item by
item. Be sure you can give a short explanation of what each
feature does and when you would use it. Take a look at the
lefthand navigation in the EC2 console. Is there anything
there you aren't fluent in? Click each option and explore.

Get hands-on knowledge. In the console, can you
perform every step in the life cycle of an AMI, EBS, EC2,
and Image Builder?

Know your auto scaling. Auto Scaling has a significant
number of options. Be sure to review these in more depth
and understand which would be appropriate for solving any
given scaling problem.

## Storage, Migration and Transfer

Understand how Amazon FSx uses multiple
availability zones. AWS FSx as a service is a fully
managed AWS service designed to increase fault tolerance
and high availability. You can increase fault tolerance and
high availability with Amazon FSx storage services by
enabling cross-region replication or by extending the
storage services using a hybrid architecture approach.

Understand how to use AWS DataSync in
migrations. AWS DataSync provides an automated
option for keeping migration data updated until the
application migration date. Once the application is ready to
move fully into AWS, the data has already been
synchronously updated and ready for migration completion.
You can also use AWS DataSync as a migration tool to
transfer large datasets during off-peak business hours to
reduce network bandwidth.

Understand how to implement AWS Backup for cloud-
native backup management. AWS Backup provides a
centralized and automated method for managing backups
across supported AWS services. You can create and
maintain backups centrally using backup and restoration
plans. You can use on-demand backups for resources as
needed to augment scheduled frequency backups in backup
plans. AWS Backup integration with AWS Organizations
allows full management across all AWS accounts in an AWS
Organization.

Understand how to implement Amazon Data Lifecycle
Manager. Amazon Data Lifecycle Manager provides
automated EBS Snapshot and EBS-backed AMI creation
and management within an AWS account. Amazon Data
Lifecycle Manager creates EBS Snapshots using snapshot
Lifecycle policies to automate protection of individual EBS
volumes or all EBS volumes attached to an EC2 instance.
Amazon Data Lifecycle Manager supports cross-account
copy event policies to automate snapshot copies across
accounts. Policy schedules handle the frequency of EBS
Snapshots, fast snapshot restore settings, and cross-region
copy rules.

Understand use cases for enabling Amazon S3 cross-
region replication. Amazon S3 cross-region replication
increases the fault tolerance of application data stored in
Amazon S3 buckets. This feature is also useful in creating
backup and disaster recovery options for application data
between regions, overall increasing data fault tolerance
and in some cases application fault tolerance.

Understand how to implement Amazon S3 Lifecycle
rules. You can use Amazon S3 Lifecycle rules to move
data between storage classes. Lifecycle rules can assist in
reducing storage costs by moving data between Amazon S3
Standard storage class into other longer-term storage
classes like Amazon S3 Glacier Flexible Retrieval tier or
Amazon S3 Deep Archive tier. You can configure Lifecycle
rules to move data based on the needs of your organization
and the retention needs using Amazon S3 Deep Archive and
Amazon S3 Glacier storage tiers.

Understand use cases for Amazon S3 Glacier storage
classes. You can use Amazon S3 Glacier storage classes
for longer-term cold storage of data that does not require
frequent access. Financial services, healthcare, and
organizations required to maintain data for extended
periods of time can benefit from the cost savings of Amazon
S3 Glacier storage classes. Depending on the frequency of
retrieval, each Amazon S3 Glacier Storage class offers
different recovery times and associated costs when
retrieving data from the service. When designing a backup
and recovery plan, take into consideration the potential
duration of recovery that can impact recovery time
objectives (RTOs).

Understand how to configure Amazon S3 static web
hosting. Amazon S3 static web hosting enables a cost-
effective solution to provide static web content, web
redirects, or simple web solutions to expand business
capabilities. Organizations often configure Amazon S3
static web hosting to provide splash pages or scalable
short-term web file sharing. You can also use S3 static web
hosting as a disaster recovery method to supply vital details
or serve as a landing page when an organization is
experiencing issues.

Understand how to monitor Amazon EBS volume
performance. Each Amazon EBS volume type offers
unique performance benefits to applications running on
Amazon EC2. Depending on the needs of the application,
increasing read or write IOPS can drastically improve
performance of an application. Monitoring EBS volume
performance using Amazon CloudWatch is critical when
working with high-performance applications to determine
bottlenecks and potential performance risks, or to ensure
the proper volume types and features are enabled.

Understand how to implement S3 performance
features. Amazon S3 offers several performance features
to enhance upload reliability for network outage sensitive
areas using multipart uploads into Amazon S3 buckets and
to increase transfer speeds to and from Amazon S3 buckets
using Amazon S3 Transfer Acceleration. Multipart uploads
offer significant performance benefits when working with
large datasets by offering improved throughput, the ability
to pause and resume, and quick recovery from any network
issues. Amazon S3 Transfer Acceleration shortens the
distance between client applications and AWS servers by
using the CloudFront Edge locations for Amazon S3 bucket
access. Amazon S3 Transfer Acceleration also maximizes
bandwidth utilization by minimizing the effect of distance
on bandwidth.

## Databases

Know the engines supported by RDS. This may seem
pretty basic, but don't overlook some basic memorization.
Amazon Aurora is one of the engines in RDS. Don't be
confused that Aurora is compatible with PostgreSQL and
MySQL. So, the engines are Oracle, SQL Server, MySQL,
MariaDB, PostgreSQL, IBM DB2, and Amazon Aurora.

Be able to compare Memcached and Redis. Both are
supported caching engines in Amazon ElastiCache, but they
have different features and capabilities. At a basic level,
Memcached is easier to get set up but lacks some of the
more advanced features of Redis. You will want to be able
to compare and contrast the two engines and recognize
when to use each.

Know what can be monitored and where to find the
data. Databases are very resource intensive as well as
business critical. Performance monitoring is an essential
task, and AWS provides a variety of ways to monitor
performance. Of particular importance are Enhanced
Metrics and Performance Insights. However, don't forget
about common tools like CloudWatch, SNS, and
EventBridge.

Have a caching strategy. Given a scenario, be able to
select an appropriate caching strategy. Two of the most
common strategies are lazy loading and write-through.

Understand pricing. Remember that for the exam you
will not need to know exact prices for any services. Instead,
you will need to be able to choose the most cost-effective
solution for a given scenario.

Understand performance and cost. You will almost
always be balancing performance and cost. Pay particular
attention to which the customer in a scenario is most
concerned with.

Understand high availability and disaster recovery.
Be able to differentiate between high availability and
disaster recovery. These concerns overlap significantly, but
there are differences. There are many options for both, so
you will want to be familiar with them and when each
should be used.

## Monitoring, Logging and Remediation

Recognize use cases for which CloudWatch is well
suited. CloudWatch is a monitoring service, and it's going
to be your first line of defense in troubleshooting. You'll
collect and track metrics and set alarms, from simple
metrics such as CPU usage to application-tuned custom
ones that you define.

Recite the core components of a CloudWatch event.
An event in CloudWatch has the event itself, a target, and a
rule. Events indicate changes in your environment, targets
process events, and rules match events and route them to
targets. Get these three concepts straight, and you'll be set
to handle the more conceptual exam questions.

Recognize names of CloudWatch metrics. You will be
asked about default AWS monitoring—CPU, status, disk,
network, but not memory—and about the various metric
names. Although memorizing all of them is tough, you
should review AWS-defined metric names before taking the
exam.

Explain how a CloudWatch alarm works. An alarm is a
construct that watches a metric and is triggered at certain
thresholds. This alarm can then itself trigger actions, such
as an Auto Scaling group scaling out or perhaps a Lambda
function running. You should be able to describe this
process and recognize its usefulness.

List and explain the three CloudWatch alarm states.
An alarm can be in three states: OK, ALARM, and
INSUFFICIENT_DATA. OK means the metric is within the
defined threshold; ALARM means the alarm is “going off”
because the metric is outside or has crossed the defined
threshold. INSUFFICIENT_DATA should be obvious:
There's not enough to report yet.

Create custom metrics for anything above the
hypervisor. It's subtle, but important: CloudWatch knows
nothing about specific tasks that are affecting performance,
because applications all live above the AWS virtualization
layer. This is why CloudWatch doesn't provide a memory
metric that lives above the hypervisor. You can create
custom metrics, but they'll require an agent, and they will
be more limited than metrics that can interact below that
virtualization layer.

Differentiate between CloudWatch, CloudTrail, and
AWS Config. In a nutshell, CloudWatch is for real-time
performance and health monitoring of your environment.
CloudTrail monitors API logs and events within your AWS
environment. AWS Config monitors the configuration of
your environment. All three provide compliance, auditing,
and security.

Describe the two types of trails: cross-region and
single-region. A cross-region trail functions in all regions
of your account. All logs are then placed in a single S3
bucket. A single-region trail applies to one region only and
can place logs in any S3 bucket, regardless of that bucket's
region.

Explain how cross-region trails automatically function
in new regions. A cross-region trail will automatically
begin capturing activity in any new region that is stood up
in an environment without any user intervention. Logs for
new activity are placed in the same S3 bucket as logs for
existing regions and aggregated in seamlessly.

Describe the best practices for acting on and
reviewing CloudTrail logs. It is not enough to simply
turn on CloudTrail and create a few trails. You should set
up CloudWatch alarms related to those trails and
potentially send events out via SNS. You should also be
continually reviewing logs via a CloudWatch (not
CloudTrail!) dashboard that has alarms connected to your
CloudTrail logs in S3. Further, you may want to consider
using a tool like Amazon Athena for deeper analysis of
large log file stores.

Explain the use of AWS Config in monitoring,
especially as compared to CloudWatch and
CloudTrail. CloudWatch monitors the status of running
applications. CloudTrail logs and provides audit trails,
especially for API calls. AWS Config is distinct from both of
these as it is concerned with the configuration of resources,
rather than their runtime state. Anything that affects the
setup of a resource and its interaction with other AWS
resources is largely under this umbrella.

List the benefits of AWS Config. AWS Config provides
centralized configuration management without requiring
third-party tools. It also provides configuration audit trails,
a sort of configuration equivalent to the API audit trails
provided by CloudTrail. And through both of these AWS
Config adds a layer of security and compliance to your
application by ensuring changes to your environments are
always surfaced and evaluated.

Explain AWS Config rules. A rule simply states that a
certain configuration—or more often, a certain part of a
configuration—should be within a set of values. That rule is
broken when a change moves configuration outside of
allowed thresholds for those values.

Explain how AWS Config rules are evaluated. There is
typically code associated with a rule defining how that rule
is evaluated. If you define a custom rule, you'll write your
own code to evaluate configuration and report back as to
whether the configuration follows or breaks the custom
rule. This code is then attached to the rule as a Lambda
function.

Describe the two ways rule evaluation can be
triggered. Two triggers cause AWS Config rules to
evaluate: change-based triggers and periodic triggers. A
change-based trigger causes a rule to evaluate a
configuration when there's a change in the environment. A
periodic trigger evaluates a configuration at a predefined
frequency.

Explain how AWS Systems Manager is able to help
with operational tasks. AWS Systems Manager provides
tools that allow you to monitor and maintain your
instances, while allowing for the creation of patch baselines
and compliance monitoring.

Explain the use of the various components of AWS
Systems Manager. Know what the various components
of AWS Systems Manager do. The Run command allows you
to execute command documents against AWS resources.
Patch Manager allows you to automate the installation of
security patches and application updates. The Parameter
Store creates a central location to store secrets and other
parameters like license keys. Session Manager allows you
to remotely administer your systems without opening up
ports in your security groups. State Manager helps you
monitor the compliance of your systems in regard to
versioning and proving that baseline software is installed.

## Networking 

Calculate CIDR. The exam will not expect you to do math
in your head, so you will not need to calculate arbitrary
CIDR ranges. However, you will want to be able to
recognize large versus small ranges. For example,
10.0.0.0/16 is the largest available range with 65,536 IP
addresses. 10.0.0.0/28 is the smallest with 16 IP addresses.
Five IP addresses are always reserved for AWS use. That
means that the available IP addresses in a /28 CIDR would
be 11.

Practice building a VPC. AWS has published a handy
reference deployment (formerly a QuickStart) at
https://aws.amazon.com/solutions/implementations/vpc. Study
the structure and addresses. Can you set this up manually?

Understand public vs. private IP addresses. All VPC
resources will receive a private IP address. There are three
private IP ranges: 10.0.0.0/8, 172.16.0.0/12,
192.168.0.0/16. Public IP addresses can, optionally, be
assigned to most resources. Know how to create elastic IP
addresses and attach them to an EC2 instance.

Know your gateways and connectivity. VPCs are
designed to be an isolated network environment in the
same way that your on-premises datacenter is an isolated
network. A variety of gateways and endpoints are available.
Be familiar with when to use each. Ask: How would I
connect to S3? How would I connect to my on-premises
network? How would I connect to another VPC?

Understand how to monitor your network. Many
monitoring tools are available in AWS, including
CloudWatch, CloudTrail, and X-Ray. For monitoring
network traffic in the VPC, Traffic Mirroring will be your
best solution. Know how to enable it and what it can
monitor.

Understand network architecture. Studying
architectural diagrams can be very helpful: for example,
see https://aws.amazon.com/architecture/reference-architecture-
diagrams. Make note of the paths and route tables. Note
which services are used in a given scenario.

## Content Delivery

Understand how DNS works. Domain Name Service
(DNS) is used to resolve names to IP addresses, and vice
versa. In a forward lookup, a name is resolved to an IP
address, and in a reverse lookup, an IP address is resolved
to a hostname. Your client will query the local DNS server
for a record. If your local DNS knows the address, it will
respond with it; if it doesn't, it will reach out to the top-
level domain (TLD) DNS servers and work its way down the
chain until it locates the authoritative DNS server and gets
the response for the query.

Know the various DNS record types. Know the main
DNS record types and when you would want to use them.
Know how to use A records, PTR records, CNAME records,
alias records, MX records, and TXT. Alias records are
important to Route 53 and the exam.

Understand what routing policies do. You should know
how to use the routing policies and set them up, including
traffic flows.

Know how health checks work. Remember the different
types of health checks and how they work in relation to
failovers.

Remember how CloudFront works. Know how to
implement a distribution, how to invalidate a cached object,
and what OAI and OAC do.

Know the purpose of AWS Global Accelerator and
when to use it. Know what an accelerator and anycast IP
addresses are.

## Deployment, Provisioning and Automation

Remember that you are responsible for managing
your app. The great thing about Elastic Beanstalk is that
you are responsible for managing your application but that
AWS is responsible for maintaining the underlying services
since Elastic Beanstalk is a managed service. You still need
to ensure that your platform is patched, a task that is made
simpler with managed updates.

Remember the deployment modes for applications.
Deployment modes are a popular line of questioning on the
exam. Remember the differences and use cases between
all-at-once, rolling, rolling with additional batches, and
immutable.

Understand what CloudFormation does.
CloudFormation allows you to build your infrastructure
from a template, which ensures that resources are built the
same way every time. CloudFormation allows you to do
infrastructure-as-a-service (IaaS).

Define the relationship between templates and
stacks. Templates are the definition of your environment,
whereas stacks are instances of the template. This means
that the stack contains all the resources defined in the
template. Stacks are an all-or-nothing deal; if any one
resource fails to be built successfully, then the entire stack
will fail and be rolled back.

Remember what the sections in a CloudFormation
template are used for. You need to remember what the
various sections in the CloudFormation template are used
for. You won't be expected to write your own template on
the exam, but you may be shown samples and asked
questions based on what you are seeing.
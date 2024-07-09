---
sectionid: negron-book
sectionclass: h2
parent-id: Questions
title: Negron AWS Study Guide
number: 2900
---

## AWS Fundamentals

### Review Questions

1. Which of the following injects an additional piece of information into the authentication process?

    A. Defining a secret access ley
    B. Using AWS CloudShell
    C. Implementing MFA
    D. Defining an access key ID

1. C Implementing multifactor authentication (MFA)
injects an additional piece of information into the
authentication process. MFA can be implemented using
software or hardware tools and will add protection to
your root account and users that goes beyond simple
username and password. Use MFA for all accounts and
users if possible.


2. Which of the following are required to implement CLI programmatic access? (Choose two.)

    A. Defining a secret access key
    B. Using SSH Keygen
    C. Implementing MFA
    D. Defining an access key ID

2. A, D Configuring programmatic access for the CLI will
require four pieces of information: access key ID,
secret access key, default region name, and default
output format.

3. Which of the following are best practices for AWS account protection? (Choose three.)
    
    A. Defining an account-level password
    B. Using AWS CloudShell
    C. Implementing MFA for all users
    D. Enabling AWS Security Hub
    E. Using Session Manager for EC2 instances
    F. Using service-linked roles

3. A, C, D Defining an account-level password, enabling
MFA for all users, and enabling AWS Security Hub are
fundamental to protecting your AWS account. Using
CloudShell, Session Manager, and/or service-linked
roles provides a form of security and protection but are
not as fundamental.

4. Which of the following is a best practice for cross–AWS account access?
    
    A. Using AWS Organizations
    B. Using IAM groups
    C. Implementing MFA for all users
    D. Using IAM roles

4. D IAM roles are essential to provide cross-account
access as well as enabling AWS services to interact
with each other. Learn and understand roles and the
mechanics of role policy creation to maintain a strong
security posture.

5. Which of the following saves you from provisioning keys to operate AWS services in a programmatic way?

    A. The AWS Management Console
    B. AWS CloudShell
    C. Session Manager
    D. IAM groups

5. B AWS CloudShell provides a mechanism for operators
to use the AWS CLI without having to provision access
keys in a local machine. This adds a new layer of
security as it saves time and effort in executing one-line
and simple administrative CLI commands.



6. Which of the following saves you from configuring SSH or RDP resources to operate EC2 instances?

    A. The AWS Management Console
    B. AWS CloudShell
    C. Session Manager
    D. IAM groups

6. C Systems Manager Session Manager provides you
with a way to connect to Amazon EC2 instances that
does not require the configuration of SSH or RDP
resources to operate a particular instance. This is a
significantly more secure way to manage EC2
instances.

7. Which of the following represents the URL to log into the AWS Management Console as an IAM user? (Choose two.)

    A. https://aws.amazon.com/console/
    B. https://accountID.signin.aws.amazon.com/console
    C. https://signin.aws.amazon.com/signin
    D. https://signin.aws.amazon.com/signin/console
    E. https://account_alias.signin.aws.amazon.com/console

7. B, E For console access, IAM users need to use the URL
as follows: https://accountID.signin.aws.amazon.com/console
or https://account_alias.signin.aws.amazon.com/console.


8. Which of the following brings AWS services to the edge of a 5G network?

    A. Edge location
    B. Local zone
    C. Outpost
    D. Wavelength zone

8. D Wavelength zones bring AWS services to the edge of
a 5G network, reducing the latency to connect to your
application from a mobile device. Application traffic can
reach application servers running in wavelength zones
without leaving the mobile provider's network. They
provide single-digit millisecond latencies to mobile
devices by reducing the extra network hops that may
be needed without such a resource.

9. Which of the following is an extension of a region where you can run low-latency applications using AWS services?

    A. Edge location
    B. Local zone
    C. Outpost
    D. Wavelength zone

9. B A local zone is an extension of a region where you
can run low-latency applications using AWS services in
proximity to end users. Local zones deliver single-digit
millisecond latencies to users for use cases like media,
entertainment, and real-time gaming, among others.

10. Which of the following bring AWS services, infrastructure, and operating models to your datacenter, co-location space, or physical facility?

    A. Direct Connect location
    B. Local zone
    C. Outpost
    D. Wavelength zone

10. C Outpost is designed to support applications that need
to remain in your datacenter due to low-latency
requirements or local data processing needs. It brings
AWS services, infrastructure, and operating models to
your datacenter, co-location space, or physical facility.

11. Which of the following is the resource used by AWS to deliver reliable and low-latency performance globally?

    A. Region
    B. Local zone
    C. Edge location
    D. Wavelength zone

11. C Edge locations are the resource used by AWS to
deliver reliable and low-latency performance globally.
Edge locations are how AWS attains high performance
in countries and territories where a region does not
exist. The global edge network connects thousands of
Tiers 1, 2, and 3 telecom carriers globally and delivershundreds of terabits of capacity. Edge locations are
connected with regions using the AWS backbone, which
is a fully redundant, multiple 100 Gigabit Ethernet
(GbE) parallel fiber infrastructure. The AWS edge
network consists of over 400 edge locations.


12. Which of the following represents a logical group of AWS datacenters?

    A. Region
    B. Local zone
    C. Edge location
    D. Availability zone

12. D An availability zone is a logical group of datacenters.
These groups are isolated and physically separate.
Each of them includes independent power, cooling,
physical security, and interconnectivity using high
bandwidth and low-latency links. All traffic between
availability zones is encrypted. Also, each availability
zone is implemented separately from other availability
zones but within 60 miles of each other.


13. Which of the following CLI commands will guide you through the process of managing AWS resources?

    A. aws configure wizard
    B. aws configure sso
    C. aws configure import –csv file://path/to/creds.csv
    D. aws configure

13. A The AWS CLIv2 wizards feature is an improved
version of the –cli-auto-prompt command-line option.
Wizards guide you through the process of managing
AWS resources. You can access the wizards feature by
using the command line:
aws <service-name> wizard <wizard-name>

14. Which AWS services have CLI wizards available? (Choose three.)

    A. Amazon EC2
    B. AWS Lambda functions
    C. Amazon DynamoDB
    D. AWS IAM
    E. Amazon RDS
    F. Amazon S3

14. B, C, D Wizards will query existing resources and
prompt you for data in the process of setting up for the
service invoked. As of this writing, wizards are
available for configure, dynamodb, iam, and lambda
functions. For example, the command:
aws dynamodb wizard new-table
will guide you in creating a DynamoDB table. Also, note
that the configure command does not use a wizard
name. It's invoked as aws configure wizard.

15. Which of the following CLI commands creates an S3 bucket?

    A. aws s3 ls s3://my-bucket
    B. aws s3 cp file s3://my-bucket/file
    C. aws s3 ls
    D. aws s3 mb s3://my-bucket

15. D The CLI command to create an Amazon S3 bucket is:
aws s3 mb s3://my-bucket
You can type aws s3 help for details.

16. Which of the following CLI commands copies the content of a local directory to an S3 bucket?

    A. aws s3 cp s3://bucket1/file s3://bucket2/file
    B. aws s3 cp file s3://my-bucket/file
    C. aws s3 sync my-directory s3://my-bucket/
    D. aws s3 mb s3://my-

16. C The CLI command to copy the contents of a directory
to an Amazon S3 bucket is:
aws s3 sync my-directory s3://my-bucket/
You can type aws s3 help for details.
    

17. Which of the following CLI options provide filtering of the output? (Choose two.)

    A. --query
    B. --filter
    C. --search
    D. --dry-run
    E. --cli-auto-prompt

17. A, B The --query option can be used to limit the results
displayed from a CLI command. The query is expected
to be structured according to the JMESPath
specification, which defines the syntax for searching a
JSON document.
The --filter option can also be used to manage the
results displayed. However, with the --filter option,
the output is restricted on the server side whereas --
query filters the results at the client side.
The --dry-run option is used to verify that you have the
required permissions to make the request and gives
you an error if you are not authorized. The --dry-run
option does not make the request.

18. Which of the following support options give you access to the AWS Health API? (Choose two.)

    A. Basic
    B. Developer
    C. Business
    D. Enterprise
    E. AWS IQ

18. C, D The AWS Health API is available directly as part of
an AWS Business Support or AWS Enterprise Support
plan. It allows for chat integration and ingesting events
into Slack, Microsoft Teams, and Amazon Chime. It also
allows integration with dozens of AWS partners such as
DataDog and Splunk, among many others.

19. What is the AWS default quota value for EC2-VPC Elastic IPs?

    A. 50
    B. 5
    C. 5,000
    D. 500

19. B The AWS default quota value for EC2-VPC Elastic IPs
is 5 and will need an adjustment if you need more IPs.
You can use the Service Quotas page on your
management console to make a request to support and
have the limit increased if needed.

20. Which of the following URLs are useful for the purpose of pricing a solution using AWS? (Choose three.)

    A. https://calculator.s3.amazonaws.com
    B. https://aws.amazon.com/free
    C. https://aws.amazon.com/migration-evaluator
    D. https://calculator.aws
    E. https://tco.aws.amazon.com

20. B, C, D For details about service pricing and usage
limits included in the AWS free tier, you can visit
https://aws.amazon.com/free.The logic for AWS TCO calculator now resides in the
Migration Evaluator at https://aws.amazon.com/migrationevaluator.
The AWS Pricing Calculator is available at
https://calculator.aws.
The older, simple monthly calculator and TCO
calculator have been deprecated
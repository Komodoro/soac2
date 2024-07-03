Review Questions
1. What is the primary function of the AWS IAM service?
A. Identity and access management
B. Access key management
C. SSH key pair management
D. Federated access management
2. Which of the following are requirements you can include in an IAM
password policy? (Select THREE.)
A. Require at least one uppercase letter.
B. Require at least one number.
C. Require at least one space or null character.
D. Require at least one nonalphanumeric character.
3. Which of the following should you do to secure your AWS root user?
(Select TWO.)
A. Assign the root user to the “admins” IAM group.
B. Use the root user for day-to-day administration tasks.
C. Enable MFA.
D. Create a strong password.
4. How does multi-factor authentication work?
A. Instead of an access password, users authenticate via a physical
MFA device.
B. In addition to an access password, users also authenticate via a
physical MFA device.
C. Users authenticate using tokens sent to at least two MFA devices.
D. Users authenticate using a password and also either a physical or
virtual MFA device.
5. Which of the following SSH commands will successfully connect to
an EC2 Amazon Linux instance with an IP address of 54.7.35.103
using a key named mykey.pem?
A. echo "mykey.pem ubuntu@54.7.35.103" | ssh -i
B. ssh -i mykey.pem ec2-user@54.7.35.103
C. ssh -i mykey.pem@54.7.35.103
D. ssh ec2-user@mykey.pem:54.7.35.103 -i
6. What’s the most efficient method for managing permissions for
multiple IAM users?
A. Assign users requiring similar permissions to IAM roles.
B. Assign users requiring similar permissions to IAM groups.
C. Assign IAM users permissions common to others with similar
administration responsibilities.
D. Create roles based on IAM policies, and assign them to IAM
users.
7. What is an IAM role?
A. A set of permissions allowing access to specified AWS resources
B. A set of IAM users given permission to access specified AWS
resources
C. Permissions granted a trusted entity over specified AWS
resources
D. Permissions granted an IAM user over specified AWS resources
8. How can federated identities be incorporated into AWS workflows?
(Select TWO.)
A. You can provide users authenticated through a third-party identity
provider access to backend resources used by your mobile app.
B. You can use identities to guide your infrastructure design
decisions.
C. You can use authenticated identities to import external data (like
email records from Gmail) into AWS databases.
D. You can provide admins authenticated through AWS Microsoft
AD with access to a Microsoft SharePoint farm running on AWS.
9. Which of the following are valid third-party federated identity
standards? (Select TWO.)
A. Secure Shell
B. SSO
C. SAML 2.0
D. Active Directory
10. What information does the IAM credential report provide?
A. A record of API requests against your account resources
B. A record of failed password account login attempts
C. The current state of your account security settings
D. The current state of security of your IAM users’ access
credentials
11. What text format does the credential report use?
A. JSON
B. CSV
C. ASCII
D. XML
12. Which of the following IAM policies is the best choice for the admin
user you create in order to replace the root user for day-to-day
administration tasks?
A. AdministratorAccess
B. AmazonS3FullAccess
C. AmazonEC2FullAccess
D. AdminAccess
13. What will you need to provide for a new IAM user you’re creating
who will use “programmatic access” to AWS resources?
A. A password
B. A password and MFA
C. An access key ID
D. An access key ID and secret access key
14. What will IAM users with AWS Management Console access need to
successfully log in?
A. Their username, account_number, and a password
B. Their username and password
C. Their account number and secret access key
D. Their username, password, and secret access key
15. Which of the following will encrypt your data while in transit between
your office and Amazon S3?
A. DynamoDB
B. SSE-S3
C. A client-side master key
D. SSE-KMS
16. Which of the following AWS resources cannot be encrypted using
KMS?
A. Existing AWS Elastic Block Store volumes
B. RDS databases
C. S3 buckets
D. DynamoDB databases
17. What does KMS use to encrypt objects stored on your AWS account?
A. SSH master key
B. KMS master key
C. Client-side master key
D. Customer master key
18. Which of the following standards governs AWS-based applications
processing credit card transactions?
A. SSE-KMS
B. FedRAMP
C. PCI DSS
D. ARPA
19. What is the purpose of the Service Organization Controls (SOC)
reports found on AWS Artifact?
A. They can be used to help you design secure and reliable credit
card transaction applications.
B. They attest to AWS infrastructure compliance with data
accountability standards like Sarbanes–Oxley.
C. They guarantee that all AWS-based applications are, by default,
compliant with Sarbanes–Oxley standards.
D. They’re an official, ongoing risk-assessment profiler for AWSbased deployments.
20. What role can the documents provided by AWS Artifact play in your
application planning? (Select TWO.)
A. They can help you confirm that your deployment infrastructure is
compliant with regulatory standards.
B. They can provide insight into various regulatory and industry
standards that represent best practices.
C. They can provide insight into the networking and storage design
patterns your AWS applications use.
D. They represent AWS infrastructure design policy.

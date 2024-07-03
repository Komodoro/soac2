Review Questions
1. When trying to create an S3 bucket named documents, AWS informs you that the
bucket name is already in use. What should you do in order to create a bucket?
A. Use a different region.
B. Use a globally unique bucket name.
C. Use a different storage class.
D. Use a longer name.
E. Use a shorter name.
2. Which S3 storage classes are most cost-effective for infrequently accessed data
that can’t be easily replaced? (Select TWO.)
A. STANDARD_IA
B. ONEZONE_IA
C. GLACIER
D. STANDARD
E. INTELLIGENT_TIERING
3. What are the major differences between Simple Storage Service (S3) and Elastic
Block Store (EBS)? (Select TWO.)
A. EBS stores volumes.
B. EBS stores snapshots.
C. S3 stores volumes.
D. S3 stores objects.
E. EBS stores objects.
4. Which tasks can S3 object life cycle configurations perform automatically?
(Select THREE.)
A. Deleting old object versions
B. Moving objects to Glacier
C. Deleting old buckets
D. Deleting old objects
E. Moving objects to an EBS volume
5. What methods can be used to grant anonymous access to an object in S3? (Select
TWO.)
A. Bucket policies
B. Access control lists
C. User policies
D. Security groups
6. Your budget-conscious organization has a 5 TB database file it needs to retain offsite for at least 5 years. In the event the organization needs to access the database,
it must be accessible within 8 hours. Which cloud storage option should you
recommend, and why? (Select TWO.)
A. S3 has the most durable storage.
B. S3.
C. S3 Glacier.
D. Glacier is the most cost effective.
E. S3 has the fastest retrieval times.
F. S3 doesn’t support object sizes greater than 4 TB.
7. Which of the following actions can you perform from the S3 Glacier service
console?
A. Delete an archive
B. Create a vault
C. Create an archive
D. Delete a bucket
E. Retrieve an archive
8. Which Glacier retrieval option generally takes 3 to 5 hours to complete?
A. Provisioned
B. Expedited
C. Bulk
D. Standard
9. What’s the minimum size for a Glacier archive?
A. 1 byte
B. 40 TB
C. 5 TB
D. 0 bytes
10. Which types of AWS Storage Gateway let you connect your servers to block
storage using the iSCSI protocol? (Select TWO.)
A. Cached gateway
B. Tape gateway
C. File gateway
D. Volume gateway
11. Where does AWS Storage Gateway primarily store data?
A. Glacier vaults
B. S3 buckets
C. EBS volumes
D. EBS snapshots
12. You need an easy way to transfer files from a server in your data center to S3
without having to install any third-party software. Which of the following services
and storage protocols could you use? (Select FOUR.)
A. AWS Storage Gateway—file gateway
B. iSCSI
C. AWS Snowball
D. SMB
E. AWS Storage Gateway—volume gateway
F. The AWS CLI
13. Which of the following are true regarding the AWS Storage Gateway—volume
gateway configuration? (Select THREE.)
A. Stored volumes asynchronously back up data to S3 as EBS snapshots.
B. Stored volumes can be up to 32 TB in size.
C. Cached volumes locally store only a frequently used subset of data.
D. Cached volumes asynchronously back up data to S3 as EBS snapshots.
E. Cached volumes can be up to 32 TB in size.
14. What’s the most data you can store on a single Snowball device?
A. 42 TB
B. 50 TB
C. 72 TB
D. 80 TB
15. Which of the following are security features of AWS Snowball? (Select TWO.)
A. It enforces encryption at rest.
B. It uses a Trusted Platform Module (TPM) chip.
C. It enforces NFS encryption.
D. It has tamper-resistant network ports.
16. Which of the following might AWS do after receiving a damaged Snowball device
from a customer?
A. Copy the customer’s data to Glacier
B. Replace the Trusted Platform Module (TPM) chip
C. Securely erase the customer’s data from the device
D. Copy the customer’s data to S3
17. Which of the following can you use to transfer data to AWS Snowball from a
Windows machine without writing any code?
A. NFS
B. The Snowball Client
C. iSCSI
D. SMB
E. The S3 SDK Adapter for Snowball
18. How do the AWS Snowball and Snowball Edge devices differ? (Select TWO.)
A. Snowball Edge supports copying files using NFS.
B. Snowball devices can be clustered together for storage.
C. Snowball’s QSFP+ network interface supports speeds up to 40 Gbps.
D. Snowball Edge can run EC2 instances.
19. Which of the following Snowball Edge device options is the best for running
machine learning applications?
A. Compute Optimized
B. Compute Optimized with GPU
C. Storage Optimized
D. Network Optimized
20. Which of the following hardware devices offers a network interface speed that
supports up to 100 Gbps?
A. Snowball Edge with the Storage Optimized configuration
B. Snowball Edge with the Compute Optimized configuration
C. Storage Gateway
D. 80 TB Snowball

1. Which of the following is not one of the pillars of the Well-Architected
Framework?
A. Performance efficiency
B. Reliability
C. Resiliency
D. Security
E. Cost optimization
2. Which of the following are examples of applying the principles of the
security pillar of the Well-Architected Framework? (Select TWO.)
A. Granting each AWS user their own IAM username and password
B. Creating a security group rule to deny access to unused ports
C. Deleting an empty S3 bucket
D. Enabling S3 versioning
3. You’re hosting a web application on two EC2 instances in an Auto
Scaling group. The performance of the application is consistently
acceptable. Which of the following can help maintain or improve
performance efficiency? (Select TWO.)
A. Monitoring for unauthorized access
B. Doubling the number of instances in the Auto Scaling group
C. Implementing policies to prevent the accidental termination of
EC2 instances in the same Auto Scaling group
D. Using CloudFront
4. Which of the following can help achieve cost optimization? (Select
TWO.)
A. Deleting unused S3 objects
B. Deleting empty S3 buckets
C. Deleting unused application load balancers
D. Deleting unused VPCs
5. Which of the following is a key component of operational excellence?
A. Adding more security personnel
B. Automating manual processes
C. Making minor improvements to bad processes
D. Making people work longer hours
6. Your default VPC in the us-west-1 Region has three default subnets.
How many Availability Zones are in this Region?
A. 2
B. 3
C. 4
D. 5
7. Your organization is building a database-backed web application that
will sit behind an application load balancer. You add an inbound
security group rule to allow HTTP traffic on TCP port 80. Where
should you apply this security group to allow users to access the
application?
A. The application load balancer listener
B. The database instance
C. The subnets where the instances reside
D. None of these
8. How does an application load balancer enable reliability?
A. By routing traffic away from failed instances
B. By replacing failed instances
C. By routing traffic to the least busy instances
D. By caching frequently accessed content
9. Which of the following contains the configuration information for
instances in an Auto Scaling group?
A. Launch directive
B. Dynamic scaling policy
C. CloudFormation template
D. Launch template
10. You’ve created a target tracking policy for an Auto Scaling group. You
want to ensure that the number of instances in the group never exceeds
5. How can you accomplish this?
A. Set the group size to 5.
B. Set the maximum group size to 5.
C. Set the minimum group size to 5.
D. Delete the target tracking policy.
11. Which of the following is an example of a static website?
A. A WordPress blog
B. A website hosted on S3
C. A popular social media website
D. A web-based email application
12. Which of the following features of S3 improve the security of data you
store in an S3 bucket? (Select TWO.)
A. Objects in S3 are not public by default.
B. All objects are readable by all AWS users by default.
C. By default, S3 removes ACLs that allow public read access to
objects.
D. S3 removes public objects by default.
13. Which of the following is required to enable S3 static website hosting
on a bucket?
A. Enable bucket hosting in the S3 service console.
B. Disable default encryption.
C. Disable object versioning.
D. Enable object versioning.
E. Make all objects in the bucket public.
14. You’ve created a static website hosted on S3 and given potential
customers the URL that consists of words and numbers. They’re
complaining that it’s too hard to type in. How can you come up with a
friendlier URL?
A. Re-create the bucket using only words in the name.
B. Use a custom domain name.
C. Re-create the bucket in a different Region.
D. Re-create the bucket using only numbers in the name.
15. Which of the following is true regarding static websites hosted in S3?
A. The content served is not encrypted in transit.
B. Anyone can modify the content.
C. You must use a custom domain name.
D. A website hosted on S3 is stored in multiple Regions.
16. Which of the following can impact the reliability of a web application
running on EC2 instances?
A. Taking EBS snapshots of the instances.
B. The user interface is too difficult to use.
C. Not replacing a misconfigured resource that the application
depends on.
D. Provisioning too many instances.
17. You have a public web application running on EC2 instances. Which
of the following factors affecting the performance of your application
might be out of your control?
A. Storage
B. Compute
C. Network
D. Database
18. An Auto Scaling group can use an EC2 system health check to
determine whether an instance is healthy. What other type of health
check can it use?
A. S3
B. SNS
C. VPC
D. ELB
19. You’re hosting a static website on S3. Your web assets are stored under
the Standard storage class. Which of the following is true regarding
your site?
A. Someone may modify the content of your site without
authorization.
B. You’re responsible for S3 charges.
C. You’re charged for any compute power used to host the site.
D. An Availability Zone outage may bring down the site.
20. You’re hosting a static website on S3. Your web assets are stored in the
US East 1 Region in the bucket named mygreatwebsite. What is the
URL of the website?
A. http://mygreatwebsite.s3-website-us-east-1.amazonaws.com
B. http://mygreatwebsite.s3.amazonaws.com
C. http://mygreatwebsite.s3-website-us-east.amazonaws.com
D. http://mygreatwebsite.s3-us-east-1.amazonaws.com

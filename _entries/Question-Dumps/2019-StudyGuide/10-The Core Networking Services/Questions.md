1. Which of the following are true of a default VPC? (Select TWO.)
A. A default VPC spans multiple regions.
B. AWS creates a default VPC in each region.
C. AWS creates a default VPC in each Availability Zone.
D. By default, each default VPC is available to one AWS account.
2. Which of the following is a valid CIDR for a VPC or subnet?
A. 10.0.0.0/28
B. 10.0.0.0/29
C. 10.0.0.0/8
D. 10.0.0.0/15
3. Which of the following are true regarding subnets? (Select TWO.)
A. A VPC must have at least two subnets.
B. A subnet must have a CIDR that’s a subset of the CIDR of the
VPC in which it resides.
C. A subnet spans one Availability Zone.
D. A subnet spans multiple Availability Zones.
4. Which of the following is true of a new security group?
A. It contains an inbound rule denying access from public IP
addresses.
B. It contains an outbound rule denying access to public IP
addresses.
C. It contains an outbound rule allowing access to any IP address.
D. It contains an inbound rule allowing access from any IP address.
E. It contains an inbound rule denying access from any IP address.
5. What’s the difference between a security group and a network access
control list (NACL)? (Select TWO.)
A. A network access control list operates at the instance level.
B. A security group operates at the instance level.
C. A security group operates at the subnet level.
D. A network access control list operates at the subnet level.
6. Which of the following is true of a VPC peering connection?
A. It’s a private connection that connects more than three VPCs.
B. It’s a private connection between two VPCs.
C. It’s a public connection between two VPCs.
D. It’s a virtual private network (VPN) connection between two
VPCs.
7. What are two differences between a virtual private network (VPN)
connection and a Direct Connect connection? (Select TWO.)
A. A Direct Connect connection offers predictable latency because it
doesn’t traverse the internet.
B. A VPN connection uses the internet for transport.
C. A Direct Connect connection uses AES 128- or 256-bit
encryption.
D. A VPN connection requires proprietary hardware.
8. Which of the following are true about registering a domain name with
Route 53? (Select TWO.)
A. The registrar you use to register a domain name determines who
will host DNS for that domain.
B. You can register a domain name for a term of up to 10 years.
C. Route 53 creates a private hosted zone for the domain.
D. Route 53 creates a public hosted zone for the domain.
9. Which of the following Route 53 routing policies can return set of
randomly ordered values?
A. Simple
B. Multivalue Answer
C. Failover
D. Latency
10. Which of the following Route 53 routing policies doesn’t use health
checks?
A. Latency
B. Multivalue Answer
C. Simple
D. Geolocation
11. Which of the following types of Route 53 health checks works by
making a test connection to a TCP port?
A. Simple
B. CloudWatch alarm
C. Endpoint
D. Calculated
12. You have two EC2 instances hosting a web application. You want to
distribute 20 percent of traffic to one instance and 80 percent to the
other. Which of the following Route 53 routing policies should you
use?
A. Weighted
B. Failover
C. Multivalue Answer
D. Simple
13. Resources in a VPC need to be able to resolve internal IP addresses for
other resources in the VPC. No one outside of the VPC should be able
to resolve these addresses. Which of the following Route 53 resources
can help you achieve this?
A. A public hosted zone
B. A private hosted zone
C. Domain name registration
D. Health checks
14. You want to provide private name resolution for two VPCs using the
domain name company.pri. How many private hosted zones do you
need to create?
A. 1
B. 2
C. 3
D. 4
15. On how many continents are CloudFront edge locations distributed?
A. 7
B. 6
C. 5
D. 4
16. From where does CloudFront retrieve content to store for caching?
A. Regions
B. Origins
C. Distributions
D. Edge locations
17. Which CloudFront distribution type requires you to provide a media
player?
A. Streaming
B. RTMP
C. Web
D. Edge
18. You need to deliver content to users in the United States and Canada.
Which of the following edge location options will be the most cost
effective for your CloudFront distribution?
A. United States, Canada, and Europe
B. United States, Canada, Europe, and Asia
C. United States, Canada, Europe, Asia, and Africa
D. All edge locations
19. Approximately how many different CloudFront edge locations are
there?
A. About 50
B. More than 150
C. More than 300
D. More than 500
20. Which of the following are valid origins for a CloudFront distribution?
(Select TWO.)
A. EC2 instance
B. A public S3 bucket
C. A private S3 bucket that you don’t have access to
D. A private S3 bucket that you own

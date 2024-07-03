---
sectionid: Module4Quiz
sectionclass: h3
parent-id: Skillbuilder
title: Module 4 Quiz
number: 14340
---

Module 4 quiz

Test your knowledge of some of the key concepts from this module by answering the questions in this quiz.

After answering each question, review the detailed answer explanations and external links to reinforce your understanding of the concepts.

Your company has an application that uses Amazon EC2 instances to run the customer-facing website and Amazon RDS database instances to store customers’ personal information. How should the developer configure the VPC according to best practices?

Place the Amazon EC2 instances in a private subnet and the Amazon RDS database instances in a public subnet.

Place the Amazon EC2 instances in a public subnet and the Amazon RDS database instances in a private subnet.

Place the Amazon EC2 instances and the Amazon RDS database instances in a public subnet.

Place the Amazon EC2 instances and the Amazon RDS database instances in a private subnet.

Incorrect

The correct response option is Place the Amazon EC2 instances in a public subnet and the Amazon RDS databases instances in a private subnet.

 

A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private.

 

Public subnets contain resources that need to be accessible by the public, such as an online store’s website.

 

Private subnets contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories.


Learn more:

    Amazon VPC
    VPCs and subnets

Which component can be used to establish a private dedicated connection between your company’s data center and AWS?

Private subnet

DNS

AWS Direct Connect

Virtual private gateway

Incorrect

The correct response option is AWS Direct Connect.

 

The other response options are incorrect because:

    A private subnet is a section of a VPC in which you can group resources that should be accessed only through your private network. Although it is private, it is not used for establishing a connection between a data center and AWS.
    DNS stands for Domain Name System, which is a directory used for matching domain names to IP addresses.
    A virtual private gateway enables you to create a VPN connection between your VPC and a private network, such as your company’s data center. Although this connection is private and encrypted, it travels through the public internet, not through a dedicated connection.

Learn more:

    AWS Direct Connect

Which statement best describes security groups?

They are stateful and deny all inbound traffic by default.

They are stateful and allow all inbound traffic by default.

They are stateless and deny all inbound traffic by default.

They are stateless and allow all inbound traffic by default.

Incorrect

The correct response option is Security groups are stateful and deny all inbound traffic by default.


Security groups are stateful. This means that they use previous traffic patterns and flows when evaluating new requests for an instance.


By default, security groups deny all inbound traffic, but you can add custom rules to fit your operational and security needs.


Learn more:

    Security groups for your VPC

Which component is used to connect a VPC to the internet?

Public subnet

Edge location

Security group

Internet gateway

Incorrect

The correct response option is Internet gateway.


 The other response options are incorrect because:

    A public subnet is a section of a VPC that contains public-facing resources.
    An edge location is a site that Amazon CloudFront uses to store cached copies of your content for faster delivery to customers.
    A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.

Learn more:

    Internet gateways

Which service is used to manage the DNS records for domain names?

Amazon Virtual Private Cloud

AWS Direct Connect

Amazon CloudFront

Amazon Route 53
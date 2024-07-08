---
sectionid: ExamTopicsDump
sectionclass: h2
parent-id: Questions
title: ExamTopics
number: 2200
---

### Question 1

*  A company has an internal web application that runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto
Scaling group in a single Availability Zone. A SysOps administrator must make the application highly available.
Which action should the SysOps administrator take to meet this requirement?

    A. Increase the maximum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    
    B. Increase the minimum number of instances in the Auto Scaling group to meet the capacity that is required at peak usage.
    
    C. Update the Auto Scaling group to launch new instances in a second Availability Zone in the same AWS Region.
    
    D. Update the Auto Scaling group to launch new instances in an Availability Zone in a second AWS Region.

**Correct Answer: C**

### Question 2

*  A company hosts a website on multiple Amazon EC2 instances that run in an Auto Scaling group. Users are reporting slow responses during peak times between
6 PM and 11 PM every weekend. A SysOps administrator must implement a solution to improve performance during these peak times.
What is the MOST operationally efficient solution that meets these requirements?

    A. Create a scheduled Amazon EventBridge (Amazon CloudWatch Events) rule to invoke an AWS Lambda function to increase the desired capacity before peak times.
    
    B. Configure a scheduled scaling action with a recurrence option to change the desired capacity before and after peak times.
    
    C. Create a target tracking scaling policy to add more instances when memory utilization is above 70%.
    
    D. Configure the cooldown period for the Auto Scaling group to modify desired capacity before and after peak times.

**Correct Answer: C**
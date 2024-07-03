---
sectionid: M1CC
sectionclass: h2
parent-id: Module1
number: 2200
title: Cloud Computing
---

### Video Transcript
    Before we get deeper into the pieces and parts of AWS, let's zoom out and get a good working definition of cloud. Cloud computing is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing. Let's break this down. On-demand delivery indicates that AWS has the resources you need, when you need them. You don't need to tell us in advance that you're going to need them. Suddenly you find yourself needing 300 virtual servers. Well, just a few clicks and launch them. Or you need 2000 terabytes of storage. You don't have to tell us in advance, just start using the storage you need, when you need it. Don't need them anymore, just as quickly, you can return them and stop paying immediately. That kind of flexibility is just not possible when you're managing your own data centers.


    The idea of IT resources is actually a big part of the AWS philosophy. We often get asked why AWS has so many products and the answer is really simple: Because businesses need them. If there are IT elements that are common across a number of businesses, then this is not a differentiator.


    Take a MySQL database as an example. If your business runs a MySQL database, does your ability to install the MySQL engine make you a better company than your competitors? Well, probably not that. Do you keep backups in a way that makes you superior to other players in your vertical? Again, doubtful. The data inside your database, now that's critically different. The way you build your tables and manage the structures, absolutely separates you from the competition. But the engine is just the engine. 


    At AWS, we call that the *undifferentiated heavy lifting of IT*[^1]. Tasks that are common, often repetitive and ultimately time-consuming; these are the tasks AWS wants to help you with. So you can focus on what makes you unique. Over the internet, seems simple enough, but it implies that you can access those resources using a secure webpage console or programmatically. 


    No additional contracts or sales calls are needed. With pay-as-you-go pricing, we re-emphasize what we pointed out here in the coffee shop. You don't staff a shop with employees 24 hours a day at the same levels you do during peak hours. In fact, some hours, you might not even staff them at all. So why pay for developer environments, for example, on weekends, if your developers aren't working on the weekends?


[^1] https://aatt.io/newsletters/undifferentiated-heavy-lifting-274176
https://github.com/knstvk/mariodavid.github.io/blob/master/_drafts/undifferentiated-heavy-lifting-of-business-apps.md

Undifferentiated heavy lifting, a term coined in the origins of AWS is also applicable for other parts of the IT industry. Creating business applications has a lot of things in common with IT infrastructure.

A few years ago i stumbled upon the term "undifferentiated heavy lifting". As it turns out it was most prominently used by Jeff Bezos and Werner Vogels, C level executives at Amazon. When you look at the origins of the Amazon Web Services offerings, this is basically the core of why they exists.

### Deployment models for cloud computing

When selecting a cloud strategy, a company must consider factors such as required cloud application components, preferred resource management tools, and any legacy IT infrastructure requirements.

The three cloud computing deployment models are cloud-based, on-premises, and hybrid. 

(Select each tab to learn about each category.) See below:
- Cloud-Based Deployment
- On-Premises Deployment
- Hybrid Deployment

#### Cloud-Based Deployment

- Run all parts of the application in the cloud.
- Migrate existing applications to the cloud.
- Design and build new applications in the cloud.

In a cloud-based deployment model, you can migrate existing applications to the cloud, or you can design and build new applications in the cloud. You can build those applications on low-level infrastructure that requires your IT staff to manage them. Alternatively, you can build them using higher-level services that reduce the management, architecting, and scaling requirements of the core infrastructure.

For example, a company might create an application consisting of virtual servers, databases, and networking components that are fully based in the cloud.

#### On-Premises Deployment

- Deploy resources by using virtualization and resource management tools.
- Increase resource utilization by using application management and virtualization technologies.

**On-premises deployment** is also known as a private cloud deployment. In this model, resources are deployed on premises by using virtualization and resource management tools.

For example, you might have applications that run on technology that is fully kept in your on-premises data center. Though this model is much like legacy IT infrastructure, its incorporation of application management and virtualization technologies helps to increase resource utilization.

#### Hybrid Deployment

- Connect cloud-based resources to on-premises infrastructure.
- Integrate cloud-based resources with legacy IT applications.

In a **hybrid deployment**, cloud-based resources are connected to on-premises infrastructure. You might want to use this approach in a number of situations. For example, you have legacy applications that are better maintained on premises, or government regulations require your business to keep certain records on premises.

For example, suppose that a company wants to use cloud services that can automate batch data processing and analytics. However, the company has several legacy applications that are more suitable on premises and will not be migrated to the cloud. With a hybrid deployment, the company would be able to keep the legacy applications on premises while benefiting from the data and analytics services that run in the cloud.

### Benefits of cloud computing

Consider why a company might choose to take a particular cloud computing approach when addressing business needs.

(To learn more, select the + symbol next to each category.) Check below:
- Trade upfront expense for variable expense
- Stop spending money to run and maintain data centers
- Stop guessing capacity
- Benefit from massive economies of scale
- Increase speed and agility
- Go global in minutes

#### Trade upfront expense for variable expense

    Upfront expense refers to data centers, physical servers, and other resources that you would need to invest in before using them. Variable expense means you only pay for computing resources you consume instead of investing heavily in data centers and servers before you know how you’re going to use them.

    By taking a cloud computing approach that offers the benefit of variable expense, companies can implement innovative solutions while saving on costs.

#### Stop spending money to run and maintain data centers

    Computing in data centers often requires you to spend more money and time managing infrastructure and servers. 

    A benefit of cloud computing is the ability to focus less on these tasks and more on your applications and customers.

#### Stop guessing capacity

    With cloud computing, you don’t have to predict how much infrastructure capacity you will need before deploying an application. 

    For example, you can launch Amazon EC2 instances when needed, and pay only for the compute time you use. Instead of paying for unused resources or having to deal with limited capacity, you can access only the capacity that you need. You can also scale in or scale out in response to demand.

#### Benefit from massive economies of scale

    By using cloud computing, you can achieve a lower variable cost than you can get on your own.

    Because usage from hundreds of thousands of customers can aggregate in the cloud, providers, such as AWS, can achieve higher economies of scale. The economy of scale translates into lower pay-as-you-go prices.

#### Increase speed and agility

    The flexibility of cloud computing makes it easier for you to develop and deploy applications.

    This flexibility provides you with more time to experiment and innovate. When computing in data centers, it may take weeks to obtain new resources that you need. By comparison, cloud computing enables you to access new resources within minutes.

#### Go global in minutes

    The global footprint of the AWS Cloud enables you to deploy applications to customers around the world quickly, while providing them with low latency. This means that even if you are located in a different part of the world than your customers, customers are able to access your applications with minimal delays. 

    Later in this course, you will explore the AWS global infrastructure in greater detail. You will examine some of the services that you can use to deliver content to customers around the world.

## Additional resources

To learn more about the concepts that were explored in Module 1, review these resources.

    AWS glossary - https://docs.aws.amazon.com/general/latest/gr/glos-chap.html
    Whitepaper: Overview of Amazon Web Services - https://d0.awsstatic.com/whitepapers/aws-overview.pdf
    AWS Fundamentals: Overview - https://aws.amazon.com/getting-started/fundamentals-overview/
    What is cloud computing? - https://aws.amazon.com/what-is-cloud-computing/
    Types of cloud computing - https://aws.amazon.com/types-of-cloud-computing/
    Cloud computing with AWS - https://aws.amazon.com/what-is-aws/
## Topic 1: AWS Overview
-----------------------------
```
This topic covers
- Overview of AWS
- Benifits of using AWS.
- Example of what you can do with AWS.
- Exploring AWS services.
- Interacting with AWS.
```
### 1. Cloud computing.
-----

###### :dart: What is cloud computing?
Here's a more official definition from the National Institute of Standards and Technology:

>Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers,storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.*
                               :smile: —The NIST Definition of Cloud Computing,
                                 National Institute of Standards and Technology

![](imgs/cloud_computing.png)

###### :dart:Clouds are often divided into the following types:
- `Public`: A cloud managed by an organization and open to use by the general public.
- `Private`: A cloud that virtualizes and shares the IT infrastructure within a single
organization.
- `Hybird`: A mixture of a public and a private cloud.

:dart:Cloud computing services also have several classifications:

- `Infrastructure as a service (IaaS)`: Offers fundamental resources like computing,
storage, and networking capabilities, using virtual servers such as Amazon EC2,
Google Compute Engine, and Microsoft Azure virtual machines.
- `Platform as a service (PaaS)`: Provides platforms to deploy custom applications to
the cloud, such as AWS Elastic Beanstalk, Google App Engine, and Heroku.
- `Software as a service (SaaS)`: Combines infrastructure and software running in
the cloud, including office applications like Amazon WorkSpaces, Google Apps
for Work, and Microsoft Office 365

###### :books: Note:
> - AWS is a public cloud
> - The AWS product portfolio contains IaaS, PaaS, and SaaS. Let’s take a more concrete look at what you can do with AWS. 

![](imgs/cloud_computing_models.png)

### 2. AWS overview.
------

###### :dart:What is AWS?
>Amazon Web Services (AWS) is a secure cloud services platform, offering compute power, database storage, content delivery and other functionality to help businesses scale and grow. Explore how millions of customers are currently leveraging AWS cloud products and solutions to build sophisticated applications with increased flexibility, scalability and reliability.*

###### :dart:History.
![](imgs/amazon_history_timeline.png)

###### :dart:What can we do with AWS?
You can run any application on AWS by using one or a combination of services.The examples in this section will give you an idea of what you can do with AWS.

_**Example:**_  Hosting the web shop.

![](imgs/runing_a_web_shop_on_premises_vs._on_AWS.PNG).

###### :dart:How you can benefit from using AWS?

What’s the most important advantage of using AWS? Cost savings, you might say. But
saving money isn’t the only advantage. Let’s look at other ways you can benefit from
using AWS.

- **_Easy to use_**:
AWS is designed to allow application providers, ISVs, and vendors to quickly and securely host your applications – whether an existing application or a new SaaS-based application. You can use the AWS Management Console or well-documented web services APIs to access AWS’s application hosting platform.

- **_Flexible_**:
AWS enables you to select the operating system, programming language, web application platform, database, and other services you need. With AWS, you receive a virtual environment that lets you load the software and services your application requires. This eases the migration process for existing applications while preserving options for building new solutions.

- **_Cost-Effective_**:
You pay only for the compute power, storage, and other resources you use, with no long-term contracts or up-front commitments. For more information on comparing the costs of other hosting alternatives with AWS, see the AWS Economics Center.

- **_Reliable_**:
With AWS, you take advantage of a scalable, reliable, and secure global computing infrastructure, the virtual backbone of Amazon.com’s multi-billion dollar online business that has been honed for over a decade.

- **_Scalable and high-performance_**:
Using AWS tools, Auto Scaling, and Elastic Load Balancing, your application can scale up or down based on demand. Backed by Amazon’s massive infrastructure, you have access to compute and storage resources when you need them.

- **_Secure._**:
AWS utilizes an end-to-end approach to secure and harden our infrastructure, including physical, operational, and software measures. For more information, see the AWS Security Center.

###### :dart:How much does it cost?

- **_Free Tier_**: 

You can use some AWS services for free during the first 12 months after you sign up.
The idea behind the Free Tier is to enable you to experiment with AWS and get some
experience. Here is what’s included in the Free Tier:   

      ■ 750 hours (roughly a month) of a small virtual server running Linux or Windows. This means you can run one virtual server the whole month or you can run 750 virtual servers for one hour.
    
      ■ 750 hours (or roughly a month) of a load balancer.      
    
      ■ Object store with 5 GB of storage.
      
      ■ Small database with 20 GB of storage, including backup.

- **_Billing example_**: 

As mentioned earlier, you can be billed in several ways:

      ■ Based on hours of usage—If you use a server for 61 minutes, that’s usually counted as 2 hours.
      
      ■ Based on traffic—Traffic can be measured in gigabytes or in number of requests.
      
      ■ Based on storage usage—Usage can be either provisioned capacity (for example, 50 GB volume no matter how much you use) or real usage (such as 2.3 GB used).

- **_Pay-per-use opportunities_**: 

###### :dart:Comparing alternatives.

- Following are some common features of cloud providers:
  - Virtual servers (Linux and Windows)
  - Object store
  -  Load balancer
  -  Message queuing
  - Graphical user interface
  - Command-line interface

- Differences between AWS, Microsoft Azure, Google Cloud Platform, and OpenStack AWS Azure, Google Cloud.

![](imgs/difference_aws_azure_google_cloud_and_openstack.PNG)

![](imgs/difference_aws_azure_google_cloud_and_openstack_2.PNG)

###### :dart: Exploring AWS services.

```
- Analytics**: help make sense of big data
- Application Integration
- AR and VR
- AWS Cost Management
- Blockchain
- Business Applications
- Compute Services
- Customer Engagement
- Database
- Desktop and App Streaming (End User computing)
- Developer Tools
- Game Tech
- Internet of Things (IoT)
- Machine Learning
- Management and Governance
- Media Services
- Migration and Transfer
- Mobile Services
- Networking and Content Delivery
- Robotics
- Satellite
- Security, Identity, and Compliance
- Storage
```

###### :dart:Interacting with AWS.

When you interact with AWS to configure or use services, you make calls to the API. 
Next, we’ll give you an overview of the tools available to make calls to the AWS API.
You can compare the ability of these tools to automate your daily tasks.

![](imgs/interact_with_AWS_API.PNG)

- **_Management console_**: 

![](imgs/management_console.png)

- **_Command line interface_**: 

![](imgs/command_line.png)

- **_SDKs_**: 

Sometimes you need to call AWS from within your application. With SDKs, you can use
your favorite programming language to integrate AWS into your application logic. AWS
provides SDKs for the following: 

```
- Android
- Node.js (Javascript)
- Browsers(Javascript)
- PHP
- iOS
- Python
- Java
- Ruby
- .NET
- Go
```

SDKs are typically used to integrate AWS services into applications. If you’re doing software development and want to integrate an AWS service like a NoSQL database or a
push-notification service, an SDK is the right choice for the job. Some services, such as
queues and topics, must be used with an SDK in your application. 

- **_Blueprints_**: 

A blueprint is a description of your system containing all services and dependencies. The
blueprint doesn’t say anything about the necessary steps or the order to achieve the
described system. 

![](imgs/blueprints.PNG)

Consider using blueprints if you have to control many or complex environments.
Blueprints will help you to automate the configuration of your infrastructure in the
cloud. You can use blueprints to set up virtual networks and launch different servers
into that network, for example.
A blueprint removes much of the burden from you because you no longer need to
worry about dependencies during system creation—the blueprint automates the
entire process. You’ll learn more about automating your infrastructure in chapter 4.
It’s time to get started creating your AWS account and exploring AWS practice after
all that theory. 

Summary
----------

```
■ Amazon Web Services (AWS) is a platform of web services offering solutions for
computing, storing, and networking that work well together.
■ Cost savings aren’t the only benefit of using AWS. You’ll also profit from an
innovative and fast-growing platform with flexible capacity, fault-tolerant services,
and a worldwide infrastructure.
■ Any use case can be implemented on AWS, whether it’s a widely used web application
or a specialized enterprise application with an advanced networking
setup.
■ You can interact with AWS in many different ways. You can control the different services
by using the web-based GUI; use code to manage AWS programmatically from
the command line or SDKs; or use blueprints to set up, modify, or delete your infrastructure
on AWS.
■ Pay-per-use is the pricing model for AWS services. Computing power, storage,
and networking services are billed similarly to electricity.

```

Resource
--------

[1] [AWS in action](<https://s3-ap-southeast-1.amazonaws.com/tv-prod/documents%2Fnull-Amazon+Web+Services+in+Action.pdf>)

[2]  [AWS overview](<https://docs.aws.amazon.com/aws-technical-content/latest/aws-overview/aws-overview.pdf>)

[3] [AWS document](<https://aws.amazon.com/>)

















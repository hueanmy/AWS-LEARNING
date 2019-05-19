# AWS Overview
## What is the AWS cloud?
 - Data centers distributed Worldwide
 - On-demand delivery of IT resource
 - Shared and dedicated resource
 - Benefits:
   - Economies of scale
   - Accounts isolated at the hypervisor level
   - Pay-as-you-go pricing. When you use it you pay by the hour or the minute or the second and some services even provide billing by the millisecond 
   - No up front cost
   - Reduced maintenance & admin costs
   - Organised into product categories (compute, storage, database, machine learning, etc...)

## The AWS global infrastructure
The AWS global infrastructure is massive and is divided into geographic regions and those geographic regions are divided into separate availability zones
 - Choose a region to optimise latency, minimise costs or address regulatory requirment
 - Each AWS Region has multiple physically isolated Availability Zones. Connected to each other with fast, orivate fiber-optic networking
 - Edge Locations: CloudFront CDN cached content at the edge locations for high performance delivery of content. Also provides DDOS protection.

## AWS Management Console
 - Web-based user interface to AWS
 - Requires an AWS account
 - Monitor costs
 - AWS Console Mobile App

## SDK&CLI Access
 - Software Development Kits
   - Create application that user AWS services
   - SDKs for Javascript, NodeJS, Java, Python, .Net, PHP, Ruby, Go, C++
   - Modile SDKs for Android, iOS, React Native, Unity, Xamarin
   - Application Programming Interface enabled access to AWS using http calls
 - Command Line Interface
   - Control multiple AWS services from the command line and automate them through scripts
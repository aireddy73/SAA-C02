# SAA-C02
AWS Certified Solutions Architect - Associate

SAA-C02 Notes
These are my personal notes from Adrian Cantrill's (SAA-C02) course. Learning Aids from aws-sa-associate-saac02. There may be errors, so please purchase his course to get the original content and show support https://learn.cantrill.io.

Table of Contents 

https://github.com/aireddy73/SAA-C02#Cloud-Computing-Fundamentals

Cloud-Computing-Fundamentals
AWS-Fundamentals
IAM-Accounts-AWS-Organizations
Simple-Storage-Service-S3
Virtual-Private-Cloud-VPC
Elastic-Cloud-Compute-EC2
Containers-and-ECS
Advanced-EC2
Route-53
Relational-Database-Service-RDS
Network-Storage-EFS
HA-and-Scaling
Serverless-and-App-Services
CDN-and-Optimization
Advanced-VPC
Hybrid-and-Migration
Security-Deployment-Operations
NoSQL-and-DynamoDB

Cloud-Computing-Fundamentals

Cloud computing provides

On-Demand Self-Service: Provision and terminate using a UI/CLI without human interaction.
Broad Network Access: Access services over any networks on any devices using standard protocols and methods.
Resource Pooling: Economies of scale, cheaper service.
Rapid Elasticity: Scale up and down automatically in response to system load.
Measured Service: Usage is measured. Pay only for what you consume.
Public vs Private vs Multi Cloud
Public Cloud: using 1 public cloud such as AWS, Azure, Google Cloud.
Private Cloud: using on-premises real cloud. Must meet 5 requirements.
Multi-Cloud: using more than 1 public cloud in one deployment.
Hybrid Cloud: using public and private clouds in one environment
This is NOT using Public Cloud and Legacy on-premises hardware.
Cloud Service Models
The Infrastructure Stack or Application Stack contains multiple components that make up the total service. There are parts that you manage as well as portions the vendor manages. The portions the vendor manages and you are charged for is the unit of consumption

On-Premises: The individual manages all components from data to facilities. Provides the most flexibility, but also most IT intensive.
Data Center Hosting: Place equipment in a building managed by a vendor. You pay for the facilities only.
Infrastructure as a Service (IaaS): Vendor manages facilities and everything else related to servers up to the OS. You pay per second or minute for the OS used to the vendor. Lose some flexibility, but big risk reductions.
Platform as a Service (PaaS): Good for running an application only. The unit of consumption is the runtime environment. You manage the application and the data, but the vendor manges all else.
Software as a Service (SaaS): You consume the software as a service. This can be Outlook or Netflix. There are almost no risks or additional costs, but very little control.
There are additional services such as Function as a Service, Container as a Service, and DataBase as a Service which be explained later.


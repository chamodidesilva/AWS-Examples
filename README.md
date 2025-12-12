<div align="center">
<h3 align="center">AWS Sandbox</h3>
  <p>AWS hands-On lab repository for cloud architecture practice</p>
</div>

## About The Project

This is a project created for practicing hands-on AWS cloud architecture provisioning using AWS CLI and IaC. This project is used for the practical learning alongside an AWS Solutions Architect Associate certification preparation course and covers some core services mentioned below in detail.\
Each service has its own dedicated folder containing reference commands, explanations, and supporting documentation. Some operations are also explored using the AWS SDK for Ruby.

## Covered Services

<div align="left">
  <img src="https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist/NetworkingContentDelivery/VirtualPrivateCloud.png" height="40" alt="VPC" />&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/icacho-dev/aws-architecture-icons/main/Architecture-Service-Icons_02072025/Arch_Compute/48/Arch_Amazon-EC2_48.svg" height="40" alt="EC2" />&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist/Storage/SimpleStorageService.png" height="40" alt="S3" />&nbsp;&nbsp;&nbsp;
  <img height="40" alt="image" src="https://github.com/user-attachments/assets/68499ba5-3449-4a76-b9f3-65a0c5abb455" />&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist/Compute/Lambda.png" height="40" alt="Lambda" />&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist/Database/DynamoDB.png" height="40" alt="DynamoDB" />&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/main/dist/Database/ElastiCache.png" height="40" alt="ElastiCache" />
</div>
<br>

* **VPC**
  
Covered basic operations via AWS CLI like creating, deleting, updating VPC components like subnets, route tables, NACLs and internet gateways. Used CloudFormation templates to set up a VPC with basic operations. 

* **EC2**

Setup EC2 instances via CLoudFormation for testing VPC behaviour on a resource and for connecting to the Redis cache. Provisioned the instances with an IAM role and inserted user data at the creation to run an Apache server.

* **S3**

Experimented with IaC tools: CloudFormation, CDK and Terraform with basic S3 operations. 
Basic bucekt operations: creating, updating, deleting, listing buckets, listing and uploading and downloading objects, creating and updating ACLs, bucket policies, changing storage class on objects, uploading objects with checksums, experimented with CORS on a static website and server side encryption with SSE-KMS and SSE-C, using etags, uploading objects with metadata, working with prefixes.

* **IAM**

Experimented with creating, attaching and updating policies to IAM identities.

* **Lambda**

Used SAM CLI to build and deploy a function as a containerized image.

* **DynamoDB**

Used CloudFormation to provision a simple table and use SAM CLI to insert items.

* **ElastiCache**

Created a Redis serverless cache and used Redis client to connect to the cache and used an EC2 instance to connect to the cache. 

* **STS**

Used STS to gain temporary access to users.

## Acknowledgements

This project is created to follow the [AWS SAA certification exam course](https://www.youtube.com/watch?v=c3Cn4xYfxJY) conducted by [Andrew Brown](https://github.com/omenking).

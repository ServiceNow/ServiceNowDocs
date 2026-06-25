---
title: Amazon Web Services \(AWS\) shapes
description: The AWS shapes library in EA Workspace helps in modeling cloud architectures. These shapes allow architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-aws-shapes.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Shapes to create a modeling diagram, Exploring Enterprise Modeling and Visualization in the EA Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Amazon Web Services \(AWS\) shapes

The AWS shapes library in EA Workspace helps in modeling cloud architectures. These shapes allow architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.

## AWS shapes in Enterprise Modeling and Visualization

You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes**

You can also adjust the size of shapes by selecting a shape and then drag any of its edges or corner handles. Pulling outward increases the shape's dimensions, while dragging inward reduces its size.

**Note:** Connector ports on AWS shapes, including AWS Group shapes, are bi-directional. You can use any connector port—top, bottom, left, or right—as either an input or an output when connecting shapes in a diagram.

|Shape name|Description|
|----------|-----------|
|AWS Account \[Omitted image "modeling-aws-account.png"\] Alt text: AWS account|Represents a single AWS account, which acts as an isolated container for resources, billing, and security policies. Use this shape to group all resources belonging to one account, especially in multi-account architectures.|
|Availability Zone \[Omitted image "modeling-aws-availability-zone.png"\] Alt text: Availability zone|A physically separate data center within an AWS Region, designed for fault isolation. Place inside a Region shape to show redundancy and high availability.|
|Private Subnet \[Omitted image "modeling-aws-private-subnet.png"\] Alt text: Private subnet|A subnet within a VPC that does not have direct internet access. Used for backend services or databases. Nest inside a VPC shape and indicate routing through NAT Gateway for outbound traffic.|
|Amazon Virtual Private Cloud \[Omitted image "modeling-aws-amazon-virtual-pvt-cld.png"\] Alt text: Amazon virtual private cloud|A logically isolated section of the AWS cloud where you define IP addressing, subnets, and routing. Acts as the primary network boundary. Group subnets, gateways, and security components inside this shape.|
|Security Group \[Omitted image "modeling-aws-security-group.png"\] Alt text: Security group|A virtual firewall that controls inbound and outbound traffic for AWS resources. Attach to EC2 instances or other resources to indicate security controls.|
|Auto Scaling Group \[Omitted image "modeling-aws-autoscaling-group.png"\] Alt text: Auto scaling group|A collection of EC2 instances managed together for scaling based on demand. Represent elasticity and resilience for compute workloads. Often linked to load balancers.|
|EC2 Instance Contents \[Omitted image "modeling-aws-ec2-inst-cont.png"\] Alt text: EC2 instance contents|Represents the internal components or applications running on an EC2 instance. Use this shape to detail what is deployed inside the instance \(for example, web server, app server\).|
|Region \[Omitted image "modeling-aws-region.png"\] Alt text: Region|A geographical area that contains multiple Availability Zones. Acts as the top-level grouping for all resources deployed in a specific location.|

|Shape|Description|
|-----|-----------|
|Kinesis \[Omitted image "modeling-aws-kinesis.png"\] Alt text: Kinesis|A suite of services for real-time data streaming and processing. It enables ingesting, analyzing, and storing streaming data at scale. Use the general Kinesis shape when referring to the overall streaming platform or architecture.|
|Kinesis Data Firehouse \[Omitted image "modeling-aws-kinesis-datafirehouse.png"\] Alt text: Kinesis data firehouse|A fully managed service for delivering real-time streaming data to destinations like Amazon S3, Redshift, OpenSearch Service, and third-party tools. Represented as the delivery pipeline for streaming data.|
|Kinesis Video Streams \[Omitted image "modeling-aws-kinesis-videotreams.png"\] Alt text: Kinesis video streams|A service for securely streaming video from connected devices to AWS for analytics, machine learning, and storage. Shown in IoT or media architectures for video ingestion.|
|Kinesis Data Streams \[Omitted image "modeling-aws-kinesis-datastreams.png"\] Alt text: Kinesis data streams|A core service for ingesting and processing real-time data streams. Represented as the main streaming data source feeding analytics or applications.|
|Opensearch Service \[Omitted image "modeling-aws-opensearch-serv.png"\] Alt text: Opensearch service|A managed service for deploying and operating OpenSearch \(formerly Elasticsearch\) clusters for search and analytics. Shown as the search and indexing layer for logs and structured data.|
|Redshift \[Omitted image "modeling-aws-redshift.png"\] Alt text: Redshift|A fully managed, petabyte-scale data warehouse for analytics and BI workloads. Represented as the central analytics engine for structured data.|

|Shape|Description|
|-----|-----------|
|Task \[Omitted image "modeling-aws-task.png"\] Alt text: Task|Represents a single unit of work in Amazon ECS \(Elastic Container Service\). A task is the instantiation of a task definition, which specifies the container images, CPU/memory requirements, and networking settings. Use this shape to show individual workloads running inside ECS clusters. Tasks can include one or more containers.|
|Amazon Elastic Kubernetes Service \[Omitted image "modeling-aws-elastic-kubermetes-serv.png"\] Alt text: Amazon elastic kubernetes service|A managed Kubernetes service that simplifies running Kubernetes clusters on AWS without managing the control plane. Represented as the orchestration layer for containerized workloads. Often shown with worker nodes, pods, and integrated with IAM, VPC, and EBS for storage.|
|Elastic Container Service \(Amazon ECS\) \[Omitted image "modeling-aws-elastic-cont-serv.png"\] Alt text:|A fully managed container orchestration service for running Docker containers on AWS. Shown as the orchestration layer for ECS clusters, managing tasks and services.|

|Shape|Description|
|-----|-----------|
|Amazon Elastic Compute Cloud \[Omitted image "modeling-aws-elastic-comp-cloud.png"\] Alt text: Amazon elastic compute cloud|Amazon EC2 provides resizable compute capacity in the cloud. It allows you to run virtual servers \(instances\) on-demand, enabling flexible scaling for applications.|
|Lambda Function \[Omitted image "modeling-aws-lambda.png"\] Alt text: Lambda function|AWS Lambda is a serverless compute service that runs code in response to events without provisioning or managing servers. Represented as a function icon, often linked to API Gateway, S3, DynamoDB, or event sources. It’s used in microservices and event-driven architectures.|

|Shape|Description|
|-----|-----------|
|MemoryDB \[Omitted image "modeling-aws-memorydb.png"\] Alt text: MemoryDB|MemoryDB is a fully managed, Redis-compatible, in-memory database service designed for ultra-fast performance and durability. Use this shape to represent caching or real-time data processing layers in applications requiring microsecond latency.|
|Relational Database Service \(Amazon RDS\) \[Omitted image "modeling-aws-rel-db-service.png"\] Alt text: Relational Database Service \(RDS\)|RDS is a managed service for relational databases, supporting engines like MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server. Represents the managed database layer for transactional workloads.|
|Elasticache \[Omitted image "modeling-aws-elasticache.png"\] Alt text: Elasticache|ElastiCache provides managed in-memory caching using Redis or Memcached. Shown as a caching layer between application and database tiers to reduce latency.|
|Keyspaces \(for Apache Cassandra\) \[Omitted image "modeling-aws-keyspaces.png"\] Alt text: Keyspaces \(for Apache Cassandra\)|A scalable, managed database service compatible with Apache Cassandra for wide-column data models. Represents NoSQL workloads requiring high throughput and low latency.|
|DynamoDB \[Omitted image "modeling-aws-dynamodb.png"\] Alt text: DynamoDB|A fully managed NoSQL database service for key-value and document data. Commonly used for serverless applications, microservices, and real-time data access.|
|RDS Instance \[Omitted image "modeling-aws-rds-instance.png"\] Alt text: RDS Instance|Represents an individual database instance within Amazon RDS. Used to show specific database nodes in multi-AZ or read replica configurations.|

|Shape|Description|
|-----|-----------|
|VPN Gateway \[Omitted image "modeling-aws-vpn-gateway.png"\] Alt text: VPM Gateway|A Virtual Private Network \(VPN\) Gateway enables secure connectivity between your AWS Virtual Private Cloud \(VPC\) and on-premises networks over an IPsec VPN tunnel. Place inside the VPC boundary to show hybrid connectivity.|
|API Gateway \[Omitted image "modeling-aws-api-gateway.png"\] Alt text: API Gateway|Amazon API Gateway is a fully managed service for creating, publishing, and securing APIs at scale. Represented as the entry point for REST, HTTP, or WebSocket APIs, often linked to Lambda or backend services.|
|Customer Gateway \[Omitted image "modeling-aws-customer-gateway.png"\] Alt text: Customer Gateway|Represents the on-premises endpoint for a VPN connection to AWS. Shown outside the AWS cloud, connected to VPN Gateway.|
|Route 53 \[Omitted image "modeling-aws-route-53.png"\] Alt text:|AWS Route 53 is a scalable DNS and domain name management service. Typically placed at the edge for routing traffic to AWS resources or external endpoints.|
|Network ACL \[Omitted image "modeling-aws-network-acl.png"\] Alt text: Network ACL|A Network Access Control List provides stateless filtering of inbound and outbound traffic at the subnet level. Attach to subnets inside a VPC to indicate additional security.|
|Internet Gateway \[Omitted image "modeling-aws-internet-gateway.png"\] Alt text: Internet gateway|Enables communication between resources in a VPC and the internet.Shown at the VPC edge for public connectivity|
|VPN Connection \[Omitted image "modeling-aws-vpn-connection.png"\] Alt text: VPN connection|Represents the secure IPsec tunnel between AWS VPN Gateway and Customer Gateway. Connects hybrid environments for secure data transfer.|
|Application Load Balancer \[Omitted image "modeling-aws-app-load-bal.png"\] Alt text: Application load balancer|Distributes HTTP/HTTPS traffic across multiple targets \(EC2, containers, Lambda\). Shown in front of application tiers for high availability.|
|Route Table \[Omitted image "modeling-aws-route-table.png"\] Alt text: Route table|Defines how traffic is directed within a VPC. Attach to subnets to show routing logic.|
|NAT Gateway \[Omitted image "modeling-aws-nat-gateway.png"\] Alt text: Nat gateway|Enables instances in private subnets to access the internet without exposing them publicly. Placed in a public subnet, linked to private subnets via route tables.|
|Elastic Network Interface \[Omitted image "modeling-aws-elast-net-intrfc.png"\] Alt text: Elastic network interface|A virtual network interface that can be attached to an EC2 instance. Represented as a component of EC2 for network connectivity|

|Shape|Description|
|-----|-----------|
|WAF \[Omitted image "modeling-aws-waf.png"\] Alt text: WAF|AWS WAF protects web applications from common exploits and attacks such as SQL injection and cross-site scripting. It enables you to define custom security rules to filter HTTP\(S\) traffic. Represented as a security layer in front of Amazon CloudFront, Application Load Balancer, or API.|
|Certificate Manager \(ACM\) \[Omitted image "modeling-aws-cert-man-acm.png"\] Alt text: Certificate manager \(ACM\)|SACM simplifies the provisioning, management, and deployment of SSL/TLS certificates for AWS services and internal resources. Typically shown alongside Elastic Load Balancers, CloudFront, or API Gateway to indicate encrypted communication.|
|Cognito \[Omitted image "modeling-aws-cognito.png"\] Alt text: Cognito|Cognito provides user authentication, authorization, and user management for web and mobile apps. It supports social identity providers and enterprise federation. Represented as an identity layer for applications, often linked to API Gateway or Lambda.|

|Shape|Description|
|-----|-----------|
|Simple Storage Service \(Amazon S3\) \[Omitted image "modeling-aws-s3.png"\] Alt text: Simple Storage Service \(Amazon S3\)|Amazon S3 is an object storage service designed for storing and retrieving any amount of data from anywhere on the web. It’s highly durable, scalable, and secure. Use this shape to represent object storage buckets in AWS architecture diagrams.|
|Volume \[Omitted image "modeling-aws-volume.png"\] Alt text: Volume|Represents an Amazon Elastic Block Store \(EBS\) volume, which is a block-level storage device that can be attached to EC2 instances. Use this shape to indicate persistent storage for compute resources.|
|Volume Gateway \[Omitted image "modeling-aws-volume-gateway.png"\] Alt text: Volume gateway|Represents the AWS Storage Gateway Volume Gateway, which provides hybrid cloud storage by exposing cloud-backed volumes to on-premises applications. Use this shape to show integration between on-premises environments and AWS storage.|

**Parent Topic:**[Shapes to create a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-shapes.md)

**Related topics**  


[AWS shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-modeling-aws.md)

[Working with Amazon Web Services \(AWS\) shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-aws-shapes.md)

[Create a diagram using AWS shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-create-diagram-aws.md)


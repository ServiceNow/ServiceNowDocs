---
title: Detailed information on products discovered by ITOM Visibility
description: Discovery and Service Mapping can discover a wide range of operating systems and applications.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 67
keywords: [ITOM, Visibility, ServiceNow, Discovery, Cloud, API, Permissions, Patterns, AWS, Azure, GCP, IBM, Oracle, OCI]
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Detailed information on products discovered by ITOM Visibility

Discovery and Service Mapping can discover a wide range of operating systems and applications.

Discovery finds computers, servers, printers, a variety of IP-enabled devices, and the applications that run on them. It can then update the CIs in your CMDB with the data it collects. This discovery method is referred to as horizontal discovery. Service Mapping maps dependencies, based on a connection between devices and applications. This method is referred to as top-down mapping. The top-down mapping helps you immediately see the impact of a problematic object on the rest of the service instance operation.

On top of hosts and applications supported by default, you can discover additional hosts and applications by deploying patterns available on Store. For reference information on store released patterns, see [Available on-premise discovery patterns](../concept/available-patterns.md).

If your organization uses devices or applications, which are not supported by default or using patterns available at ServiceNow Store, you can configure Discovery and Service Mapping to discover them as described in [Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md).

Cloud Discovery Patterns find the cloud resources of AWS, Azure, Google Cloud Platform \(GCP\), IBM, and Oracle.

If you want to validate the necessary pattern commands before running discovery, use the Command Validation Tool. For more information, see [Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md).

ITOM Content Service Provides visibility to your applications by using AI capabilities that cluster and classify running application processes. For more information, see [ITOM Content Service](../../discovery/concept/discovery-content-services.md).

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

<table id="table_fzm_nmw_mdb" class="custom-rows"><thead><tr><th>

Name

</th><th class="filter">

Platform

</th><th>

Version

</th><th class="filter">

Protocol

</th><th class="filter">

Discovery type

</th><th>

Pattern \(or probe if indicated\)

</th></tr></thead><tbody><tr><td>

.Net Framework

</td><td>

Windows

</td><td>

1.x.x, 2.x.x, 3.x.x, 4.x.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

.NET Application

</td></tr><tr><td>

[A10 load balancer](../../discovery/reference/r_DataCollDiscoA10LoadBalancers.md)

</td><td>

A10

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

A10 Load Balancer

</td></tr><tr><td>

[Adobe JRun](../../discovery/reference/r-AdobeJRun.md)

</td><td>

Windows

 UNIX

</td><td>

4.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Jrun

</td></tr><tr><td>

[Apache Cassandra database and DataStax](cassandra-discovery.md)

</td><td>

UNIX

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

Cassandra

</td></tr><tr><td>

[Apache HBase](../../discovery/reference/r_DiscoverHBaseInstances.md)

</td><td>

UNIX

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Probes:-   HBase - Version
-   HBase - Main Class
-   HBase - Configuration

</td></tr><tr><td>

Apache HTTP Server

</td><td>

Windows

 UNIX

</td><td>

2.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Apache

</td></tr><tr><td>

[Apache Kafka and Zookeeper](kafka-zookeeper-discovery.md)

</td><td>

Apache

 Kafka

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Kafka and Zookeeper

</td></tr><tr><td>

[Apache Tomcat Servlet container HTTP web server](../../discovery/reference/r_DataCollDiscoTomcatServers.md)

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x, 8.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Tomcat

</td></tr><tr><td>

[Apigee Edge Enterprise edition](../concept/apigee-edge-discovery.md)

</td><td>

Linux

</td><td>

4.x.x

</td><td>

SSH

 HTTP

</td><td>

Horizontal and top-down

</td><td>

APIGee

</td></tr><tr><td>

[Avi Vantage load balancer including Avi Controller and GSLB](avi-load-balancer-discovery.md)

</td><td>

VMware

 AWS

 Avi Networks

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

AVI LB - Avi Vantage load balancer

 AVI LB - AVI Top Down

 AVI Session - Avi Controller

 AVI GSLB support

</td></tr><tr><td>

[Alibaba Cloud availability zone](alibaba-availability-zone.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Availability Zone \(LP\)

</td></tr><tr><td>

[Alibaba Cloud cloud hardware type](alibaba-cloud-hardware-type.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Cloud Hardware Type \(LP\)

</td></tr><tr><td>

[Alibaba Cloud cloud OS images](alibaba-cloud-os-image.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Cloud OS Image \(LP\)

</td></tr><tr><td>

[Alibaba Cloud datacenters](alibaba-datacenter-discovery.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Datacenter \(LP\)

</td></tr><tr><td>

[Alibaba Cloud service accounts](alibaba-service-account-discovery.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Service Account Validation

</td></tr><tr><td>

[Alibaba Cloud storage volume](alibaba-storage-volume.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Storage Volume \(LP\)

</td></tr><tr><td>

[Alibaba Cloud virtual machines](alibaba-virtual-machine.md)

</td><td>

Alibaba Cloud

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Alibaba - Virtual Machine \(LP\)

</td></tr><tr><td>

[Amazon API Gateway](../concept/aws-api-gateway-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Amazon AWS API Gateway

</td></tr><tr><td>

[Amazon API Gateway Domain Name](../../patterns/aws-api-gateway-domain-name.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - API Gateway Domain Name - Extended Inventory \(LP\)

</td></tr><tr><td>

Amazon Application Load Balancer Service

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Top-down

</td><td>

Amazon AWS application ELB service - TD

</td></tr><tr><td>

[Amazon Bedrock](../../ai-agent-topology-mapping/reference/amazon-bedrock-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Bedrock Agents

</td></tr><tr><td>

[Amazon Cognito](aws_cognito-discovery-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Cognito

</td></tr><tr><td>

[Amazon DB cluster discovery with Patterns](aws-db-cluster-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Amazon AWS DB Cluster

</td></tr><tr><td>

[Amazon DynamoDB](../concept/aws-dynamoDB-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Amazon AWS DynamoDB \(pattern\)

</td></tr><tr><td>

[Amazon DynamoDB Cluster](../../patterns/aws-dynamodb-cluster.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - DynamoDB Cluster - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon EC2 Amazon EBS Snapshot](../../patterns/aws-ec2-ebs-snapshot.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic Compute Cloud EBS Snapshot - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon EC2 Reserved Instance](../../patterns/aws-ec2-reserved-instance.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic Compute Cloud Reserved Instance - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon EC2 VPC Endpoint Service](../../patterns/aws-ec2-vpc-endpoint-service.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic Compute Cloud VPC Endpoint Service - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon EC2 VPC Peering Connection](../../patterns/aws-ec2-vpc-peering-connection.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic Compute Cloud VPC Peering Connection - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon ECS resource](aws-ecs-fargate-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

AWS ECS/Fargate

</td></tr><tr><td>

[Amazon Elastic File System \(Amazon EFS\)](../../patterns/aws-elastic-file-system.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic File System - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon ElastiCache](amazon-aws-elasticache-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon ElastiCache discovery

</td></tr><tr><td>

[Amazon ElastiCache Snapshot](../../patterns/aws-elasticache-snapshot.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - ElastiCache Snapshot - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon MWAA Environment](../../patterns/aws-mwaa-environment.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Managed Workflows for Apache Airflow Environment - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Relational Database Service](aws-rds-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Amazon AWS Relational Database Service

</td></tr><tr><td>

[Amazon RDS DB Snapshot](../../patterns/aws-rds-db-snapshot.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Relational Database Services DB Snapshot - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Redshift](amazon-redshift-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Redshift

</td></tr><tr><td>

[Amazon Redshift Serverless Namespace](../../patterns/aws-redshift-serverless-namespace.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Redshift Serverless Namespace - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Redshift Serverless Snapshot](../../patterns/aws-redshift-serverless-snapshot.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Redshift Serverless Snapshot - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Redshift Serverless Workgroup](../../patterns/aws-redshift-serverless-workgroup.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Redshift Serverless Workgroup - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Route 53](aws-route-53-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Route53

</td></tr><tr><td>

[Amazon SageMaker Training Job](../../patterns/aws-sagemaker-training-job.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - SageMaker Training Job - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Simple Storage Service \( AWS S3\)](../concept/aws-s3-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

AWS S3

</td></tr><tr><td>

[Amazon Timestream for InfluxDB Database Instance](../../patterns/aws-timestream-influxdb-db-instance.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Timestream for InfluxDB Database Instance - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS application ELB Service](aws-application-elb-service-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS application ELB Service

</td></tr><tr><td>

[AWS Auto Scaling groups discovery with Patterns](aws-auto-scaling-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

AWS Auto Scaling groups \(LP\) \(pattern\)

</td></tr><tr><td>

[AWS Batch Compute Environment](../../patterns/aws-batch-compute-environment.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Batch Compute Environment - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS classic ELB Service](aws-classic-elb-service-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS classic ELB Service

</td></tr><tr><td>

[AWS CloudHSM HSM](../../patterns/aws-cloudhsm-hsm.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CloudHSM HSM - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS CloudTrail Trail](../../patterns/aws-cloudtrail-trail.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CloudTrail Trail - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS datacenter](aws-datacenter-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Datacenter discovery

</td></tr><tr><td>

[AWS DataSync Task](../../patterns/aws-datasync-task.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - DataSync Task - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Elastic Load Balancer Service](aws-application-elb-service-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Top-down

</td><td>

Amazon AWS classic ELB Service - TD

</td></tr><tr><td>

[AWS Global Accelerator](../../patterns/aws-global-accelerator.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Global Accelerator - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS hardware type](aws-hardware-type-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Amazon AWS - Hardware Type \(LP\)
-   Amazon AWS - Cloud Hardware Type \(LP\)

</td></tr><tr><td>

[AWS Keyspaces](amazon-keyspaces-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Keyspaces

</td></tr><tr><td>

[AWS Kinesis Discovery](amazon-kinesis-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Amazon AWS - Kinesis Video Stream Services \(LP\)
-   Amazon AWS - Kinesis Data Stream Services \(LP\)
-   Amazon AWS - Kinesis Firehose Stream Services \(LP\)
-   Amazon AWS - Kinesis Data Analytics Stream Services \(LP\)

</td></tr><tr><td>

[AWS Lambda discovery with Patterns](../concept/aws-lambda-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Amazon AWS Lambda

</td></tr><tr><td>

[AWS MemoryDB for Redis discovery with Patterns](aws-memorydb-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

AWS MemoryDB \(pattern\)

</td></tr><tr><td>

[AWS Network Firewall](../../patterns/aws-network-firewall.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Network Firewall - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS OpenSearch](amazon-opensearch-discovery.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS OpenSearch

</td></tr><tr><td>

[AWS Organizations](aws-organizations-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Organizations

</td></tr><tr><td>

[AWS OS images](aws-os-image-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Amazon AWS - Owned Template \(LP\)
-   Amazon AWS - Executable Template \(LP\)
-   Amazon AWS - Owned Cloud OS Image \(LP\)
-   Amazon AWS - Executable Cloud OS Image \(LP\)

</td></tr><tr><td>

[AWS Resource Inventory discovery with Patterns](aws-resource-inventory.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

AWS Resource Inventory

</td></tr><tr><td>

[AWS Serverless Database](aws-serverless-database-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS Serverless Database

</td></tr><tr><td>

[AWS Services discovery using patterns](aws-service-discovery-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

See the link

</td></tr><tr><td>

[AWS Storage Gateway File Share](../../patterns/aws-storage-gateway-file-share.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Storage Gateway File Share - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS sub accounts](aws-sub-account-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS sub account discovery

</td></tr><tr><td>

[AWS Virtual Server](aws-virtual-server-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Virtual Server \(LP\)

</td></tr><tr><td>

[Azure App Configuration store](../../patterns/azure-app-configuration-store.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - App Configuration Configuration Store - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure App Service App Service Plan](../../patterns/azure-app-service-plan.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - App Service App Service Plan - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Application Gateway](../concept/azure-application-gateway-discovery.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure Application Gateway \(LP\)

</td></tr><tr><td>

[Azure Application Insight Component](../../patterns/azure-app-insight-component.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Application Insight Component - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Application Insight Data Collection Rule](../../patterns/azure-app-insight-data-collect-rule.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Application Insight Data Collection Rule - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Application Security Group](../../patterns/azure-app-security-group.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Application Security Group - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Automation Account](../../patterns/azure-automation-account.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Automation Account - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure availability sets](azure-availability-sets-patterns.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Availability Set \(LP\)

</td></tr><tr><td>

[Azure availability zones](azure-availability-zones-patterns.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Availability Zones \(LP\)

</td></tr><tr><td>

[Azure Blob Storage](azure-blob-storage-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Storage Blobs\(LP\)

</td></tr><tr><td>

[Azure Classic Load Balancer](azure-classic-load-balancer-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Classic LB \(LP\)

</td></tr><tr><td>

[Azure Compute Gallery Image Definition](../../patterns/azure-compute-gallery-img-definition.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Compute Gallery Image Definition - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Compute Snapshot](../../patterns/azure-compute-snapshot.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Compute Snapshot - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Container Registry](../../patterns/azure-container-registry.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Container Registry - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Cosmos DB for PostgreSQL Cluster](../../patterns/azure-cosmos-db-postgresql-cluster.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Cosmos DB for PostgreSQL Cluster - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Data Explorer Cluster](../../patterns/azure-data-explorer-cluster.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Data Explorer Cluster - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Data Factory](../../patterns/azure-data-factory.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Data Factory - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Data Protection Backup Vault](../../patterns/azure-data-protection-backup-vault.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Data Protection Backup Vault - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Database Service](../../discovery/reference/data-collected-azure-discovery.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Azure DataBase \(pattern\)

</td></tr><tr><td>

[Azure Databricks Workspace](../../patterns/azure-databricks-workspace.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Databricks Workspace - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Datacenter discovery](azure-datacenter-discovery-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure Datacenter discovery

</td></tr><tr><td>

[Azure Dev Center](../../patterns/azure-dev-center.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Dev Center - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Disk Encryption Set](../../patterns/azure-disk-encryption-set.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Disk Encryption Set - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure DNS zones and record sets discovery using Patterns](azure-dns-discovery.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:Azure DNS Zones HD

or

Azure DNS Zones \(LP\)

Azure DNS Zone Recordsets \(LP\)

</td></tr><tr><td>

[Azure Event Grid System Topic](../../patterns/azure-event-grid-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Event Grid System Topic - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Event Hub Namespace](../../patterns/azure-event-hub-namespace.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Event Hub Namespace - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Express Route Circuit](azure-express-route-circuit-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Express Route Circuit \(LP\)

</td></tr><tr><td>

[Azure File Share](azure-file-share-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - File Share \(LP\)

</td></tr><tr><td>

[Azure Firewall Network Security](../../patterns/azure-firewall-network-security.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Network Security Azure Firewall - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Functions](../concept/azure-function-discovery.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Patterns:Azure Functions TD

or

Azure Functions \(LP\)

</td></tr><tr><td>

[Azure hardware type](azure-hardware-type-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Pattens:-   Azure - Hardware Type \(LP\)
-   Azure - Cloud Hardware Type \(LP\)

</td></tr><tr><td>

[Azure Host](azure-host-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Host \(LP\)

</td></tr><tr><td>

[Azure Key Vault](../../patterns/azure-key-vault.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Key Vault - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure LoadBalancer Service TD](azure-classic-load-balancer-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Top-down

</td><td>

Azure LoadBalancer TD

</td></tr><tr><td>

[Azure Local Network Gateway](azure-local-network-gateway-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Local Network Gateway \(LP\)

</td></tr><tr><td>

[Azure Log Analytics Workspace](../../patterns/azure-log-analytics-workspace.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Log Analytics Workspace - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Logic App](../../patterns/azure-logic-app.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Logic App - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Managed Identity User Assigned Identity](../../patterns/azure-managed-id-user-assigned-id.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Managed Identity User Assigned Identity - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure NAT Gateway](azure-nat-gateway-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - NAT Gateway \(LP\)

</td></tr><tr><td>

[Azure Networks IP Group](../../patterns/azure-networks-ip-group.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Networks IP Group - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure OS image](azure-os-image-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Azure - Image \(LP\)
-   Azure - Cloud OS Image \(LP\)

</td></tr><tr><td>

[Azure Private DNS Zone](azure-private-dns-zone-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Private DNS Zone \(LP\)

</td></tr><tr><td>

[Azure Private Link Private Endpoint](../../patterns/azure-private-link-private-endpoint.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Private Link Private Endpoint - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Recovery Services Vault](../../patterns/azure-recovery-services-vault.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Recovery Services Vault - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Recovery Services Vault Backup Item](../../patterns/azure-recovery-services-vault-backup.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Recovery Services Vault Backup Item - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Resource Inventory](azure-resource-inventory-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure Inventory and tags

</td></tr><tr><td>

[Azure Service Bus Namespace](../../patterns/azure-service-bus-namespace.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Service Bus Namespace - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Service Bus Queue](../../patterns/azure-service-bus-queue.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Service Bus Queue - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Service Bus Topic](../../patterns/azure-service-bus-topic.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Service Bus Topic - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Service Endpoint Policy](../../patterns/azure-service-endpoint-policy.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Service Endpoint Policy - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure Subscriptions Discovery For Management Group](azure-sub-mgmt-group-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure Subscriptions Discovery For Management Group

</td></tr><tr><td>

Azure SQL Database

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Cloud Database Instance

</td></tr><tr><td>

[Azure Virtual Machine](azure-vm-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Virtual Machine \(LP\)

</td></tr><tr><td>

[Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery](../../discovery/reference/AzureVMScaleSetInstance.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:

-   Azure - VM Scale Set \(LP\)
-   Azure VM Instance - Uniform Scale Set

</td></tr><tr><td>

[Azure Virtual Network Gateway Connection](azure-vng-connection-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Virtual Network Gateway Connection \(LP\)

</td></tr><tr><td>

[Azure Web Application Firewall Policy](../../patterns/azure-web-app-firewall-policy.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Web Application Firewall Policy - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure WebSite Service and Database](azure-cloud-discovery-patterns.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:Azure WebSite

Azure WebSite \(LP\)

Collect Azure Database Tags and WebSite tags

</td></tr><tr><td>

BMC Control-M

</td><td>

UNIX

 Windows

</td><td>

6.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal

</td><td>

Cntl-M Enterprise Manager

</td></tr><tr><td>

Bring Your Own License \(BYOL\)

</td><td>

Amazon AWS Cloud

 Microsoft Azure Cloud

 Google Cloud Platform \(GCP\)

</td><td>

N/A

</td><td>

REST

 Azure Resource Graph

</td><td>

Horizontal

</td><td>

The “Image License” shared library is an extension of the patterns:

-   Amazon AWS - Executable Template \(LP\)
-   Amazon AWS - Owned Template \(LP\)

 The "Azure Virtual Machine License" shared library is an extension of the "Azure - Virtual Machine \(LP\)" pattern.

 The "Google Cloud Platform \(GCP\) – VM license" shared library is an extension of the "Google Cloud Platform \(GCP\) - Virtual Server" pattern.

</td></tr><tr><td>

CA eTrust Directory server

</td><td>

Windows

</td><td>

7.x, 8.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

CA eTrust Directory server

</td></tr><tr><td>

CA Identity Manager Provisioning Server

</td><td>

Windows

</td><td>

11.x, 12.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

CA Identity Manager Provisioning Server for Windows

</td></tr><tr><td>

CA Introscope Enterprise Manager

</td><td>

Windows

 Unix

</td><td>

8.x, 9.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

CA Introscope Enterprise Manager

</td></tr><tr><td>

CA Policy Server

</td><td>

Windows

 Unix

</td><td>

11.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

CA Policy Server

</td></tr><tr><td>

CA Site Minder Agent

</td><td>

Windows

 Unix

</td><td>

11.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

CA Site Minder Agent

</td></tr><tr><td>

[Cisco Content Services Switch Load balancer](../../discovery/concept/c_LoadBalancerCSS.md)

</td><td>

ACE

</td><td>

6.x

</td><td>

SNMP

 SSH

</td><td>

Horizontal and top-down

</td><td>

Cisco CSS SNMP

</td></tr><tr><td>

[Cisco ACE Application Control Engine](../../discovery/concept/ace-load-balancer-discovery.md)

</td><td>

ACE

</td><td>

2.x

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

ACE Load Balancer

</td></tr><tr><td>

Cisco Call Manager

</td><td>

Cisco

</td><td>

3.x, 4.x

</td><td>

SNMP

 SSH

</td><td>

Top-down

</td><td>

Cisco CallManager

</td></tr><tr><td>

Cisco Fiber Connect

</td><td>

Cisco

</td><td>

No data

</td><td>

SNMP

 SSH

</td><td>

Top-down

</td><td>

Cisco Fibre Connect

</td></tr><tr><td>

[Cisco Global Site Selector Load Balancer](../../discovery/concept/c_LoadBalancerGSS.md)

</td><td>

ACE

</td><td>

3.x

</td><td>

SNMP

 SSH

</td><td>

Horizontal and top-down

</td><td>

Cisco GSS

</td></tr><tr><td>

[Cisco Unified Computing System](../../discovery/reference/r-CiscoUCSHD.md)

</td><td>

UCS

</td><td>

3.x

</td><td>

REST

</td><td>

Horizontal

</td><td>

UCS - HD

</td></tr><tr><td>

[Citrix Delivery Controller](../../discovery/concept/citrix-lic-server-deliv-controller.md)

</td><td>

Windows

</td><td>

7.x&gt;7.5, 8.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Delivery Controller

</td></tr><tr><td>

Citrix Netscaler Global Server Load Balancing \(GSLB\)

</td><td>

Netscaler

</td><td>

10.x

</td><td>

SNMP

 SSH

 NS.conf

</td><td>

Horizontal and top-down

</td><td>

Netscaler GLB

</td></tr><tr><td>

Citrix Netscaler Load Balancer

</td><td>

Netscaler

</td><td>

9.x, 10.x

</td><td>

SNMP

 SSH

 NS.conf

</td><td>

Horizontal and top-down

</td><td>

Citrix Netscaler

</td></tr><tr><td>

[Citrix Netscaler SDX](citrix-netscaler-sdx-discovery.md)

</td><td>

Citrix NetScaler SDX

</td><td>

13

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Citrix NetScaler SDX

</td></tr><tr><td>

[Citrix License Server](../../discovery/concept/citrix-lic-server-deliv-controller.md)

</td><td>

Windows

</td><td>

7.x

</td><td>

WMI

</td><td>

Horizontal

</td><td>

License Server

</td></tr><tr><td>

[Citrix Xen Hyper-V](citrix-xen-hyper-v-discovery.md)

</td><td>

Xen Server

</td><td>

7.6

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Citrix Xen Hyper-V

</td></tr><tr><td>

[Cloudian Storage](cloudian-storage-discovery.md)

</td><td>

Linux

</td><td>

7.x

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Cloudian Storage discovery

</td></tr><tr><td>

Connect APK

</td><td>

Windows

</td><td>

1.x.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Connect-It Service

</td></tr><tr><td>

[Container image scanning for software decomposition](../concept/container-image-concept.md)

</td><td>

Linux

</td><td>

 

</td><td>

REST

 HTTP

</td><td>

Horizontal

</td><td>

container image scan

</td></tr><tr><td>

[Software Bill of Material \(SBOM\)](generate-sbom-pattern.md)

</td><td>

Linux

</td><td>

N/A

</td><td>

REST

 HTTP

</td><td>

Horizontal

</td><td>

SBOM is an extension section of the container image scan pattern

</td></tr><tr><td>

[Docker virtualization](../../discovery/concept/c-docker-virtualization.md)

</td><td>

Linux

</td><td>

N/A

</td><td>

N/A

</td><td>

Horizontal

</td><td>

Docker \(pattern\)

</td></tr><tr><td>

Epic Systems Corporation

</td><td>

UNIX

</td><td>

2014.x.x, 2015.x.x

</td><td>

SSH

</td><td>

Top-down

</td><td>

EPIC Cache

</td></tr><tr><td>

[Database Administrator \(DBA\) report discovery](../../discovery/concept/dba-report-discovery-pattern.md)

</td><td>

N/A

</td><td>

N/A

</td><td>

N/A

</td><td>

Horizontal

</td><td>

DBA is an extension section of the patterns:

-   Cassandra DB
-   MSSQL DB
-   MySQL DB
-   Oracle DB

</td></tr><tr><td>

[Dell PowerMax storage discovery with Patterns](../../discovery/reference/emc-powermax-discovery-pattern.md)

</td><td>

Dell EMC

</td><td>

9 and 10

</td><td>

N/A

</td><td>

Horizontal

</td><td>

EMC PMAX phase1 \(pattern\)

 EMC PMAX phase2 \(pattern\)

</td></tr><tr><td>

[Dell Data Domain storage discovery using Patterns](emc-data-domain-pattern.md)

</td><td>

DD OS

</td><td>

DD OS 7.3 or later

</td><td>

REST

</td><td>

Horizontal

</td><td>

DELL EMC Data Domain \(pattern\)

</td></tr><tr><td>

[Dell EMC XtremIO storage array discovery](xtreamio-storage-array-discovery.md)

</td><td>

Linux

</td><td>

6.3.0 and 6.3.1

</td><td>

REST

</td><td>

Horizontal

</td><td>

EMC XtremIO \(pattern\)

</td></tr><tr><td>

[EMC Isilon](../concept/emc-isilon-discovery.md)

</td><td>

OneFS

</td><td>

8.0

</td><td>

SNMP

 REST

</td><td>

Horizontal

</td><td>

EMC Isilon

</td></tr><tr><td>

F5 BIG-IP Device Service Clustering

</td><td>

F5

</td><td>

11.x, 12.x

</td><td>

SNMP

 SSH

 REST

</td><td>

Horizontal

</td><td>

F5 Cluster

</td></tr><tr><td>

[F5 BIG-IP](../../discovery/concept/c_LoadBalancerF5BIGIP.md)

</td><td>

F5

</td><td>

11.x, 12.x

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

F5 Load Balancer, F5 Load Balancer SSH

</td></tr><tr><td>

[Fortinet firewalls](fortinet-fw-discovery.md)

</td><td>

Fortinet Firewall device

</td><td>

FortiOS 5.2.x, FortiOS 5.4.x, FortiOS 5.6.x, FortiOS 6.2.x, FortiOS 6.4.x, FortiOS 7.2.x

</td><td>

SNMP

</td><td>

Horizontal

</td><td>

Next Generation Fortinet Network Firewall

</td></tr><tr><td>

[Fortinet firewalls and FortiGate VDOMs](fortinet-fw-vdoms-rest-discovery.md)

</td><td>

Fortinet Firewall device

</td><td>

FortiOS 6.2.x, FortiOS 6.4.x, FortiOS 7.x

</td><td>

REST

</td><td>

Horizontal

</td><td>

Next Generation Fortinet Network Firewall - REST

</td></tr><tr><td>

Google Cloud Apigee API Platform

</td><td>

Linux

</td><td>

4.x.x

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

APIGee Service

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) AlloyDB for PostgreSQL](gcp-alloydb-postgresql-patterns.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - AlloyDB for PostgreSQL

</td></tr><tr><td>

[Google Cloud BigQuery](gcp-bigquery-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - BigQuery DB

</td></tr><tr><td>

[Google Cloud Bigtable](gcp-bigtable-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Bigtable DB

</td></tr><tr><td>

[Google Cloud FireStore](gcp-firestore-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Firestore DB

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Cloud Functions](gcp-cloud-functions-patterns.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\)- Cloud Functions

</td></tr><tr><td>

[Google Cloud SQL](gcp-cloud-sql-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Cloud SQL DB

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Disk Types](gcp-disk-types-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Disk Types

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Events](gcp-events-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

-   Google Cloud Platform \(GCP\) - Networking - Events
-   Google Cloud Platform \(GCP\) - Networking Firewall - Events
-   Google Cloud Platform \(GCP\) - Subnetwork - Events

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) External IP Addresses](gcp-external-ip-addresses-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - External IP Addresses

</td></tr><tr><td>

[Google Firebase Realtime DB](gcp-firebase-realtime-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Firebase Realtime DB

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Load Balancer](gcp-load-balancer-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

-   Google Cloud Platform \(GCP\) - Load Balancer - HTTP
-   Google Cloud Platform \(GCP\) - Load Balancer - TCP - UDP

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Memorystore](gcp-memorystore-patterns.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Memorystore DB

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Networking](gcp-networking-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Networking

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Organization](google-gcp-organization-discovery.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

GCP Organization

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) resource inventory](gcp-resource-inventory-discovery.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) Resource Inventory

</td></tr><tr><td>

[Google Cloud Spanner](gcp-spanner-db-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Spanner DB

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) SSH Keys](gcp-ssh-keys-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - SSH Keys

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) storage](gcp-storage-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Storage

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) Virtual Server](gcp-virtual-server-pattern.md)

</td><td>

GCP

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Google Cloud Platform \(GCP\) - Virtual Server

</td></tr><tr><td>

[HAProxy Community edition load balancers](haproxy-lb-discovery-pattern.md)

</td><td>

UNIX

</td><td>

1.5, 1.6, 1.7

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

HA Proxy

</td></tr><tr><td>

[HP Operations Manager](../../discovery/reference/r-HPOP.md)

</td><td>

Windows

Unix

</td><td>

9.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

HP Operations Manager

</td></tr><tr><td>

HP Quality Center

</td><td>

Windows

</td><td>

10.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

HP Quality Center on Windows

</td></tr><tr><td>

[HP Service Manager](../../discovery/reference/r-HPServiceManager.md)

</td><td>

Windows

 Unix

</td><td>

9.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

HP Service Manager Application Server

</td></tr><tr><td>

HP UCMDB

</td><td>

Windows

</td><td>

N/A

</td><td>

WMI

WinRM

</td><td>

Horizontal and top-down

</td><td>

HP uCMDB on Windows

</td></tr><tr><td>

HP-UX UNIX Server

</td><td>

HP-UX

</td><td>

11i

</td><td>

SSH

</td><td>

Horizontal

</td><td>

HP-UX Server

</td></tr><tr><td>

IBM AIX

</td><td>

UNIX

</td><td>

6.x, 7.x

</td><td>

SSH

</td><td>

Top-down

</td><td>

AIX Server

</td></tr><tr><td>

IBM CICS Transaction Gateway

</td><td>

Windows

 UNIX

</td><td>

5.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

CTG

</td></tr><tr><td>

[IBM Cloud Platform](google-gcp-discovery-pattern.md)

</td><td>

IBM Cloud Platform

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

IBM Cloud Load Balancer, IBM Cloud Location Groups, IBM Cloud Network, IBM Cloud Organizations and Spaces, IBM Cloud Resource Groups, IBM Cloud SSH Key, IBM Cloud Storage, IBM Cloud Virtual Server

</td></tr><tr><td>

IBM Customer Information Control System

</td><td>

Windows

 UNIX

</td><td>

4.x, 5.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

CICS

</td></tr><tr><td>

[IBM Db2 on Unix](ibm-db2-linux-discovery.md)

</td><td>

UNIX

</td><td>

8.x, 9.x, 10.x, 11.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal

</td><td>

DB2

</td></tr><tr><td>

[IBM Db2 on Windows](ibm-db2-windows-discovery.md)

</td><td>

Windows

</td><td>

8.x, 9.x, 10.x, 11.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal

</td><td>

DB2

</td></tr><tr><td>

[IBM Virtualization and Hardware Management Console \(HMC\) components](ibm-hmc-discovery.md)

</td><td>

UNIX

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

IBM HMC Server

</td></tr><tr><td>

[IBM PowerHA Cluster \(HACMP\)](ibm-powerha-hamcp-discovery.md)

</td><td>

IBM

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

IBM PowerHA Cluster \(HACMP\)

</td></tr><tr><td>

IBM Security Access Manager

</td><td>

ISAM

</td><td>

8.0.1

</td><td>

SNMP

 REST

</td><td>

Horizontal and top-down

</td><td>

ISAM Server

</td></tr><tr><td>

[IBM WebSEAL discovery](ibm_webseal_discovery_patterns.md)

</td><td>

ISAM

</td><td>

9.\*,10.\*.

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

IBM WebSEAL

</td></tr><tr><td>

IBM Tivoli Access Manager

</td><td>

Windows

 UNIX

</td><td>

6.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

ITAM - Asset Center

</td></tr><tr><td>

IBM Tivoli WebSEAL

</td><td>

Windows

 UNIX

</td><td>

5.x, 6.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Webseal \(pattern\)

</td></tr><tr><td>

IBM Websphere Application server

</td><td>

Windows

 UNIX

</td><td>

5.x, 6.x, 7.x, 8.x, 9.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Websphere

</td></tr><tr><td>

IBM WebSphere DataPower SOA Appliance

</td><td>

DataPower

</td><td>

I40, I50

</td><td>

SNMP

 REST

</td><td>

Horizontal and top-down

</td><td>

DataPower

</td></tr><tr><td>

IBM WebSphere Message Queue

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x, 8.x, 9.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

The following patterns: -   WMQ On Unix
-   WMQ On Windows
-   WMQ Queue Unix
-   WMQ Queue Windows

</td></tr><tr><td>

[IBM App Connect Enterprise and HTTP listener discovery](../../discovery/reference/r_IBMWMB.md)

</td><td>

UNIX

</td><td>

6, 7, 8, 9, 10, 11, 12.

</td><td>

N/A

</td><td>

Horizontal and top-down

</td><td>

WMB on UNIX \(pattern\)

</td></tr><tr><td>

IBM WebSphere Portal

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x, 8.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Websphere Portal On Windows

</td></tr><tr><td>

IBM Z mainframe

</td><td>

Z/OS

</td><td>

OS/390

</td><td>

SSH

</td><td>

Horizontal

</td><td>

IBM zOS Server

</td></tr><tr><td>

[Infini-Box](infinibox-discovery.md)

</td><td>

 

</td><td>

5.0.x

</td><td>

REST

 HTTP

</td><td>

Horizontal

</td><td>

InfiniBox

</td></tr><tr><td>

Interconnect Web Service

</td><td>

Windows

</td><td>

2014

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Inter Connect

</td></tr><tr><td>

[Istio Service Mash](../concept/kubernetes-discovery.md)

</td><td>

Kubernetes

</td><td>

1.15 and later

</td><td>

HTTP

</td><td>

Horizontal

</td><td>

ISTIO Service mesh

</td></tr><tr><td>

[Kubernetes](../concept/kubernetes-discovery.md)

</td><td>

Kubernetes

</td><td>

1.21 - 1.30

</td><td>

REST

 HTTP

</td><td>

Horizontal

</td><td>

Kubernetes

</td></tr><tr><td>

[Linux Server](../../discovery/reference/r_DataCollDiscoLinuxComputers-1.md)

</td><td>

UNIX

</td><td>

Ubuntu 16, RHEL 5.x, CentOS 7.x

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Linux Server

</td></tr><tr><td>

[Linux Pacemaker Cluster](linux-pacemaker-cluster-discovery.md)

</td><td>

Linux

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Pacemaker Linux cluster

</td></tr><tr><td>

Microsoft BizTalk Orchestration Server

</td><td>

Windows

</td><td>

2004, 2006, 2007, 2009, 2010

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

BizTalk server

</td></tr><tr><td>

[Microsoft Certificate Authority](microsoft-ca-discovery.md)

</td><td>

Microsoft

</td><td>

N/A

</td><td>

WMI

</td><td>

Horizontal

</td><td>

Microsoft Certificate Authority

</td></tr><tr><td>

Microsoft Dynamics CRM

</td><td>

Windows

</td><td>

2003, 2005, 2007, 2010

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Dynamic CRM Component

</td></tr><tr><td>

Microsoft Fast Search

</td><td>

Windows

</td><td>

2005

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

Fast Search

</td></tr><tr><td>

[Microsoft Foundry \(Classic\)](../../ai-agent-topology-mapping/reference/microsoft-foundry-classic-pattern.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Azure - AI Foundry Agents
-   Azure - AI Service Foundry
-   Azure - AI Service Foundry Project

</td></tr><tr><td>

[Microsoft Hyper-V Server](../../discovery/reference/r_DiscoveryForHyperV.md#)

</td><td>

Windows

</td><td>

2008, 2012, 2016

</td><td>

WMI

 WinRM

</td><td>

Horizontal

</td><td>

Hyper-V Server

</td></tr><tr><td>

Microsoft Identity Integration Server

</td><td>

Windows

</td><td>

2003

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

IIFP On Windows Pattern

</td></tr><tr><td>

Microsoft Internet Information Services

</td><td>

Windows

</td><td>

6.0, 7.x, 8.x

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

IIS

</td></tr><tr><td>

Microsoft Message Queuing

</td><td>

Windows

</td><td>

3.x, 4.x, 5.x

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

MSMQ \(pattern\)

</td></tr><tr><td>

[Microsoft SharePoint](../../discovery/reference/r-MSSharepoint.md)

</td><td>

Windows

</td><td>

2003, 2007, 2010, 2013

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

Microsoft SharePoint

</td></tr><tr><td>

[Microsoft SQL Server and Cluster discovery](../../discovery/reference/mssql-data-collected-pattern.md#)

</td><td>

Windows

</td><td>

2014, 2016, 2017, 2019, 2022

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

MSSQL DB On Windows \(pattern\)

</td></tr><tr><td>

[Microsoft SQL Server Analysis Services \(SSAS\)](../../discovery/reference/r-SSAS-MSSQL.md)

</td><td>

Windows

</td><td>

2014, 2016, 2017, 2019, 2022

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

SSAS \(pattern\)

</td></tr><tr><td>

[Microsoft SQL Server Integration Services \(SSIS\) discovery](../../discovery/reference/ms-ssis-pattern.md)

</td><td>

Windows

</td><td>

2014, 2016, 2017, 2019, 2022

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

SSIS \(pattern\)

</td></tr><tr><td>

Microsoft SQL Server Reporting Services

</td><td>

Windows

</td><td>

2014, 2016, 2017, 2019, 2022

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

SSRS \(pattern\)

</td></tr><tr><td>

Microsoft Windows Desktops

</td><td>

Windows

</td><td>

2003, 2008, 2012,

</td><td>

WMI

 WinRM

</td><td>

Horizontal

</td><td>

Windows OS - Desktops

</td></tr><tr><td>

Microsoft Windows Server

</td><td>

Windows

</td><td>

2003, 2008,2012,2016, 2022

</td><td>

WMI

 WinRM

</td><td>

Horizontal

</td><td>

Windows OS - Servers

</td></tr><tr><td>

[MongoDB](../../discovery/reference/r_DiscoverMongoDBInstances.md)

</td><td>

Windows

 UNIX

</td><td>

3.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

mongos server

</td></tr><tr><td>

[NetApp Server and Cluster discovery](../../discovery/concept/netapp-discovery.md)

</td><td>

NetApp

</td><td>

7.x,8.x

</td><td>

SNMP

</td><td>

Horizontal

</td><td>

Patterns:NetApp Storage 7-Mode

NetApp Cluster SNMP

</td></tr><tr><td>

[NetApp Server and Cluster discovery](../../discovery/concept/netapp-discovery.md)

</td><td>

NetApp

</td><td>

7.x,8.x,9.x

</td><td>

HTTP

</td><td>

Horizontal

</td><td>

NetApp Cluster HTTP

 \(pattern\)

</td></tr><tr><td>

[NetApp SolidFire storage system](solidfire-storage-pattern.md)

</td><td>

NetApp SolidFire

</td><td>

N/A

</td><td>

HTTP

</td><td>

Horizontal

</td><td>

NetApp SolidFire storage system

</td></tr><tr><td>

[Network router](network-router-patterns.md)

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

SNMP

</td><td>

Horizontal

</td><td>

Network Router

</td></tr><tr><td>

[Network switch](network-switch-patterns.md)

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

SNMP

</td><td>

Horizontal

</td><td>

Network Switch

</td></tr><tr><td>

[NGINX Web Server](../../discovery/concept/c_NGINXWebServerDiscovery.md)

</td><td>

Windows

 UNIX

</td><td>

1.10, 1.10.1

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Nginx Pattern

</td></tr><tr><td>

[Nutanix Acropolis \(AOS\)](nutanix-pattern.md)

</td><td>

UNIX

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Nutanix Components

</td></tr><tr><td>

[Nutanix Prism Central](nutanix-pattern.md)

</td><td>

UNIX

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Nutanix Components

</td></tr><tr><td>

OpenText Documentum

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Pattern for license server

</td></tr><tr><td>

[OpenStack resources](openstack-discovery.md)

</td><td>

OpenStack

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

OpenStack \(pattern\)

</td></tr><tr><td>

Oracle Application Server

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Oracle iAS

</td></tr><tr><td>

Oracle Concurrent Server

</td><td>

Windows

 UNIX

</td><td>

10.x, 11.x, 12.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Concurrent Server

</td></tr><tr><td>

[Oracle Cloud Infrastructure](oracle-cloud-infrastructure-discovery.md)

</td><td>

Oracle

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Oracle Cloud Infrastructure

</td></tr><tr><td>

Oracle Clusterware

</td><td>

Linux

</td><td>

10.x, 11.x, 12.x

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Oracle CRS

</td></tr><tr><td>

[Oracle Database](../../discovery/concept/c_OracleDatabaseDiscovery.md)

</td><td>

Windows

 UNIX

</td><td>

8.x.x, 9.x.x, 10.x.x, 11.x.x, 12.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Oracle DB

</td></tr><tr><td>

Oracle Database Advanced Queuing

</td><td>

Windows

 UNIX

</td><td>

9.x.x, 10.x.x, 11.x.x, 12.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Advanced Queue Queue

</td></tr><tr><td>

[Oracle Database 12c](oracle-cdb-pdb-discovery.md)

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal

</td><td>

PDB/CDB

</td></tr><tr><td>

Oracle Discover Server

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Discoverer Engine

</td></tr><tr><td>

Oracle E-Business Suite

</td><td>

Windows

 UNIX

</td><td>

10.x, 11.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

E-Business Suite

</td></tr><tr><td>

Oracle Forms

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Forms Engine

</td></tr><tr><td>

Oracle Fulfillment Server

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Fulfillment Server

</td></tr><tr><td>

[Oracle GoldenGate](../concept/oracle-golden-gate-discovery.md)

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

WMI

 SSH

</td><td>

Horizontal and top-down

</td><td>

Oracle GG

</td></tr><tr><td>

[Oracle Linux Virtualization Manager \(OLVM\) and Red Hat Virtualization \(RHV\)](red-hat-virtualization-discovery.md)

</td><td>

OLVM and RHV

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   oVirt Clusters and Hosts
-   oVirt Discover Logical Datacenters
-   oVirt Discover Manager Instance
-   oVirt Virtual Machines
-   oVirt Templates

</td></tr><tr><td>

[Oracle Global License Advisory Services \(GLAS\)](oracle-glas-discovery.md)

</td><td>

N/A

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Oracle GLAS Data Collection \(pattern\)

</td></tr><tr><td>

[Oracle Java processes](oracle-glas-discovery.md)

</td><td>

JDK

</td><td>

All

</td><td>

N/A

</td><td>

Horizontal

</td><td>

Java installation pattern

 ACC based discovery

</td></tr><tr><td>

[Oracle Solaris LDOM](solaris-ldom-discovery.md)

</td><td>

Solaris

</td><td>

10, 11

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Solaris Logical Domain \(LDOM\) infrastructure

</td></tr><tr><td>

Oracle HTTP Server

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

HTTP Server

</td></tr><tr><td>

Oracle iPlanet Web Server

</td><td>

Solaris

</td><td>

4.x, 6.x, 7.x

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

Sun iPlanet Webserver

</td></tr><tr><td>

Oracle Java Enterprise System\(JES\)

</td><td>

Solaris

</td><td>

7.x

</td><td>

SSH

</td><td>

Top-down

</td><td>

Sun JES pattern

</td></tr><tr><td>

[Oracle Listener](oracle-listener-hd-discovery.md)

</td><td>

Linux

</td><td>

12.2.x.x

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Oracle Listener HD

</td></tr><tr><td>

Oracle Metric Server

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Metric Server

</td></tr><tr><td>

Oracle MySql Server

</td><td>

Windows

 UNIX

</td><td>

4.x, 5.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

My SQL server On Windows and Linux \(pattern\)

</td></tr><tr><td>

Oracle Notification Server

</td><td>

Windows

 UNIX

</td><td>

9.x, 10.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Oracle Notification Server

</td></tr><tr><td>

Oracle Peoplesoft

</td><td>

Windows

/Unix

</td><td>

8.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Peoplesoft Application Server

</td></tr><tr><td>

Oracle Process Manager

</td><td>

Windows

/Unix

</td><td>

9.x.x, 10.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Process Manager

</td></tr><tr><td>

Oracle RAC

</td><td>

Windows

 UNIX

</td><td>

9.x.x, 10.x.x, 11.x.x, 12.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

App TNS Service

</td></tr><tr><td>

Oracle Report Server

</td><td>

Windows

 UNIX

</td><td>

9.x.x, 10.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

Report Server

</td></tr><tr><td>

Oracle Solaris Server

</td><td>

Solaris

</td><td>

9, 10, 11, SPARC

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Solaris Server

</td></tr><tr><td>

[Oracle Solaris Logical Domain infrastructure](solaris-ldom-discovery.md)

</td><td>

Solaris

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Solaris LDOM

</td></tr><tr><td>

Oracle Weblogic Application Server

</td><td>

Windows

 UNIX

</td><td>

8.x, 9.x, 10.x, 11.x, 12.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

WebLogic

</td></tr><tr><td>

[Pivotal Cloud Foundry](../concept/pivotal-cloud-foundry.md)

</td><td>

PCF

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal and top-down

</td><td>

Patterns:Pivotal cloud foundry

Bosh

</td></tr><tr><td>

Pivotal RabbitMQ

</td><td>

Windows

 UNIX

</td><td>

3.x.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Top-down

</td><td>

RabbitMQ Cluster Unix pattern

</td></tr><tr><td>

PostgreSQL DB

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x, 8.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

PostgreSQL DB

</td></tr><tr><td>

Puppet

</td><td>

UNIX

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Probes: -   Puppet – Master Info
-   Puppet – Certificate Requests
-   Puppet – Manifest
-   Puppet – Modules

</td></tr><tr><td>

[Pure Storage FlashArray discovery](../../discovery/concept/flasharray-discovery.md)

</td><td>

Pure Storage

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Pure Flash Array Storage \(pattern\)

</td></tr><tr><td>

[Pure Storage FlashBlade](../concept/pure-storage-discovery.md)

</td><td>

Pure Storage

</td><td>

4.10.7

</td><td>

REST

 SSH

</td><td>

Horizontal

</td><td>

Pure Storage

</td></tr><tr><td>

[Radware Alteon RadWare ADC](../../discovery/concept/alteon-load-balancer-discovery.md)

</td><td>

Alteon

</td><td>

v31, v29.5

</td><td>

SNMP

</td><td>

Horizontal and top-down

</td><td>

Alteon Load Balancer

</td></tr><tr><td>

[RadWare AppDirector Load Balancer](../../discovery/concept/radware-appdirector.md)

</td><td>

Radware

</td><td>

N/A

</td><td>

SNMP

</td><td>

Horizontal and top-down

</td><td>

AppDirector Load Balancer

</td></tr><tr><td>

Red Hat Cluster Suite

</td><td>

Linux

</td><td>

RH 5.x, 6.x, 7.x

</td><td>

SSH

</td><td>

Horizontal

</td><td>

RH Cluster

</td></tr><tr><td>

[Red Hat JBoss Application Server](../../discovery/concept/c_DataCollDiscoJBossServers.md)

</td><td>

Windows

 UNIX

</td><td>

6.x, 7.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Jboss \(pattern\)

</td></tr><tr><td>

[Red Hat JBoss Fuse discovery](../concept/jboss-fuse-discovery.md)

</td><td>

Windows

 UNIX

</td><td>

N/A

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

Jboss Fuse \(pattern\)

</td></tr><tr><td>

[Red Hat OpenShift components of Kubernetes](../concept/kubernetes-discovery.md)

</td><td>

RHEL

</td><td>

API 1.x

</td><td>

REST

</td><td>

Horizontal

</td><td>

Collect OpenShift info library used as an extension section of the Kubernetes pattern

</td></tr><tr><td>

[Rubrik cluster](rubrik-discovery.md)

</td><td>

 

</td><td>

N/A

</td><td>

HTTP

 HTTPS

</td><td>

Horizontal

</td><td>

Multiple patterns

</td></tr><tr><td>

SAP Business Object XI Scheduler

</td><td>

Windows

</td><td>

2004, 2005, 2008

</td><td>

WMI

 WinRM

</td><td>

Horizontal and top-down

</td><td>

SAP BO BOXIScheduleRouter on Windows Pat

</td></tr><tr><td>

SAP Crystal Management Server

</td><td>

Windows

</td><td>

2004, 2005, 2008

</td><td>

WinRM

</td><td>

Horizontal and top-down

</td><td>

SAP Business Objects CMS Server on Windows

</td></tr><tr><td>

[SAP HANA](../concept/sap-discovery.md#)

</td><td>

Windows

 UNIX

</td><td>

2015, 2016, 2017

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

SAP HANA DB \(pattern\)

</td></tr><tr><td>

[SAP HANA Catalog](../concept/sap-discovery.md#)

</td><td>

UNIX

</td><td>

N/A

</td><td>

N/A

</td><td>

Horizontal

</td><td>

SAP Hana 2.0 DB Catalog \(pattern\)

</td></tr><tr><td>

[SAP Sybase ASE discovery](../../discovery/reference/r-Sybase.md)

</td><td>

Windows

 UNIX

</td><td>

16

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Sybase \(pattern\)

</td></tr><tr><td>

[SAP Sybase ASE discovery](../../discovery/reference/r-Sybase.md) catalog

</td><td>

UNIX

</td><td>

16

</td><td>

SSH

</td><td>

Horizontal

</td><td>

Sybase \(pattern extension\)

</td></tr><tr><td>

[Cisco Switch Wireless Access Point \(WAP\)](cisco-waps-discovery.md)

</td><td>

Cisco Network Switch

</td><td>

N/A

</td><td>

SNMP

</td><td>

Horizontal

</td><td>

WAP

</td></tr><tr><td>

Sun Directory Proxy Server

</td><td>

Solaris

</td><td>

4.0.8

</td><td>

SSH

</td><td>

Top-down

</td><td>

Sun Directory Proxy Server

</td></tr><tr><td>

Sun Java System Directory Server

</td><td>

Solaris

</td><td>

6.3

</td><td>

SSH

</td><td>

Top-down

</td><td>

Sun Directory Server

</td></tr><tr><td>

Thunder ADC

</td><td>

A10

</td><td>

2.x, 4.x

</td><td>

SNMP/SSH

</td><td>

Horizontal and top-down

</td><td>

A10 Load Balancer

</td></tr><tr><td>

Tibco ActiveMatrix Adapter

</td><td>

UNIX

</td><td>

7.1.0

</td><td>

SSH

</td><td>

Top-down

</td><td>

Tibco Adapter

</td></tr><tr><td>

[Tibco BusinessWorks](../concept/mapping-services-tibco.md#)

</td><td>

Windows

 UNIX

</td><td>

5.7.2

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal

</td><td>

ActiveMatrix Business Works

</td></tr><tr><td>

[Tibco Enterprise Message Service \(EMS\)](../concept/mapping-services-tibco.md#)

</td><td>

Windows

 UNIX

</td><td>

5.x, 6.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Enterprise Message Service

</td></tr><tr><td>

[Tibco Enterprise Message Service \(EMS\) Queue](../concept/mapping-services-tibco.md#)

</td><td>

Windows

 UNIX

</td><td>

5.x, 6.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Enterprise Message Service

</td></tr><tr><td>

Tibco Hawk

</td><td>

UNIX

</td><td>

5.2.0

</td><td>

SSH

</td><td>

Top-down

</td><td>

TibcoHawk

</td></tr><tr><td>

Veritas Enterprise Vault

</td><td>

Windows

</td><td>

14.1

</td><td>

WMI

 WinRM

</td><td>

Top-down

</td><td>

Enterprise Vault

</td></tr><tr><td>

[Veritas Cluster Server](../concept/veritas-cluster-server-discovery.md)

</td><td>

UNIX

</td><td>

6.x.x

</td><td>

SSH

</td><td>

Horizontal and top-down

</td><td>

Veritas Cluster

</td></tr><tr><td>

[VMware NSX Advanced Load Balancer](vmware-nsx-lb-discovery.md)

</td><td>

VMware

</td><td>

1

</td><td>

REST API

</td><td>

Horizontal and top-down

</td><td>

NSX

</td></tr></tbody>
</table>**Parent Topic:**[Data collected by ITOM Visibility](../../discovery/reference/data-collected-by-itom-visibility.md)


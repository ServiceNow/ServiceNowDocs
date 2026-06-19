---
title: Detailed information on products discovered by ITOM Visibility
description: Discovery and Service Mapping can discover a wide range of operating systems and applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/r\_SupportedApplications.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 77
keywords: [ITOM, Visibility, ServiceNow, Discovery, Cloud, API, Permissions, Patterns, AWS, Azure, GCP, IBM, Oracle, OCI]
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Detailed information on products discovered by ITOM Visibility

Discovery and Service Mapping can discover a wide range of operating systems and applications.

Discovery finds computers, servers, printers, a variety of IP-enabled devices, and the applications that run on them. It can then update the configuration items \(CIs\) in your Configuration Management Database \(CMDB\) with the data it collects. This discovery method is referred to as horizontal discovery. Service Mapping maps dependencies, based on a connection between devices and applications. This method is referred to as top-down mapping. The top-down mapping helps you immediately see the impact of a problematic object on the rest of the service instance operation.

On top of hosts and applications supported by default, you can discover additional hosts and applications by deploying patterns available on Store. For reference information on store released patterns, see [Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md).

If your organization uses devices or applications, which are not supported by default or using patterns available at ServiceNow Store, you can configure Discovery and Service Mapping to discover them as described in [Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md).

Cloud Discovery Patterns find the cloud resources of AWS, Azure, Google Cloud Platform \(GCP\), IBM, and Oracle.

If you want to validate the necessary pattern commands before running discovery, use the Command Validation Tool. For more information, see [Validate commands used in pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/validate-discovery-commands.md).

ITOM Content Service Provides visibility to your applications by using AI capabilities that cluster and classify running application processes. For more information, see [ITOM Content Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/discovery-content-services.md).

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

[A10 load balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoA10LoadBalancers.md)

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

[Adobe JRun](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-AdobeJRun.md)

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

[Apache Cassandra database and DataStax](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/cassandra-discovery.md)

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

[Apache HBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DiscoverHBaseInstances.md)

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

[Apache Kafka and Zookeeper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/kafka-zookeeper-discovery.md)

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

[Apache Tomcat Servlet container HTTP web server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoTomcatServers.md)

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

[Apigee Edge Enterprise edition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/apigee-edge-discovery.md)

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

[Avi Vantage load balancer including Avi Controller and GSLB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/avi-load-balancer-discovery.md)

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

[Alibaba Cloud availability zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-availability-zone.md)

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

[Alibaba Cloud cloud hardware type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-cloud-hardware-type.md)

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

[Alibaba Cloud cloud OS images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-cloud-os-image.md)

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

[Alibaba Cloud datacenters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-datacenter-discovery.md)

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

[Alibaba Cloud service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-service-account-discovery.md)

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

[Alibaba Cloud storage volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-storage-volume.md)

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

[Alibaba Cloud virtual machines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/alibaba-virtual-machine.md)

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

[Amazon API Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-api-gateway-discovery.md)

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

[Amazon API Gateway Domain Name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-api-gateway-domain-name.md)

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

[Amazon Athena Workgroups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-athena-workgroup.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Athena Workgroup - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Bedrock](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/amazon-bedrock-pattern.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Patterns:-   Amazon AWS - Bedrock Agents
-   Amazon AWS - Bedrock Foundation Model

</td></tr><tr><td>

[Amazon CloudFront Distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-cloudfront-distribution.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CloudFront Distribution - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon CloudWatch Log Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-cloudwatch-log-group.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CloudWatch Log Group - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Cognito](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws_cognito-discovery-pattern.md)

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

[Amazon DB cluster discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-db-cluster-discovery.md)

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

[Amazon DynamoDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-dynamoDB-discovery.md)

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

[Amazon DynamoDB Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-dynamodb-cluster.md)

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

[Amazon EC2 Amazon EBS Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-ec2-ebs-snapshot.md)

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

[Amazon EC2 Reserved Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-ec2-reserved-instance.md)

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

[Amazon EC2 VPC Endpoint Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-ec2-vpc-endpoint-service.md)

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

[Amazon EC2 VPC Peering Connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-ec2-vpc-peering-connection.md)

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

[Amazon ECS resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-ecs-fargate-discovery.md)

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

[Amazon Elastic File System \(Amazon EFS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-elastic-file-system.md)

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

[Amazon ElastiCache](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/amazon-aws-elasticache-discovery.md)

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

[Amazon ElastiCache Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-elasticache-snapshot.md)

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

[Amazon EMR Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-emr-cluster.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - EMR Cluster - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon EventBridge Event Bus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-eventbridge-event-bus.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - EventBridge Event Bus - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon FSx Backup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-fsx-backup.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - FSx Backup - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon FSx File System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-fsx-file-system.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - FSx File System - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon MQ Broker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-mq-broker.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - MQ Broker - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon MQ Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-mq-configuration.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - MQ Configuration - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon MWAA Environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-mwaa-environment.md)

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

[Amazon Relational Database Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-rds-discovery.md)

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

[Amazon RDS DB Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-rds-db-snapshot.md)

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

[Amazon Redshift](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/amazon-redshift-discovery.md)

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

[Amazon Redshift Serverless Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-redshift-serverless-namespace.md)

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

[Amazon Redshift Serverless Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-redshift-serverless-snapshot.md)

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

[Amazon Redshift Serverless Workgroup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-redshift-serverless-workgroup.md)

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

[Amazon Route 53](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-route-53-pattern.md)

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

[Amazon S3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-s3-discovery.md)

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

[Amazon S3 Glacier Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-s3-glacier-vault.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - S3 Glacier Vault - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon SageMaker Notebook Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-sagemaker-notebook-instance.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon SageMaker Training Job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-sagemaker-training-job.md)

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

[Amazon Simple Email Service Identity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-simple-email-service-identity.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Simple Email Service Identity - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon SQS Queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-sqs-queue.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - SQS Queue - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon Timestream for InfluxDB Database Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-timestream-influxdb-db-instance.md)

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

[Amazon VPC Flow Log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-vpc-flow-log.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - VPC Flow Log - Extended Inventory \(LP\)

</td></tr><tr><td>

[Amazon VPC Managed Prefix List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-vpc-managed-prefix-list.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - VPC Managed Prefix List - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS application ELB Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-application-elb-service-discovery.md)

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

[AWS AppSync API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-appsync-api.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - AppSync API - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Auto Scaling groups discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-auto-scaling-discovery.md)

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

[AWS Backup Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-backup-plan.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Backup Backup Plan - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Backup Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-backup-vault.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Backup Backup Vault - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Batch Compute Environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-batch-compute-environment.md)

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

[AWS classic ELB Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-classic-elb-service-discovery.md)

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

[AWS CloudHSM HSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-cloudhsm-hsm.md)

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

[AWS CloudTrail Trail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-cloudtrail-trail.md)

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

[AWS CodeDeploy Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-codedeploy-deployment.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CodeDeploy Deployment - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS CodePipeline Pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-codepipeline-pipeline.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - CodePipeline Pipeline - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-datacenter-pattern.md)

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

[AWS DataSync Task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-datasync-task.md)

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

[AWS DMS Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-dms-endpoint.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - DMS Endpoint - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Elastic Beanstalk Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-elastic-beanstalk-application.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Elastic Beanstalk Application - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Elastic Load Balancer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-application-elb-service-discovery.md)

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

[AWS Global Accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-global-accelerator.md)

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

[AWS Glue Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-glue-database.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Glue Database - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS hardware type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-hardware-type-pattern.md)

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

[AWS IAM Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-iam-policy.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - IAM Policy - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS IAM Role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-iam-role.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - IAM Role - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS IAM User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-iam-user.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - IAM User - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Keyspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/amazon-keyspaces-discovery.md)

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

[AWS Kinesis Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/amazon-kinesis-discovery.md)

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

[AWS KMS Key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-kms-key.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - KMS Key - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Lambda discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-lambda-discovery.md)

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

[AWS MemoryDB for Redis discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-memorydb-discovery.md)

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

[AWS Network Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-network-firewall.md)

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

[AWS OpenSearch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/amazon-opensearch-discovery.md)

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

[AWS Organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-organizations-pattern.md)

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

[AWS OS images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-os-image-pattern.md)

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

[AWS Resource Inventory discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-resource-inventory.md)

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

[AWS Secret Manager Secret](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-secrets-manager-secret.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Serverless Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-serverless-database-pattern.md)

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

[AWS Step Functions State Machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-step-functions-state-machine.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Step Functions State Machine - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Storage Gateway File Share](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-storage-gateway-file-share.md)

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

[AWS Storage Gateway Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-storage-gateway-gateway.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS sub accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-sub-account-pattern.md)

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

[AWS Systems Manager Document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-systems-manager-document.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Systems Manager Document - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Systems Manager Parameter Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-systems-manager-parameter-store.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Systems Manager Parameter Store - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Transfer Family Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-transfer-family-server.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - Transfer Family Server - Extended Inventory \(LP\)

</td></tr><tr><td>

[AWS Virtual Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-virtual-server-pattern.md)

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

[AWS X-Ray Sampling Rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-xray-sampling-rule.md)

</td><td>

AWS

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Amazon AWS - XRay Sampling Rule - Extended Inventory \(LP\)

</td></tr><tr><td>

[Azure App Configuration store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-configuration-store.md)

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

[Azure App Service App Service Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-service-plan.md)

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

[Azure Application Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-application-gateway-discovery.md)

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

[Azure Application Insight Component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-insight-component.md)

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

[Azure Application Insight Data Collection Rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-insight-data-collect-rule.md)

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

[Azure Application Security Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-app-security-group.md)

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

[Azure Automation Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-automation-account.md)

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

[Azure availability sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-availability-sets-patterns.md)

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

[Azure availability zones](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-availability-zones-patterns.md)

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

[Azure Blob Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-blob-storage-pattern.md)

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

[Azure Classic Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-classic-load-balancer-pattern.md)

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

[Azure Compute Gallery Image Definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-compute-gallery-img-definition.md)

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

[Azure Compute Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-compute-snapshot.md)

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

[Azure Container Registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-container-registry.md)

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

[Azure Cosmos DB for PostgreSQL Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cosmos-db-postgresql-cluster.md)

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

[Azure Data Explorer Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-data-explorer-cluster.md)

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

[Azure Data Factory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-data-factory.md)

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

[Azure Data Protection Backup Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-data-protection-backup-vault.md)

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

[Azure Database Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/data-collected-azure-discovery.md)

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

[Azure Databricks Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-databricks-workspace.md)

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

[Azure Datacenter discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-datacenter-discovery-pattern.md)

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

[Azure Dev Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-dev-center.md)

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

[Azure Disk Encryption Set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-disk-encryption-set.md)

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

[Azure DNS zones and record sets discovery using Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-dns-discovery.md)

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

[Azure Event Grid System Topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-event-grid-pattern.md)

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

[Azure Event Hub Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-event-hub-namespace.md)

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

[Azure Express Route Circuit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-express-route-circuit-pattern.md)

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

[Azure File Share](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-file-share-pattern.md)

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

[Azure Firewall Network Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-firewall-network-security.md)

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

[Azure Functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-function-discovery.md)

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

[Azure hardware type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-hardware-type-pattern.md)

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

[Azure Host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-host-pattern.md)

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

[Azure Key Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-key-vault.md)

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

[Azure Key Vault Key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-key-vault-key.md)

</td><td>

Microsoft Azure

</td><td>

N/A

</td><td>

REST

</td><td>

Horizontal

</td><td>

Azure - Key Vault Key - Extended Inventory\(LP\)

</td></tr><tr><td>

[Azure LoadBalancer Service TD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-classic-load-balancer-pattern.md)

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

[Azure Local Network Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-local-network-gateway-pattern.md)

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

[Azure Log Analytics Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-log-analytics-workspace.md)

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

[Azure Logic App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-logic-app.md)

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

[Azure Managed Identity User Assigned Identity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-managed-id-user-assigned-id.md)

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

[Azure NAT Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-nat-gateway-pattern.md)

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

[Azure Networks IP Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-networks-ip-group.md)

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

[Azure OS image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-os-image-pattern.md)

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

[Azure Private DNS Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-private-dns-zone-pattern.md)

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

[Azure Private Link Private Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-private-link-private-endpoint.md)

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

[Azure Recovery Services Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-recovery-services-vault.md)

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

[Azure Recovery Services Vault Backup Item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-recovery-services-vault-backup.md)

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

[Azure Resource Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-resource-inventory-pattern.md)

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

[Azure Service Bus Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-service-bus-namespace.md)

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

[Azure Service Bus Queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-service-bus-queue.md)

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

[Azure Service Bus Topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-service-bus-topic.md)

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

[Azure Service Endpoint Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-service-endpoint-policy.md)

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

[Azure Subscriptions Discovery For Management Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-sub-mgmt-group-pattern.md)

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

[Azure Virtual Machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vm-pattern.md)

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

[Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/AzureVMScaleSetInstance.md)

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

[Azure Virtual Network Gateway Connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vng-connection-pattern.md)

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

[Azure Web Application Firewall Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-web-app-firewall-policy.md)

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

[Azure WebSite Service and Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

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

[Cisco Content Services Switch Load balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_LoadBalancerCSS.md)

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

[Cisco ACE Application Control Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ace-load-balancer-discovery.md)

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

[Cisco Global Site Selector Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_LoadBalancerGSS.md)

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

[Cisco Unified Computing System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-CiscoUCSHD.md)

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

[Citrix Delivery Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/citrix-lic-server-deliv-controller.md)

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

[Citrix Netscaler SDX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/citrix-netscaler-sdx-discovery.md)

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

[Citrix License Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/citrix-lic-server-deliv-controller.md)

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

[Citrix Xen Hyper-V](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/citrix-xen-hyper-v-discovery.md)

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

[Cloudian Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/cloudian-storage-discovery.md)

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

[Container image scanning for software decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/container-image-concept.md)

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

[Software Bill of Material \(SBOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/generate-sbom-pattern.md)

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

[Docker virtualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c-docker-virtualization.md)

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

[Database Administrator \(DBA\) report discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/dba-report-discovery-pattern.md)

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

[Dell PowerMax storage discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/emc-powermax-discovery-pattern.md)

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

[Dell Data Domain storage discovery using Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/emc-data-domain-pattern.md)

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

[Dell EMC XtremIO storage array discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/xtreamio-storage-array-discovery.md)

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

[EMC Isilon](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/emc-isilon-discovery.md)

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

[F5 BIG-IP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_LoadBalancerF5BIGIP.md)

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

[Fortinet firewalls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/fortinet-fw-discovery.md)

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

[Fortinet firewalls and FortiGate VDOMs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/fortinet-fw-vdoms-rest-discovery.md)

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

[Google Cloud Platform \(GCP\) AlloyDB for PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-alloydb-postgresql-patterns.md)

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

[Google Cloud BigQuery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-bigquery-db-pattern.md)

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

[Google Cloud Bigtable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-bigtable-db-pattern.md)

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

[Google Cloud FireStore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-firestore-db-pattern.md)

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

[Google Cloud Platform \(GCP\) Cloud Functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-cloud-functions-patterns.md)

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

[Google Cloud SQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-cloud-sql-db-pattern.md)

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

[Google Cloud Platform \(GCP\) Disk Types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-disk-types-pattern.md)

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

[Google Cloud Platform \(GCP\) Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-events-pattern.md)

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

[Google Cloud Platform \(GCP\) External IP Addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-external-ip-addresses-pattern.md)

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

[Google Firebase Realtime DB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-firebase-realtime-db-pattern.md)

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

[Google Cloud Platform \(GCP\) Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-load-balancer-pattern.md)

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

[Google Cloud Platform \(GCP\) Memorystore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-memorystore-patterns.md)

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

[Google Cloud Platform \(GCP\) Networking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-networking-pattern.md)

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

[Google Cloud Platform \(GCP\) Organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/google-gcp-organization-discovery.md)

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

[Google Cloud Platform \(GCP\) resource inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-resource-inventory-discovery.md)

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

[Google Cloud Spanner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-spanner-db-pattern.md)

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

[Google Cloud Platform \(GCP\) SSH Keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-ssh-keys-pattern.md)

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

[Google Cloud Platform \(GCP\) storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-storage-pattern.md)

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

[Google Cloud Platform \(GCP\) Virtual Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/gcp-virtual-server-pattern.md)

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

[HAProxy Community edition load balancers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/haproxy-lb-discovery-pattern.md)

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

[HP Operations Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-HPOP.md)

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

[HP Service Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-HPServiceManager.md)

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

[IBM Cloud Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/google-gcp-discovery-pattern.md)

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

[IBM Db2 on Unix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm-db2-linux-discovery.md)

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

[IBM Db2 on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm-db2-windows-discovery.md)

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

[IBM Virtualization and Hardware Management Console \(HMC\) components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm-hmc-discovery.md)

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

[IBM PowerHA Cluster \(HACMP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm-powerha-hamcp-discovery.md)

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

[IBM WebSEAL discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm_webseal_discovery_patterns.md)

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

[IBM App Connect Enterprise and HTTP listener discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_IBMWMB.md)

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

[Infini-Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/infinibox-discovery.md)

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

[Istio Service Mash](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/kubernetes-discovery.md)

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

[Kubernetes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/kubernetes-discovery.md)

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

[Linux Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

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

[Linux Pacemaker Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/linux-pacemaker-cluster-discovery.md)

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

[Microsoft Certificate Authority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/microsoft-ca-discovery.md)

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

[Microsoft Foundry \(Classic\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/microsoft-foundry-classic-pattern.md)

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
-   Azure - AI Foundry Models

</td></tr><tr><td>

[Microsoft Hyper-V Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DiscoveryForHyperV.md)

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

[Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-MSSharepoint.md)

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

[Microsoft SQL Server and Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/mssql-data-collected-pattern.md)

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

[Microsoft SQL Server Analysis Services \(SSAS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-SSAS-MSSQL.md)

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

[Microsoft SQL Server Integration Services \(SSIS\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ms-ssis-pattern.md)

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

[MongoDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DiscoverMongoDBInstances.md)

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

[NetApp Server and Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/netapp-discovery.md)

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

[NetApp Server and Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/netapp-discovery.md)

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

[NetApp SolidFire storage system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/solidfire-storage-pattern.md)

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

[Network router](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/network-router-patterns.md)

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

[Network switch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/network-switch-patterns.md)

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

[NGINX Web Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_NGINXWebServerDiscovery.md)

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

[Nutanix Acropolis \(AOS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

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

[Nutanix Prism Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

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

[OpenStack resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/openstack-discovery.md)

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

[Oracle Cloud Infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

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

[Oracle Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_OracleDatabaseDiscovery.md)

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

[Oracle Database 12c](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-cdb-pdb-discovery.md)

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

[Oracle GoldenGate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-golden-gate-discovery.md)

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

[Oracle Linux Virtualization Manager \(OLVM\) and Red Hat Virtualization \(RHV\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/red-hat-virtualization-discovery.md)

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

[Oracle Global License Advisory Services \(GLAS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md)

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

[Oracle Java processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md)

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

[Oracle Solaris LDOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/solaris-ldom-discovery.md)

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

[Oracle Listener](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-listener-hd-discovery.md)

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

[Oracle Solaris Logical Domain infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/solaris-ldom-discovery.md)

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

[Pivotal Cloud Foundry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/pivotal-cloud-foundry.md)

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

[Pure Storage FlashArray discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/flasharray-discovery.md)

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

[Pure Storage FlashBlade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/pure-storage-discovery.md)

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

[Radware Alteon RadWare ADC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/alteon-load-balancer-discovery.md)

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

[RadWare AppDirector Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/radware-appdirector.md)

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

[Red Hat JBoss Application Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_DataCollDiscoJBossServers.md)

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

[Red Hat JBoss Fuse discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/jboss-fuse-discovery.md)

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

[Red Hat OpenShift components of Kubernetes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/kubernetes-discovery.md)

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

[Rubrik cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.md)

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

[SAP HANA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/sap-discovery.md)

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

[SAP HANA Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/sap-discovery.md)

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

[SAP Sybase ASE discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-Sybase.md)

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

[SAP Sybase ASE discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r-Sybase.md) catalog

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

[Cisco Switch Wireless Access Point \(WAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/cisco-waps-discovery.md)

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

[Tibco BusinessWorks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/mapping-services-tibco.md)

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

[Tibco Enterprise Message Service \(EMS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/mapping-services-tibco.md)

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

[Tibco Enterprise Message Service \(EMS\) Queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/mapping-services-tibco.md)

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

[Veritas Cluster Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/veritas-cluster-server-discovery.md)

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

[VMware NSX Advanced Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/vmware-nsx-lb-discovery.md)

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

</td></tr><tr><td>

[VMware NSX-T infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nsx-t-cluster-pattern.md)

</td><td>

VMware

</td><td>

1

</td><td>

REST API

</td><td>

Horizontal

</td><td>

NSX Cluster

</td></tr></tbody>
</table>**Parent Topic:**[Data collected by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/data-collected-by-itom-visibility.md)


---
title: Supported Wiz types
description: The Wiz types and corresponding native types are imported as CMDB data and saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-types.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Supported Wiz types

The Wiz types and corresponding native types are imported as CMDB data and saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

For information on Wiz types and Wiz native types, see [Security Graph Object Normalization](https://integrate.wiz.io/docs/security-graph-object-normalization) on the Wiz documentation site \(requires Wiz login\).

<table id="table_tvd_3tq_k1c"><thead><tr><th>

Wiz types

</th><th>

Wiz native types

</th><th>

CMDB CI classes

</th></tr></thead><tbody><tr><td rowspan="2">

Cloud Organization

</td><td>

AWS OrganizationGCP Organization

</td><td>

[Cloud Organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

GCP Folder

</td><td>

[Google Organization Folder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td rowspan="6">

Subscription

</td><td>

AWS Account

</td><td rowspan="2">

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Subscription

</td></tr><tr><td>

GCP Project

</td><td>

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

 [Google Organization Project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

OCI Compartment​

</td><td rowspan="3">

[VMware vCenter Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Alibaba Account​

</td></tr><tr><td>

vSphere Datacenter​

</td></tr><tr><td rowspan="5">

Region

</td><td>

AWS Region

</td><td>

[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Location

</td><td>

[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

GCP Region

</td><td>

[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

OCI Region​

</td><td>

[OCI Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Alibaba Region

</td><td>

[Logical Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Resource Group

</td><td>

Azure Resource Group

</td><td>

[Resource Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td rowspan="2">

Compute Instance Group

</td><td>

AWS Auto Scaling Group​

</td><td rowspan="2">

[Instance Scale Set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Compute Virtual Machine Scale Set

</td></tr><tr><td rowspan="3">

Network Interface

</td><td>

AWS Network Interface

</td><td rowspan="3">

[Cloud Mgmt Network Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Network Interface

</td></tr><tr><td>

GCP Compute Network Interface

</td></tr><tr><td rowspan="2">

Virtual Network

</td><td>

AWS VPC

</td><td rowspan="2">

[Cloud Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Virtual Network

</td></tr><tr><td rowspan="5">

Firewall

</td><td>

AWS EC2 Security Group

</td><td rowspan="5">

[Compute Security Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Network Security Group

</td></tr><tr><td>

GCP Firewall

</td></tr><tr><td>

OCI Network Security Group​

</td></tr><tr><td>

OCI Security List

</td></tr><tr><td rowspan="4">

Volume

</td><td>

AWS EC2 Volume \(EBS\)

</td><td rowspan="3">

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS Lightsail Disk

</td></tr><tr><td>

Azure Disk

</td></tr><tr><td>

GCP Compute Disk

</td><td>

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md), [Cloud Disk Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td rowspan="8">

Virtual Machine

</td><td>

AWS EC2 Instance

</td><td rowspan="8">

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md), [Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md), [Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS Lightsail Instance

</td></tr><tr><td>

Azure Scale Set Virtual Machine

</td></tr><tr><td>

Azure Compute Virtual Machine

</td></tr><tr><td>

GCP Compute Instance

</td></tr><tr><td>

OCI Compute Instance​

</td></tr><tr><td>

Alibaba ECS Instance

</td></tr><tr><td>

vSphere Virtual Machine

</td></tr><tr><td rowspan="16">

Snapshot

</td><td>

AWS EBS Unencrypted Snapshot​

</td><td rowspan="16">

[Storage Volume Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS DB Cluster Snapshot​​

</td></tr><tr><td>

AWS DB Instance Snapshot​

</td></tr><tr><td>

AWS DocumentDB Elastic Cluster Snapshot​

</td></tr><tr><td>

AWS EBS Encrypted Snapshot​

</td></tr><tr><td>

AWS Elasticache Snapshot​

</td></tr><tr><td>

AWS MemoryDB Snapshot​

</td></tr><tr><td>

AWS DynamoDB Backup​

</td></tr><tr><td>

AWS Neptune Analytics Graph Snapshot​

</td></tr><tr><td>

AWS Redshift Cluster Snapshot​

</td></tr><tr><td>

Azure Compute Public Snapshot​

</td></tr><tr><td>

Azure SQL LTR Backup​

</td></tr><tr><td>

GCP Compute Snapshot​

</td></tr><tr><td>

GCP AlloyDB Backup​

</td></tr><tr><td>

GCP Cloud SQL Backup​

</td></tr><tr><td>

GCP Cloud SQL Backup Run

</td></tr><tr><td rowspan="2">

Gateway

</td><td>

AWS Egress Only Internet Gateway​

</td><td rowspan="2">

[Internet Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS VPN Gateway

</td></tr><tr><td rowspan="4">

Virtual Machine Image

</td><td>

AWS Machine Image \(AMI\)

</td><td rowspan="4">

[Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Compute Virtual Machine Image

</td></tr><tr><td>

Azure Compute Gallery VM image version

</td></tr><tr><td>

GCP Compute Image

</td></tr><tr><td rowspan="10">

Load Balancer

</td><td>

AWS ELB v1

</td><td rowspan="10">

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS ELB V2 Application Load Balancer

</td></tr><tr><td>

AWS ELB V2 Gateway Load Balancer

</td></tr><tr><td>

AWS ELB V2 Network Load Balancer

</td></tr><tr><td>

AWS ELB V2

</td></tr><tr><td>

Azure Application Gateway

</td></tr><tr><td>

Azure Load Balancer

</td></tr><tr><td>

Azure Traffic Manager

</td></tr><tr><td>

GCP Compute Backend Service

</td></tr><tr><td>

GCP Compute Region Backend Service

</td></tr><tr><td rowspan="3">

Bucket

</td><td>

AWS S3 Bucket​

</td><td rowspan="3">

[Cloud Object Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Blob Storage Container​

</td></tr><tr><td>

GCP Bucket​

</td></tr><tr><td rowspan="3">

Serverless

</td><td>

AWS Lambda Function​

</td><td rowspan="3">

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Function

</td></tr><tr><td>

GCP Cloud Function

</td></tr><tr><td rowspan="31">

Database

</td><td>

AWS DynamoDB Table

</td><td>

[DynamoDB Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS ElastiCache for Memcached Cluster

</td><td rowspan="14">

[Cloud DataBase Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS ElastiCache Redis OSS Cluster

</td></tr><tr><td>

AWS ElastiCache Valkey Cluster​

</td></tr><tr><td>

AWS Elastic DocumentDB Cluster​

</td></tr><tr><td>

AWS RDS Aurora MySQL Cluster

</td></tr><tr><td>

AWS DocumentDB Cluster

</td></tr><tr><td>

AWS MemoryDB Cluster​

</td></tr><tr><td>

AWS RDS MSSQL Server Cluster

</td></tr><tr><td>

AWS RDS MariaDB Cluster

</td></tr><tr><td>

AWS RDS MySQL Cluster

</td></tr><tr><td>

AWS Neptune Cluster

</td></tr><tr><td>

AWS RDS Oracle Cluster

</td></tr><tr><td>

AWS RDS PostgreSQL Cluster

</td></tr><tr><td>

AWS RDS Aurora PostgreSQL Cluster​

</td></tr><tr><td>

Azure Cosmos DB SQL Database

</td><td rowspan="16">

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Cosmos DB Cassandra Keyspace

</td></tr><tr><td>

Azure MariaDB Database

</td></tr><tr><td>

Azure Cosmos DB MongoDB Collection

</td></tr><tr><td>

Azure Cosmos DB for PostgreSQL Node

</td></tr><tr><td>

Azure Database for MySQL Database

</td></tr><tr><td>

Azure Database for MySQL Flexible Database

</td></tr><tr><td>

Azure Database for PostgreSQL Database

</td></tr><tr><td>

Azure Database for PostgreSQL Flexible Database

</td></tr><tr><td>

Azure Redis Database

</td></tr><tr><td>

Azure Redis Enterprise Database

</td></tr><tr><td>

Azure Synapse Dedicated SQL Pool

</td></tr><tr><td>

Azure Databricks Schema

</td></tr><tr><td>

Azure SQL Database

</td></tr><tr><td>

Azure SQL Managed Instance Database

</td></tr><tr><td>

Azure Data Explorer Kusto Database Instance

</td></tr><tr><td rowspan="3">

Bucket

</td><td>

AWS S3 Bucket

</td><td rowspan="3">

[Cloud Object Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Blob Storage Container

</td></tr><tr><td>

GCP Bucket

</td></tr><tr><td rowspan="3">

Serverless

</td><td>

AWS Lambda Function

</td><td rowspan="3">

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Function

</td></tr><tr><td>

GCP Cloud Function

</td></tr><tr><td rowspan="5">

Network Address

</td><td>

AWS Elastic IP Address

</td><td rowspan="5">

[Cloud Public IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure CDN Endpoint

</td></tr><tr><td>

Azure Public IP Addresses

</td></tr><tr><td>

GCP Compute Address

</td></tr><tr><td>

GCP Endpoint

</td></tr><tr><td>

Storage Account

</td><td>

Azure Storage Account

</td><td>

[Cloud Storage Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td rowspan="3">

API Gateway

</td><td>

AWS API Gateway

</td><td rowspan="3">

[Cloud Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS API Gateway V2

</td></tr><tr><td>

Azure API Management

</td></tr><tr><td rowspan="4">

Kubernetes Cluster

</td><td>

AWS Elastic Kubernetes Service \(EKS\) Cluster

</td><td rowspan="4">

[Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Azure Kubernetes Service \(AKS\) Cluster

</td></tr><tr><td>

GCP Kubernetes Engine \(GKE\) Cluster

</td></tr><tr><td>

Kubernetes Cluster

</td></tr><tr><td>

Namespace

</td><td>

Kubernetes Namespace

</td><td>

[Kubernetes Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Kubernetes Node

</td><td>

Kubernetes Node

</td><td>

[Kubernetes Node](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Deployment

</td><td>

Kubernetes Deployment

</td><td>

[Kubernetes Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Kubernetes Service

</td><td>

Kubernetes Service

</td><td>

[Kubernetes Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Pod

</td><td>

Kubernetes Pod

</td><td>

[Kubernetes Pod](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

Replica Set

</td><td>

Kubernetes Replica Set

</td><td>

[Kubernetes ReplicaSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td rowspan="4">

Container

</td><td>

Kubernetes Container

</td><td rowspan="4">

[Docker Container](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-wiz-classes.md)

</td></tr><tr><td>

AWS ECS Container

</td></tr><tr><td>

Azure ACA Container

</td></tr><tr><td>

Azure ACI Container

</td></tr></tbody>
</table>
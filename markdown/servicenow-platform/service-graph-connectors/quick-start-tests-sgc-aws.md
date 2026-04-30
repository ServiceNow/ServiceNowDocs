---
title: Quick start tests for Service Graph Connector for AWS
description: Validate that Service Graph Connector for AWS still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Service Graph Connector for AWS

Validate that Service Graph Connector for AWS still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

|Test|Description|Release version|
|----|-----------|---------------|
|SG-AWS API Gateway|Validate the ingestion of multiple CI records in the Cloud Gateway.|Utah|
|SG-AWS DynamoDb|Validate the ingestion of multiple CI records in the DynamoDB table.|Utah|
|SG-AWS EC2|Loads data in the CMDB such as all dependent CIs such as Organizations, Service-Accounts, Networks, Subnets, and Network-Interfaces, after which mock data for SG-AWS-EC2 is prepared.|Utah|
|SG-AWS EKS Cluster|Validates the ingestion of multiple CI records in the Kubernetes Cluster table.|Utah|
|SG-AWS ELB V1|Validates the ingestion of multiple CI records in the Cloud Load Balancer.|Utah|
|SG-AWS ELB V2|Validates the ingestion of multiple CI records in the Cloud Load Balancer.|Utah|
|SG-AWS Generic Resource|Validates the ingestion of multiple CI records in the Cloud Resource table.|Utah|
|SG-AWS Hardware Type|Validates the ingestion of multiple CI records in the Hardware Type table.|Utah|
|SG-AWS Image Id|Validates the ingestion of multiple CI records in the Image table.|Utah|
|SG-AWS Image Private|Validates the ingestion of multiple CI records in the Image table.|Utah|
|SG-AWS Lambda|Validates the ingestion of multiple CI records in the Cloud function table.|Utah|
|SG-AWS Network Interface|Validates the ingestion of multiple CI records in the Cloud Mgmt Network Interface table.|Utah|
|SG-AWS Organization|Tests RTE mappings for the ingestion of CIs in the Cloud Organization table.|Utah|
|SG-AWS RDS|Validates the ingestion of mutliple CI records in the Cloud Database table.|Utah|
|SG-AWS S3|Validates the ingestion of multiple CI records in the Cloud Object Storage table.|Utah|
|SG-AWS Security Group|Validates the ingestion of multiple CI records in the Compute Security Group table.|Utah|
|SG-AWS Service Account|Tests RTE mappings for the ingestion of CIs in the Cloud Service Account table.|Utah|
|SG-AWS Software Inventory|Validates the ingestion of Software Data and classification of CI records in the Server table. It tests whether the server is classified as Linux or Windows.|Utah|
|SG-AWS Software Remove|Validates the removal of Software Data from the cmdb\_software\_instance or the cmdb\_sam\_sw\_install table.|Utah|
|SG-AWS Storage Volume|Loads mock import data for Storage Volume into the relevant staging table. Validates if fields are populated as expected in the cmdb\_ci\_storage\_volume, cmdb\_ci\_storage\_vol\_snapshot, and sn\_aws\_extension\_attributes tables and if the appropriate relationships have been created between the inserted CIs.|Utah|
|SG-AWS SSM SendCommand|Validates the ingestion of multiple CI records in the TCP Connection and Running Process tables. Updates records in the Server table.|Utah|
|SG-AWS Subnets|Validates the ingestion of multiple CIs in the Cloud Subnet table.|Utah|
|SG-AWS VM Hw Consolidation|Validates the update of multiple CI records in the Virtual Machine Instance and Server table.|Utah|
|SG-AWS VPC|Tests RTE mappings associated with SG-AWS VPC Data source. It loads import set data for VPCs, Datacenters, Service-Acccount, and Organizations. Validates if the CIs have been added to the cmdb\_ci\_network table, the fields are populated with the expected value, and appropriate relationships verified through the cmdb\_rel\_ci table.|Utah|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)


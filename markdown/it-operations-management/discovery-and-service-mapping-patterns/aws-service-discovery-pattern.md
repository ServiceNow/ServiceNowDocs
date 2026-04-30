---
title: AWS Services discovery using patterns
description: Discovery and Service Mapping Patterns application uses Amazon AWS service patterns to discover Amazon AWS Services during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-04-03"
reading_time_minutes: 8
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Services discovery using patterns

Discovery and Service Mapping Patterns application uses Amazon AWS service patterns to discover Amazon AWS Services during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The latest version of Discovery and Service Mapping Patterns supports discovering the following Amazon AWS Services:

-   AppSync API
-   Athena workgroup
-   Backup plan
-   Backup vault
-   CloudFront distribution
-   CloudWatch Logs
-   CodeDeploy deployment
-   CodePipeline pipeline
-   Database Migration Service \(DMS\) endpoints
-   Elastic BeanStalk Application
-   EMR cluster \(running on EC2\)
-   EventBridge Event Bus
-   FSx backup
-   FSx file system
-   Glue database
-   IAM policy
-   IAM role
-   IAM user
-   KMS key
-   MQ Broker
-   MQ configuration
-   S3 Glacier Vault
-   SageMaker notebook instance
-   Secrets Manager secret
-   Simple Email Service \(SES\) Identity
-   SQS Queue
-   Step Functions State Machine
-   Storage Gateway gateway
-   Systems Manager Document
-   Systems Manager Parameter Store
-   Transfer Family server
-   VPC Flow Log
-   VPC-managed prefix list
-   X-Ray sampling rule

Discovery and Service Mapping Patterns supports AWS GovCloud \(US\) accounts for the following services:

-   AppSync API
-   Elastic BeanStalk Application
-   EventBridge Event Bus
-   MQ Broker
-   SQS Queue
-   Step Functions State Machine
-   Storage Gateway gateway

Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Set up AWS service accounts](../../it-operations-management/concept/setup-aws-service-accounts.md).

## Prerequisites

-   **Verify Amazon AWS discovery prerequisites**

    For more information, see the prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [Amazon Web Services \(AWS\) Resource Inventory](aws-resource-inventory.md).

-   **Enable the relevant pattern**

    The Discovery and Service Mapping Patterns for these services are disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../task/activate-disabled-pattern.md).


## Data collected by Discovery during horizontal discovery

Discovery populates data for each of the patterns in non-CMDB tables. These tables are listed under **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

![AWS Athena Workgroup non-CMDB table navigation](../image/aws-athena-workgroup-navigation.png "Navigation example for non-CMDB table AWS Athena Workgroup")

Discovery populates data in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] CMDB table when running the following patterns:

-   Amazon AWS - Athena Workgroup - Extended Inventory \(LP\)
-   Amazon AWS - Backup Backup Plan - Extended Inventory \(LP\)
-   Amazon AWS - Backup Backup Vault - Extended Inventory \(LP\)
-   Amazon AWS - CloudFront Distribution - Extended Inventory \(LP\)
-   Amazon AWS - CloudWatch Log - Extended Inventory \(LP\)
-   Amazon AWS - CodeDeploy Deployment - Extended Inventory \(LP\)
-   Amazon AWS - CodePipeline Pipeline - Extended Inventory \(LP\)
-   Amazon AWS - DMS Endpoint - Extended Inventory \(LP\)
-   Amazon AWS - EMR Cluster - Extended Inventory \(LP\)
-   Amazon AWS - FSx Backup - Extended Inventory \(LP\)
-   Amazon AWS - FSx File System - Extended Inventory \(LP\)
-   Amazon AWS - Glue Database - Extended Inventory \(LP\)
-   Amazon AWS - IAM Policy - Extended Inventory \(LP\)
-   Amazon AWS - IAM Role - Extended Inventory \(LP\)
-   Amazon AWS - IAM User - Extended Inventory \(LP\)
-   Amazon AWS - KMS Key - Extended Inventory \(LP\)
-   Amazon AWS - MQ Configuration - Extended Inventory \(LP\)
-   Amazon AWS - S3 Glacier Vault - Extended Inventory \(LP\)
-   Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\)
-   Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\)
-   Amazon AWS - Simple Email Service Identity - Extended Inventory \(LP\)
-   Amazon AWS - Systems Manager Document - Extended Inventory \(LP\)
-   Amazon AWS - Systems Manager Parameter Store - Extended Inventory \(LP\)
-   Amazon AWS - Transfer Family Server - Extended Inventory \(LP\)
-   Amazon AWS - VPC Flow Log - Extended Inventory \(LP\)
-   Amazon AWS - VPC Managed Prefix List - Extended Inventory \(LP\)
-   Amazon AWS - XRay Sampling Rule - Extended Inventory \(LP\)

<table id="table_jmw_wjp_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the AWS resource.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Amazon Resource Name \(ARN\) for the AWS resource.

</td></tr><tr><td>

Resource type \[resource\_type\]

</td><td>

Type of resource, in the following format— **Vendor::Service::Component**.For example, for the DMS endpoint resource, the value is set to **AWS::DMS::Endpoint**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value: Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value: Operational.

</td></tr></tbody>
</table>Discovery populates the data in various CMDB tables when running the following patterns.

-   **Amazon AWS - AppSync API - Extended Inventory \(LP\)**

<table id="table_qg4_mws_n2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the AWS AppSync API, which is the GraphQL interface.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ARN for the API.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of resource, in the following format— **Vendor::Service::Component**. The value is set to **AWS::AppSync::API**.

</td></tr></tbody>
</table>-   **Amazon AWS - Elastic BeanStalk Application - Extended Inventory \(LP\)**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the application.|
    |Object ID \[object\_id\]|ARN of the application.|

-   **Amazon AWS - EventBridge Event Bus - Extended Inventory \(LP\)**

<table id="table_p2w_zxs_n2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the event bus.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ARN of the event bus.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of resource, in the following format— **Vendor::Service::Component**. The value is set to **AWS::EventBridge::EventBus**.

</td></tr></tbody>
</table>-   **Amazon AWS - MQ Broker - Extended Inventory \(LP\)**

<table id="table_ajs_mys_n2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the MQ Broker. This value must be unique in the AWS account, between 1-50 characters long, and contain only letters, numbers, dashes, and underscores. For example: MyActiveMQBroker.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ARN of the MQ Broker.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of broker engine. For example: ACTIVEMQ or RABBITMQ.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the broker engine.

</td></tr></tbody>
</table>-   **Amazon AWS - SQS Queue - Extended Inventory \(LP\)**

<table id="table_u5t_nzs_n2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the queue for which you want to fetch the URL. The name can be up to 80 characters long.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ARN of the queue.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of resource, in the following format— **Vendor::Service::Component**. The value is set to **AWS::SQS::Queue**.

</td></tr></tbody>
</table>-   **Amazon AWS - Step Functions State Machine - Extended Inventory \(LP\)**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the state machine.|
    |Object ID \[object\_id\]|ARN of the state machine.|
    |Edition \[edition\]|Edition of the state machine. Possible values: STANDARD or EXPRESS.|

-   **Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\)**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name you configured for your gateway.|
    |Object ID \[object\_id\]|ARN of the gateway.|
    |Environment \[environment\]|Type of hardware or software platform on which the gateway runs.|


## CI relationships

Discovery creates these relationships to support the Amazon AWS Services discovery.

These relationships support the discovery of AWS Services when running the following patterns.

-   Amazon AWS - Athena Workgroup - Extended Inventory \(LP\)
-   Amazon AWS - Backup Backup Plan - Extended Inventory \(LP\)
-   Amazon AWS - Backup Backup Vault - Extended Inventory \(LP\)
-   Amazon AWS - CloudFront Distribution - Extended Inventory \(LP\)
-   Amazon AWS - CloudWatch Log - Extended Inventory \(LP\)
-   Amazon AWS - CodeDeploy Deployment - Extended Inventory \(LP\)
-   Amazon AWS - CodePipeline Pipeline - Extended Inventory \(LP\)
-   Amazon AWS - DMS Endpoint - Extended Inventory \(LP\)
-   Amazon AWS - EMR Cluster - Extended Inventory \(LP\)
-   Amazon AWS - FSx Backup - Extended Inventory \(LP\)
-   Amazon AWS - FSx File System - Extended Inventory \(LP\)
-   Amazon AWS - Glue Database - Extended Inventory \(LP\)
-   Amazon AWS - IAM Policy - Extended Inventory \(LP\)
-   Amazon AWS - IAM Role - Extended Inventory \(LP\)
-   Amazon AWS - IAM User - Extended Inventory \(LP\)
-   Amazon AWS - KMS Key - Extended Inventory \(LP\)
-   Amazon AWS - MQ Configuration - Extended Inventory \(LP\)
-   Amazon AWS - S3 Glacier Vault - Extended Inventory \(LP\)
-   Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\)
-   Amazon AWS - Secrets Manager Secret - Extended Inventory \(LP\)
-   Amazon AWS - Simple Email Service Identity - Extended Inventory \(LP\)
-   Amazon AWS - Systems Manager Document - Extended Inventory \(LP\)
-   Amazon AWS - Systems Manager Parameter Store - Extended Inventory \(LP\)
-   Amazon AWS - Transfer Family Server - Extended Inventory \(LP\)
-   Amazon AWS - VPC Flow Log - Extended Inventory \(LP\)
-   Amazon AWS - VPC Managed Prefix List - Extended Inventory \(LP\)
-   Amazon AWS - XRay Sampling Rule - Extended Inventory \(LP\)

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

These relationships support the discovery of AWS Services when running the following patterns.

-   **Amazon AWS - AppSync API - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - Elastic Beanstalk Application - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud App Server \[cmdb\_ci\_cloud\_appserver\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - EventBridge Event Bus - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - MQ Broker - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - SQS Queue - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - Step Functions State Machine - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\)**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|


## AWS Tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


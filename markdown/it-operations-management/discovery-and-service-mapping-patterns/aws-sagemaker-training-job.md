---
title: Amazon SageMaker Training Job pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 3
keywords: [AWS, Discovery, ITOM, Pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon SageMaker Training Job pattern-based discovery

Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md).

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns](../service-mapping/reference/aws-resource-inventory.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](../it-operations-management/task/create-aws-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - SageMaker Training Job - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object Id \[object\_id\]|The Amazon Resource Name \(ARN\) uniquely identifying the training job.|
|Name \[name\]|The user-defined name for the training job.|
|Configuration Item \[configuration\_item\]|References the Cloud App Server \[cmdb\_ci\_cloud\_appserver\] table.|
|Secondary Status \[secondary\_status\]|The additional status information providing more detail about the training job's progress.|
|Training Job Status \[training\_job\_status\]|The current status of the training job.|
|Training Plan ARN \[training\_plan\_arn\]|The ARN of the training plan associated with the job.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - SageMaker Training Job - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The ARN uniquely identifying the training job.|
|Name \[name\]|The user-defined name for the training job.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Type \[type\]|Type of resource. The value is set to **AWS::SageMaker::Training Job**.|

## CI relationships

The Amazon AWS - SageMaker Training Job - Extended Inventory \(LP\) pattern creates these relationships to support Amazon SageMaker Training Job discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud App Server \[cmdb\_ci\_cloud\_appserver\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|AWS SageMaker - Training Job \[cmdb\_aws\_sagemaker\_training\_job\]|References|Cloud App Server \[cmdb\_ci\_cloud\_appserver\]|

## AWS tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md)


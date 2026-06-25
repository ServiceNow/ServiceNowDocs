---
title: Amazon SageMaker Notebook Instance pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon SageMaker Notebook Instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-sagemaker-notebook-instance.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [Amazon SageMaker Notebook Instance, AWS SageMaker discovery, AWS patterns, SageMaker Extended Inventory]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon SageMaker Notebook Instance pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon SageMaker Notebook Instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the notebook instance.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the notebook instance.

</td></tr><tr><td>

Instance Status \[instance\_status\]

</td><td>

The current status of the notebook instance. For example: InService, Pending, Stopped, Stopping, or Failed.

</td></tr><tr><td>

Kms Key Id \[kms\_key\_id\]

</td><td>

The ARN of the AWS KMS key used to encrypt the notebook instance's storage volume. This field is empty if no KMS key is configured.

</td></tr><tr><td>

Default Code Repository \[default\_code\_repository\]

</td><td>

The name or URL of the Git repository associated with the notebook instance as its default code repository.

</td></tr><tr><td>

Root Access \[root\_access\]

</td><td>

Indicates whether root access is enabled for the notebook instance. The value is Enabled or Disabled.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the notebook instance.|
|Object ID \[object\_id\]|The ARN of the notebook instance.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **AWS::SageMaker::NotebookInstance**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\) pattern creates the following relationships and references to support Amazon SageMaker Notebook Instance discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS SageMaker Notebook Instance \[cmdb\_aws\_sagemaker\_notebook\_instance\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## AWS Tag discovery

The Amazon AWS - SageMaker Notebook Instance - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)


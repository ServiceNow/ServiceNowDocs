---
title: AWS Storage Gateway Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Storage Gateway Gateways on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-storage-gateway-gateway.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 4
keywords: [AWS Storage Gateway Gateway, AWS Storage Gateway discovery, AWS patterns, Storage Gateway Extended Inventory]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Storage Gateway Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Storage Gateway Gateways on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the gateway.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the gateway.

</td></tr><tr><td>

Gateway ID \[gateway\_id\]

</td><td>

The unique identifier of the gateway.

</td></tr><tr><td>

Gateway Type \[gateway\_type\]

</td><td>

The type of the gateway. For example: STORED, CACHED, VTL, FILE\_S3, or FILE\_FSX\_SMB.

</td></tr><tr><td>

Gateway State \[gateway\_state\]

</td><td>

The current state of the gateway. The value is RUNNING or SHUTDOWN.

</td></tr><tr><td>

Host Environment \[host\_environment\]

</td><td>

The host environment in which the gateway is running. For example: EC2, VMWARE, HYPER-V, KVM, SNOWBALL, or OTHER.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Gateway \[cmdb\_ci\_cloud\_gateway\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\) pattern.

<table id="table_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the gateway.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ARN of the gateway.

</td></tr><tr><td>

Environment \[environment\]

</td><td>

The host environment in which the gateway is running. For example: EC2, VMWARE, HYPER-V, KVM, SNOWBALL, or OTHER.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Type of resource. The value is set to **AWS::StorageGateway::Gateway**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\) pattern creates the following relationships and references to support AWS Storage Gateway Gateway discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS Storage Gateway Gateway \[cmdb\_aws\_storage\_gateway\_gateway\]|Configuration Item \[configuration\_item\]|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|

## AWS Tag discovery

The Amazon AWS - Storage Gateway Gateway - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Gateway \[cmdb\_ci\_cloud\_gateway\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)


---
title: Amazon FSx File System pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon FSx File Systems on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-fsx-file-system.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [Amazon FSx File System, AWS FSx discovery, AWS patterns, FSx Extended Inventory]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon FSx File System pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon FSx File Systems on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - FSx File System - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The ID of the file system, used as the display name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the file system.

</td></tr><tr><td>

File System Id \[file\_system\_id\]

</td><td>

The ID of the file system.

</td></tr><tr><td>

File System Type \[file\_system\_type\]

</td><td>

The type of file system. For example: WINDOWS, LUSTRE, ONTAP, or OPENZFS.

</td></tr><tr><td>

File System Type Version \[file\_system\_type\_version\]

</td><td>

The version of the file system type.

</td></tr><tr><td>

Lifecycle \[lifecycle\]

</td><td>

The lifecycle status of the file system. For example: AVAILABLE, CREATING, DELETING, FAILED, MISCONFIGURED, or UPDATING.

</td></tr><tr><td>

Owner Id \[owner\_id\]

</td><td>

The ID of the AWS account that owns the file system.

</td></tr><tr><td>

DNS Name \[dns\_name\]

</td><td>

The Domain Name System \(DNS\) name for the file system.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - FSx File System - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The ID of the file system, used as the display name.|
|Object ID \[object\_id\]|The ARN of the file system.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **AWS::FSx::FileSystem**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - FSx File System - Extended Inventory \(LP\) pattern creates the following relationships and references to support Amazon FSx File System discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS FSx File System \[cmdb\_aws\_fsx\_file\_system\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## AWS Tag discovery

The Amazon AWS - FSx File System - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)


---
title: AWS Transfer Family Server pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Transfer Family Servers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-transfer-family-server.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [AWS Transfer Family Server, AWS Transfer Family discovery, AWS patterns, Transfer Family Extended Inventory]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Transfer Family Server pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Transfer Family Servers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - Transfer Family Server - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The server ID, used as the display name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the server.

</td></tr><tr><td>

Server ID \[server\_id\]

</td><td>

The unique identifier of the Transfer Family server.

</td></tr><tr><td>

Endpoint Type \[endpoint\_type\]

</td><td>

The type of endpoint for the server. The value is PUBLIC, VPC, or VPC\_ENDPOINT.

</td></tr><tr><td>

Identity Provider Type \[identity\_provider\_type\]

</td><td>

The mode of authentication for the server. For example: SERVICE\_MANAGED, API\_GATEWAY, AWS\_DIRECTORY\_SERVICE, or AWS\_LAMBDA.

</td></tr><tr><td>

State \[state\]

</td><td>

The current state of the server. For example: ONLINE, OFFLINE, STARTING, STOPPING, START\_FAILED, or STOP\_FAILED.

</td></tr><tr><td>

User Count \[user\_count\]

</td><td>

The number of users assigned to the server.

</td></tr><tr><td>

Logging Role \[logging\_role\]

</td><td>

The ARN of the IAM role used to write transfer activity to Amazon CloudWatch Logs.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Transfer Family Server - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The server ID, used as the display name.|
|Object ID \[object\_id\]|The ARN of the server.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **AWS::TransferFamily::Server**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - Transfer Family Server - Extended Inventory \(LP\) pattern creates the following relationships and references to support AWS Transfer Family Server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS Transfer Family Server \[cmdb\_aws\_transfer\_family\_server\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## AWS Tag discovery

The Amazon AWS - Transfer Family Server - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)


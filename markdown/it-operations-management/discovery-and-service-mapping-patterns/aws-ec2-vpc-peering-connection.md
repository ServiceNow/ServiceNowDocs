---
title: Amazon Elastic Compute Cloud \(EC2\) virtual private cloud \(VPC\) Peering Connection pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 3
keywords: [AWS, Discovery, ITOM, Pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Elastic Compute Cloud \(EC2\) virtual private cloud \(VPC\) Peering Connection pattern-based discovery

Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [Amazon AWS Cloud components discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md).

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [Amazon Web Services \(AWS\) Resource Inventory](../service-mapping/reference/aws-resource-inventory.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](../it-operations-management/task/create-aws-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - Elastic Compute Cloud VPC Peering Connection - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object Id \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) uniquely identifying the VPC Peering Connection.The ARN consists of the region, account ID, and VPC ID in the following format: **arn:aws:ec2:&lt;region&gt;:&lt;accountId&gt;:vpc-peering-connection/&lt;vpc\_id&gt;**.

</td></tr><tr><td>

Name \[name\]

</td><td>

The unique identifier of the VPC involved in the peering connection.

</td></tr><tr><td>

Status \[status\]

</td><td>

The current status of the VPC peering connection.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Gateway \[cmdb\_ci\_cloud\_gateway\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Elastic Compute Cloud VPC Peering Connection - Extended Inventory \(LP\) pattern.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The ARN uniquely identifying the VPC Peering Connection.The ARN consists of the region, account ID, and VPC ID in the following format: **arn:aws:ec2:&lt;region&gt;:&lt;accountId&gt;:vpc-peering-connection/&lt;vpc\_id&gt;**.

</td></tr><tr><td>

Name \[name\]

</td><td>

The unique identifier of the VPC involved in the peering connection.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Type of resource. The value is set to **AWS::EC2::VPCPeeringConnection**.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Elastic Compute Cloud VPC Peering Connection - Extended Inventory \(LP\) pattern creates these relationships to support Amazon EC2 VPC Peering Connection discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|AWS Elastic Compute Cloud - VPC Peering Connection \[cmdb\_aws\_elastic\_compute\_cloud\_vpc\_peering\_connection\]|References|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|

## AWS tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../service-mapping/concept/available-patterns.md)


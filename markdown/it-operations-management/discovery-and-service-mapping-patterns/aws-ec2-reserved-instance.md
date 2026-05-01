---
title: Amazon Elastic Compute Cloud \(EC2\) Reserved Instance pattern-based discovery
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

# Amazon Elastic Compute Cloud \(EC2\) Reserved Instance pattern-based discovery

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

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - Elastic Compute Cloud Reserved Instance - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object Id \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) uniquely identifying the Reserved Instance.The ARN consists of the region, account ID, and instance ID in the following format: **arn:aws:ec2:&lt;region&gt;:&lt;accountId&gt;:reserved-instances/&lt;instance\_id&gt;**.

</td></tr><tr><td>

Name \[name\]

</td><td>

The unique identifier assigned to the EC2 instance.

</td></tr><tr><td>

State \[state\]

</td><td>

The current status or lifecycle state of the EC2 instance.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.

</td></tr><tr><td>

Instance Type \[instance\_type\]

</td><td>

The type of EC2 instance. For example: t2.micro or m5.large.

</td></tr><tr><td>

Scope \[scope\]

</td><td>

The reservation scope. For example: Regional or Availability Zone.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Elastic Compute Cloud Reserved Instance - Extended Inventory \(LP\) pattern.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The ARN uniquely identifying the Reserved Instance.The ARN consists of the region, account ID, and instance ID in the following format: **arn:aws:ec2:&lt;region&gt;:&lt;accountId&gt;:reserved-instances/&lt;instance\_id&gt;**.

</td></tr><tr><td>

Name \[name\]

</td><td>

The unique identifier assigned to the EC2 instance.

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

Type of resource. The value is set to **AWS::Elastic Compute Cloud::Reserved Instance**.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Elastic Compute Cloud Reserved Instance - Extended Inventory \(LP\) pattern creates these relationships to support Amazon EC2 Reserved Instance discovery.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|AWS Elastic Compute Cloud - Reserved Instance \[cmdb\_aws\_elastic\_cloud\_compute\_reserved\_instance\]|References|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## AWS tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md)


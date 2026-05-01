---
title: Amazon Elastic Compute Cloud \(EC2\) Amazon Elastic Block Store \(EBS\) Snapshot pattern-based discovery
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

# Amazon Elastic Compute Cloud \(EC2\) Amazon Elastic Block Store \(EBS\) Snapshot pattern-based discovery

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


## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - Elastic Compute Cloud EBS Snapshot - Extended Inventory \(LP\) pattern.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) uniquely identifying the EBS Snapshot.The ARN consists of the AWS region, account ID, and snapshot ID in the following format: **arn:aws:ec2:&lt;region&gt;:&lt;accountId&gt;:snapshot/&lt;snapshot\_id&gt;**.

</td></tr><tr><td>

Name \[name\]

</td><td>

The unique identifier for the EC2 snapshot.

</td></tr><tr><td>

State \[state\]

</td><td>

The current state of the snapshot. For example: pending or completed.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Encrypted \[is\_encrypted\]

</td><td>

Indicates whether the snapshot is encrypted.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Type of resource. The value is set to **AWS::Elastic Compute Cloud::EBS Snapshot**.

</td></tr><tr><td>

Size \(GB\) \[size\]

</td><td>

The size of the resource expressed in gigabytes \(GB\).

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

The size of the snapshot in bytes.

</td></tr><tr><td>

Volume Name \[volume\_name\]

</td><td>

The identifier of the volume associated with the snapshot.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Elastic Compute Cloud EBS Snapshot - Extended Inventory \(LP\) pattern creates these relationships to support Amazon EC2 Amazon EBS Snapshot discovery.

|CI|Relationship|CI|
|---|------------|---|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## AWS tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md)


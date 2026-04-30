---
title: AWS sub account pattern-based discovery
description: Discovery and Service Mapping Patterns finds member accounts and the primary account within an AWS Organization. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-25"
reading_time_minutes: 1
keywords: [Amazon AWS sub account discovery, AWS Organizations, AWS discovery, AWS patterns, AWS sub accounts, AWS member accounts]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS sub account pattern-based discovery

Discovery and Service Mapping Patterns finds member accounts and the primary account within an AWS Organization. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS sub account discovery pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Id \[account\_id\]

</td><td>

The unique identifier \(ID\) of the AWS account.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name assigned to the account.

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

Type of datacenter. The value is set to **AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]**.

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

The URL of the AWS datacenter.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The unique ID of the AWS account.

</td></tr><tr><td>

Is management account \[is\_master\_account\]

</td><td>

Indicates whether this account is the management \(primary\) account of the organization. -   **true**: Management account
-   **false**: Member account

</td></tr><tr><td>

Discovery credentials \[discovery\_credentials\]

</td><td>

AWS credential from the Credentials \[discovery\_credentials\] table.

</td></tr><tr><td>

Parent account \[parent\_account\]

</td><td>

References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table \(management account\).

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS sub account discovery pattern creates these relationships to support AWS sub account discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(management account\)|Members::Member of|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(member account\)|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(member account\)|References|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(management account\)|
|Key Value \[cmdb\_key\_value\]|References|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(member account\)|

## AWS tag discovery

The Amazon AWS sub account discovery pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table \(member account\).|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


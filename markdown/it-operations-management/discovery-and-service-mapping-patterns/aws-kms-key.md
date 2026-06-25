---
title: AWS KMS Key pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS KMS Keys on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-kms-key.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 4
keywords: [AWS KMS Key, AWS KMS Key discovery, AWS patterns, KMS Key pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS KMS Key pattern-based discovery

Discovery and Service Mapping Patterns finds AWS KMS Keys on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - KMS Key - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the KMS Key.

</td></tr><tr><td>

Name \[name\]

</td><td>

The ARN of the KMS Key.

</td></tr><tr><td>

Arn \[arn\]

</td><td>

The ARN of the KMS Key.

</td></tr><tr><td>

Key ID \[key\_id\]

</td><td>

The unique identifier of the KMS Key.

</td></tr><tr><td>

Key State \[key\_state\]

</td><td>

The current state of the KMS Key. For example: Enabled, Disabled, or PendingDeletion.

</td></tr><tr><td>

Enabled \[enabled\]

</td><td>

Indicates whether the KMS Key is enabled.

</td></tr><tr><td>

Description \[description\]

</td><td>

Description of the KMS Key.

</td></tr><tr><td>

Key Algorithm \[key\_algorithm\]

</td><td>

The cryptographic algorithm of the key.For example: SYMMETRIC\_DEFAULT, RSA\_2048, or ECC\_NIST\_P256.

</td></tr><tr><td>

Key Usage \[key\_usage\]

</td><td>

The cryptographic operations for which the key can be used. For example: ENCRYPT\_DECRYPT, SIGN\_VERIFY, or GENERATE\_VERIFY\_MAC.

</td></tr><tr><td>

Origin \[origin\]

</td><td>

The source of the key material. For example: AWS\_KMS or EXTERNAL, or AWS\_CLOUDHSM.

</td></tr><tr><td>

Multi Region \[multi\_region\]

</td><td>

Indicates whether the key is a multi-Region key.

</td></tr><tr><td>

Multi Region Key Type \[multi\_region\_key\_type\]

</td><td>

The type of multi-Region key. For example: PRIMARY or REPLICA.

</td></tr><tr><td>

Primary Key \[primary\_key\]

</td><td>

Details of the primary key for a replica key, including the ARN and Region.

</td></tr><tr><td>

Replica Keys \[replica\_keys\]

</td><td>

Details of the replica keys for a primary key, including the ARNs and Regions.

</td></tr><tr><td>

Encryption Algorithms \[encryption\_algorithms\]

</td><td>

The encryption algorithms supported by the key.

</td></tr><tr><td>

Signing Algorithms \[signing\_algorithms\]

</td><td>

The signing algorithms supported by the key.

</td></tr><tr><td>

MAC Algorithms \[mac\_algorithms\]

</td><td>

The MAC algorithms supported by the key.

</td></tr><tr><td>

Created Date \[created\_date\]

</td><td>

Date and time when the KMS Key was created.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - KMS Key - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The ARN of the KMS Key.|
|Object ID \[object\_id\]|The ARN of the KMS Key.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **AWS::KMS::Key**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - KMS Key - Extended Inventory \(LP\) pattern creates the following relationships and references to support AWS KMS Key discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS KMS Key \[cmdb\_aws\_kms\_key\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## AWS Tag discovery

The Amazon AWS - KMS Key - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)


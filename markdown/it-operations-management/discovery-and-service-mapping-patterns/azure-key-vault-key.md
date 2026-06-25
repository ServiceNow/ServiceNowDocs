---
title: Azure Key Vault Key pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Key Vault Keys on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-key-vault-key.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-28"
reading_time_minutes: 4
keywords: [Azure Key Vault Key, Azure Key Vault Key discovery, Azure patterns, Key Vault pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Key Vault Key pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Key Vault Keys on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

The Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Key Vault Key - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Key Vault Key.

</td></tr><tr><td>

Object Id \[object\_id\]

</td><td>

Unique identifier for the Key Vault Key, in the format of the Azure Resource Manager \(ARM\) resource ID followed by /keys/&lt;key-name&gt;.For example: **/subscriptions/&lt;subscription-id&gt;/resourceGroups/&lt;resource-group&gt;/providers/Microsoft.KeyVault/vaults/&lt;vault-name&gt;/keys/&lt;key-name&gt;**.

</td></tr><tr><td>

Key ID \[key\_id\]

</td><td>

The versioned URI of the key in Azure Key Vault.

</td></tr><tr><td>

Key Type \[key\_type\]

</td><td>

The cryptographic algorithm of the key. For example: RSA or EC.

</td></tr><tr><td>

Curve \[curve\]

</td><td>

The elliptic curve name for EC keys. For example: P-256 or P-384.

</td></tr><tr><td>

Key Ops \[key\_ops\]

</td><td>

The operations permitted for the key. For example: **sign,verify** or **sign,verify,wrapKey,unwrapKey,encrypt,decrypt**.

</td></tr><tr><td>

Key Size \[key\_size\]

</td><td>

The size of the key in bits.

</td></tr><tr><td>

Enabled \[enabled\]

</td><td>

Indicates whether the key is enabled.

</td></tr><tr><td>

Recovery Level \[recovery\_level\]

</td><td>

The deletion recovery level for the key.For example: Recoverable, Purgeable, or Recoverable+Purgeable.

</td></tr><tr><td>

Created Date \[created\_date\]

</td><td>

Date and time when the key was created.

</td></tr><tr><td>

Updated Date \[updated\_date\]

</td><td>

Date and time when the key was last updated.

</td></tr><tr><td>

Expiration Date \[expiration\_date\]

</td><td>

Date and time when the key expires.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

The Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Key Vault Key - Extended Inventory\(LP\) pattern.

<table id="table_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Key Vault Key.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the Key Vault Key, in the format of the ARM resource ID followed by /keys/&lt;key-name&gt;.For example: **/subscriptions/&lt;subscription-id&gt;/resourceGroups/&lt;resource-group&gt;/providers/Microsoft.KeyVault/vaults/&lt;vault-name&gt;/keys/&lt;key-name&gt;**.

</td></tr><tr><td>

Resource type \[resource\_type\]

</td><td>

The Azure resource type: **microsoft.keyvault/vaults/keys**.

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

The Azure - Key Vault Key - Extended Inventory\(LP\) pattern creates the following relationships and references to support Azure Key Vault Key discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Members::Member of|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Azure Key Vault - Key \[cmdb\_azure\_key\_vault\_key\]|Configuration Item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## Azure Tag discovery

The Azure - Key Vault Key - Extended Inventory\(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


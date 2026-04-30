---
title: Azure Compute Snapshot pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Compute Snapshot pattern-based discovery

Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud components discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](../it-operations-management/task/setup-azure-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Compute Snapshot - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Disk State \[disk\_state\]|The current state of the disk. For example: Attached or Unattached.|
|Encryption Type \[encryption\_type\]|The encryption mechanism applied to the resource data. For example: EncryptionAtRestWithCustomerKey or EncryptionAtRestWithPlatformKey.|
|DC Location \[location\]|The geographic location where the resource is deployed.|
|Network Access Policy \[network\_access\_policy\]|The policy that governs network access to the resource.|
|Object Id \[object\_id\]|A unique identifier for the queried resource.|
|OS Type \[os\_type\]|The type of operating system associated with the resource.|
|Provisioning State \[provisioning\_state\]|Current provisioning state of the resource. For example: Succeeded or Failed.|
|Public Network Access \[public\_network\_access\]|Indicates whether the resource can be accessed via the public network.|
|Resource Group \[resource\_group\]|Name of the resource group.|
|SKU Tier \[sku\_tier\]|The tier of the stock keeping unit \(SKU\) that determines resource performance and costs.|
|Subscription Id \[subscription\_id\]|The subscription ID.|
|Tenant Id \[tenant\_id\]|The unique identifier of the tenant owning the resource.|
|Type \[type\]|The type or category of the resource.|
|Configuration Item \[configuration\_item\]|References the Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\] table.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Compute Snapshot - Extended Inventory\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Capacity \[capacity\]|The size of the disk in terms of storage capacity.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Location \[location\]|The geographic location where the resource is deployed.|
|Name \[name\]|The name of the resource.|
|Object ID \[object\_id\]|A unique identifier for the queried resource in the following format: **/subscriptions/\{subscriptionId\}/resourceGroups/\{resouceGroupName\}/providers/Microsoft.Compute/snapshots/\{snapshotName\}**.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|State \[state\]|The current state of the disk. For example: Attached or Unattached.|

## CI relationships

The pattern creates these relationships to support discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Compute - Snapshot \[cmdb\_azure\_compute\_snapshot\]|References|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|

## Azure tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../service-mapping/concept/available-patterns.md)


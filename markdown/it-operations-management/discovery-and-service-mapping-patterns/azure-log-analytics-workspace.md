---
title: Azure Log Analytics Workspace pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Log Analytics Workspace pattern-based discovery

Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](../it-operations-management/task/setup-azure-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Log Analytics Workspace - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object Id \[object\_id\]|The unique identifier of the Azure resource.|
|Kind \[kind\]|The specific kind or variant of the resource.|
|DC Location \[location\]|The geographical region where the resource is deployed.|
|Resource Group \[resource\_group\]|The Azure resource group to which the resource belongs.|
|Subscription Id \[subscription\_id\]|The unique identifier of the Azure subscription containing the resource.|
|Tenant Id \[tenant\_id\]|The identifier of the Azure Active Directory tenant associated with the resource.|
|Provisioning State \[provisioning\_state\]|The current lifecycle state of the resource. For example: Succeeded, Creating, or Failed.|
|Configuration Item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|
|Customer Id \[customer\_id\]|The unique identifier of the Log Analytics workspace or customer instance.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Log Analytics Workspace - Extended Inventory\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique identifier of the Azure resource.|
|Name \[name\]|The name of the resource.|
|Location \[location\]|The geographical region where the resource is deployed.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **microsoft.operationalinsights/workspaces**.|

## CI relationships

The Azure - Log Analytics Workspace - Extended Inventory\(LP\) pattern creates these relationships to support Azure Log Analytics Workspace discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Log Analytics - Workspace \[cmdb\_azure\_log\_analytics\_workspace\]|References|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## Azure tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md)


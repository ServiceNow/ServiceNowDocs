---
title: Azure Application Insight Data Collection Rule pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern, Azure Application Insight Data Collection Rule]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Application Insight Data Collection Rule pattern-based discovery

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

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Application Insight Data Collection Rule - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object Id \[object\_id\]|The unique resource identifier for the Azure resource.|
|Kind \[kind\]|The specific resource kind or stock-keeping unit \(SKU\), indicating variation within the type.|
|DC Location \[location\]|The Azure region where the resource is deployed.|
|Resource Group \[resource\_group\]|The name of the resource group containing the resource.|
|Subscription Id \[subscription\_id\]|The unique identifier \(GUID\) for the Azure subscription.|
|Tenant Id \[tenant\_id\]|The Azure Active Directory tenant identifier associated with the resource.|
|Provisioning State \[provisioning\_state\]|The current provisioning or deployment status of the resource.|
|Configuration Item \[configuration\_item\]|References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Application Insight Data Collection Rule - Extended Inventory\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique resource identifier for the Azure resource.|
|Name \[name\]|The name assigned to the resource.|
|Location \[location\]|The Azure region where the resource is deployed.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Resource type \[resource\_type\]|Type of resource. The value is set to **microsoft.insights/datacollectionrules**.|

## CI relationships

The Azure - Application Insight Data Collection Rule - Extended Inventory\(LP\) pattern creates these relationships to support Azure Application Insight Data Collection Rule discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Application Insight Data Collection Rule \[cmdb\_azure\_application\_insight\_data\_collection\_rule\]|References|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

## Azure tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../service-mapping/concept/available-patterns.md)


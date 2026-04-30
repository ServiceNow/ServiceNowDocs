---
title: Azure Cosmos DB for PostgreSQL Cluster pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Cosmos DB for PostgreSQL Cluster pattern-based discovery

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

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Cosmos DB for PostgreSQL Cluster - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object Id \[object\_id\]|The unique identifier of the resource.|
|Kind \[kind\]|The specific kind or stock-keeping unit \(SKU\) of the resource.|
|DC Location \[location\]|The Azure region where the resource is deployed.|
|Resource Group \[resource\_group\]|The name of the Azure resource group containing the resource.|
|Subscription Id \[subscription\_id\]|The unique identifier for the Azure subscription.|
|Tenant Id \[tenant\_id\]|The universally unique identifier \(UUID\) of the Azure Active Directory tenant associated with the resource.|
|Provisioning State \[provisioning\_state\]|The current state of the provisioning process for the resource.|
|Configuration Item \[configuration\_item\]|References the Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\] table.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Cosmos DB for PostgreSQL Cluster - Extended Inventory\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name assigned to the resource.|
|Location \[location\]|The Azure region where the resource is deployed.|
|Cluster ID \[cluster\_id\]|The unique identifier of the resource.|
|Cluster Status \[cluster\_status\]|The current operational status of the cluster.|
|Cluster Version \[cluster\_version\]|The version number of the cluster software.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Description \[short\_description\]|Type of resource. The value is set to **microsoft.dbforpostgresql/servergroupsv2**.|
|Vendor \[vendor\]|Name of vendor: Microsoft.|

## CI relationships

The Azure - Cosmos DB for PostgreSQL Cluster - Extended Inventory\(LP\) pattern creates these relationships to support Azure Cosmos DB for PostgreSQL Cluster discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Cosmos DB for PostgreSQL Cluster \[cmdb\_azure\_cosmos\_db\_for\_postgresql\_cluster\_cluster\]|References|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|

## Azure tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Available discovery patterns](../service-mapping/concept/available-patterns.md)


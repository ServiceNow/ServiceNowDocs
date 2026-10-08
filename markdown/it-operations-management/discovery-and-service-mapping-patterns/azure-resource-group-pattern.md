---
title: Azure Resource Group pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Resource Groups in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-resource-group-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure Resource Group, Azure discovery, Azure patterns, Resource Group pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Resource Group pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Resource Groups in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Resource Group \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the resource group.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the resource group.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Location \[location\]|References the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table.|

## CI relationships and references

The Azure - Resource Group \(LP\) pattern creates the following relationships and references to support Azure Resource Group discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Resource Group \[cmdb\_ci\_resource\_group\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Resource Group \[cmdb\_ci\_resource\_group\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Location \[location\]|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Azure Tag discovery

The Azure - Resource Group \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Resource Group \[cmdb\_ci\_resource\_group\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


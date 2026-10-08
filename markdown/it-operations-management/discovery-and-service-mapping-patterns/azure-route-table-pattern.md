---
title: Azure Route Table pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Route Tables in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-route-table-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure Route Table, Azure discovery, Azure patterns, Route Table pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Route Table pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Route Tables in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Route Table \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the route table.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the route table.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the route.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Destination \[destination\]|The datacenter location of the route.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships and references

The Azure - Route Table \(LP\) pattern creates the following relationships and references to support Azure Route Table discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Route Table \[cmdb\_ci\_route\_table\]|Contains::Contained by|Route \[cmdb\_ci\_route\]|
|Route Table \[cmdb\_ci\_route\_table\]|Contains::Contained by|Cloud Network \[cmdb\_ci\_network\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Route Table \[cmdb\_ci\_route\_table\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Route Table \[cmdb\_ci\_route\_table\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Route Table \[cmdb\_ci\_route\_table\]|

## Azure Tag discovery

The Azure - Route Table \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Route Table \[cmdb\_ci\_route\_table\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


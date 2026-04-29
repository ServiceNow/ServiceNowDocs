---
title: Azure Private Domain Name System \(DNS\) Zone pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Private DNS Zone resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Azure - Private DNS Zone \(LP\), Azure Private DNS Zones, Azure discovery, Azure patterns]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Private Domain Name System \(DNS\) Zone pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Private DNS Zone resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Private DNS Zone \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique Azure resource identifier for the Private DNS Zone.|
|Name \[name\]|The name of the Private DNS Zone resource.|
|State \[state\]|The operational state of the Private DNS Zone.|
|Number Of RecordSets \[number\_of\_recordsets\]|The number of DNS record sets within the Private DNS Zone.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Private DNS Zone \(LP\) pattern creates these relationships to support Azure Private DNS Zone discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|DNS Zone \[cmdb\_ci\_dns\_zone\]|
|DNS Zone \[cmdb\_ci\_dns\_zone\]|Connected by::Connects|Cloud Network \[cmdb\_ci\_network\]|
|Key Value \[cmdb\_key\_value\]|References|DNS Zone \[cmdb\_ci\_dns\_zone\]|

## Azure Tag discovery

The Azure - Private DNS Zone \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the DNS Zone \[cmdb\_ci\_dns\_zone\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)


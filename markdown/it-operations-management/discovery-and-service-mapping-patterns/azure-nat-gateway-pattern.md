---
title: Azure Network Address Translation \(NAT\) Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure NAT Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure - NAT Gateway \(LP\), Azure NAT Gateways, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Network Address Translation \(NAT\) Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds Azure NAT Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - NAT Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique Azure resource identifier for the NAT Gateway.|
|Name \[name\]|The name of the NAT Gateway resource.|
|State \[state\]|The operational state of the NAT Gateway.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - NAT Gateway \(LP\) pattern creates these relationships to support Azure NAT Gateway discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|
|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Uses::Used by|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|
|Key Value \[cmdb\_key\_value\]|References|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|

## Azure Tag discovery

The Azure - NAT Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the NAT Gateway \[cmdb\_ci\_nat\_gateway\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


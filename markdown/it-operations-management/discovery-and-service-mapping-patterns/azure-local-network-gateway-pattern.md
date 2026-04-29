---
title: Azure Local Network Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Local Network Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Azure - Local Network Gateway \(LP\), Azure Local Network Gateways, Azure discovery, Azure patterns]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Local Network Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Local Network Gateway resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Local Network Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique Azure resource identifier for the Local Network Gateway.|
|Name \[name\]|The name of the Local Network Gateway resource.|
|State \[state\]|The operational state of the Local Network Gateway.|
|IP Address \[ip\_address\]|The IP address of the on-premises VPN device that the Local Network Gateway connects to.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Local Network Gateway \(LP\) pattern creates these relationships to support Azure Local Network Gateway discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|

## Azure Tag discovery

The Azure - Local Network Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)


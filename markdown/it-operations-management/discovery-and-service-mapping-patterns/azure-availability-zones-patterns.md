---
title: Azure availability zones discovery using patterns
description: Discovery and Service Mapping Patterns uses the Azure - Availability Zones \(LP\) pattern to discover Azure availability zones during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-08-03"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure availability zones discovery using patterns

Discovery and Service Mapping Patterns uses the Azure - Availability Zones \(LP\) pattern to discover Azure availability zones during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Availability Zones \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]​|Name of the availability zone in the following format: **\{Location\} + "-"  + \{ZoneNum\}**.|
|Name \[name\]|Name of the availability zone in the following format: **\{Location\} + "-" + \{ZoneNum\}**.|
|Install Status \[install\_status\]|Install status of the availability zone. Default value is Installed.|

## CI relationships

Discovery creates these relationships to support the Azure availability zone discovery.

|CI|Relationship|CI|
|---|------------|---|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)


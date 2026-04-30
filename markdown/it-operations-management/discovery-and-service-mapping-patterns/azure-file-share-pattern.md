---
title: Azure File Share pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure File Share resources within Storage Accounts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure - File Share \(LP\), Azure File Shares, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure File Share pattern-based discovery

Discovery and Service Mapping Patterns finds Azure File Share resources within Storage Accounts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - File Share \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique Azure resource identifier for the File Share.|
|Name \[name\]|The name of the File Share resource.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - File Share \(LP\) pattern creates these relationships to support Azure File Share discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud File Service \[cmdb\_ci\_cloud\_file\_service\]|Contains::Contained by|Cloud File Share \[cmdb\_ci\_cloud\_file\_share\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


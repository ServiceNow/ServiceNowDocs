---
title: Azure availability sets discovery using patterns
description: Discovery and Service Mapping Patterns uses the Azure - Availability Set \(LP\) pattern to discover Azure availability sets during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-availability-sets-patterns.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-08-03"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure availability sets discovery using patterns

Discovery and Service Mapping Patterns uses the Azure - Availability Set \(LP\) pattern to discover Azure availability sets during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Availability Set \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]​|A unique identifier, allocated by Microsoft Azure for this resource.|
|Name \[name\]|The Name or ID if no Name is specified for the availability zone.|
|Install Status \[install\_status\]​|Resource provisioning status.|

## CI relationships

Discovery creates these relationships to support the Azure availability sets discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Availability Set \[cmdb\_ci\_availability\_set\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Availability Set \[cmdb\_ci\_availability\_set\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


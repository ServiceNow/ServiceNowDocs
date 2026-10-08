---
title: Azure Storage Containers pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Storage Containers in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-container-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [Azure Storage Containers, Azure discovery, Azure patterns, Storage Container pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Storage Containers pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Storage Containers in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Storage Container\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the storage container.|
|Object ID \[object\_id\]|A unique identifier for the storage container.|
|State \[state\]|The lease state of the storage container.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Storage Container\(LP\) pattern creates the following relationships to support Azure Storage Containers discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Object Service \[cmdb\_ci\_cloud\_object\_service\]|Contains::Contained by|Storage Container \[cmdb\_ci\_storage\_container\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


---
title: Azure Storage Volume pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Storage Volumes \(managed disks\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-volume-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 2
keywords: [Azure Storage Volume, Azure managed disk, Azure discovery, Azure patterns, Storage Volume pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Storage Volume pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Storage Volumes \(managed disks\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/setup-azure-service-accounts.md).

-   **\(Optional\) Exclude temporary Azure Databricks VMs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can reduce short-lived configuration item \(CI\) records by excluding temporary Azure Databricks VMs. For more information, see [Exclude temporary Azure Databricks virtual machines]().


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Storage Volume \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the storage volume.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Volume ID \[volume\_id\]|The resource ID of the storage volume.|
|State \[state\]|The current state of the storage volume. Possible values are: Available or Leased.|
|Storage type \[storage\_type\]|The storage type. The value is set to **PageBlob**.|
|Size \[size\]|The size of the volume in GB.|
|Size bytes \[size\_bytes\]|The size of the volume in bytes.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships and references

The Azure - Storage Volume \(LP\) pattern creates the following relationships and references to support Azure Storage Volume discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Storage Volume \[cmdb\_ci\_storage\_volume\]|

## Azure Tag discovery

The Azure - Storage Volume \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


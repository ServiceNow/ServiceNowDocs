---
title: Azure Storage Account pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Storage Accounts in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-account-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 3
keywords: [Azure Storage Account, Azure discovery, Azure patterns, Storage Account pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Storage Account pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Storage Accounts in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Storage Account \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the storage account.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Sku Name \[sku\_name\]|The name of the stock keeping unit \(SKU\) for backup frequency.|
|State \[state\]|The current state of the storage account. Possible values are: available, starting, error, cancelled, or off.|
|Blob Service \[blob\_service\]|Indicates whether the storage account has a Blob service endpoint. If a blob endpoint exists, the value is set to true.|
|File Service \[file\_service\]|Indicates whether the storage account has a File service endpoint. If a file endpoint exists, the value is set to true.|
|Table Service \[table\_service\]|Indicates whether the storage account has a Table service endpoint. If a table endpoint exists, the value is set to true.|
|Queue Service \[queue\_service\]|Indicates whether the storage account has a Queue service endpoint. If a queue endpoint exists, the value is set to true.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the blob service. The value is set to **default**.|
|Object ID \[object\_id\]|A unique identifier for this blob service.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the file service. The value is set to **default**.|
|Object ID \[object\_id\]|A unique identifier for this file service.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the table service. The value is set to **default**.|
|Object ID \[object\_id\]|A unique identifier for this table service.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the queue service. The value is set to **default**.|
|Object ID \[object\_id\]|A unique identifier for this queue service.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships and references

The Azure - Storage Account \(LP\) pattern creates the following relationships and references to support Azure Storage Account discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Contains::Contained by|Cloud Object Service \[cmdb\_ci\_cloud\_object\_service\]\*|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Contains::Contained by|Cloud File Service \[cmdb\_ci\_cloud\_file\_service\]\*|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Contains::Contained by|Cloud Table Service \[cmdb\_ci\_cloud\_table\_service\]\*|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Contains::Contained by|Cloud Queue Service \[cmdb\_ci\_cloud\_queue\_service\]\*|

\* These relationships are created only if the corresponding service endpoint exists on the storage account.

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|

## Azure Tag discovery

The Azure - Storage Account \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


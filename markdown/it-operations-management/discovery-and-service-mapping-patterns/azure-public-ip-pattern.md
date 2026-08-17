---
title: Azure Public IP pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure public IP addresses on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/azure-public-ip-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure Public IP, Azure public IP address, Azure discovery, Azure patterns, Public IP pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Public IP pattern-based discovery

Discovery and Service Mapping Patterns finds Azure public IP addresses on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Public IP \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the IP address.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the IP address.|
|Public IP Address \[public\_ip\_address\]|The address of the Elastic IP address.|
|Public DNS \[public\_dns\]|The public DNS name.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Public IP \(LP\) pattern creates the following relationships and references to support Azure Public IP discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Contains::Contained by|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|

## Azure Tag discovery

The Azure - Public IP \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


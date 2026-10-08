---
title: Azure WebSite pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure App Service web applications in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-website-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 3
keywords: [Azure WebSite, Azure App Service, Azure discovery, Azure patterns, WebSite pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure WebSite pattern-based discovery

Discovery and Service Mapping Patterns finds Azure App Service web applications in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

This pattern discovers Azure App Service web applications only. For Azure Functions discovery, see [Microsoft Azure Functions discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-function-discovery.md).

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure WebSite \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Azure web application.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name \(FQDN\) of the web application.|
|IP Address \[ip\_address\]|The inbound IP address of the web application.|
|State \[state\]|The current state of the web application. Possible values are: available or terminated.|
|Operational status \[operational\_status\]|The operational status of the web application. The value is 1 \(Operational\) when the state is available, or 2 \(Non-Operational\) otherwise.|
|Vendor \[vendor\]|The vendor of the web application. The value is set to **Microsoft**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the web application associated with this IP address.|
|IP Address \[ip\_address\]|The inbound IP address of the web application.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name \(FQDN\) of the web application.|
|Netmask \[netmask\]|The netmask of the IP address. The value is set to **0.0.0.0**.|
|Vendor \[vendor\]|The vendor of the web application. The value is set to **Microsoft**.|

\* Populated only when the web application has a non-empty inbound IP address.

## CI relationships and references

The Azure WebSite \(LP\) pattern creates the following relationships and references to support Azure WebSite discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud WebServer \[cmdb\_ci\_cloud\_webserver\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud WebServer \[cmdb\_ci\_cloud\_webserver\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]\*|

\* This relationship is created only when the web application has a non-empty inbound IP address and an FQDN.

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud WebServer \[cmdb\_ci\_cloud\_webserver\]|

## Azure Tag discovery

The Azure WebSite \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud WebServer \[cmdb\_ci\_cloud\_webserver\] table.|

## Connections found by Service Mapping during top-down discovery

The Azure WebSite TD pattern discovers the following connections during top-down discovery: Microsoft SQL Server, MySQL, Redis, and NoSQL \(Cosmos DB\).

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


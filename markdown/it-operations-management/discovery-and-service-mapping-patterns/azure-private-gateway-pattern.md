---
title: Azure Private Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure virtual network gateways on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-private-gateway-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure Private Gateway, Azure virtual network gateway, Azure discovery, Azure patterns, Private Gateway pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Private Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds Azure virtual network gateways on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Private Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the private gateway.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Connection Type \[connection\_type\]|Type of VPN connection the gateway supports.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the endpoint.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Region \[region\]|The Azure region in which the endpoint is located.|

## CI relationships

The Azure - Private Gateway \(LP\) pattern creates the following relationships and references to support Azure Private Gateway discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|Implement End Point To::Implement End Point From|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
|Cloud Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|

## Azure Tag discovery

The Azure - Private Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)


---
title: Azure Network and Subnet pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure virtual networks, subnets, and virtual network peerings on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery-and-service-mapping-patterns/azure-network-subnet-pattern.html
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure Network and Subnet, Azure virtual network, Azure subnet, Azure discovery, Azure patterns, Network and Subnet pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Network and Subnet pattern-based discovery

Discovery and Service Mapping Patterns finds Azure virtual networks, subnets, and virtual network peerings on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud components discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Network and Subnet \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the cloud network.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the network.|
|Cidr \[cidr\]|Classless Inter-Domain Routing \(CIDR\) representation of the network. For example: 10.0.0.0/24.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the cloud subnet.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the subnet.|
|CIDR \[cidr\]|CIDR representation of the subnet. For example, 10.0.0.0/24.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the virtual network peering.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|State \[state\]|The current state of the virtual network peering.|
|Use Remote Gateways \[use\_remotegateways\]|Indicates whether remote gateways are used for this peering.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Network and Subnet \(LP\) pattern creates the following relationships and references to support Azure Network and Subnet discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Network \[cmdb\_ci\_network\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Virtual Network Peering \[cmdb\_ci\_vnet\_peering\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Network \[cmdb\_ci\_network\]|

## Azure Tag discovery

The Azure - Network and Subnet \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Network \[cmdb\_ci\_network\] table.|

**Parent Topic:**[Available discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)


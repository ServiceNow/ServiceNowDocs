---
title: Azure Virtual Network Gateway Connection pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Virtual Network Gateway Connection resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure - Virtual Network Gateway Connection \(LP\), Azure Virtual Network Gateway Connections, Azure VPN Connections, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Virtual Network Gateway Connection pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Virtual Network Gateway Connection resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Virtual Network Gateway Connection \(LP\) pattern.

<table id="table_vpc_gateway_connection"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The unique Azure resource identifier for the Virtual Network Gateway Connection.

</td></tr><tr><td>

Name \[name\]

</td><td>

The name of the Virtual Network Gateway Connection resource.

</td></tr><tr><td>

State \[state\]

</td><td>

The operational state of the connection.

</td></tr><tr><td>

Protocol \[protocol\]

</td><td>

The connection protocol used by the gateway connection.

</td></tr><tr><td>

Connection Status \[connection\_status\]

</td><td>

The status of the gateway connection.For example: Connected, Disconnected, or NotConnected.

</td></tr><tr><td>

Connection Type \[connection\_type\]

</td><td>

The type of gateway connection.For example: IPsec, ExpressRoute, or Vnet2Vnet.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr></tbody>
</table>## CI relationships

The Azure - Virtual Network Gateway Connection \(LP\) pattern creates these relationships to support Azure Virtual Network Gateway Connection discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|
|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Connected by::Connects|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|
|Key Value \[cmdb\_key\_value\]|References|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|

## Azure Tag discovery

The Azure - Virtual Network Gateway Connection \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


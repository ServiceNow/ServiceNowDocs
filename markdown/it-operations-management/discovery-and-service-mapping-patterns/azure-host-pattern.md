---
title: Azure Host pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Hosts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-01-26"
reading_time_minutes: 2
keywords: [Azure Host, Azure discovery, Azure Dedicated Host, Azure patterns, Host pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Host pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Hosts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Host \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the host.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Host Type \[host\_type\]|The Stock Keeping Unit \(SKU\) name of the dedicated host.|
|Cloud Vendor \[cloud\_vendor\]|The cloud vendor: **Azure**.|
|Is Virtual \[virtual\]|Indicates whether this is a virtual host. Value is set to false.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Host \(LP\) pattern creates these relationships to support Azure Host discovery.

|CI|Relationship|CI|
|---|------------|---|
|Host \[cmdb\_ci\_cloud\_host\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Host \[cmdb\_ci\_cloud\_host\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Runs on::Runs|Host \[cmdb\_ci\_cloud\_host\]|
|Key Value \[cmdb\_key\_value\]|References|Host \[cmdb\_ci\_cloud\_host\] or Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Azure Tag discovery

The pattern extension sections discover Bring Your Own License \(BYOL\) or the included licenses for Windows VMs, and collect Azure resource tags from Hosts.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

The key is one of the following options: -   Tags: Azure resource tag name
-   License: Windows\_OS\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

The value is one of the following options: -   Tags: Azure resource tag value
-   Azure Hybrid Benefit: BYOL
-   pay-as-you-go: License Included

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

-   Tags: References the Host \[cmdb\_ci\_cloud\_host\] table
-   License: References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)


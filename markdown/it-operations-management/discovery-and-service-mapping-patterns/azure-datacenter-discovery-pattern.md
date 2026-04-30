---
title: Azure Datacenter discovery pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Datacenter resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure Datacenter discovery, Azure Regions, Azure Availability Zones, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Datacenter discovery pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Datacenter resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure Datacenter discovery pattern.

<table id="table_azure_datacenter"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The Azure region name.For example: asia, australiacentral, or eastus.

</td></tr><tr><td>

Region \[region\]

</td><td>

The Azure region name.For example: asia, australiacentral, or eastus.

</td></tr><tr><td>

Name \[name\]

</td><td>

The display name of the Azure region.For example: Asia, Australia Central, or East US.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|The Azure subscription or management group account identifier.|
|Object ID \[object\_id\]|The unique object identifier for the Azure subscription or management group.|
|Datacenter Type \[datacenter\_type\]|The type of datacenter: **Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]**.|
|Is management account \[is\_master\_account\]|Indicates whether this is a management group account that manages multiple subscriptions.|
|Datacenter URL \[datacenter\_url\]|The Azure management endpoint URL for the account.|

## CI relationships

The Azure Datacenter discovery pattern creates these relationships to support Azure Datacenter discovery.

|CI|Relationship|CI|
|---|------------|---|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


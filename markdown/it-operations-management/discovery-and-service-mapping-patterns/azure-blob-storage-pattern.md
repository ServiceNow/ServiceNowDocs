---
title: Azure Blob Storage pattern-based discovery
description: Discovery and Service Mapping Patterns finds blob resources within Azure Blob Storage on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure - Storage Blobs\(LP\), Azure Blob Storage, Azure Blobs, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Blob Storage pattern-based discovery

Discovery and Service Mapping Patterns finds blob resources within Azure Blob Storage on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Storage Blobs\(LP\) pattern.

<table id="table_storage_volume"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the storage blob.

</td></tr><tr><td>

Volume ID \[volume\_id\]

</td><td>

The unique identifier for the storage volume, matching the blob name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The unique Azure resource identifier combining the storage container path and blob name.

</td></tr><tr><td>

Volume container \[volume\_container\]

</td><td>

The name of the storage container that holds the blob.

</td></tr><tr><td>

Storage type \[storage\_type\]

</td><td>

The type of blob storage.For example: BlockBlob, PageBlob, or AppendBlob.

</td></tr><tr><td>

State \[state\]

</td><td>

The lease state of the blob.For example: Leased, Available, or Terminated.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the block endpoint, matching the blob name.|
|Object ID \[object\_id\]|The unique Azure resource identifier for the block endpoint.|

## CI relationships

The Azure - Storage Blobs\(LP\) pattern creates these relationships to support Azure Blob Storage discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


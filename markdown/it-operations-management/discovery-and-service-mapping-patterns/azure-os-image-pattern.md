---
title: Azure OS image pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure OS images on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-01"
reading_time_minutes: 2
keywords: [Azure - Image \(LP\), Azure - Cloud OS Image \(LP\), Azure Image, Azure Cloud OS Image, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure OS image pattern-based discovery

Discovery and Service Mapping Patterns finds Azure OS images on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern overview

Discovery uses the Azure - Image \(LP\) pattern to discover Azure OS images from your Azure account.

When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS Images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. When enabled, Discovery launches the Azure - Cloud OS Image \(LP\) pattern, which populates the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../../discovery/task/enable-cloud-os-image-discovery-pattern.md).

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure OS image patterns.

<table id="table_image"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the image resource.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Azure resource ID of the image.

</td></tr><tr><td>

Image Source \[image\_source\]

</td><td>

Azure resource ID of the image.

</td></tr><tr><td>

Guest OS \[guest\_os\]

</td><td>

Operating system type of the image.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **AZURE**. This field is only populated in Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>## CI relationships

The Azure OS image patterns create these relationships to support Azure OS image discovery.

|CI|Relationship|CI|
|---|------------|---|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|
|Key Value \[cmdb\_key\_value\]|References|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|

## Azure Tag discovery

The Azure OS image patterns collect tags and populate them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Image \[cmdb\_ci\_os\_template\] table or the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


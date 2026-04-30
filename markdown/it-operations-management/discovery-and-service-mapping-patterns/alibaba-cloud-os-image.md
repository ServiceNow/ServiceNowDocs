---
title: Alibaba Cloud cloud OS image pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Cloud OS Image \(LP\) pattern to discover cloud OS images during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 2
keywords: [Alibaba, Cloud OS Image]
breadcrumb: [Alibaba Cloud discovery, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud cloud OS image pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Cloud OS Image \(LP\) pattern to discover cloud OS images during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Cloud OS Image \(LP\) pattern.

<table id="table_ypr_rwl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Image name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ID of the image.-   IDs of public images contain the operating system version, architecture, language, and release date.

For example: **win2008r2\_64\_ent\_sp1\_en-us\_40G\_alibase\_20190318.vhd**.

-   IDs of custom, shared, and community images start with m.

For example: **m-0a1b2c3defghijklm4n5o**.


</td></tr><tr><td>

Guest OS \[guest\_os\]

</td><td>

Operating system \(OS\) type of the image. Possible values are Windows or Linux.

</td></tr><tr><td>

OS Status \[status\]

</td><td>

Status of the image. The default value is Available and this field can contain multiple values separated with a comma.For example: Creating, Available, or Unavailable.

If you don’t specify a parameter, only Available status images are returned.

</td></tr><tr><td>

Image Type \[image\_type\]

</td><td>

Architecture of the image.Possible values:

-   i386 
-   x86\_64 
-   arm64 

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the image. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the image. Default value is Operational.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

Image cloud provider: Alibaba.

</td></tr></tbody>
</table>## CI relationships

Discovery creates these relationships to support the Alibaba Cloud cloud OS image discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|

## Tag discovery

The Alibaba - Cloud OS Image \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)


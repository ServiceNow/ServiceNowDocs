---
title: Alibaba Cloud storage volume pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Storage Volume \(LP\) pattern to discover storage volumes during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Alibaba, Storage Volume]
breadcrumb: [Alibaba Cloud discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud storage volume pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Storage Volume \(LP\) pattern to discover storage volumes during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Storage Volume \(LP\) pattern.

<table id="table_s3z_dwl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the disk.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ID of the disk.

</td></tr><tr><td>

State \[state\]

</td><td>

Status of the disk. Default value is All.For example: In\_use, Available, or Attaching.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

Disk size in bytes.

</td></tr><tr><td>

Storage type \[storage\_type\]

</td><td>

Type of the disk.Possible values are system or data.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the disk. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the disk. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships

Discovery creates these relationships to support the Alibaba Cloud storage volume discovery.

|CI|Relationship|CI|
|---|------------|---|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Uses::Used by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Key Value \[cmdb\_key\_value\]|References|Storage Volume \[cmdb\_ci\_storage\_volume\]|

## Tag discovery

The Alibaba - Storage Volume \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)


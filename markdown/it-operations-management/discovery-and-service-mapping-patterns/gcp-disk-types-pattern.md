---
title: GCP Disk Types pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Disk Types on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-01-12"
reading_time_minutes: 2
keywords: [Google Cloud Platform \(GCP\) - Disk Types, GCP Disk Types, Disk Types, GCP discovery, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Disk Types pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Disk Types on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Disk Types pattern.

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Name of the project used for the discovery.|
|Object ID \[object\_id\]|Name of the project used for the discovery.|
|Datacenter Type \[datacenter\_type\]|Datacenter type: Google Datacenter \[cmdb\_ci\_google\_datacenter\].|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the availability zone.|
|Description \[short\_description\]|Description of the availability zone.|
|State \[state\]|State of the Availability Zone. Possible values are Available or Terminated.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Datacenter or region name.|
|Region \[region\]|Datacenter or region name.|
|Object ID \[object\_id\]|Unique identifier allocated by GCP for this resource.|
|Description \[short\_description\]|Datacenter or region description.|

<table id="table_disk_type"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the disk type in the format **zone:disk-type-name**.

</td></tr><tr><td>

Name \[name\]

</td><td>

Display name of the disk type in the format **disk-type-name@zone**.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Description of the disk type.

</td></tr><tr><td>

Valid Disk Size \(GB\) \[valid\_disk\_size\]

</td><td>

Valid disk size range for this disk type, in gigabytes \(GB\). For example **10GB-65536GB**.

</td></tr><tr><td>

Default Disk Size \(GB\) \[default\_disk\_size\_gb\]

</td><td>

Default disk size in GB for this disk type.

</td></tr></tbody>
</table>## CI relationships

The Google Cloud Platform \(GCP\) - Disk Types pattern creates these relationships to support GCP Disk Types discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Disk Type \[cmdb\_ci\_disk\_type\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Disk Type \[cmdb\_ci\_disk\_type\]|Hosted on::Hosts|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


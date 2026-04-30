---
title: GCP Storage pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP persistent disks and snapshots on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-22"
reading_time_minutes: 2
keywords: [Google Cloud Platform Storage pattern, GCP storage discovery, GCP persistent disk, GCP disk snapshots, GCP storage volumes, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Storage pattern-based discovery

Discovery and Service Mapping Patterns finds GCP persistent disks and snapshots on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Storage pattern.

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

<table id="table_storage_volume"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The unique identifier for the persistent disk.

</td></tr><tr><td>

Name \[name\]

</td><td>

The name of the persistent disk.

</td></tr><tr><td>

Volume ID \[volume\_id\]

</td><td>

The unique identifier for the persistent disk.

</td></tr><tr><td>

Storage type \[storage\_type\]

</td><td>

The type of persistent disk.For example: pd-standard, pd-balanced, or pd-ssd.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

The size of the persistent disk in bytes.

</td></tr><tr><td>

State \[state\]

</td><td>

The operational state of the disk. For example: Available, In Use, or Terminated.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

The description of the persistent disk.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique identifier for the snapshot.|
|Name \[name\]|The name of the snapshot.|
|Volume Name \[volume\_name\]|The name of the source persistent disk.|
|Capacity \[capacity\]|The storage size of the snapshot in bytes.|

|Field|Description|
|-----|-----------|
|Disks size \(GB\) \[disks\_size\]|The total size of all attached disks in gigabytes \(GB\).|

## CI relationships

The Google Cloud Platform \(GCP\) - Storage pattern creates these relationships to support GCP storage discovery.

|CI|Relationship|CI|
|---|------------|---|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Replicates to::Replicated by|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Provisioned From::Provisioned|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Key Value \[cmdb\_key\_value\]|References|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Key Value \[cmdb\_key\_value\]|References|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

## GCP Tag discovery

The Google Cloud Platform \(GCP\) - Storage pattern collects labels and populates them in two entries in the Key Value \[cmdb\_key\_value\] table. One entry references the Storage Volume table, the other entry references the Storage Volume Snapshot table.

|Field|Description|
|-----|-----------|
|Key \[key\]|The label key.|
|Value \[value\]|The label value.|
|Configuration item \[configuration\_item\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|
|Configuration item \[configuration\_item\]|References the Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


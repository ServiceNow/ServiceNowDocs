---
title: GCP Cloud SQL pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Cloud SQL instances and their databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Google Cloud Platform \(GCP\) - Cloud SQL DB, Cloud SQL, GCP discovery, GCP patterns]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Cloud SQL pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Cloud SQL instances and their databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Google Cloud Platform \(GCP\) - Cloud SQL DB pattern to discover hardware type configurations for Cloud SQL instances from your GCP account.

When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. When enabled, Discovery populates the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md).

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Cloud SQL DB pattern.

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

<table id="table_cloud_database"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The unique resource identifier URL for the Cloud SQL instance.

</td></tr><tr><td>

Name \[name\]

</td><td>

The name of the Cloud SQL instance.

</td></tr><tr><td>

Type \[type\]

</td><td>

The database engine type for the Cloud SQL instance.

</td></tr><tr><td>

State \[state\]

</td><td>

The state of the Cloud SQL instance. For example: Available or Terminated.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Version \[version\]

</td><td>

The database version.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

The unique resource identifier URL for the Cloud SQL instance.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the database within the Cloud SQL instance.|
|Type \[type\]|The type of database.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

<table id="table_hardware_type"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The machine type for the Cloud SQL instance.

</td></tr><tr><td>

Name \[name\]

</td><td>

The machine type for the Cloud SQL instance.

</td></tr><tr><td>

vCPUs \[vcpus\]

</td><td>

The number of virtual CPUs \(vCPUs\) for the Cloud SQL instance.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is GCP. This field is only populated in Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>## CI relationships

The Google Cloud Platform \(GCP\) - Cloud SQL DB pattern creates these relationships to support GCP Cloud SQL DB discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Contains::Contained by|Database \[cmdb\_ci\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## GCP Tag discovery

The Google Cloud Platform \(GCP\) - Cloud SQL DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)


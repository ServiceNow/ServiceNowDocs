---
title: GCP Spanner pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Spanner instances and databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Google Cloud Platform \(GCP\) - Spanner DB, Spanner, Cloud Spanner, GCP discovery, GCP patterns]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Spanner pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Spanner instances and databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Spanner DB pattern.

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

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The full resource name of the Spanner instance.|
|Name \[name\]|The display name of the Spanner instance.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|State \[state\]|The state of the Spanner instance.|
|Type \[type\]|The type of cloud database resource.|
|Node Count \[node\_count\]|The number of nodes allocated to the Spanner instance.|
|Processing Units \[processing\_units\]|The number of processing units allocated to the Spanner instance.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name \(FQDN\) for the Spanner instance.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Spanner database.|
|Type \[type\]|The type of database.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Google Cloud Platform \(GCP\) - Spanner DB pattern creates these relationships to support GCP Spanner discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Contains::Contained by|Database \[cmdb\_ci\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## GCP Tag discovery

The Google Cloud Platform \(GCP\) - Spanner DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)


---
title: GCP Bigtable pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Bigtable instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-12"
reading_time_minutes: 3
keywords: [Google Cloud Platform \(GCP\) - Bigtable DB, Bigtable, GCP discovery, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Bigtable pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Bigtable instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Bigtable DB pattern.

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
|Name \[name\]|Display name of the Bigtable instance.|
|Object ID \[object\_id\]|Unique identifier for the Bigtable instance resource.|
|Location \[location\]|Geographic regions where the Bigtable instance clusters are deployed.|
|Install Status \[install\_status\]|Install status of the Bigtable instance. Default value is Installed.|
|State \[state\]|Current operational state of the Bigtable instance. For example, Available or Terminated.|
|Operational status \[operational\_status\]|Operational status of the Bigtable instance. Default value is Operational.|
|Type \[type\]|Resource type identifier. Value is set to **bigtable-instance**.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) for the Bigtable instance.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Bigtable cluster extracted from the cluster identifier.|
|Install Status \[install\_status\]|Install status of the cluster. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the cluster. Default value is Operational.|
|Node Count \[node\_count\]|Number of nodes allocated to serve the cluster.|
|Cluster Type \[cluster\_type\]|Type of database cluster. Value is set to **GCP Bigtable**.|
|Location \[location\]|Geographic region where the cluster is deployed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Full resource identifier of the Bigtable table.|
|Type \[type\]|Database type identifier. Value is set to **bigtable**.|
|Install Status \[install\_status\]|Install status of the table. Default value is Installed.|

## CI relationships

The Google Cloud Platform \(GCP\) - Bigtable DB pattern creates these relationships to support GCP Bigtable discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Contains::Contained by|Database \[cmdb\_ci\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Cluster of::Cluster|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## GCP Tag discovery

The Google Cloud Platform \(GCP\) - Bigtable DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


---
title: GCP BigQuery pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP BigQuery datasets and tables on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-05"
reading_time_minutes: 2
keywords: [Google Cloud Platform \(GCP\) - BigQuery DB, BigQuery, GCP discovery, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP BigQuery pattern-based discovery

Discovery and Service Mapping Patterns finds GCP BigQuery datasets and tables on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - BigQuery DB pattern.

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
|Name \[name\]|Name of the BigQuery dataset.|
|Object ID \[object\_id\]|The fully qualified unique identifier of the dataset in the format **projectId:datasetId**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|State \[state\]|State of the dataset.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) for accessing the dataset.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the public BigQuery dataset.|
|Object ID \[object\_id\]|The fully qualified unique identifier of the dataset in the format **projectId:datasetId**.|
|Vendor \[vendor\]|Cloud vendor. Value is set to GCP.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|State \[state\]|State of the public dataset.|
|Fully qualified domain name \[fqdn\]|FQDN for accessing the public dataset.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the BigQuery table.|
|Type \[type\]|Database type. Value is set to **bigquery**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Google Cloud Platform \(GCP\) - BigQuery DB pattern creates these relationships to support GCP BigQuery discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Uses::Used by|Cloud Public DataBase \[cmdb\_ci\_cloud\_public\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Public DataBase \[cmdb\_ci\_cloud\_public\_database\]|Replicates to::Replicated by|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Contains::Contained by|Database \[cmdb\_ci\_database\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## GCP Tag discovery

The Google Cloud Platform \(GCP\) - BigQuery DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


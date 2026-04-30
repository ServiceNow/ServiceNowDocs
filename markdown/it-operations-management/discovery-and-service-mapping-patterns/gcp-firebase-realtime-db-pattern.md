---
title: GCP Firebase Realtime Database pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Firebase Realtime Database instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-12"
reading_time_minutes: 2
keywords: [Google Cloud Platform \(GCP\) - Firebase Realtime DB, Firebase Realtime Database, GCP discovery, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Firebase Realtime Database pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Firebase Realtime Database instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Firebase Realtime DB pattern.

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
|Object ID \[object\_id\]|Unique identifier for the Firebase Realtime Database instance.|
|Name \[name\]|Name of the Firebase Realtime Database instance.|
|Type \[type\]|Type of Firebase database instance.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|State \[state\]|State of the Firebase Realtime Database instance.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) for the Firebase Realtime Database instance.|

## CI relationships

The Google Cloud Platform \(GCP\) - Firebase Realtime DB pattern creates these relationships to support GCP Firebase Realtime DB discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


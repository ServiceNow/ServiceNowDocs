---
title: GCP External IP Addresses pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP external IP addresses on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Google Cloud Platform \(GCP\) - External IP Addresses, GCP External IP Addresses, External IP Addresses, GCP discovery, GCP patterns]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP External IP Addresses pattern-based discovery

Discovery and Service Mapping Patterns finds GCP external IP addresses on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - External IP Addresses pattern.

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
|Object ID \[object\_id\]|Unique identifier for the external IP address resource.|
|IP Address \[ip\_address\]|The external IP address.|
|Public IP Address \[public\_ip\_address\]|The public IP address.|
|Name \[name\]|Name of the external IP address resource.|
|State \[state\]|State of the IP address.|
|Scope \[scope\]|Geographic scope of the IP address.|
|Network Interface Owner \[network\_interface\_owner\]|The resource that is using this IP address.|
|Public DNS \[public\_dns\]|Public Domain Name System \(DNS\) name associated with the IP address.|

## CI relationships

The Google Cloud Platform \(GCP\) - External IP Addresses pattern creates these relationships to support GCP External IP Addresses discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)


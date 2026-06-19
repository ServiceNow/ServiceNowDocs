---
title: Google Cloud Platform \(GCP\) Memorystore discovery using patterns
description: Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Memorystore DB pattern to discover Memorystore for Memcached and Memorystore for Redis during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/gcp-memorystore-patterns.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [GCP Memorystore, GCP Memorystore for Redis, GCP Memorystore for Memcached, Google Cloud Platform \(GCP\) Memorystore for Redis, Google Cloud Platform \(GCP\) Memorystore for Memcached, Memorystore for Redis, Memorystore for Memcached]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) Memorystore discovery using patterns

Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Memorystore DB pattern to discover Memorystore for Memcached and Memorystore for Redis during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/gcp-cloud-discovery-patterns.md).

## GCP Memorystore data model

The Google Cloud Platform \(GCP\) - Memorystore DB pattern introduces the following CI class that extends an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Cluster \[cmdb\_ci\_cluster\]|

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Memorystore DB pattern.

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
|Name \[name\]|Name of the cluster.|
|Cluster ID \[cluster\_id\]|ID of the cluster.|
|Install Status \[install\_status\]|Install status of the cluster. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the cluster. Default value is Operational.|
|Cluster Status \[cluster\_status\]|Current state of this cluster. For example: READY or STOPPED.|
|Cluster Type \[cluster\_type\]|Type of the cluster: Redis Cluster.|
|Disk Space \(GB\) \[disk\_space\]|Disk space in gigabytes \(GB\).|
|IAM Authentication Enabled \[iam\_authentication\_enabled\]|Determines whether the IAM authentication is enabled. Possible values are true or false.|
|Node Count \[node\_count\]|Number of replica nodes per shard.|
|Deletion Protection Enabled \[deletion\_protection\_enabled\]|Determines whether the deletion protection is enabled. Possible values are true or false.|
|Asset tag \[asset\_tag\]|NodeType of a Redis cluster node. For example: REDIS\_SHARED\_CORE\_NANO or REDIS\_HIGHMEM\_MEDIUM.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique name of the resource in this scope, including the project and location.|
|Name \[name\]|Unique name of the resource, parsed from the Object ID.|
|Type \[type\]|Type of database. Possible values are memcache-instance or redis-instance.|
|Install Status \[install\_status\]|Install status of the database. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the database. Default value is Operational.|
|State \[state\]|State of the database. Possible values are Available or Terminated.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) for the resource type.|
|IP Address \[ip\_address\]|Hostname or IP address of the exposed endpoint used by clients to connect to the service.|

On the Dependency Views map, you can view all discovered Memorystore for Memcached or Memorystore for Redis resources in your organization and the relationships between them.

\[Omitted image "gcp-memorystore-instance-dependency-view.png"\] Alt text: Memorystore for Memcached or Memorystore for Redis instance CIs and connections on a Dependency View map

\[Omitted image "gcp-memorystore-redis-cluster-dependency-view.png"\] Alt text: Memorystore for Redis Cluster CIs and connections on a Dependency View map

## CI relationships

The Google Cloud Platform \(GCP\) - Memorystore DB pattern creates the following relationships and references to support Memorystore discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## Tag discovery

The Google Cloud Platform \(GCP\) - Memorystore DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/gcp-cloud-discovery-patterns.md)


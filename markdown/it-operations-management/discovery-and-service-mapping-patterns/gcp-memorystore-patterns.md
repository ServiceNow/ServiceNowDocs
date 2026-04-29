---
title: Google Cloud Platform \(GCP\) Memorystore discovery using patterns
description: Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Memorystore DB pattern to discover Memorystore for Memcached and Memorystore for Redis during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [GCP Memorystore, GCP Memorystore for Redis, GCP Memorystore for Memcached, Google Cloud Platform \(GCP\) Memorystore for Redis, Google Cloud Platform \(GCP\) Memorystore for Memcached, Memorystore for Redis, Memorystore for Memcached]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) Memorystore discovery using patterns

Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Memorystore DB pattern to discover Memorystore for Memcached and Memorystore for Redis during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

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

<table id="table_qwt_3vd_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the cluster.

</td></tr><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

ID of the cluster.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the cluster. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the cluster. Default value is Operational.

</td></tr><tr><td>

Cluster Status \[cluster\_status\]

</td><td>

Current state of this cluster.​ For example: READY or STOPPED.

</td></tr><tr><td>

Cluster Type \[cluster\_type\]

</td><td>

Type of the cluster: Redis Cluster.

</td></tr><tr><td>

Disk Space \(GB\) \[disk\_space\]

</td><td>

Disk space in gigabytes \(GB\).

</td></tr><tr><td>

IAM Authentication Enabled \[iam\_authentication\_enabled\]

</td><td>

Determines whether the IAM authentication is enabled. Possible values are true or false.

</td></tr><tr><td>

Node Count \[node\_count\]

</td><td>

Number of replica nodes per shard.

</td></tr><tr><td>

Deletion Protection Enabled \[deletion\_protection\_enabled\]

</td><td>

Determines whether the deletion protection is enabled. Possible values are true or false.

</td></tr><tr><td>

Asset tag \[asset\_tag\]

</td><td>

NodeType of a Redis cluster node. For example: REDIS\_SHARED\_CORE\_NANO or REDIS\_HIGHMEM\_MEDIUM.

</td></tr></tbody>
</table><table id="table_df4_h22_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique name of the resource in this scope, including the project and location.

</td></tr><tr><td>

Name \[name\]

</td><td>

Unique name of the resource, parsed from the Object ID.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of database. Possible values are memcache-instance or redis-instance.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the database. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the database. Default value is Operational.

</td></tr><tr><td>

State \[state\]

</td><td>

State of the database. Possible values are Available or Terminated.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) for the resource type.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Hostname or IP address of the exposed endpoint used by clients to connect to the service.

</td></tr></tbody>
</table>On the Dependency Views map, you can view all discovered Memorystore for Memcached or Memorystore for Redis resources in your organization and the relationships between them.

![Memorystore for Memcached or Memorystore for Redis instance CIs and connections on a Dependency View map](../image/gcp-memorystore-instance-dependency-view.png "Memorystore for Memcached or Memorystore for Redis instance dependency view")

![Memorystore for Redis Cluster CIs and connections on a Dependency View map](../image/gcp-memorystore-redis-cluster-dependency-view.png "Memorystore for Redis Cluster dependency view")

## CI relationships

Discovery creates these relationships to support the Memorystore discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Replicates to::Replicated by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Extends from|Cluster \[cmdb\_ci\_cluster\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## Tag discovery

The Google Cloud Platform \(GCP\) - Memorystore DB pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)


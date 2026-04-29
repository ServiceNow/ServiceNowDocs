---
title: Google Cloud Platform \(GCP\) AlloyDB for PostgreSQL discovery using patterns
description: Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - AlloyDB for PostgreSQL pattern to discover AlloyDB for PostgreSQL during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [GCP AlloyDB for PostgreSQL, AlloyDB for PostgreSQL, Google Cloud Platform \(GCP\) AlloyDB for PostgreSQL, AlloyDB]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) AlloyDB for PostgreSQL discovery using patterns

Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - AlloyDB for PostgreSQL pattern to discover AlloyDB for PostgreSQL during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - AlloyDB for PostgreSQL pattern.

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

<table id="table_brd_ck2_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

The GCP system-generated unique identifier \(UID\) of the resource.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the cluster resource.

</td></tr><tr><td>

Automated Backups \[automated\_backup\]

</td><td>

Determines whether automated backups are enabled. Possible values are Enabled or Disabled.

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

Cluster Version \[cluster\_version\]

</td><td>

Optional field that displays the database engine's major version.

</td></tr><tr><td>

Cluster Type \[cluster\_type\]

</td><td>

Type of cluster. Possible values are AlloyDB – Primary cluster or AlloyDB – Secondary cluster.

</td></tr></tbody>
</table><table id="table_ctw_mk2_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The GCP system-generated UID of the resource.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the instance resource.

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

CPU Count \[cpu\_count\]

</td><td>

Number of central processing units \(CPUs\) in the virtual machine \(VM\) instance.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of database: AlloyDB – PostgreSQL.

</td></tr><tr><td>

Replication Type \[replication\_type\]

</td><td>

Type of the instance specified at creation time. For example: Primary instance, Read pool instance, or Secondary instance.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address for the Instance, which is the endpoint for an end-user application.

</td></tr></tbody>
</table>On the Dependency Views map, you can view all discovered AlloyDB for PostgreSQL resources in your organization and the relationships between them.

![AlloyDB for PostgreSQL instance CIs and connections on a Dependency View map](../image/gcp-alloydb-postgressql-instance-dependency-view.png "AlloyDB for PostgreSQL instance dependency view")

![AlloyDB for PostgreSQL Cluster CIs and connections on a Dependency View map](../image/gcp-alloydb-postgressql-cluster-depndency-view.png "AlloyDB for PostgreSQL Cluster dependency view")

## CI relationships

Discovery creates these relationships to support the AlloyDB for PostgreSQL discovery.

|CI|Relationship|CI|
|---|------------|---|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Cluster of::Cluster|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Replicates::Replicated by|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|

## Tag discovery

The Google Cloud Platform \(GCP\) - AlloyDB for PostgreSQL pattern collects tags and populates them in two entries in the Key Value \[cmdb\_key\_value\] table. One entry references the Cloud DataBase table, the other entry references the Cloud DataBase Cluster table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table|
|Configuration item \[configuration\_item\]|References the Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\] table|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)


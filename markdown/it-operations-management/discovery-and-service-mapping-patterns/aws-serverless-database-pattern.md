---
title: AWS Serverless Database pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon Aurora Serverless databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-02"
reading_time_minutes: 3
keywords: [Amazon AWS Serverless Database, Amazon Aurora Serverless, RDS database discovery, AWS discovery, AWS patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Serverless Database pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon Aurora Serverless databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS Serverless Database pattern.

<table id="table_cloud_db_cluster2"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

User-supplied identifier for the DB cluster.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the database cluster. If a database cluster name isn't provided, the value is the same as the Cluster ID.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) for the DB cluster.

</td></tr><tr><td>

Cluster Version \[cluster\_version\]

</td><td>

Database engine version number.

</td></tr><tr><td>

Vendor \[vendor\]

</td><td>

Database vendor. Value is set to **Amazon**.

</td></tr><tr><td>

Automated Backups \[automated\_backup\]

</td><td>

Indicates whether automated backups are enabled and the retention period. Possible values are either **Disabled** or **Enabled \(X Days\)**, where X represents the backup retention period in days.

</td></tr><tr><td>

Deletion Protection Enabled \[deletion\_protection\_enabled\]

</td><td>

Indicates whether deletion protection is enabled for the DB cluster. Possible values are **true** or **false**. -   **true**: Deletion protection is enabled and the database cannot be deleted
-   **false**: Deletion protection is disabled

</td></tr><tr><td>

IAM Authentication Enabled \[iam\_authentication\_enabled\]

</td><td>

Indicates whether AWS Identity and Access Management \(IAM\) database authentication is enabled. Possible values are **true** or **false**. -   **true**: IAM authentication is enabled and you can use IAM credentials to authenticate to the database
-   **false**: IAM authentication is disabled

</td></tr><tr><td>

Storage Encrypted \[storage\_encrypted\]

</td><td>

Indicates whether the DB cluster storage is encrypted.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the cluster. Default value is Operational.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Database instance identifier or Aurora Serverless cluster identifier.|
|Name \[name\]|Name of the database instance or Aurora Serverless cluster.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) for the DB cluster.|
|Version \[version\]|Database engine version number.|
|Vendor \[vendor\]|Database vendor. Value is set to **Amazon**.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Availability zone name.|
|Name \[name\]|Availability zone name.|

|Field|Description|
|-----|-----------|
|Netmask \[netmask\]|Netmask for the IP address. Value is set to 0.0.0.0.|
|Name \[name\]|IP address of the database cluster.|

## CI relationships

The Amazon AWS Serverless Database pattern creates these relationships to support AWS database discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Cluster of::Cluster|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## AWS Tag discovery

The Amazon AWS Serverless Database pattern collects tags and populates them in two entries in the Key Value \[cmdb\_key\_value\] table. One entry references the Cloud DataBase table, the other entry references the Cloud DataBase Cluster table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


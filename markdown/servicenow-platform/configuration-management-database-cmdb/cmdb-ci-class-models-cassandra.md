---
title: Cassandra extension classes
description: The CMDB CI Class Models store app adds or updates classes for Cassandra databases.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cassandra extension classes

The CMDB CI Class Models store app adds or updates classes for Cassandra databases.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships \(if applicable\). You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Cassandra

Cassandra is a distributed database that is treated as one database and that runs on a cluster of Linux nodes. A Cassandra cluster CI represents a logical entity that doesn’t refer to a Linux node.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.

CMDB CI Class Models: For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_h2r_d5z_ryb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cassandra cluster node\[cmdb\_ci\_cassandra\_cluster\_node\]

</td><td>

Cluster node\[cmdb\_ci\_cluster\_node\]

</td><td>

-   “Hosts” cmdb\_ci\_cassandra\_instance
-   “Cluster Of” cmdb\_ci\_cassandra\_cluster
-   “Hosted On” cmdb\_ci\_ server

</td></tr><tr><td>

Cassandra instance\[cmdb\_ci\_cassandra\_instance\]

</td><td>

DB instance\[cmdb\_ci\_db\_instance\]

</td><td>

-   “Runs On” cmdb\_ci\_server
-   “Hosted on” cmdb\_ci\_cassandra\_cluster\_node
-   “Contains” cmdb\_ci\_config\_file\_tracked

</td></tr><tr><td>

Cassandra keyspace\[cmdb\_ci\_cassandra\_keyspace\]

</td><td>

DB catalog\[cmdb\_ci\_db\_catalog\]

</td><td>

“Hosted On” cmdb\_ci\_cassandra\_cluster

</td></tr></tbody>
</table>![Cassandra cluster node class schema.](../image/cmdb-ci-cassandra-cluster-node.png) ![Cassandra instance class schema.](../image/cmdb-ci-cassandra-instance.png) ![Cassandra keyspace class schema.](../image/cmdb-ci-cassandra-keyspace.png)


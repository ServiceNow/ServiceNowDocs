---
title: Cassandra extension classes
description: The CMDB CI Class Models store app adds or updates classes for Cassandra databases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-cassandra.html
release: zurich
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cassandra extension classes

The CMDB CI Class Models store app adds or updates classes for Cassandra databases.

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the CMDB CI Class Models release notes.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Cassandra

Cassandra is a distributed database that is treated as one database and that runs on a cluster of Linux nodes. A Cassandra cluster CI represents a logical entity that doesn’t refer to a Linux node.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md).

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
</table>\[Omitted image "cmdb-ci-cassandra-cluster-node.png"\] Alt text: Cassandra cluster node class schema. \[Omitted image "cmdb-ci-cassandra-instance.png"\] Alt text: Cassandra instance class schema. \[Omitted image "cmdb-ci-cassandra-keyspace.png"\] Alt text: Cassandra keyspace class schema.


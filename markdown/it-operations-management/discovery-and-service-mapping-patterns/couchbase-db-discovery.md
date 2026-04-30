---
title: Couchbase Database discovery
description: The ServiceNow Discovery application uses the Couchbase Instance discovery pattern to find and map Couchbase Database instances and their clusters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Couchbase Database discovery

The ServiceNow Discovery application uses the Couchbase Instance discovery pattern to find and map Couchbase Database instances and their clusters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Couchbase Database is an open source, distributed database that manages JSON documents. One or more instances of a Couchbase Server constitute a cluster. Data and services are shared across the cluster.

Discovery uses the Couchbase Instance discovery pattern to run horizontal and top-down discovery. You can use this pattern on the ServiceNow AI Platform® using the Quebec release or later.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   The Couchbase Database must be installed on a Linux Server: Red Hat 7.9 or Ubuntu 20.
-   Ensure that CLI tools are installed on the servers.
-   On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). Configure the credentials with the following permissions:
    -   Discovery permissions
    -   Permissions to list files, such as VERSION.txt, in the Couchbase installation folders on the Linux Server.
    -   Permissions to execute the command, `systemctl status couchbase-server`, on the Linux Server.

On the ServiceNow AI Platform, configure applicative credentials for the table cmdb\_ci\_couchbase\_instance. The credentials must have sufficient permissions to execute the following commands on the Couchbase Server:

-   `<couchbase install dir>/bin/curl -u <username>:'<password>' http://"<couchbase server>:<access_port>/pools/`
-   `<couchbase install dir>/bin/curl -u <username>:'<password>' http://"<couchbase server>:<access_port>/pools/<default Pool name>`
-   `<couchbase install dir>/bin/curl -u <username>:'<password>' http://"<couchbase server>:<access_port>/pools/<default Pool name>/buckets`
-   `<couchbase install dir>/bin/curl -u <username>:'<password>' http://"<couchbase server>:<access_port>/pools/<default Pool name>/remoteClusters`

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Main CI \(Couchbase Instance\) \[cmdb\_ci\_couchbase\_instance\]|
|name|The name of the Couchbase instance.|
|install\_directory|The installation folder or directory of the Couchbase instance.|
|config\_file|The main configuration file of the Couchbase instance.|
|version|The version of the Couchbase instance.|
|tcp\_port|The port used for command line and Rest API access.|
|edition|Either the Basic or Enterprise edition of the Couchbase instance.|
|start\_date|The date from which the Couchbase instance has been active.|
|Couchbase Cluster \[cmdb\_ci\_couchbase\_cluster\]|
|name|The name of the Couchbase cluster.|
|cluster\_id|The ID of the Couchbase cluster.|
|install\_status|The installed status, set to "1"/"installed".|
|cluster\_type|The operational status, set to "1"/"operational".|
|Couchbase Cluster Node \[cmdb\_ci\_couchbase\_cluster\_node\]|
|name|The name of the Cluster node.|
|install\_status|The installed status, set to "1"/"installed".|
|operational\_status|The operational status, set to "1"/"operational".|
|node\_status|The Cluster node health status.|
|node\_encryption|Field that indicates whether the node is encrypted.|
|configured\_host\_name|The configured host name of the Cluster node.|
|host\_name|The actual host name of the Cluster node.|
|total\_memory|The total memory.|
|free\_memory|The free memory.|
|mcd\_reserved\_memory|The reserved MCD memory.|
|mcd\_allocated\_memory|The allocated MCD memory.|
|couch\_api\_base|The Couchbase base API URL.|
|couch\_api\_base\_https|The Couchbase HTTPS API URL.|
|recovery\_type|The recovery type.|
|otpnode|The OTP node.|
|node\_uuid|The UUID of the Cluster node.|
|cluster\_compatibility|The cluster compatibility of the Cluster node.|
|version|The version of the Cluster node.|
|os|The OS of the Cluster node.|
|cpu\_count|The CPU count of the Cluster node.|
|edition|The Cluster node edition. The edition is the same as that of the Couchbase instance.|
|Couchbase Bucket \[cmdb\_ci\_couchbase\_bucket\]|
|name|The name of Couchbase bucket.|
|cluster|Reference to the Couchbase cluster.|
|install\_status|The installed status, set to "1"/"installed".|
|Couchbase Cluster Resource \[cmdb\_ci\_couchbase\_cluster\_resource\]|
|name|The name of the Couchbase service.|
|install\_status|The installed status, set to "1"/"installed".|
|operational\_status|The operational status, set to "1"/"operational".|
|cluster|Reference to the Couchbase cluster.|

## CI relationships

These relationships are created to support Couchbase DB discovery.

<table id="table_wpv_b3l_hsb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Couchbase Instance \[cmdb\_ci\_couchbase\_instance\]

</td><td>

Runs on::Runs Reference

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr><tr><td>

Couchbase Cluster Node \[cmdb\_ci\_couchbase\_cluster\_node\]

</td><td>

Cluster of::Cluster Reference

</td><td>

Couchbase Cluster \[cmdb\_ci\_couchbase\_cluster\]

</td></tr><tr><td>

Couchbase Cluster Node \[cmdb\_ci\_couchbase\_cluster\_node\]

</td><td>

Hosted on::Hosts Reference

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr><tr><td>

Couchbase Bucket \[cmdb\_ci\_couchbase\_bucket\]

</td><td>

Uses::Used by Reference

</td><td>

Couchbase Instance \[cmdb\_ci\_couchbase\_instance\]

</td></tr><tr><td>

Couchbase Bucket \[cmdb\_ci\_couchbase\_bucket\]

</td><td>

Hosted on::Hosts Reference

</td><td>

Couchbase Cluster \[cmdb\_ci\_couchbase\_cluster\]

</td></tr><tr><td>

Couchbase Cluster \[cmdb\_ci\_couchbase\_cluster\]

</td><td>

Replicates to::Replicated by

</td><td>

Couchbase Cluster \[cmdb\_ci\_couchbase\_cluster\]

</td></tr></tbody>
</table>## CMDB data model

![Couchbase DB discovery CMDB data model.](../image/couchbase-db-discovery-model.png "Couchbase DB discovery CMDB data model")

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)


---
title: Apache Cassandra database discovery
description: ServiceNow Discovery finds the Apache and the DataStax Cassandra database on UNIX using the Cassandra Distributed DB pattern. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Apache Cassandra database discovery

ServiceNow Discovery finds the Apache and the DataStax Cassandra database on UNIX using the Cassandra Distributed DB pattern. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns from the ServiceNow® Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Provide credentials for discovering the host**

    Identify the servers hosting a Cassandra database and provide credentials necessary for horizontal discovery of these servers. For more information, see [Credentials required for host discovery](r_Credentials4HostDiscovery.md).

-   **Verify CMDB CI Class Models store app is up to date**

    Ensure that your instance supports the Cassandra CI class models by deploying the 1.14.0 version of the CMDB CI Class Models store app from the ServiceNow Store.

-   **Verify permissions for Cassandra commands for UNIX**

    For the list of Cassandra commands, see the [Cassandra \(for UNIX\)](r_NonSudoCommands.md#table_dxn_bml_mmb) section in [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

-   **Verify read access to cassandra.yaml**

    Possible locations of the cassandra.yaml file:

    -   `$config_directory + "/cassandra.yaml"`
    -   `$process.environmentVariables.CASSANDRA_CONF.value + "/cassandra.yaml"`
    -   `$install_directory + "/conf/cassandra.yaml"`

## Data collected by Discovery for Cassandra database

Discovery populates the data in the CMDB when running the Cassandra Distributed DB pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the cluster as well serves as a display name|

|Field|Description|
|-----|-----------|
|Cluster \[cluster\]|Reference of the Cassandra cluster CI in which this node is part of.|
|Cluster Name \[cluster\_name\]|Name of the cluster.|
|IP Address \[ip\_address\]|IP Address of the cluster node \(host machine\).|
|Name \[name\]|Display name in the following format: cluster\_name@hostname.|
|Operational status \[operational\_status\]|Operational status of the cluster node.|
|Server \[server\]|Reference of server \(host machine\) CI|

|Field|Description|
|-----|-----------|
|Cluster Name \[cluster\_name\]|Name of the cluster.|
|Configuration directory \[config\_directory\]|Directory path where configuration files are available.|
|Configuration file \[config\_file\]|File path of base init configuration file where other configuration-related paths can be configured.|
|Data Center \[data\_center\]|Data center in which the cluster node is part of a cluster.|
|Installation directory \[install\_directory\]|The installation path.|
|IP Address \[ip\_address\]|IP address of the host machine where the process is running.|
|Name \[name\]|Display name which is the same as the &lt;uid&gt;.|
|PID \[pid\]|Process ID running on the host machine.|
|Rack \[rack\]|The rack information in which the cluster node is part of.|
|Description \[short\_description\]|The short description of the instance.|
|TCP port\(s\) \[tcp\_port\]|List of TCP ports configured as in “cassandra.yaml” configuration file \(Format: “:port1:port2:port3:”\)|
|UID \[uid\]|The unique ID to identify the instance \(Format: &lt;cluster\_name&gt;\_\_&lt;data\_center&gt;\_\_&lt;rack&gt;@hostname\).|
|Vendor \[vendor\]|Vendor name for reference from “core\_company” table if already available. If it is not available, a new entry is logically created with the name “Apache” or “DataStax”.|
|Workload Running \[workload\_running\]|The name of the workload running on the instance.|

|Field|Description|
|-----|-----------|
|Cluster \[cluster\]|The reference of Cassandra cluster CI in which the keyspace is part of.|
|Cluster Name \[cluster\_name\]|Name of the cluster in which the keyspace is part of.|
|Keyspace Name \[keyspace\_name\]|Name of the keyspace.|
|Name \[name\]|The display name in the following format: &lt;keyspace\_name&gt;@&lt;cluster\_name&gt;.|

![Dependency Views showing discovered Apache Cassandra deployment.](../../discovery/image/apache-cassandra-dependency-view.png "Dependency Views showing discovered Apache Cassandra deployment")

## CI relationships

Discovery creates these relationships to support the Apache Cassandra database discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cassandra Instance \[cmdb\_ci\_cassandra\_instance\]|Runs on::Runs|Server \[cmdb\_ci\_server\]|
|Cassandra Cluster Node \[cmdb\_ci\_cassandra\_cluster\_node\]|Hosted on::Hosts|Server \[cmdb\_ci\_server\]|
|Cluster of::Cluster|Cassandra Cluster \[cmdb\_ci\_cassandra\_cluster\]|
|Cassandra Keyspace \[cmdb\_ci\_cassandra\_keyspace\]|Hosted on::Hosts|Cassandra Cluster \[cmdb\_ci\_cassandra\_cluster\]|

## Data discovered by Service Mapping during top-down discovery

Service Mapping performs the top-down discovery of Cassandra, which typically runs as a distributed database on a cluster of server nodes. During top-down discovery, Service Mapping discovers instances running on nodes and displays them on the application service map.

In addition to the tables and fields discovered during horizontal discovery, the top-down discovery also discovers the fields listed in the following table.

|Field|Description|
|-----|-----------|
|Keyspaces \[keyspaces\]|Keyspace\(s\) the instance can access \(populated only in top-down discovery\).|

For incoming connections, the instance is discovered, as shown in the following image.

![Cassandra discovery top-down service map](../image/cassandra-discovery-top-down.png "Cassandra discovery top-down service map")

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

**Related topics**  


[Database Administrator \(DBA\) report discovery](../../discovery/concept/dba-report-discovery-pattern.md)


---
title: Cohesity storage system discovery
description: The Discovery and Service Mapping Patterns application uses the Cohesity Storage System pattern to find clusters, nodes, and chassis for the Cohesity DataPlatform. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Cohesity storage system discovery

The Discovery and Service Mapping Patterns application uses the Cohesity Storage System pattern to find clusters, nodes, and chassis for the Cohesity DataPlatform. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Cohesity develops software that are used to consolidate and simplify data management, and it includes analytics capabilities. Their software also solves the problem of mass data fragmentation with data that extends across multiple systems or cloud providers.

The company's main product, DataPlatform, is a hyper-converged software that allows businesses to consolidate a variety of workloads, including backups, archives, test, development, and analytics data onto a single cloud-native platform. It works with physical servers as well as virtual machines.

Cohesity extends backup capabilities to NoSQL workload distributed databases like MongoDB, Apache Cassandra, Couchbase, and Apache HBase, as well as Apache Hadoop data on Hadoop Distributed File System \(HDFS\) datastores.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   CMDB CI Class Models, from version 1.37.0
    -   Discovery and Service Mapping Patterns, from version 1.0.91
-   **Verify MID Server configuration**

    Verify the MID Server is set to Active and is reachable to the Cohesity storage cluster.

-   **Verify API permissions**

    Verify you have a basic authentication account configured with proper permissions for the following API calls:

    -   `https://" + ${cluster_ip} + "/irisservices/api/v1/public/cluster?fetchStats=true`
    -   `https://" + ${cluster_ip} + "/irisservices/api/v1/nexus/cluster/status`
    -   `https://" + ${cluster_ip} + "/irisservices/api/v1/public/nodes?fetchStats=true`
    -   `https://" + nodeIp + "/irisservices/api/v1/nexus/node/hardware_info`
-   **Create an alias for the basic authentication credential**

    For more information, see [Create an alias for a basic authentication credential for Cohesity storage system discovery](../task/create-alias-basic-auth-cred-cohesity.md).

-   **Create a serverless discovery schedule**

    For more information, see [Create a serverless schedule for Cohesity storage system discovery](../task/create-serverless-schedule-cohesity.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Cohesity Storage System pattern.

|Label|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the cluster.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) of the cluster.|

|Label|Field Name|
|-----|----------|
|Manufacturer \[manufacturer\]|Manufacturer of the cluster node, which could be Cohesity or third-party.|
|Fully qualified domain name \[fqdn\]|FQDN of the node within the cluster.|
|Operational status \[operational\_status\]|Operational status. Default value: Installed.|
|Description \[short\_description\]|Description of the cluster node: Cohesity Backup Server.|

|Label|Field Name|
|-----|----------|
|Manufacturer \[manufacturer\]|Manufacturer of the chassis.|
|Description \[short\_description\]|Description of the chassis: Cohesity Chassis.|
|Serial number \[serial\_number\]|Serial number of the chassis.|

|Label|Field Name|
|-----|----------|
|Name \[name\]|Name of the Cohesity node.|
|IP Address \[ip\_address\]|IP address of the Cohesity node.|
|IP version \[ip\_version\]|IP version of the Cohesity node.|

## CI relationships

Discovery creates these relationships to support the Cohesity storage system discovery.

<table id="table_nxq_dcc_x5b"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Cohesity Node \[cmdb\_ci\_cohesity\_node\]

</td><td>

Owns::Owned by

</td><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

Cohesity Node \[cmdb\_ci\_cohesity\_node\]

</td><td>

Cluster of::Cluster

</td><td>

Cohesity Cluster \[cmdb\_ci\_cohesity\_cluster\]

</td></tr><tr><td>

Cohesity Node \[cmdb\_ci\_cohesity\_node\]

</td><td>

Hosted on::Hosts

</td><td>

Chassis \[cmdb\_ci\_chassis\]

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)


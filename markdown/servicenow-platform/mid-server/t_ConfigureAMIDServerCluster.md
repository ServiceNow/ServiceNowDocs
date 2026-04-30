---
title: Configure a MID Server cluster
description: Group multiple MID Servers to form clusters, then configure clusters for fail-over protection or load balancing. Load-balancing clusters automatically balance work between each MID Server to improve stability and performance, as well as handle fail-over. Fail-over clusters have a configured order used to determine which MID Server to use next if a failure occurs.MID Server clusters enable multiple MID Servers with the appropriate capabilities to be grouped together for load balancing and fail-over protection.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure a MID Server cluster

Group multiple MID Servers to form clusters, then configure clusters for fail-over protection or load balancing. Load-balancing clusters automatically balance work between each MID Server to improve stability and performance, as well as handle fail-over. Fail-over clusters have a configured order used to determine which MID Server to use next if a failure occurs.

## Before you begin

Ensure that all MID Servers in the cluster have the same [capabilities](t_ConfigureCapabilities.md#) \(Supported Applications, IP Ranges, and Capabilities\). A MID Server should not belong to more than one cluster.

Role required: admin

<table id="table_q4n_5s4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

Create a new cluster or edit an existing cluster.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Clusters**.

2.  Click **New** to create a new cluster, or open an existing cluster's record to edit.

3.  Name the cluster and select the cluster type: **Failover** or **Load Balance**.

4.  Right click in the header bar and select **Save** from the context menu.

5.  Click **Edit** in the **Includes MID Servers** Related List.

6.  Select appropriate MID Servers for this cluster from the slushbucket.


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)

## MID Server clusters

MID Server clusters enable multiple MID Servers with the appropriate capabilities to be grouped together for load balancing and fail-over protection.

### External data sources

For performance and reliability reasons, these data sources should not be used with MID Server clusters. These external data sources should only be used with dedicated MID Servers.

-   LDAP
-   Export sets
-   JDBC data sources

**Note:** If a MID Server in a cluster fails, the fail-over MID Server starts over at the beginning of the ECC queue task even if much of the information from the JDBC data source was already returned. This can result in duplicate data. For more details, see the [Using MID Server clusters for JDBC data sources can cause duplicate and out-of-date data \[KB0727739\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0727739) article in the HI Knowledge Base.

### How clusters work

MID Servers in clusters must be able to connect to the instance and to all the devices with which they are expected to communicate. If all MID Servers in a cluster are down, the discovery is canceled. Make sure all the MID Servers are added to any Access Control List \(ACL\) in use. MID Server clusters are managed by a business rule called MID Server Cluster Management, which checks to see if the MID Server assigned to a job in the ECC Queue belongs to a cluster.

-   **Load balancing**

    If the cluster business rule determines that a MID Server is part of a load balancing cluster, the application using the MID Server automatically balances the work between the MID Servers in that cluster. It is good practice to put MID Servers with the same [capabilities](../reference/r_MIDServerCapabilities.md) in a load balancing cluster.

-   **Fail-over protection**

    MID Servers in a fail-over cluster each have a configured order that the platform uses to determine which MID Server to use next in case of failure. MID Servers in a fail-over cluster work independently and do not load balance with other MID Servers in that cluster \(although they might also be members of load balancing clusters\). When a MID Server fails, the MID Server Cluster Management business rule selects the highest available MID Server in the order to take over the work. The selected MID Server checks the ECC Queue and starts with jobs that are either Processing or Ready.

    **Note:** MID Server clustering does not support the ECC queue topics `Command` or `SystemCommand`. If these commands are received, the clustered MID Servers do not redirect the ECC queue to another MID Server. The ECC queue records stay on the ECC queue without being processed.

    Configure a fail-over MID Server with at least the same capabilities as the MID Server it is intended to relieve.

    **Note:** If a MID Server fails while the [Shazzam probe](https://www.servicenow.com/docs/access?context=t_ConfigureTheShazzamProbe&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) is running and auto-selection is configured, failover is not available. The Shazzam discovery stops. Discovery does not automatically choose another MID Server.


### MID Server cluster event

The following event is triggered when the platform cannot find a MID Server with the appropriate capabilities to replace a MID Server in a fail-over cluster. Use this event to create an email to notify appropriate users that the cluster has failed.

|Event|Table|Description|Business Rule|
|-----|-----|-----------|-------------|
|mid\_server.cluster.down|MID Server Cluster`[ecc_agent_cluster]`|A MID Server cluster has failed|MID Server Cluster Management|

### Specifying a specific MID Server cluster

You can specify a specific MID Server cluster for a Discovery schedule. The discovery process uses that cluster only. You cannot chain clusters or specify a single MID Server that belongs to multiple clusters.

### Distributed MID Server clusters for Operational Intelligence

The distributed MID Server cluster type is used exclusively in Operational Intelligence, which analyzes Event Management events and generates anomaly alerts. These MID Servers communicate with one another to distribute and balance the workload. For details, see [MID Server distributed clusters for Operational Intelligence](https://www.servicenow.com/docs/access?context=ops-intelligence-mid-server&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

### Smart Workload Manager

Using Smart Workload Manager, an application assigns jobs to MID Servers based on true load. The application may used cluster based MID Server selection. In cases where some MID Servers in the cluster slow in processing jobs, the MID Servers which are processing records faster are assigned more jobs.

The instance is aware of individual MID Servers in the cluster and their work load capacity. Work assignments are dynamically distributed based on the real-time performance and metric data of each MID Server. By considering key factors such as current task queue size, processing speed, and system load, tasks will be assigned more efficiently to prevent overloading any single server and enhance overall system stability. MID Servers with lower workload and higher processing speed receive more tasks.

### Combining legacy clusters

Combining MID Server Clusters is only for use with legacy selection methods. A MID Server can be added to both types of clusters at the same time. This diagram shows a scenario in which a MID Server from a load balancing cluster \(MID Server D\) is also present in a fail-over cluster. If MID Server D fails, MID Server E in the failover cluster is available to the load balancing cluster to perform the tasks previously assigned to MID Server D.

![MID Server failover example](../image/MIDServerClustersDiagram.png)


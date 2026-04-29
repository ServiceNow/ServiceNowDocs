---
title: IBM PowerHA SystemMirror for AIX discovery
description: The ServiceNow Discovery application uses the IBM PowerHA Cluster \(HACMP\) pattern to find IBM PowerHA SystemMirror for AIX \(formerly HACMP\) high-availability clusters on AIX UNIX and Linux systems running on IBM platforms. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [IBM PowerHA SystemMirror, IBM PowerHA SystemMirror for AIX, IBM PowerHA, HACMP]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM PowerHA SystemMirror for AIX discovery

The ServiceNow Discovery application uses the IBM PowerHA Cluster \(HACMP\) pattern to find IBM PowerHA SystemMirror for AIX \(formerly HACMP\) high-availability clusters on AIX UNIX and Linux systems running on IBM platforms. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses this pattern to run horizontal discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following application is up to date**

    Discovery and Service Mapping Patterns

-   **Verify the IBM PowerHA Cluster \(HACMP\) pattern is in Triggers probes tab**

    1.  Navigate to **CI Classification** &gt; **UNIX**.
    2.  Select **AIX**.
    3.  In The **Triggers probes** tab, verify that the IBM PowerHA Cluster \(HACMP\) pattern is listed as an exploration that runs after the AIX Server pattern.
    For more information on AIX Server discovery, see [AIX server discovery](../../discovery/reference/r_DataCollDiscoAIXComputers.md).

-   **Verify server IP address or hostname**

    Verify that the server IP address or hostname are used during discovery. For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).

-   **Verify MID Server access**

    Verify that the MID Server has access to the target host and can execute all the commands that are implemented in the pattern.

-   **Configure a UNIX user with the following permissions**

    Configure a UNIX user with permissions to run all commands defined in the official IBM documentation, and the following commands on AIX.

    |Command|Description|
    |-------|-----------|
    |`lssrc -s clstrmgrES`|Verify that the clstrmgrES process is running|
    |`lslpp -l cluster.license`|Get the license and version data of the cluster|
    |`lslpp -l cluster.license | awk '{$1=$2=$3=\"\"; print $0}' |sed -e 's/^[[:space:]]*//'`|Get the software label version data of the cluster|
    |`/usr/es/sbin/cluster/utilities/clRGinfo -a | awk '{print $1,$2}' | grep -E -v 'denied|error'`|Get resource groups name and type|
    |`/usr/es/sbin/cluster/utilities/clRGinfo -s | grep -E -v 'denied|error'`|Get more information about resource groups|
    |`/usr/es/sbin/cluster/utilities/clfindres -s | grep -E -v 'denied|error'`|Alternative command to get more information about resource groups|
    |`/usr/es/sbin/cluster/utilities/clshowres | grep -E 'Resource Group Name|Volume' | grep -E -v 'Concurrent|Automatically|error|denied' | sed 's/Volume Groups/Volume Groups Names/' | awk '{print substr($0, index($0,$4))}' | sed 'N;s/\n/ /'`|Get volume groups associated to resource groups|
    |`/usr/es/sbin/cluster/clstat -o | grep 'Resource Group' | grep -E -v 'error|denied' | awk '{print $3, $5, $6}'`|Get the state of the resource group\(s\)|
    |`/usr/es/sbin/cluster/utilities/cltopinfo -c`|Get the cluster name|
    |`/usr/es/sbin/cluster/utilities/cllscf`|Alternative command to get the cluster name|
    |`lssrc -ls clstrmgrES`|Get cluster current state|
    |`/usr/es/sbin/cluster/clstat -o |awk '{$1=$2=\"\"; print $0}' |sed -e 's/^[[:space:]]*//'`|Get the cluster ID|
    |`/usr/es/sbin/cluster/utilities/cllsclstr | grep -E -v 'error|denied' | awk '{print $1}'`|Alternative command to get the cluster ID|
    |`/usr/bin/odmget HACMPcluster| grep -w id | grep -E -v 'error|denied'`|Alternative command to get the cluster ID|
    |`/usr/es/sbin/cluster/utilities/cltopinfo -n | grep -E -v 'error|denied'`|Get the cluster node\(s\) name\(s\)|
    |`/usr/es/sbin/cluster/utilities/cllsnode | grep -E -v 'error|denied'`|Alternative command to get cluster node\(s\) name\(s\)|
    |`/usr/es/sbin/cluster/clstat -o | grep -i 'Node:' | awk '{print $2, $4}'`|Get cluster node\(s\) state\(s\)|
    |`lscluster -m | grep -E 'Node name|State of node' | grep -E -v 'ERROR|lscluster' | awk '{print $2, $3, $4}' | sed 'N;s/\n/ /'`|Alternative command get cluster node\(s\) state\(s\)|
    |`/usr/es/sbin/cluster/utilities/cllsif | grep -E -v 'error|denied' | awk '{print $1, $2, $6, $7}'`|Get network interface information|
    |`lspv | grep -E -v 'error|denied'`|Get physical volumes information|
    |`lsvg | grep -E -v 'error|denied'`|Get volume groups information|
    |`lsvg -o | grep -E -v 'error|denied'`|Get information about the active volume groups|
    |`/usr/es/sbin/cluster/utilities/clshowres | grep 'Concurrent Volume Group' | awk '{$1=$2=$3=\"\"; print $0}' |sed -e 's/^[[:space:]]*//'`|Get information about the concurrent volume groups|
    |`hostname`|Get current node host name|
    |`nslookup hostname`|Convert hostname to FQDN|


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the IBM PowerHA Cluster \(HACMP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the resource group configured into the cluster context.|
|Server \[server\]|The name of the PowerHA/HACMP cluster.|
|Resource Group Status \[resource\_group\_status\]|The status of the resource group into the cluster context. Example: Online.|
|Resource Group Type \[resource\_group\_type\]|The type of the resource group. Examples: Concurrent, non-concurrent.|
|Cluster \[cluster\]|The name of the PowerHA/HACMP cluster to which the resource group belongs.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the volume group into the cluster context.|
|Resource Type \[resource\_type\]|The resource type \(volume group\).|
|Resource Status \[resource\_status\]|The status of the volume group. Examples: Online, Offline.|
|Cluster \[cluster\]|The name of the PowerHA/HACMP cluster to which the volume group belongs.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the node that participates in the cluster.|
|Node State \[node\_state\]|The state of the cluster node in the context of the CI state. For example: UP, DOWN, UNKNOWN.|
|Node Status \[node\_status\]|The status of the node in the context of the resource group to which it belongs.|
|IP Address \[ip\_address\]|The IP addresses assigned to the node.|
|Cluster \[cluster\]|The name of the cluster to which the cluster node belongs.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the AIX server, representing the cluster node into the context of the PowerHA/HACMP cluster.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the PowerHA/HACMP cluster.|
|Cluster ID \[cluster\_id\]|The ID of the PowerHA/HACMP cluster. Example: 0123456789.|
|Cluster Status \[cluster\_status\]|The current state of the PowerHA/HACMP cluster. Examples: ST\_STABLE, NOT\_CONFIGURED.|
|Cluster Version \[cluster\_version\]|The version of the PowerHA/HACMP cluster. Examples: 5.5; 6.1; 7.2.|
|Cluster Type \[cluster\_type\]|The type of the PowerHA/HACMP cluster. Relevant only for versions 7.2 and above. Example: Stretched.|
|Description \[short\_description\]|Description of the PowerHA/HACMP cluster \(version, ID\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|The cluster node interface name.|
|IP Address \[ip\_address\]|Hostname or IP address where the Hostname represents the cluster node network interface name and the IP address the IPv4 address associated to the network interface name. \(As the IBM PowerHA/HACMP cluster does not have dedicated VIP address\).|
|Cluster \[cluster\]|The name of the PowerHA/HACMP cluster.|

On the Dependency Views map you can see all discovered cluster CIs in your organization and the relationships between them.

In this example, UNIX Cluster Node represents a cluster of UNIX Clusters. UNIX Cluster Node gets resources from UNIX Cluster Resource and uses Cluster Virtual IP. UNIX Cluster Node contains three Cluster Resource Groups.

![CIs and connections on a Dependency Views map](../image/ibm-hacmp-dependency-view.png "Dependency Views sample map")

## CI relationships

These relationships are created to support IBM HACMP/PowerHA cluster discovery:

|CI|Relationship|CI|
|---|------------|---|
|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|Cluster of::Cluster|UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|
|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|Contains::Contained by|Cluster Resource Group \[cmdb\_ci\_cluster\_resource\_group\]|
|Cluster Resource Group \[cmdb\_ci\_cluster\_resource\_group\]|Contains::Contained by|UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]|
|UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]|Defines resources for::Gets resources from|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]|Defines resources for::Gets resources from|UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|
|Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]|Used by::Uses|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|Virtualized by::Virtualizes|Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]|
|UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|Contains::Contained by|Cluster Resource Group \[cmdb\_ci\_cluster\_resource\_group\]|
|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|Hosted on::Hosts|AIX Server \[cmdb\_ci\_aix\_server\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)


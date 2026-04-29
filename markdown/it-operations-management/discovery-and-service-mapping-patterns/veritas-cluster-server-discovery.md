---
title: Veritas Cluster Server discovery
description: The ServiceNow Discovery application uses the Unix Cluster – VERITAS Cluster pattern to find Veritas Cluster Server components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Veritas Cluster Server discovery

The ServiceNow Discovery application uses the Unix Cluster – VERITAS Cluster pattern to find Veritas Cluster Server components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

You can use this pattern on the ServiceNow AI Platform using Kingston Patch 8, London, or Madrid.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **SSH credentials**

    On the ServiceNow AI Platform®, configure the SSH credentials for a user with elevated rights for running the **cat** command. For more information about commands, see Service Mapping commands requiring a privileged user under Service Mapping documentation.

-   **Permissions to read the Veritas Cluster Server configuration file**

    Give the Unix OS user permissions to read the following configuration file: `/etc/VRTSvcs/conf/config/main.cf`.

-   **Permissions to run Veritas Cluster commands**

    Give the Unix OS user permissions to run the following commands against the Veritas Cluster Server:

    |Command|Parameter|Mandatory/Optional|Description|
    |-------|---------|------------------|-----------|
    |“privilege user” + cat /etc/VRTSvcs/conf/config/main.cf|-|Mandatory|Read the Veritas Cluster Server configuration file.|
    |“privilege user” + /opt/VRTSvcs/bin/haclus -value ClusterUUID 2&gt;/dev/null|-|Mandatory|Get the Veritas Cluster Server cluster UUID.|
    |“privilege user” + /opt/VRTSvcs/bin/haclus -value ClusterName 2&gt;/dev/null|-|Mandatory|Get the Veritas Cluster Server cluster name.|
    |“privilege user” + /opt/VRTSvcs/bin/haclus -value EngineVersion|-|Mandatory|Get the Veritas Cluster Server cluster version.|
    |“privilege user” + /opt/VRTSvcs/bin/haclus -value ClusterAddress|-|Mandatory|Get the Veritas Cluster Server cluster address.|
    |“privilege user” + /opt/VRTSvcs/bin/haclus -value ClusState|-|Mandatory|Get the Veritas Cluster Server cluster status.|
    |“privilege user” + /opt/VRTSvcs/bin/hasys -state|-|Mandatory|Get the Veritas Cluster Server cluster nodes.|
    |“privilege user” + /opt/VRTSvcs/bin/hares -state|-|Mandatory|Get the cluster resources of the Veritas Cluster Server.|
    |“privilege user” + /opt/VRTSvcs/bin/hares -display \|grep -w 'Type' \|grep 'global' 2&gt;/dev/null|-|Mandatory|Get the cluster resource type of the Veritas Cluster Server.|
    |“privilege user” + /opt/VRTSvcs/bin/hares -display \| grep Group 2&gt;/dev/null|-|Mandatory|Get the cluster resource group of the Veritas Cluster Server.|
    |“privilege user” + /opt/VRTSvcs/bin/hagrp -state 2&gt;/dev/null|-|Mandatory|Get the resource group name and status of the Veritas Cluster Server.|

-   **Classification probe for triggering the UNIX Cluster – VERITAS Cluster pattern**

    Verify that the classification probe is set to trigger the UNIX Cluster – VERITAS Cluster pattern:

    1.  Navigate to **Discovery Definition** &gt; **CI Classification** &gt; **CI Classification** &gt; **UNIX**.
    2.  In the **UNIX Classification** list, click **Solaris** or **Linux**.
    3.  On the **Triggers probes** tab, check that the **HorizontalDiscoveryProbe-HorizontalPatt** probe is assigned to the **UNIX Cluster – VERITAS Cluster** pattern.

        ![Probe triggering the pattern for Veritas Cluster Server discovery](../image/VeritasClusterServer-probe-triggers.png)

        **Note:** The discovery log shows the error for OS discovery step even if the discovery finished successfully.

-   **System property for the new host class**

    Add a system property \[sys\_property\] **sa.host\_classes** and set the value to cmdb\_ci\_unix\_cluster. Creating a new host class for Veritas Cluster servers helps to identify this type of hosts correctly.


## Limitations

You cannot customize the Unix Cluster – VERITAS Cluster pattern in the Debug mode in the Pattern Designer.

## Data collected by Discovery during horizontal discovery

|Table and field|Description|
|---------------|-----------|
|Unix Cluster \[cmdb\_ci\_unix\_cluster\]|The attributes of the Unix Cluster.|
|IP address \[ip\_address\]|
|Cluster type \[cluster\_type\]|
|Name \[name\]|
|Cluster version \[cluster\_version\]|
|Cluster status \[cluster\_status\]|
|Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|The attributes of the Unix Cluster Node.|
|Name \[name\]|
|Cluster \[cluster\]|
|Server \[server\]|
|Node state \[node\_status\]|
|IP address \[ip\_address\]|
|UNIX Cluster Resource Group \[cmdb\_ci\_unix\_cluster\_resource\_group\]|The attributes of the UNIX Cluster Resource Group.|
|Name \[name\]|
|Node \[node\]|
|Server \[server\]|
|Cluster \[cluster\]|
|Resource group status \[resource\_group\_status\]|
|UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]|The attributes of the UNIX Cluster Resource.|
|Resource type \[resource\_type\]|
|Name \[name\]|
|Resource status \[resource\_status\]|
|Cluster Virtual IPs \[cmdb\_ci\_cluster\_vip\]|The attributes of the Cluster Virtual IP addresses.|
|IP address \[ip\_address\]|
|name \[name\]|
|Cluster \[cluster\]|
|Cluster status \[cluster\_status\]|
|Node \[node\]|

The graphic illustrates CIs that are part of Veritas Cluster Server discovery.

![The Veritas Cluster Server components](../image/VeritasClusterServer-components.png)

## CI relationships

The Unix Cluster – VERITAS Cluster pattern creates the following CI relationships:

|CI|Relationship|CI|
|---|------------|---|
|Unix Cluster \[cmdb\_ci\_unix\_cluster\]|Hosts: Hosted on|Linux Server \[cmdb\_ci\_linux\_server\]|
|Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|Hosts: Hosted on|Linux Server \[cmdb\_ci\_linux\_server\]|
|Cluster Virtual IPs \[cmdb\_ci\_cluster\_vip\]|Virtualized by: Virtualized|Unix Cluster \[cmdb\_ci\_unix\_cluster\]|
|Cluster Virtual IPs \[cmdb\_ci\_cluster\_vip\]|Uses: Used by|Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|Cluster of: Cluster|Unix Cluster \[cmdb\_ci\_unix\_cluster\]|
|Unix Cluster resource \[cmdb\_ci\_unix\_cluster\_resource\]|Defines resources for: Gets resources from|Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|Unix Cluster resource \[cmdb\_ci\_unix\_cluster\_resource\]|Defines resources for: Gets resources from|The Cluster field on \[cmdb\_ci\_unix\_cluster\]|
|Unix Cluster resource group \[cmdb\_ci\_unix\_cluster\_resource\_group \]|Contains: Contained by|The Cluster field on UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|
|Unix Cluster resource group \[cmdb\_ci\_unix\_cluster\_resource\_group \]|Contains: Contained by|The Node field on Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|Unix Cluster resource group \[cmdb\_ci\_unix\_cluster\_resource\_group \]|Contains: Contained by|Unix Cluster resource \[cmdb\_ci\_unix\_cluster\_resource\]|

**Parent Topic:**[Available on-premise discovery patterns](available-patterns.md)


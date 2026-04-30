---
title: Linux Pacemaker Cluster discovery
description: The ServiceNow Discovery application uses the Linux Pacemaker Cluster discovery pattern to find high-availability cluster data and populate the CMDB with the discovered information. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Linux Pacemaker Cluster discovery

The ServiceNow Discovery application uses the Linux Pacemaker Cluster discovery pattern to find high-availability cluster data and populate the CMDB with the discovered information. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

This pattern is an extension section of the [Linux Server](../../discovery/reference/r_DataCollDiscoLinuxComputers.md) pattern. Discovery uses the pattern to run horizontal discovery.

You can use this pattern on the ServiceNow AI Platform® using the Madrid release or later.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for the Linux server.
-   Provide a user with permissions to read the following files:
    -   `/etc/hosts`
    -   `/etc/corosync/corosync.conf`
    -   `/var/lib/heartbeat/crm/cib.xml`, or `/var/lib/pacemaker/cib/cib.xml` from Linux SP3
-   Provide a user with permissions to run the following commands:

    `ps -ef | grep corosync | grep -v grep`

    `ps -ef | grep pacemaker | grep -v grep`

    `ifconfig | grep 'inet addr:' |awk '{print $1, $2 }'`

    `hostname -s`

    `hostname -f`


## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Main CI - UNIX Cluster \[cmdb\_ci\_unix\_cluster\]|
|name|Cluster name.|
|cluster\_id|Cluster ID. Contains the nodes ID.|
|cluster\_type|Cluster type.|
|cluster\_status|Cluster status: Online/offline.|
|cluster\_version|Cluster version.|
|UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]|
|name|Resource name.|
|resource\_type|Resource type.|
|resource\_status|Resource status. For example, Started.|
|ip\_address|IP address of the machine where the resource is running.|
|fqdn|FQDN of the machine where the resource is running.|
|Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]|
|name|Cluster VIP name.|
|ip\_address|IP address of the VIP.|
|Cluster Resource Group \[cmdb\_ci\_cluster\_resource\_group\]|
|name|Resource group name.|
|node|Resource group node.|
|resource\_group\_status|Resource group status.|
|server|Resource group server.|
|fqdn|FQDN of the machine where the resource group is running.|
|UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]|
|name|Node name and node ID.|
|node\_status|Node status.|
|node\_state|Node state.|
|fqdn|FQDN of the machine where the node is running.|

The Dependency Views map shows discovered load balancer CIs and the relationships between them.

![CIs and connections on a Dependency Views map](../image/linux-pacemaker-cluster-dep-view.png)

## CI relationships

These relationships are created to support Linux Pacemaker Cluster discovery:

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_unix\_cluster|Hosts::Hosted on|cmdb\_ci\_linux\_server|
|cmdb\_ci\_unix\_cluster\_node|Hosted on::Hosts|cmdb\_ci\_linux\_server|
|Cluster of::Cluster|cmdb\_ci\_unix\_cluster|
|cmdb\_ci\_cluster\_vip|Uses::Used by|cmdb\_ci\_unix\_cluster\_node|
|Virtualized by::Virtualized|cmdb\_ci\_unix\_cluster|
|cmdb\_ci\_unix\_cluster\_resource|Defines resources for::Gets resources from|cmdb\_ci\_unix\_cluster|
|Defines resources for::Gets resources from|cmdb\_ci\_unix\_cluster\_node|
|cmdb\_ci\_cluster\_resource\_group|Contains::Contained by|cmdb\_ci\_unix\_cluster|
|Contains::Contained by|cmdb\_ci\_unix\_cluster\_node|
|Contains::Contained by|cmdb\_ci\_unix\_cluster\_resource|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)


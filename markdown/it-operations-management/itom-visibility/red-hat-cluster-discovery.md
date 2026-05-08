---
title: Linux Red Hat cluster discovery
description: Discovery can find Linux Red Hat clusters that offer high availability and load balancing.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Linux, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Linux Red Hat cluster discovery

Discovery can find Linux Red Hat clusters that offer high availability and load balancing.

## Required credentials

Configure SSH credentials.

## Additional requirements

You also need permissions to read the `/etc/hosts/` and `/etc/cluster/cluster.conf` file, which associates host names with IP addresses.

The following commands are run for Oracle clusterware:

<table id="table_nfs_4tn_ndb"><thead><tr><th>

Command

</th></tr></thead><tbody><tr><td>

``ps -ef | grep corosync | grep -v grep``

</td></tr><tr><td>

`clustat -x`

</td></tr><tr><td>

`ifconfig | grep 'inet addr:' |awk '{print $1, $2 }'`

</td></tr><tr><td>

`hostname -s`

</td></tr><tr><td>

`hostname -s`

</td></tr></tbody>
</table>Sudo permission to run: `sudo /u01/app/12.1.0.2/grid/bin/ocrcheck | egrep -v 'error|return code'`

## Classifier, probes, and pattern

<table id="table_nww_wmf_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Linux\(Unix classification\)

</td><td>

Horizontal discovery probe: launches patterns

</td><td>

These patterns are an extension of the [Linux Server](../reference/r_DataCollDiscoLinuxComputers.md) pattern:

-   UNIX Cluster - Linux Red hat cluster
-   Linux - Red Hat Cluster

 The pattern uses the `clustat -x` command and looks at this cluster configuration file: `/etc/cluster/cluster.conf`

</td></tr></tbody>
</table>## Data collected

<table id="table_rvs_gjl_mdb"><thead><tr><th>

Table

</th><th>

Labels and field names

</th></tr></thead><tbody><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Name \[name\]

 Cluster status \[cluster\_status\]

 Cluster type \[cluster\_type\]

 IP address \[ip\_address\]

 Cluster ID \[cluster\_id\]

 Cluster version \[cluster\_version\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Name \[name\]

 Node state \[node\_state\]

 IP address \[ip\_address\]

 Node status \[node\_status\]

</td></tr><tr><td>

Unix Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

Name \[name\]

 Resource type \[resource\_type\]

 Resource status \[resource\_status\]

 Properties \[properties\]

</td></tr><tr><td>

Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td><td>

Name \[name\]

 IP address \[ip\_address\]

 Cluster ID \[cluster\_id\]

</td></tr></tbody>
</table>## Relationships

<table id="table_bgt_zkg_ndb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Virtualizes::Virtualized by

</td><td>

Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td></tr><tr><td>

Unix Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

Defines resources for::Gets resources from

</td><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td></tr><tr><td>

Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td><td>

Uses::Used by

</td><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Cluster of::Cluster

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Hosted on:Hosts

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

Defines resources for::Gets resources from

</td><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td></tr><tr><td>

Unix Cluster \[cmdb\_ci\_unix\_cluster\]

</td><td>

Hosts::Hosted on

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr><tr><td>

Unix Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

</td><td>

Hosted on::Hosts

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td></tr></tbody>
</table>
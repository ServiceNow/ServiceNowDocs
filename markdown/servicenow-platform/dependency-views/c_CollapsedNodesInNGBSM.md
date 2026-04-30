---
title: Cluster nodes in a Dependency Views map
description: Dependency Views maps can display cluster group nodes alongside individual CI nodes, and the child nodes of these cluster groups.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cluster nodes in a Dependency Views map

Dependency Views maps can display cluster group nodes alongside individual CI nodes, and the child nodes of these cluster groups.

Clusters are CIs in the Cluster \[cmdb\_ci\_cluster\] table. A cluster CI is an organized set of computer CIs that work together as a single system. Each node in a cluster group represents a CI, typically a server, that can have referenced hardware, such as disks and network adapters.

Cluster nodes on a Dependency Views map can display in two modes:

-   Collapsed mode: Displays only the cluster CI node without its child CI nodes. This mode avoids unnecessary clutter in large maps.
-   Expanded mode: Displays the cluster CI node and all its child CI nodes.

Menu options available for a clustered node include **Collapse** and **Expand**, which allow you to control the density on the map.

By default, Dependency Views collapses all cluster groups and displays clusters in collapsed mode on the map.

## Annotation

Icons for cluster nodes and cluster group CI nodes are noted by the string "Cluster" and by a unique cluster icon. The system searches through all the component nodes in a cluster CI or collapsed node looking for tasks, outages, and trouble, such as incidents, problems, or change requests. This search evaluates only the number of levels that are displayed in the diagram.

![An expanded cluster node displays its child nodes.](../image/ClusterExpandedandCollapsed.png "An expanded cluster node displaying its child nodes")


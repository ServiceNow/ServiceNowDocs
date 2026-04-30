---
title: Operational Technology Network Map
description: The Operational Technology \(OT\) Network Map is an interactive map that visualizes your OT network through connected nodes.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2026-01-22"
reading_time_minutes: 4
breadcrumb: [Explore, Industrial Workspace, Operational Technology]
---

# Operational Technology Network Map

The Operational Technology \(OT\) Network Map is an interactive map that visualizes your OT network through connected nodes.

## OT Network Map overview

The OT Network Map provides a real‑time and accurate representation of your OT environment by modeling subnets and device‑to‑device connections across your industrial network. This visual map helps you understand how OT devices are connected and how data flows between them.

With this visibility, you can analyze the impact of network changes, identify connectivity risks, and make informed operational and security decisions. It enables faster troubleshooting, improves risk awareness, and provides better visibility into complex OT network relationships. It helps you move from reactive troubleshooting to proactive decision‑making across your industrial environment.

You can access the OT Network Map by navigating to Equipment Model Manager in the Industrial Workspace and selecting a site.

The following image is an example of the network map in its default state.![OT Network Map filtered by subnet](../image/ot-network-map.png)

## Node map representation

The node at the center of the network map represents your equipment model entity site. Connected to the site, you can see the nodes that represent the site's subnets. On each subnet node, there's a number indicating how many OT devices exist within that subnet. When you select the device number on the subnet node, the network map expands to show all the device nodes within the subnet.

**Subnet node details**

When you hover over the subnet node, you can view the following information for that subnet:

-   Subnet name
-   Number of critical devices
-   Total number of OT devices
-   Managed Network name, if available

**Device node details**

When you hover over the device node, you can view the following information for that device:

-   Device name
-   Device type
-   Criticality status

The device node also contains an option to view its device-to-device connections. For more information about device-to-device connections, see [OT device related items and related lists](../../mftg-manufacturing-oper-tech-mgr/reference/ot-assets-related-links-and-lists.md) and [View and edit device to device connections](../../mftg-manufacturing-oper-tech-mgr/task/view-device-to-device-connections.md).

**Map refresh**

When the **OT Network Map Cache Handler** scheduled job runs and the **Refreshed at** field in the map is updated with the new refresh time. For more information about the scheduled job, see [Run the OT Network Map Cache Handler scheduled job](../task/run-ot-network-map-cache-handler-scheduled-job.md).

## Populating the map

To populate the OT Network Map, you must run the **OT Network Map Cache Handler** scheduled job. For more information about the scheduled job, see [Run the OT Network Map Cache Handler scheduled job](../task/run-ot-network-map-cache-handler-scheduled-job.md).

The data must be available in the following tables for the network map to load properly.

-   IP Address \[cmdb\_ci\_ip\_address\]
-   OT Discovered Subnet \[sn\_ot\_discovered\_subnet\]

## Map legend

The OT Network Map contains a legend that describes the visual components of the map and their meaning. The legend covers the relationship lines between nodes, the different nodes you may see in your network, and the device node criticality. The following image shows the map legend made available by selecting the **Legend** ![](../image/legend-icon.png) icon from node map control panel in the top-right corner.![Legend in the OT Network Map](../image/network-map-legend.png)

## Map filters

The following table contains the additional filters that you can apply to the OT Network Map for your equipment model entity.

|Filter|Description|
|------|-----------|
|Class|The name of the assigned class for the OT device.|
|Criticality|The measure of the relative risk to the site process due to failure of the device.|
|Manufacturer|The device manufacturer.|
|Purdue level|The assigned Purdue level. Ranges 0–5.|
|Discovery source|The Discovery source for the OT device data.|

## Roles required

You must be assigned both the **cmdb\_ot\_isa\_viewer** role and **cmdb\_ot\_viewer** role.

## Limitations of the network map

The following list contains the limitations of the network map.

-   Subnets without any configuration items \(CIs\) don't show up in the network map.
-   CIs that aren’t part of any subnet don't show up in the network map.
-   For a site with more than 10K CIs, only 10K CIs are considered in the OT network map calculations.

## What to do next

-   [Setting up the OT Network Map](setting-up-ot-network-map.md)
    -   [Run the OT Network Map Cache Handler scheduled job](../task/run-ot-network-map-cache-handler-scheduled-job.md)
    -   [Set the system property for the OT Network Map](../task/set-the-system-property-ot-network-map.md)
-   [View and edit the OT Network Map](../task/view-edit-ot-network-map.md)

**Parent Topic:**[Exploring the Industrial Workspace](../../operational-technology-management/concept/exploring-industrial-workspace.md)


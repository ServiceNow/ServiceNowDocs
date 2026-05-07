---
title: Select resource layer clustering
description: Select resource layer clustering in the Crisis map within the BCM Configurable Workspace to view assets or resources on the map.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for Crisis map, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Select resource layer clustering

Select resource layer clustering in the Crisis map within the BCM Configurable Workspace to view assets or resources on the map.

## Before you begin

Role required: sn\_bcm.admin or sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select **Crisis map** in the list view.

2.  Select the **Layers** icon.

    The layers on the map appear just as pins on a Google map and are configurable. All the layer details like the asset locations, assets, datacenters, and core companies are displayed on the map by their configured icons.

    Use the layers control to view only the selected or all assets that can be toggled on and off on the map. As a crisis manager, you can review active alerts and focus on individual assets that require immediate attention.

3.  Display a selective resource or asset on the map by selecting the check box of that asset.

    The icons of the selected asset are displayed on the map. Layer icons are displayed within black borders, whereas alert icons are within a white circle.

4.  Select the **Asset** icon on the map to view its details.

    For example, when you select a datacenter icon without a count indicator, a popover displays the information configured in the Resource Configuration table \[sn\_fam\_resource\_config\].

    If you configure the **Power** and **Power consumption** fields from the datacenter table \[cmdb\_co\_datacenter\] as display fields in the Resource Configuration form, the popover shows the datacenter's power consumption details and location coordinates.

5.  Select the **Asset** icon with a number next to it.

    The map zooms in to show all the assets that match with the count in that cluster. You can further select each asset within the cluster and drill down to any asset to view its details on the popover.

    You can view only one popover at a time. When you select another node, the popover disappears.

6.  Select the **Reset** icon in the map to clear the search results on the map.


**Parent Topic:**[Structured workflows for Crisis map](../concept/crisis-map-collective-tasks.md)


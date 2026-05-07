---
title: View resource layer clustering
description: View your assets or resources on the map.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View resource layer clustering

View your assets or resources on the map.

## Before you begin

Role required: BCM admin or BCM Program Manager

## About this task

The layers that you see in the map like the assets, datacenters, and core companies are the resources that you have configured. Each of these layers fetches data from the respective resource tables. The assets, datacenters, and core companies resources retrieve data from the location, datacenter, and company tables, respectively.

Asset locations that are nearby to each other are clustered and a cumulative count of the assets is displayed next to the asset icon.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the map icon \(![Crisis map icon](../image/CrisisMapIcon.png)\).

3.  Click the layers icon \(![Layers control icon.](../image/BCMLayersIcon.png)\).

    The layers on the map appear just as pins on a Google map and are configurable. All the layer details like the asset locations, assets, datacenters, and core companies are displayed on the map by their configured icons.

    Use the layers control to view only the selected or all assets that can be toggled on and off on the map. As a crisis manager, when viewing the active alerts you can make an informed decision by concentrating on a single asset that can be critical at that moment from the rest.

4.  To display a selective resource or asset on the map, select the check box of that asset.

    ![Control assets on the map.](../image/AssetLayersControls.png "Control assets on the map")

    The icons of the selected asset are displayed on the map. Layer icons are displayed within black borders, whereas alert icons are within a white circle.

5.  Click an asset icon on the map to view its details.

    For example, if you click a datacenter icon \(![datacenter icon.](../image/BCMDatacenterIcon.png)\) that has no number or a count next to it, a pop over appears with the display information that you have configured in the Resource Configuration table \[sn\_fam\_resource\_config\].

    If you have configured **Power** and **Power consumption** fields of the datacenter table \[cmdb\_co\_datacenter\] as the display fields in the Resource Configuration form, then the power consumption details of that datacenter are displayed on the pop over along with its location coordinates.

6.  Click an asset icon with a number next to it.

    The map zooms in to show all the assets that match with the count in that cluster. You can further click each asset within the cluster and drill down to any asset to view its details on the pop over.

    You can view only one pop over at a time. The pop over disappears on clicking another node.

7.  Click the reset icon \(![Map reset icon.](../image/BCMResetIcon.png)\) to clear the search results on the map.



---
title: Map a Configuration Item to a floor map
description: Map a Configuration Item \(CI\) to a place on your floor map in the Telecommunications Network Inventory application so you can view its details.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Floor map, Network visualization view, Use, Telecommunications Network Inventory]
---

# Map a Configuration Item to a floor map

Map a Configuration Item \(CI\) to a place on your floor map in the Telecommunications Network Inventory application so you can view its details.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent

## About this task

Associate a CI such as facility hardware to a place on the floor map to view its details. You can also understand how your network assets are arranged and placed in the datacenter floor.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the blue hub icon ![Blue Hub Icon.](../image/icon-blue-hub.png).

    The Network viewer window is displayed.

3.  Select the **Floor map** tab.

4.  In the **Choose location** field, select your Site, Building, and Floor.

    The floor map appears.

5.  Select a place on the map.

    If you’re mapping an equipment rack, then select the location with Rack place type.

6.  On the details pane, select the more options icon \(![More Options Icon.](../image/icon-more-option.png)\), and then select **Create place mapping**.

7.  On the details pane, select the more options icon \(![More Options Icon.](../image/icon-more-option.png)\), and then select **Open record**.

    The place record opens. Select the **Place documents** tab, and then select **New**.

8.  On the **Place document** form, fill in the fields.

<table id="table_f3c_dmd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Place

</td><td>

The name of the place record automatically appears based on the place that you select on the floor.

</td></tr><tr><td>

Document table

</td><td>

Type of inventory class that you want to map.

</td></tr><tr><td>

Configuration Item

</td><td>

CI that you want to map to the place.**Note:** A CI must be mapped to only one place. Mapping the same CI to multiple places cause visualization issues on the floor map.

</td></tr></tbody>
</table>9.  Select **Save**.


## Result

The CI is mapped to the place on the floor map. The color of the place is changed and reflects the selected inventory class according to the map legend. Select the CI on the map pane to view its details.

**Parent Topic:**[Floor map](../concept/using-floor-map.md)

**Related topics**  


[Floor map](../concept/visualization-floor-maps.md)

[Upload and manage floor map for your datacenter](create-floor-map-data-center.md)


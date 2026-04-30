---
title: View details of the geo map
description: Use the geo map to view the geographical location of a network site and datacenter and its details in the Telecommunications Network Inventory application. You can understand the detailed overview of the site and information about the connections.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using the geo map, Using Network visualization view, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# View details of the geo map

Use the geo map to view the geographical location of a network site and datacenter and its details in the Telecommunications Network Inventory application. You can understand the detailed overview of the site and information about the connections.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent

## About this task

Use the geo map to do the following:

-   View the details of a network site and datacenter.
-   View the details of the sites in the same location.
-   View the physical and logical connections and topology associated with the site.
-   View the cable routes associated with a site.
-   View the capacity information.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the blue hub icon ![Blue Hub Icon.](../image/icon-blue-hub.png).

    The Network visualization window is displayed.

3.  Select the **Geo map** tab.

4.  View the details of the site by performing the following actions on the map pane.

<table id="choicetable_qtk_fr3_yxb"><thead><tr><th align="left" id="d24631e172">

Action

</th><th align="left" id="d24631e175">

Details

</th></tr></thead><tbody><tr><td id="d24631e181">

**View the details of a site.**

</td><td>

Hover over the map icon on the map pane and then select **View Details**. You can view the site details on the details pane. You can also view the image of the site. To learn more about how to upload an image, see [Add images to a network inventory record](add-image-network-invetory-record.md).

 **Note:** If you select the datacenter on the map pane, select **View floor map** to view the floor map. The **View Floor Map** automatically populates the campus only. You must manually select a building and floor to view the corresponding floor map.

</td></tr><tr><td id="d24631e222">

**View the details of the sites in the same location.**

</td><td>

1.  Hover over the map icon in the map pane and then select **View Details**.
2.  Select next or previous buttons to view the details about other site.


</td></tr><tr><td id="d24631e243">

**View the physical and logical connections and topology details**

</td><td>

1.  Select a site.
2.  On the **Connectivity** filter option, select the option that you want to view the details.

    -   Physical Connections
    -   Logical Connections
    -   Topologies
These connection elements appear as dashed lines between the sites.

3.  Select a line to view the details on the details pane. The bar chart graph shows the available connection elements.


</td></tr><tr><td id="d24631e283">

**View the cable route between sites**

</td><td>

1.  Select a site.
2.  On the Connectivity filter, select **Cables**.
 The map pane displays the cable route between the sites.

**Note:** You must only select **Cables** to view the cable route.

</td></tr><tr><td id="d24631e322">

**View the capacity information**

</td><td>

Select a site and view the capacity information on the details pane. The bar chart graph represents the available capacity of the following:

-   Bearable weights
-   Rack Units
-   Allotted Power
-   Equipment Slots
-   Equipment Interfaces
-   Equipment Bandwidth
-   Card Slots
-   Card Interfaces
-   Card Bandwidth
 Select the a bar on the graph to redirect to the corresponding capacity metrics list.

</td></tr><tr><td id="d24631e369">

**View the change requests**

</td><td>

Select a site to view the number of associated change requests on the details pane. Only the change requests assigned to the logged-in user are displayed.

</td></tr></tbody>
</table>
**Parent Topic:**[Using the geo map](../concept/using-network-site-map.md)

**Related topics**  


[Visualization of geo map](../concept/visualization-map.md)


---
title: View details of the geo map
description: Use the geo map to view the geographical location of a network site and datacenter and its details in the Telecommunications Network Inventory application. You can understand the detailed overview of the site and information about the connections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/view-details-network-site-map.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Geo map, Network visualization view, Use, Telecommunications Network Inventory]
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

2.  Select the blue hub icon \[Omitted image "icon-blue-hub.png"\] Alt text: Blue Hub Icon..

    The Network visualization window is displayed.

3.  Select the **Geo map** tab.

4.  View the details of the site by performing the following actions on the map pane.

<table id="choicetable_qtk_fr3_yxb"><thead><tr><th align="left" id="d28424e121">

Action

</th><th align="left" id="d28424e124">

Details

</th></tr></thead><tbody><tr><td id="d28424e130">

**View the details of a site.**

</td><td>

Hover over the map icon on the map pane and then select **View Details**. You can view the site details on the details pane. You can also view the image of the site. To learn more about how to upload an image, see [Add images to a network inventory record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/add-image-network-invetory-record.md).

 **Note:** If you select the datacenter on the map pane, select **View floor map** to view the floor map. The **View Floor Map** automatically populates the campus only. You must manually select a building and floor to view the corresponding floor map.

</td></tr><tr><td id="d28424e161">

**View the details of the sites in the same location.**

</td><td>

1.  Hover over the map icon in the map pane and then select **View Details**.
2.  Select next or previous buttons to view the details about other site.


</td></tr><tr><td id="d28424e182">

**View the physical and logical connections and topology details**

</td><td>

1.  Select a site.
2.  On the **Connectivity** filter option, select the option that you want to view the details.

    -   Physical Connections
    -   Logical Connections
    -   Topologies
These connection elements appear as dashed lines between the sites.

3.  Select a line to view the details on the details pane. The bar chart graph shows the available connection elements.


</td></tr><tr><td id="d28424e218">

**View the cable route between sites**

</td><td>

1.  Select a site.
2.  On the Connectivity filter, select **Cables**.
 The map pane displays the cable route between the sites.

**Note:** You must only select **Cables** to view the cable route.

</td></tr><tr><td id="d28424e248">

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

</td></tr><tr><td id="d28424e293">

**View the change requests**

</td><td>

Select a site to view the number of associated change requests on the details pane. Only the change requests assigned to the logged-in user are displayed.

</td></tr></tbody>
</table>
**Parent Topic:**[Geo map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-network-site-map.md)

**Related topics**  


[Geo map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/visualization-map.md)


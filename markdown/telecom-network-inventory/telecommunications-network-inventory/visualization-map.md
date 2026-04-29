---
title: Geo map
description: Use the geo map in Telecommunications Network Inventory to view the geographical location of your network sites and datacenters. You can use the geo map to get the details of the network site and datacenters such as site details, connectivity, and capacity information.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Visualize network infrastructure, Explore, Telecommunications Network Inventory]
---

# Geo map

Use the geo map in Telecommunications Network Inventory to view the geographical location of your network sites and datacenters. You can use the geo map to get the details of the network site and datacenters such as site details, connectivity, and capacity information.

## Geo map overview

The geo map \(outdoor map\) geographically displays the network sites and datacenters on a map pane including the details of the connections. It provides an overview of the site and details about the various connections that are connected between the sites. You can view the following information using the geo map.

-   Geographical location of network sites and datacenters.
-   Connection elements associated with the site such as physical and logical connection, topology, and cable route.
-   Associated sites of a network site that you're selected.
-   Related information of a site including the capacity information.

## Map layout and features

The following example shows the geo map layout in the Telecommunications Network Inventory application.

![View of a Geo map layout.](../image/network-site-map.png "Geo map layout")

<table id="table_crd_4hd_ndc"><thead><tr><th>

Callout

</th><th>

Feature

</th><th>

 

</th></tr></thead><tbody><tr><td>

1

</td><td>

Navigation panel

</td><td>

Use the navigation panel to view a list of locations and sites they’re associated with each location. The navigation panel has the following tabs:

-   **All Sites**

Lists all network sites and datacenters.

-   **My Sites**

Lists the network sites and datacenters that you’re managing.


 **Note:** Sites without any location details are listed under **Other sites** and are displayed as inactive.

 Select location or site in the navigation panel to zoom to its corresponding area in the map pane.

</td></tr><tr><td>

2

</td><td>

Filter options

</td><td>

Map pane displays the network sites and datacenters based on the filter condition that you set. Use the following options to filter the network sites:

-   **Domain**

Filters the sites based on the domain name.

-   **Stage**

Filters the sites based on the life-cycle stage.

-   **Connectivity**

Displays the type of connections such as physical and logical connection, topology, and cable for a network site that you’re selected on the map pane.


**Note:** The datacenter doesn't show cable filter option.

</td></tr><tr><td>

3

</td><td>

Map pane

</td><td>

The map pane displays the network site and datacenter with a location icon \(![Location Icon](../image/icon-location.png)\). You can zoom in or out of the map using the plus \(+\) or minus \(-\) buttons. When you zoom out, the sites that are closely situated near each other geographically, appear as cluster icon \(![Cluster Icon](../image/icon-cluster.png)\) on the map pane. The number that is next to a cluster indicates the number of sites in that cluster. If a same location has multiple sites, it shows as a location cluster icon \(![Location Cluster Icon](../image/icon-location-cluster.png)\). The location icon with red color \(![Red Location Icon](../image/icon-location-red.png)\) indicates that the site exceeds the capacity threshold. By default the map pane shows all the sites that are exceeded the capacity threshold. The `sn_ni_adv.threshold_capacity_site_usage` system property maintains the value of the threshold of site capacity usage in percentage.

 You can view the following information with the map pane:

-   View the associated sites by selecting a network site or datacenter.
-   Hover over a site shows the site-specific information.
-   View the physical and logical connections between the sites.
-   View the cable route between the sites.
-   View the topology that is associated with a site.

</td></tr><tr><td>

4

</td><td>

Details pane

</td><td>

The details pane shows the related information about a network site or datacenter that you’re selected in the map pane. You can select the info icon \( ![Info Icon](../image/icon-info.png)\) to view the details pane. If a location has multiple sites, the details pane shows the related information about all the sites. You can also view the available capacity of the site in the details pane.

</td></tr><tr><td>

5

</td><td>

Search box

</td><td>

Use the search box to select a site to view its location and details. You can select one site at a time.

</td></tr></tbody>
</table>## Access

You can access the geo map in the Telecommunications Network Inventory workspace as follows:

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Select the blue hub icon \(![Blue Hub Icon.](../image/icon-blue-hub.png)\) to open the Network visualization window.
3.  Select **Geo map** tab.

To learn more about how to use the geo map, see [View details of the geo map](../task/view-details-network-site-map.md).

**Related topics**  


[Geo map](using-network-site-map.md)


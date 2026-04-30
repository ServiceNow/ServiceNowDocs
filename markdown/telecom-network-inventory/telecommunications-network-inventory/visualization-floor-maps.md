---
title: Visualization of floor map
description: Use the floor map in the Telecommunications Network Inventory application to view a layout of your datacenter infrastructure. You can view the network assets placement and monitor the operational data on the map.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-05-06"
reading_time_minutes: 4
breadcrumb: [Visualization of your network infrastructure, Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Visualization of floor map

Use the floor map in the Telecommunications Network Inventory application to view a layout of your datacenter infrastructure. You can view the network assets placement and monitor the operational data on the map.

## Floor map overview

The floor map provides a visual representation of your datacenter floor. Use the floor map to view the layout of your datacenter infrastructure including network asset placement and operational details to monitor power, thermal, and usage data. You can view alerts, incidents, changes requests, and capacity information of the datacenter.

You can view the following information using the floor map.

-   Details of the objects on the floor
-   View operational data
-   View alert information
-   Visualize a rack
-   View floor and rack health information

## Floor map layout and features

The following example shows a floor map layout in the Telecommunications Network Inventory application.

![View of a floor map layout.](../image/floor-map.png "Floor map layout")

<table id="table_crd_4hd_ndc"><thead><tr><th>

Callout

</th><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Filter options

</td><td>

The map pane shows the floor map based on the filters that you set. Use the following options to filter the floor:

-   **Site**

Select the campus. A campus must be associated with any network site or datacenter. The associated configuration item \(CI\) must also have TNI entity attributes.

-   **Building**

Select the building within a campus.

-   **Floor**

Select the floor in the building. The map pane displays the floor map for the selected floor.

-   **Filter By Account**

Select the company account to group the network assets. You can filter accounts to show that service-related infrastructure.

-   **View By**

Select the type of overlay to view the operational data such as Power, Temperature, and RU Utilization.

-   **Time duration**

Select the time duration for the operational metric data.


</td></tr><tr><td>

2

</td><td>

Map pane

</td><td>

The map pane displays the objects of a datacenter floor, including the following details.

-   Places with boundary line.
-   Markers on the datacenter floor.
-   Places that are associated with a rack or cabinet CI in bluish green color.
-   Places that are associated with other facility hardware in yellow color.
-   Selected place borders are highlighted in black color.
-   Places that haven't been mapped with a CI appears in gray color.
-   Alert information with an alert icon \(![Alert Icon.](../image/icon-alert-floor-map.png)\) on a place that is associated with a rack CI.
-   Temperature, Power, and RU Utilization data with color-coded rack overlays according to map legend.
-   View map legends of metric overlay and network assets color codes.

 You can zoom in or out of the map using the plus \(+\) or minus \(-\) buttons.

</td></tr><tr><td>

3

</td><td>

Details pane

</td><td>

The details pane shows the related information about a place that you’re selected in the map pane. Select the info icon \( ![Info Icon](../image/icon-info.png)\) to view the details pane. When you first open the details pane, it shows the details of the floor. Select a place to learn more about it. If a configuration item \(CI\) is associated with that place, you see the details about that CI.

 Select the alert icon \(![Alert Icon.](../image/icon-alert-floor-map.png)\) on the map pane to view the details of the alerts, incidents, and change requests that are associated with the corresponding CI. You can also select the green lightening bolt icon \( ![Green Lightening Bolt Icon.](../image/icon-green-lightening-bolt.png)\) on the details pane to view the same details.

 **Note:** Alerts are displayed when the Telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) plugin is installed. Incidents are displayed when the Customer Service Problem Management \(sn\_sprb\_mgmt\) plugin is installed.

</td></tr><tr><td>

4

</td><td>

Search box

</td><td>

Use the search box to find hardware on the map pane. The searched hardware is highlighted on the map. If the hardware is located directly on the floor \(not inside a rack\), the system highlights the exact location of the hardware on the floor map. Search option also highlights the hardware within the Rack view if the searched hardware is placed within a rack or cabinet.

</td></tr><tr><td>

5

</td><td>

Rack view

</td><td>

Rack view shows the visual representation of a rack. The Rack view also shows the warning labels for alerts, incidents, and change requests. Select a rack CI in the map pane to open the Rack view.

</td></tr></tbody>
</table>## Managing your floor map

You can upload and manage the datacenter map objects using the Indoor Mapping Map Studio. You can view the respective floor plans for a selected building in a datacenter campus using the floor map. To learn more, see [Upload and manage floor map for your datacenter](../task/create-floor-map-data-center.md).

## Access

Access the floor map in the Telecommunications Network Inventory workspace as follows:

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Select the blue hub icon \(![Blue Hub Icon.](../image/icon-blue-hub.png)\).
3.  Select the **Floor map** tab.

To learn more about how to use the floor map, see [Using the floor map](using-floor-map.md).


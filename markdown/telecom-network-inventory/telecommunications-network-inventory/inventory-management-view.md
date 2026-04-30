---
title: Management view
description: Use the Inventory management view in the Telecommunications Network Inventory Workspace to get a detailed view of your network inventory.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Network Inventory Workspace, Explore, Telecommunications Network Inventory]
---

# Management view

Use the Inventory management view in the Telecommunications Network Inventory Workspace to get a detailed view of your network inventory.

The Inventory management view displays the network inventory details such as equipment, equipment holders, network sites, and connections. Use the following tabs to view the inventory details and take appropriate actions:

-   **Overview**

    View various inventory data, such as total number of equipment grouped by the model, manufacturer, and life-cycle state, and availability of racks, ports, and slots within a site that you’re selected.

-   **Inventory List**

    View a list of network sites or network assets such as equipment and connections based on the option that you’re selected in the side panel.


## Overview tab

Use the **Overview** tab for a consolidated view of various network inventory data within a network site that you’re selected.

![Inventory Management view of the current status of network assets.](../image/inventory-management-view.png "Inventory management view")

Select any widget or chart to view the list of items that needs your action.

<table id="table_lwq_tml_lzb"><thead><tr><th>

Widget or chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Equipment by model

</td><td>

Number of the individual pieces of equipment grouped by model. The widget contains a standard set of the five most used telecommunications equipment models. For each equipment model, you can view a total count of the equipment.

</td></tr><tr><td>

Equipment by manufacturers

</td><td>

Donut chart grouping of equipment by the manufacturers who supply them. The widget contains a standard set of the five most used telecommunications equipment manufacturers. For each manufacturer, you can view a total count of equipment.

</td></tr><tr><td>

Equipment by life-cycle state

</td><td>

Donut chart grouping of equipment by the current life-cycle state. The widget contains the number of equipment in the network sites that you’re selected, grouped by the following life-cycle states.-   In Use
-   Empty
-   Reserved
-   Available
-   In Maintenance
-   Other

</td></tr><tr><td>

Racks at capacity threshold

</td><td>

Number of racks that are occupied more than threshold capacity.

</td></tr><tr><td>

Racks with available RUs

</td><td>

Number of racks with available rack units.

</td></tr><tr><td>

Rack availability by maximum contiguous RU

</td><td>

Bar chart representation of available racks with maximum contiguous rack units.

</td></tr><tr><td>

Slot availability

</td><td>

Number of available slots across the equipment models.

</td></tr><tr><td>

Port availability

</td><td>

Number of available ports across the equipment models.

</td></tr></tbody>
</table>**Note:** To learn more about how the count data is collected and refreshed in the workspace landing page, see [Data collection and refresh for the Network Inventory Workspace widgets](data-collection-niw-widgets.md). To learn how to customize the content that appears in each widget, see [Customizing the content in your Network Inventory Workspace widgets](customizing-content-in-your-network-inventory-workspace-widgets.md).

## Inventory list tab

Use the **Inventory list** tab to view a list of network sites or network assets based on the item that you selected in the side panel and take appropriate actions. The side panel lists the following:

-   All the locations that are available in the global location.
-   All the network sites that are available in the global location.
-   Network assets such as equipment and connections that are associated with each network site.

![List view of network sites in the Hyderabad location.](../image/inventory-list-view.png "Inventory list tab")

You can perform the following actions in the **Inventory list** tab.

-   In the side panel, expand the location to view the associated network sites.
-   Select a location to view the associated network site records in the list view.
-   In the side panel, expand each network site to view any associated connections or equipment.
-   Select**Equipment** to view the list of associated connections or equipment records.
-   Select **Connection** to view the list of associated physical and logical connection records within the network site.
-   Select a record in the list view to redirect to its form view.

## Accessing the Inventory management view

To open the Inventory management view, select the database search icon \(![Database Search Icon](../image/icon-database-search.png)\) on the side panel.

**Parent Topic:**[Network Inventory Workspace](exploring-network-inventory-workspace.md)


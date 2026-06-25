---
title: Visualization of a rack or cabinet
description: Using rack or cabinet visualization in the Telecommunications Network Inventory application, you can visualize a rack or cabinet in the canvas. Here you can observe the loading of equipment and shelves into the front and rear accessible racks or cabinets, with each item placed in its designated Rack Units.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/visualization-of-rack.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Visualization of a rack or cabinet

Using rack or cabinet visualization in the Telecommunications Network Inventory application, you can visualize a rack or cabinet in the canvas. Here you can observe the loading of equipment and shelves into the front and rear accessible racks or cabinets, with each item placed in its designated Rack Units.

## Rack visualization overview

Rack or cabinet visualization is a graphical representation of a datacenter rack or cabinet used to store and organize all equipment.

\[Omitted image "rack-visualization.png"\] Alt text: A rack where front and rear view of a rack loaded with equipments, and shelves along with the equipment or shelf details.

The previous screenshot is an example of a rack. From the **Overview** tab of a rack or cabinet, you can:

-   See the KPI \(Key Performance Indicator\) of a rack using rack utilization.

    **Note:** This KPI is only for racks.

-   See the percentage of allocated power currently utilized by all equipment within the rack. This value is derived from the equipment model details. However, the actual power consumption might vary.

    **Note:** This KPI is only for racks.

-   See the percentage of allocated weight currently utilized by all equipment within the rack. This value is derived from the equipment model details. However, the actual weight consumption might vary.

    **Note:**

    -   All rack capacities are calculated based on the capacity definition - rack capacity. To change the evaluation of the capacity, you can create a capacity definition and function. To learn more, see [Configuring capacity management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/configuring-capacity-management.md).
    -   This KPI is only for racks.
-   Explore different equipment types to optimize the placement of routers, shelves, or other network infrastructure.
-   See both the front and rear views of the rack or cabinet.
-   See all the reserved units and reserved by which user.
-   See the rack or cabinet and rack or cabinet models.
-   Create equipment from a rack or cabinet view. To learn more, see [Create a rack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-a-rack.md).
-   Edit a rack. To learn more, see [Edit rack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-rack.md).
-   Edit a cabinet. To learn more, see [Edit a cabinet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-a-cabinet.md).
-   Add packs
-   Decommission a rack or cabinet. To learn more, see [Decommission an inventory record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/decommision-an-inventory-record.md).
-   Delete a rack or cabinet. To learn more, see [Delete a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/delete-inventory-record.md).
-   Navigate to the rack/cabinets/slots form either from the canvas or the menu item.
-   See life-cycle stage of equipment.
-   See all the equipment and shelf details by selecting the info icon \(\[Omitted image "icon-info.png"\] Alt text: Info Icon.\).
-   See the number of total and occupied slots available.
-   Switch between the default and dark view using the preferences settings.

## Pre-requisites

To instantiate the creation of a rack or cabinet, you must:

1.  Create or select a model in the equipment holder model with the Equipment Rack or Cabinet **Model categories** to associate it with a rack or cabinet respectively.

    To learn more, see [Create an equipment holder model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-equipment-holder-models.md).

2.  Create or select a relationship in the network model relationships with the Rack/Cabinet to Rack/Cabinet Slot **Relationship type** to define the number of rack slots.

    To learn more, see [Define a network model relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-network-model-relationships.md).

3.  Create or select a template having the rack or cabinet model in the **inventory model** field.

    To learn more, see [Create an inventory template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-inventory-templates.md).


## Visualize and manage a rack or cabinet

1.  Initiate the rack or cabinet creation based on the rack or cabinet model, and rack or cabinet slots based on the template. To learn more, see [Create a change request from Network Inventory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_a_change_request_in_tni.md).

    **Note:**

    -   You can create a rack using [Create a rack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-a-rack.md).
    -   You can create a cabinet using [Create a cabinet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-a-cabinet.md).
2.  Add an equipment or shelf to a rack or cabinet. To learn more, see [Create a change request from Network Inventory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_a_change_request_in_tni.md).

    **Note:** You can also edit, add, move, and remove an equipment using [Edit rack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-rack.md) and [Edit a cabinet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-a-cabinet.md).

3.  Remove an equipment or shelf from a rack or cabinet.

    To learn more, see [Create a change request from Network Inventory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create_a_change_request_in_tni.md).


**Related topics**  


[Create a rack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/edit-a-rack.md)

[Create a cabinet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-a-cabinet.md)


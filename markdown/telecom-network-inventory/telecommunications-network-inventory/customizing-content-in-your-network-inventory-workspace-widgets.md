---
title: Customizing the content in your Network Inventory Workspace widgets
description: The Network Inventory Workspace is delivered in the base system with a standard set of information in each landing page widget. You can easily customize this content to include other Telecommunications Network Inventory data.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Define inventory records, Use, Telecommunications Network Inventory]
---

# Customizing the content in your Network Inventory Workspace widgets

The Network Inventory Workspace is delivered in the base system with a standard set of information in each landing page widget. You can easily customize this content to include other Telecommunications Network Inventory data.

## Standard CMDB groups and naming conventions for Network Inventory Workspace widget data

The data collection process for the Network Inventory Workspace landing page uses a standard CMDB group structure to retrieve data that appears in its widgets, including:

-   Network sites overview
-   Network entities by category
-   Network equipment by manufacturer
-   Network equipment by states

For example, the following shows a listing of some of the CMDB groups that are used for the Network Inventory Workspace data collection:

![CMDB groups view for the Network Inventory Workspace with the list of standard CMDB groups.](../image/ni-workspace-cmdb-groups.png "Standard CMDB groups for the Network Inventory Workspace")

**Note:** To learn how the data collection process operates, see [Data collection and refresh for the Network Inventory Workspace widgets](data-collection-niw-widgets.md).

These CMDB groups follow the following standard naming convention:

1.  The first segment represents the assigned domain for the network sites and entities. You use the Network domain selector in the Network Inventory Workspace to filter the data that appears by selecting one of the following types of network domains:
    -   **Core**

        Network domain for the core telecom equipment.

    -   **Mobility**

        Network domain for the mobile telecom equipment.

    -   **Telco**

        Network domain for the telecom equipment in general.

    -   **All**

        All equipment network domains that are combined into a single one for reporting purposes.

2.  The remaining segments represent a specific type of field data. For example:
    -   **Available Status Equipment**

        Reports the Available status for the equipment.

    -   **Pending Repair Status Equipment**

        Reports the Pending Repair status for the equipment.

    -   **Ericsson Manufacturer Equipment**

        Reports the percentage of the total equipment that is supplied by Ericsson.

    -   **Nokia Manufacturer Equipment**

        Reports the percentage of the total equipment that is supplied by Nokia.


The following examples show how the name segments are combined in the CMDB groups to report the data that appears in the widgets in the Network Inventory Workspace:

-   **All Available Status Equipment**

    CMDB group data that is used in the Network equipment by states widget to report the percentage of equipment that is in the Available status in all network domains.

-   **Core Available Status Equipment**

    CMDB group data used in the Network equipment by states widget to report the percentage of equipment that is in an Available status in the Core network domain.

-   **Mobility Pending Repair Status Equipment**

    CMDB group data used in the Network equipment by states widget to report the percentage of equipment that is in a Pending Repair status in the Mobility network domain.

-   **All Ericsson Manufacturer Equipment**

    CMDB group data that is used in the Network equipment by manufacturer widget to report the total piece count for the equipment that is supplied by Ericsson in all network domains.

-   **Telecom Nokia Manufacturer Equipment**

    CMDB group data that is used in the Network equipment by manufacturer widget to report the total piece count for the equipment that is supplied by Nokia in the Telecom network domain.


## Modifying the Network equipment by manufacturer widget

This widget contains a pie chart with a standard set of the five most recognizable telecommunications equipment manufacturers.

![Donut chart for the five most recognizable telecommunications equipment manufacturers.](../image/ni-workspace-network-equipment-by-manufacturer.png "Network equipment by manufacturer widget")

A pre-defined CMDB group structure supports retrieval of the data that appears in the widget pie chart. The following example shows the standard CMDB groups that are used to retrieve the manufacturer data for the Network Inventory Workspace.

![CMDB groups view for the Network Inventory Workspace with the list of standard CMDB groups.](../image/ni-workspace-network-equipment-manufacturer-cmdb-groups.png "Standard CMDB groups used for the Network equipment by manufacturer widget")

To add or change the data in a widget, use the CMDB Groups function to create CMDB group codes or modify the accompanying query conditions for existing ones. To update any of the existing CMDB groups, you must follow the standard CMDB group naming convention used for the Network Inventory Workspace widgets.

**Note:** To learn more about creating, updating, or naming CMDB groups, see CMDB groups.

For example, let's say that you want to add another equipment manufacturer to the widget. To accomplish this task, you can use existing CMDB groups for a manufacturer, for each of the network domains, as the base for the new manufacturer. In this example, you use the existing CMDB groups for Ericsson as the base for the CMDB groups that you create for the new manufacturer.

This table shows what the existing CMDB group codes look like for Ericsson, and what they look like when you create the CMDB group codes for Dell.

|Existing CMDB Group|Existing CMDB Group|
|-------------------|-------------------|
|All Ericsson Manufacturer Equipment|All Dell Manufacturer Equipment|
|Core Ericsson Manufacturer Equipment|Core Dell Manufacturer Equipment|
|Mobility Ericsson Manufacturer Equipment|Mobility Dell Manufacturer Equipment|
|Telco Ericsson Manufacturer Equipment|Telco Dell Manufacturer Equipment|

-   **[Update CMDB groups for use in the data collection process](../task/updating-cmdb-groups-niw-data-collection-process.md)**  
Add or change the data that you see in a Network Inventory Workspace widget by using the CMDB Groups function. You create CMDB group codes as needed or modify the query conditions for existing ones. By changing the CMDB groups, you affect what data the collection process retrieves for the widgets on the Network Inventory Workspace landing page.

**Parent Topic:**[Reviewing and updating your network inventory with the Network Inventory Workspace](tni-workspace.md)

**Related topics**  


[Network Inventory Workspace](exploring-network-inventory-workspace.md)


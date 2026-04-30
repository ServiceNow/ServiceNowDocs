---
title: Service Operations Workspace for Telecommunications Network Inventory user interface
description: Explore the Service Operations Workspace for Telecommunications Network Inventory interface to understand how an operator can prioritize network inventory tasks and offer solutions.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-06-05"
reading_time_minutes: 4
breadcrumb: [Service Operations Workspace for Telecommunications Network Inventory, Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Service Operations Workspace for Telecommunications Network Inventory user interface

Explore the Service Operations Workspace for Telecommunications Network Inventory interface to understand how an operator can prioritize network inventory tasks and offer solutions.

## Accessing Service Operations Workspace

From the **Workspaces** menu, select **Service Operations Workspace**.

## Landing page

The landing page in the Service Operations Workspace for Telecommunications Network Inventory provides an overview of the current operational landscape of your datacenter. The landing page includes the important items such as datacenter overview, list of your and your team's assignments including change requests, alerts, and incidents.

![Service Operations Workspace for TNI landing page view of the current status of your assignments.](../image/sow-tni-landing-page.png "Example of the landing page of Service Operations Workspace for Telecommunications Network Inventory")

Widgets in the landing page might look different based on the Telecommunications Service Management \(TSOM\) and Telecommunications Service Operations Management \(TSOM\) applications you have installed.

<table id="table_mlf_3g4_4fc"><thead><tr><th>

Widget type

</th><th>

Widget and Description

</th></tr></thead><tbody><tr><td>

Important Items

</td><td>

-   **Critical incidents**

Total count of incidents that are critical.

-   **Critical alerts**

Total count of alerts that are critical.

-   **My open change requests**

Total count of open change requests.

-   **Critical change requests**

Total count of change requests that are critical.

-   **Critical tasks**

Total count of change tasks that are critical.

-   **Warranty expired**

Total count of network assets with expired warranties.


 **Note:**

With TSOM is installed, the following widgets appear.

-   Critical incidents
-   Critical alerts
-   Critical change requests
-   Warranty expired

With TSM is installed, the following widgets appear.

-   Critical incidents
-   Critical change requests
-   Critical tasks
-   Warranty expired

Without TSOM and TSM are installed, the following widgets appear.

-   My open change requests
-   Critical change requests
-   Critical tasks
-   Warranty expired

</td></tr><tr><td>

Data Center overview

</td><td>

-   **Power consumption**

Bar chart representation of total power supplied to datacenter.

-   **Rack Unit consumption**

Bar chart representation of rack usage of datacenter.

-   **Power usage effectiveness**

Bar chart representation of power usage of datacenter. Power Usage Effectiveness \(PUE\) is a measure of how efficiently a datacenter uses energy. It compares the total power used by the datacenter to the power used only by the equipment \(like servers\).


</td></tr><tr><td>

Your work/Your team's work

</td><td>

Select **Your work** to view your assignments, or select **Your team's work** to view your team's assignments.-   **Incidents**

List of all incidents.

-   **Alerts**

List of all alerts.

-   **Open change requests**

List of all open network change requests.

-   **Open change tasks**

List of all open network change tasks.


**Note:**

With TSOM is installed, the following widgets appear.

-   Incidents
-   Alerts

With TSM is installed, the following widgets appear.

-   Incidents
-   Open change requests

Without TSOM and TSM are installed, the following widgets appear.

-   Open change requests
-   Open change tasks

</td></tr></tbody>
</table>## Lists

From the Lists view, you can access most of the Telecommunications Network Inventory classes and functions. An agent can analyze the individual lists of incidents, alerts, change tasks, and so on, and take appropriate action. To learn more, see [Network Inventory Workspace Lists view](network-inventory-workspace-list-view.md).

To access the Lists view, select the list icon \(![List Icon.](../image/ni-workspace-list-icon.png)\)

![List tab in Service Operations Workspace.](../image/sow-list-view.png "List view tab")

The menus you see depend on the applications you have installed. If you install the TSOM and TSM, the Incidents and Alerts menu appears on the Lists view.

**Note:** You must install Service Operations Workspace Alert Management \(sn\_sow\_em\)" plugin to view the Alerts in the List menu.

To learn more about Telecommunications Network Inventory features, see [Exploring Telecommunications Network Inventory](exploring-telecommunicatons-network-inventory.md).

## Network visualization

The Network visualization view provides various options to explore the network infrastructure-related functions. You can use the Network visualization to view the geographical location of your network sites, the floor plan of a datacenter, and the topology of your network. To learn more, see [Visualization of your network infrastructure](data-center-inventory-management.md).

To access the Network visualization page, select the blue hub icon \(![Blue Hub Icon.](../image/icon-blue-hub.png)\).

![Network visualization page view.](../image/network-visualization-view.png "Example of Network visualization page")

## Inventory management

Use the Inventory management view in the Service Operations Workspace to get a detailed view of your network inventory. To learn more, [Network Inventory management view](inventory-management-view.md).

To open the Inventory management view, select the database search icon \(![Database Search Icon](../image/icon-database-search.png)\) on the side panel.

![Inventory Management view of the current status of network assets.](../image/inventory-management-view.png "Example of Inventory management view")

## Design and Assign your network service

The Design and Assign function provides step-by-step guidance for designing a network service. You can use the Design and Assign function to complete guided activities to design the network services and assign the network inventories. To learn more, see [Design and assign your network services](design-assign-playbook.md).

To access the Network visualization page, select the network visualization icon \(![Design Assign Icon](../image/icon-design-assign.png)\).

![Design and Assign home page with list of change requests.](../image/design-assign-homepage.png "Example of Design and Assign home page")

**Related topics**  


[Visualization of your network infrastructure](data-center-inventory-management.md)


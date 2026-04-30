---
title: Interacting with the Nexus map UI from the Workspace
description: Use the Nexus map \(Resilience map\) to define relationships between different records and configuration to show related data with hierarchy and plot those in a node map. You can examine the map's current configuration and identify areas for change. By modifying the configuration, you can observe how the map is updated accordingly.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 8
breadcrumb: [Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Interacting with the Nexus map UI from the Workspace

Use the Nexus map \(Resilience map\) to define relationships between different records and configuration to show related data with hierarchy and plot those in a node map. You can examine the map's current configuration and identify areas for change. By modifying the configuration, you can observe how the map is updated accordingly.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Operational Resilience Workspace** &gt; **List** &gt; **Services**.

2.  From any of the Services modules, open the desired record that you want to work on.

    You can open the record from one of the following Services modules:

    -   Services
    -   Business services
    -   Offerings
    -   Business processes
    -   Application services
    The following example shows the service record for IRCTC Web Portal.

    ![IRCTC Web Portal Application service record.](../image/appl-service-record-for-resil-map.png)

3.  To open and update the map view of the configuration record, select the **Resilience map** UI action.

    The **Resilience map** UI action is the default entry point for the node map and it’s configured as the primary access point. You can navigate to this map from any entity overview, such as a service or business service overview in the Operational Resilience Workspace. After doing so, you’re directed to the default resilience map that has been configured.

    **Note:** The sys\_id of the nexus map is defined in the respective declarative actions.

    Multiple Nexus maps: You can configure multiple Nexus maps for a single main node. When configuring a specific entity, such as a business service, you can create multiple Nexus map configurations. For example, you can configure a Nexus map for a business service resilience map group, which includes multiple buttons that link to different node maps. The group name can be customized to suit your needs.

    In the following example, two buttons are configured for the business service resilience map group, each depicting a specific node map. This functionality enables for a tailored visualization of the business service and its associated nodes. By customizing the group name and node maps, you can create a more informative and user-friendly Nexus map.

    ![Multiple Nexus maps.](../image/multiple-nexus-map-configs.png)

    When you navigate to the Resilience map, the default configuration loads automatically. Selecting a specific root node as shown in the example, displays the corresponding configuration associated with that node.

    ![Default configuration.](../image/appl-service-record-for-resil-map-root-node.png)

    The root node's styling is displayed, referencing a specific node within the map. The Main node configuration supports both top-to-bottom and bottom-to-top directions, enabling for flexible hierarchical visualization.

    The Direction column in the example shows that both upstream and downstream Main node configurations are enabled, reflecting the same hierarchy in the map.

    ![Direction.](../image/main-node-config-direction.png)

4.  To designate a different node as the primary node, simply select it from the map, select and hold \(or right-click\) on it, and choose the **Make this primary** option.

    The **Make this primary** option is shown in the example.

    ![Primary.](../image/appl-service-record-for-resil-map-root-node-primary.png)

    When you select this option, the map reloads, and a breadcrumb is added to reflect the newly designated root node. You can navigate back to the root node by selecting on the Home icon, which centers the root node on the page. The map then displays the upstream and downstream connections related to the root node.

    When you update a node to be the primary \(root\) node, the available options are limited to **Open record** and **Open 360° view** as shown in the example.

    ![Primary (root) node options.](../image/primary-node-two-options.png)

5.  To open the record associated with the node, select **Open record**.

    If you choose **Open record**, it redirects you to the node's overview page.

    ![Overview page.](../image/open-record.png)

6.  To open the 360º view associated with the node, select **Open 360º view**.

    Selecting **Open 360° view** loads the 360° view configured for that node, as defined in the node configuration settings.

    ![360° view.](../image/record-360-view.png)

7.  To navigate to the Service record or the list view, use the breadcrumb menu option in the UI.

    The example displays the breadcrumb trail navigation to the Service record.

    ![360° view.](../image/record-360-view.png)

8.  To search for a specific service on the map, select **Find on map**.

    The node map includes a "Find on map" feature that enables you to search for a specific service.

    ![Find on map.](../image/find-on-map.png)

    When you initiate a search, the corresponding node is highlighted in the map, and you can select it for further actions. Clearing the search returns the map to its previous state. You can also designate the searched node as the primary node, which updates the map to display the node as the root, along with its upstream and downstream connections.

9.  To view the list of grouped nodes or expand them individually, right-select on the grouped nodes.

    The node map displays grouped nodes, such as first node, second node, and third group as expandable.

    ![Grouped node.](../image/expand-fun-node.png)

    Right-selecting on the grouped node provides options to either view the open list, which lists the number of nodes grouped at that point, or expand the node.

    ![Open list option.](../image/open-list-option.png)

10. To view additional nodes associated with the selected node, expand the nodes.

    The node expansion feature enables you to view additional nodes associated with the selected node, such as the "passenger information" level shown in the example. The expansion of the nodes is updated dynamically based on the number of levels available, enabling a more detailed and controlled exploration of the node map. By using the expand and open list options, you can efficiently navigate the map and better understand the relationships between nodes.

    ![Grouped node.](../image/expand-fun-node.png)

11. To aggregate nodes at a specific level, change the main node configuration type from "Default" to "Group" and display the consolidated view.

    The node map includes an aggregation feature that enables you to group nodes at a specific level. You can change the main node configuration type from "Default" to "Group" as shown in the example.

    ![Group type.](../image/main-node-config-group-type.png)

    This action aggregates the nodes at the selected level, providing a more consolidated view.

12. To open the grouped nodes in the list format, right-select on the grouped node and select **Open list**.

    This action lists the entities that have been aggregated at that point, giving you a clear understanding of the nodes involved.

    ![Open list option.](../image/open-list-option.png)

13. To access information about the selected node from the side panel, choose the **Info** icon in the side-panel summary.

    The node map includes a side panel that provides an overview of the selected configuration. When a node is selected, the side panel displays its details, which update dynamically as you switch between nodes. The default information is shown initially. The **Info** icon is displayed in the side-panel summary as shown in the example.

    ![Info.](../image/info-icon-node.png)

14. To access information about the related lists for the selected node, choose the **Related lists** icon in the side-panel summary.

    For a selected node, the side panel shows its associated services and dependencies. For example, if you select the "delay alerts process" node, the side panel displays its three application services or dependencies. Switching to a different node, such as the root node, updates the services and dependencies displayed in the side panel.

    ![Related lists.](../image/related-lists-icon.png)

    For the selected node, you can view its associated services and dependencies. The **Refresh** option reloads the related lists to verify you have the most up-to-date information. Meanwhile, the **View all** option displays all available related lists, providing a comprehensive overview.

15. To access information about the red flags for the selected node, choose the **Red flags** icon in the side-panel summary.

    The side panel also displays red flags, which indicate issues or outages related to the selected node. When a node has a red flag, it’s marked as critical with an exclamation mark. For instance, if there's an outage or issue with a node like "SMS alert" or "live status update," it’s highlighted in red.

    ![Red flags for services.](../image/red-flag.png)

    For the selected node, the following red flags are displayed:

    -   Issues
    -   High risks
    -   Failed controls
    -   Change requests
    -   Tasks
    -   Operational vulnerabilities
    -   Incidents
    -   Outages
    -   Crisis events
    -   Vulnerabilities
    -   Third party risk assessments
16. Change the node configuration by modifying the Node Configuration setting in the Nexus map.

    The example shows how to update the Node Configuration setting in the Nexus map.

    ![Node configuration.](../image/node-config-modified.png)

    The modified Node configuration is shown in the example.

    ![Modified icons.](../image/node-config-modified-icons.png)

17. To customize the Edge status configuration such as changing the color, modify the settings in the Edge status configuration within the Nexus map configuration.

    In the example, the node's edges are highlighted in magenta.

    ![Edges of the node.](../image/edge-status-config-for-node.png)

    The example illustrates how to modify Edge status settings such as color and type.

    ![Modified Edge status configuration.](../image/edge-status-config-updated.png)

    When you save and reload the map, it reflects the updated edge configuration, displaying all edges as dashed lines in blue as shown in the example.

    ![Edges.](../image/edge-status-config-modified.png)

    To refresh the map, you can either return to the initial main node configuration or simply reload it.

18. To update the zoom level of the map, adjust the percentage of the map in the Zoom level window.

19. To zoom in or zoom out of the map, select "**+**" or "**-**" in the position menu bar.

    The Zoom in icon is shown in the example.

    ![Zoom in.](../image/zoom-in-icon.png)

20. To align the map to the home node, select the **Home** icon in the position menu bar.

    The Home icon is shown in the example.

    ![Home.](../image/align-to-home-node-icon.png)

21. To resize the map or fit the node to the screen, select the **Fit to screen** icon in the position menu bar.

    The Fit to screen icon is shown in the example.

    ![Fit to screen.](../image/fit-to-screen-icon.png)

22. To export the map, select the **Export map** icon in the position menu bar.

    The Export map icon is shown in the example.

    ![Export map.](../image/export-map-icon.png)



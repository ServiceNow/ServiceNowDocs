---
title: Unified Map
description: The Unified Map feature displays a graphical hierarchical map of the CMDB — CIs and the connections between them. Unified Map combines some of the capabilities of Dependency Views and of Service Mapping into a single map experience.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Unified Map

The Unified Map feature displays a graphical hierarchical map of the CMDB — CIs and the connections between them. Unified Map combines some of the capabilities of Dependency Views and of Service Mapping into a single map experience.

## Unified Map

Unified Map is included in CMDB Workspace.

Nodes on the map represent CIs in the CMDB and lines represent connections between CIs \(relationships, references, and other kinds of connection\). The relationships help you, for example, to assess the impact of a change to a selected node by showing CIs that are connected to it through relationships. Products such as [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), and [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) benefit from such information.

When the Service Mapping application is active, the map also shows the composition of service instances — useful with products such as [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) and [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US). For example, you can view all CIs that are members of the 'Revenue App' service instance. You can review historical changes and then, for example, filter the CIs so that only application CIs appear on the map.

## Opening a map

Use any of the following methods to open Unified Map:

-   Navigate to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
-   While working in the Service Graph Workspace, select **Use Unified Map to view CI relationships** in the Recommended tools section.
-   While working in the CMDB Workspace, select **Unified Map** in the Quick Links section.
-   On a CI form for any CI in an **operational** state, select **Open Map** to open a map with the CI as the home node.

    **Note:** An admin can specify additional *operational status* values for this option. For more information, see [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md).


**Tip:** To view a map in full-screen mode, select the Unpin All icon.

## Work areas on the map

![Elements of the Unified Map.](../image/um-annotated.png)

-   **A: Map**

    The map displays specified CIs and their connections \(CI relationships, references, and endpoint chains\). In the example, the CRM CI is the home node and the connections represent relationships with other CIs. Select any node to view details like related service instances, change history, and so on. For more information, see [Controlling Unified Map contents and appearance](../reference/unified-map-appearance.md).

    Two CIs might be connected by one or more relationships \(stored in the CI Relationship \[cmdb\_rel\_ci\] table\). For example, two CIs might be connected by the **Runs On::Runs**, **Depends On::Discovered From**, and by the **Owned By::Owns** relationships.

    -   A solid line indicates a relationship. The arrowhead indicates the dependent node.
    -   A dashed line indicates a reference.
    -   A badge on a line indicates the number of relationships between the CIs.
-   **B: Content controls**
    -   **Home node search box:** Search for and select the home node — the node to focus on \(CRM in the image\). For more information, see [Controlling Unified Map contents and appearance](../reference/unified-map-appearance.md).
    -   **Levels:** Specify the number of CI relationship levels that should appear on the map.
    -   **Filters ![](../image/icon-um-filter-outline.png):** Customize the map to focus on the CIs that you want to work on by filtering out \(hiding\) irrelevant CIs. You can filter by layer count, CI class, relationship type, discovery source, location, and CI ownership. Select the view icon ![](../image/icon-um-show-hide-filtered-items.png) to hide or show filtered CIs as dimmed view-only nodes. For more information, see [Use filters to specify which nodes should appear on a map](../task/unified-map-configure-filters.md).
    -   **Reload map ![](../image/icon-um-reload-map.png):** Reload the map after making changes.
    -   **Timeline ![](../image/icon-um-toggle-timeline.png):** The timeline indicates related items like incidents, problems, and changes over a specified period of time for the selected CI. You can use the timeline to visualize the history of changes to a CI and how they affect the topology of the CMDB. For more information, see [Viewing related items on the Unified Map timeline](unified-map-timeline-working-on.md).
    -   **Map editor ![](../image/icon-um-edit-map.png):** Use the map editor to add CIs to or remove CIs from the map and to update relationships in the CMDB. For more information, see [Editing maps in Unified Map](unified-map-editing-map.md)
-   **C: Toolbox**
    -   Use the toolbox to control visual aspects of the map such as zoom level or layout mode. For more information, see [Controlling Unified Map contents and appearance](../reference/unified-map-appearance.md).
    -   In the toolbox, select the Export map icon ![](../image/icon-um-save-as-pdf.png) to save the current appearance of the map as a PDF document on your local drive.
-   **D: Contextual side panel**
    -   The **Overview** panel \(![](../image/icon-um-overview-panel.png)\) displays summary data for all CIs that are associated with the home node — counts and types of CIs and connections, discovery sources, and so on. For more information, see [View a summary of map contents on the Overview panel](../task/unified-map-show-overview-panel.md).
    -   The **Attributes** panel \(![](../image/icon-um-attributes-panel.png)\) lists attributes like location and operational status for the selected CI or relationship. For more information, see [View the attributes of a CI or a relationship](../task/unified-map-show-attributes.md).
    -   The **Service instances** panel \(![](../image/icon-um-app-services-panel.png)\) lists details of mapped application services \(service instances\) associated with the selected CI. The Service Mapping application generates this type of map content. For more information, see [View service instances for a CI](../task/unified-map-show-app-service.md).
    -   The **Related items** panel \(![](../image/icon-um-related-items-panel.png)\) shows related items such as changes, active incidents, or active problems for the selected CI. For more information, see [View related items for a CI](../task/unified-map-show-related-items.md).
    -   The **Changes** panel \(![](../image/icon-um-changes-panel.png)\) lists changes to the selected CI such as changes to life cycle stage or operational state. For more information, see [View historical changes for a CI](../task/unified-map-show-ci-changes.md).

        Changes are also indicated on the timeline. For more information, see [Viewing related items on the Unified Map timeline](unified-map-timeline-working-on.md).

-   **E: Mini-map navigator**

    Use the navigator to set the zoom level or move the view to an area of interest. Select the icon to show or hide the navigator. For more information, see [Controlling Unified Map contents and appearance](../reference/unified-map-appearance.md).

-   **F: Timeline**

    The timeline indicates related items like incidents, problems, and changes over a specified period of time for the selected CI. You can use the timeline to visualize the history of changes to a CI and how they affect the topology of the CMDB. For more information, see [Viewing related items on the Unified Map timeline](unified-map-timeline-working-on.md).


**Related topics**  


[CMDB Workspace store app](cmdb-workspace.md)


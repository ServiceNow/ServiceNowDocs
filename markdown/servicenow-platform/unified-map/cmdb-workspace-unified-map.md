---
title: Unified Map
description: The Unified Map feature displays a graphical hierarchical map of the CMDB — CIs and the connections between them. Unified Map combines some of the capabilities of Dependency Views and of Service Mapping into a single map experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/unified-map/cmdb-workspace-unified-map.html
release: yokohama
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2025-04-04"
reading_time_minutes: 7
breadcrumb: [Unified Map, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Unified Map

The Unified Map feature displays a graphical hierarchical map of the CMDB — CIs and the connections between them. Unified Map combines some of the capabilities of Dependency Views and of Service Mapping into a single map experience.

## Unified Map

Unified Map is included in CMDB Workspace.

Nodes on the map represent CIs in the CMDB and lines represent connections between CIs. The connections help you, for example, to assess the impact of a change to a selected node by showing CIs that are connected to it through relationships. Products such as [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_ITILChangeManagement.md), [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_IncidentManagement.md), and [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/c_EM.md) benefit from such information.

The map also shows the composition of service instances — useful with products such as [Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/c_EM.md) and [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_IncidentManagement.md). For example, you can view all CIs that are members of the 'Revenue App' service instance. You can review historical changes and then, for example, filter the CIs so that only application CIs appear on the map.

## Accessing Unified Map

To enable Unified Map, enable the **sn\_sm\_scoped\_app.sa.unified\_map.enabled** system property.

Use either of the following methods to open a map:

-   Navigate to **Workspaces** &gt; **CMDB Workspace**. In the Quick Links section on the CMDB Workspace, select **Unified Map**.
-   On a CI form for a CI in an operational state, select **Open Map** to open a map with the CI as the home node.

    **Note:** An admin can specify additional operational status values for this option. For more information, see [Configure CIs to appear based on life cycle stage value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-confg-operational-state.md).


## Work areas on the map

\[Omitted image "um-annotated.png"\] Alt text: Elements of the Unified Map.

-   **A: Map**

    The map displays specified CIs and their connections. In the example, the CRM CI is the home node and the connections represent relationships with other CIs. Select any node to view details like related service instances, change history, and so on. For more information, see [Controlling Unified Map contents and appearance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-appearance.md).

    Two CIs might be connected by one or more relationships \(stored in the CI Relationship \[cmdb\_rel\_ci\] table\). For example, two CIs might be connected by the **Runs On::Runs**, **Depends On::Discovered From**, and by the **Owned By::Owns** relationships.

    -   A solid line indicates a relationship. The arrowhead indicates the dependent node.
    -   A dashed line indicates a reference.
    -   A badge on a line indicates the number of relationships between the CIs.
-   **B: Content controls**
    -   Search for and select the home node, specify the number of relationship levels to display for service instances, and reload the map after making changes. For more information, see [Controlling Unified Map contents and appearance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-appearance.md).
    -   Use filters to limit CI types and relationship types that appear on the map. For more information, see [Use filters to specify which nodes should appear on a map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-configure-filters.md).
    -   Show or hide the timeline of related items \(typically events\) for the selected CI. For more information, see [Viewing related items on the Unified Map timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-timeline-working-on.md).
    -   Open the map editor \(\[Omitted image "icon-um-edit-map.png"\]\) to add or remove CIs and to update relationships in the CMDB. For more information, see [Editing maps in Unified Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-editing-map.md)
-   **C: Toolbox**
    -   Use the toolbox to control visual aspects of the map, such as zoom level or layout mode. For more information, see [Controlling Unified Map contents and appearance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-appearance.md).
    -   In the toolbox, select the Export map icon \[Omitted image "icon-um-save-as-pdf.png"\] to save the current appearance of the map as a PDF document on your local drive.
-   **D: Contextual side panel**
    -   The **Overview** panel \(\[Omitted image "icon-um-overview-panel.png"\]\) displays summary data for all CIs that are associated with and downstream of the home node — counts and types of CIs and connections, discovery sources, and so on. For more information, see [View a summary of map contents on the Overview panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-show-overview-panel.md).
    -   The **Attributes** panel \(\[Omitted image "icon-um-attributes-panel.png"\]\) lists attributes like location and operational status for the selected CI or relationship. For more information, see [View the attributes of a CI or a relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-show-attributes.md).
    -   The **Service instances** panel \(\[Omitted image "icon-um-app-services-panel.png"\]\) lists details of service instances associated with the selected CI. For more information, see [View service instances for a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-show-app-service.md).
    -   The **Related items** panel \(\[Omitted image "icon-um-related-items-panel.png"\]\) shows related items such as changes, active incidents, or active problems for the selected CI. For more information, see [View related items for a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-show-related-items.md).
    -   The **Changes** panel \(\[Omitted image "icon-um-changes-panel.png"\]\) lists changes such as changes to operational status for the selected CI. For more information, see [View historical changes for a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-show-ci-changes.md).

        Changes are also indicated on the timeline. For more information, see [Viewing related items on the Unified Map timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-timeline-working-on.md).

-   **E: Mini-map navigator**

    Use the navigator to set the zoom level or move the view to an area of interest. Select the icon to show or hide the navigator. For more information, see [Controlling Unified Map contents and appearance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-appearance.md).

-   **F: Timeline**

    The timeline indicates related items like incidents, problems, and changes over a specified period of time for the selected CI. You can use the timeline to visualize the history of changes to a CI and how they affect the topology of the CMDB. For more information, see [Viewing related items on the Unified Map timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-timeline-working-on.md).


**Related topics**  


[CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)


---
title: Modify view for an application service map
description: Customize a map view to display relevant information and increase clarity.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Modify view for an application service map

Customize a map view to display relevant information and increase clarity.

## Before you begin

Role required: app\_service\_admin, app\_service\_user, service\_mapping\_admin, or service\_mapping\_user

## About this task

By default, service maps are concise and contain every detail about all CIs that you added manually or that Service Mapping mapped. While it provides a complete picture, using such a map might be difficult. Customizing maps allows you to:

-   make it easier to navigate the map.
-   hide irrelevant information.
-   show essential information.

Attributes you show or hide when you customize maps are not removed permanently and can be displayed or hidden again as you need. The system saves the changes to the map view and displays the last map view when you reopen a service instance.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Select the **Additional actions** menu.

    ![Select the Additional actions menu on the Map page.](../image/MapAdditionalActionsButton.png)

3.  Select the relevant option:

<table id="table_zww_2g4_ww"><thead><tr><th>

Option

</th><th>

When Enabled

</th><th>

When Disabled

</th></tr></thead><tbody><tr><td>

**Display in Host View** This option is available only when the Service Mapping plugin is activated.

 Switch between the CI view that hides hosts and the host view that hides CIs.

 The host view can help determine that Service Mapping discovered and mapped all hosts correctly as well as help locate connections to each host. The host view also simplifies the map especially when many applications are running on a few hosts.

 The Host View is useful only for service instances discovered using Service Mapping. This view does not offer additional information for manually created service instances.

</td><td>

The service map shows host CIs.

 ![Hosts displayed on the map.](../image/MapMoreOptionsHostOn.png)

 Click the plus icons to see application CIs running on the hosts.

 ![Applications running on a host displayed on the map](../image/MapMoreOptionsHostPlusSign.png)

 The **Properties** pane shows only information about servers who act as hosts.

</td><td>

The service map shows application CIs.

 ![CIs displayed on the map.](../image/MapMoreOptionsHostOff.png)

 The **Properties** pane shows information about both servers who act as hosts and applications running on the hosts.

</td></tr><tr><td>

**Group CIs on map** Simplify maps by grouping CIs belonging to the same type and hosted on servers sharing a prefix and domain name.

 The map still reflects the application flow correctly, because grouped CIs belong to the same tier.

 This option is relevant for service instances consisting of more than 10 CIs.

</td><td>

The service instance map shows groups of CIs. The map is more compact.

</td><td>

The service instance map shows all CIs separately. The map is larger.

</td></tr><tr><td>

**Remove Topology Cycles** This option is available only for users with these roles: Service Mapping administrator \[service\_mapping\_admin\] and Service Mapping user \[service\_mapping\_user\].

 Hide connections returning to the same configuration item \(CI\) that originated them to reduce map cluttering.

 Usually these returning connections are not important for analysis or troubleshooting of service instances.

</td><td>

The service instance map hides topology cycles.

 ![Topology cycles hidden on the map.](../image/MapMoreOptionsTopCyclOn.png)

</td><td>

The service instance map shows topology cycles.

 ![Topology cycles displayed on the map.](../image/MapMoreOptionsTopCyclOff.png)

</td></tr><tr><td>

**Show Traffic Based CIs** This option is available only for users with these roles: Service Mapping administrator \[service\_mapping\_admin\] and Service Mapping user \[service\_mapping\_user\].

 Display configuration items \(CIs\) found using traffic-based mapping.

</td><td>

The service instance map displays CIs and hosts that Service Mapping discovered using both patterns and traffic-based discovery.

 While detecting CIs inbound and outbound traffic creates an inclusive map, it may also result in mapping many redundant CIs that do not influence the service instance operation.

</td><td>

The service instance map shows only CIs and hosts discovered using patterns.

</td></tr><tr><td>

**Merge error nodes** This option is available only for users with the Service Mapping administrator \[service\_mapping\_admin\] role.

 Merge CIs with errors caused by the same source CI to declutter a service instance map.

 A discovery or operational error in a CI is often propagated to all its connections down the hierarchy crowding your view. You can remove identical errors caused by the same CI by consolidating them in one object on the map. For example, if one CI causes an error in six CIs that are connected to it, you can show only one CI with this error on the map. The connector line shows the number of actual connections.

</td><td>

The service instance map merges all CIs with identical errors into one. The number on the connector line indicates the number of CIs with this error.

 ![CIs displayed on the map.](../image/MapAddOptionsMergeErrorOn.png)

</td><td>

The service instance map shows all CIs with identical errors separately.

 ![CIs displayed on the map.](../image/MapAddOptionsMergeErrorOff.png)

</td></tr><tr><td rowspan="2">

**Map indicators** This option is available only for users with these roles: Service user \[app\_service\_user\] and Service Mapping user \[service\_mapping\_user\].

 Display additional information for a CI or service instance itself by displaying related records such as alerts, outages, incidents, and problems.

 The base system provides map indicators for the following record types:

-   Affected CIs
-   Open alerts
-   Current, planned, or recent change requests
-   Open incidents
-   Current, planned, or recent outages
-   Open problems
For more information, see [Event Management Map Indicators \(Video\)](https://www.youtube.com/watch?v=wjtpJe8J3iA).

</td><td>

For each record type that is set to display, the corresponding indicator and the tab display. For example, the **Incidents** tab appears underneath the map and the **Incidents** indicator shows next to CIs that have incidents associated with them.

 ![Map showing CI-related indicators.](../image/MapAddOptionsIndicOn.png)

</td><td>

The service instance map shows CIs without related indicators.

 ![Map with CI-related indicators hidden.](../image/MapAddOptionsIndicOff.png)

</td></tr><tr><td>

If a record is associated with the service instance itself, the indicator shows next to the service instance name.

 ![Map showing service instance related indicators.](../image/MapBSAddOptionsIndicOn.png)

</td><td>

No map indicators appear next to the service instance name.

 ![Map indicators for a service instance hidden.](../image/MapBSAddOptionsIndicOff.png)

</td></tr><tr><td>

**Spanning tree view** Simplify the map by organizing CIs into a tree structure and concealing some connection lines.

 This option is especially useful for very large maps.

</td><td>

The map displays a service instance as a tree.

 ![Map showing an service instance in the spanning tree view.](../image/MapAddOptionsSpanningTreeOn.png)

 To view actual connections, point to a CI. For more information on viewing connections, see [View CI connection attributes in an application service map in classic Service Mapping](view-connector-properties.md).

</td><td>

The map reflects the actual structure of a service instance.

 ![Map showing an service instance not in the spanning tree view.](../image/MapAddOptionsSpanningTreeOff.png)

</td></tr><tr><td>

**Include ignored errors** This option is available only for users with the Service Mapping administrator \[service\_mapping\_admin\] role.

 You can display errors which were previously hidden from the map.

</td><td>

The map shows all errors: both active and ignored.

</td><td>

The map does not show ignored errors.

</td></tr></tbody>
</table>
**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Create or modify map indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/t_CreateModifyNGBSMMapIndicators.md)


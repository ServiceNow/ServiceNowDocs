---
title: Modify view for an application service map in legacy Agent Workspace
description: Customize a map view to display relevant information and increase clarity.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Application service analysis and maintenance using legacy Agent Workspace, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Modify view for an application service map in legacy Agent Workspace

Customize a map view to display relevant information and increase clarity.

## Before you begin

Role required: service\_mapping\_user, sm\_app\_owner, evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

By default, service maps are concise and contain every detail about all CIs that you added manually or that Service Mapping mapped. While it provides a complete picture, using such a map might be difficult. Customizing maps allows you to:

-   make it easier to navigate the map.
-   hide irrelevant information.
-   show essential information.

Attributes you show or hide when you customize maps are not removed permanently and can be displayed or hidden again as you need. The system saves the changes to the map view and displays the last map view when you reopen a service instance.

The service instance map in the Event Management view reflects the severity status of CIs belonging to the service instance.

## Procedure

1.  In Agent Workspace, click the **Lists** icon on the left pane.

2.  Navigate to **Services** &gt; **All Services**.

    The list of services displays services in Operational status.

3.  Click the name of the relevant service instance.

    The service tab opens showing service details on the Details tab.

4.  Click **Service Map**.

5.  Click the **Open Map Display Settings** button.

    ![The Open Map Display Settings button](../image/ws-map-display-settings.png)

6.  Select the relevant option:

<table id="table_zww_2g4_ww"><thead><tr><th>

Option

</th><th>

When Enabled

</th><th>

When Disabled

</th></tr></thead><tbody><tr><td>

**Display in Host View** The host view also simplifies the map especially when many applications are running on a few hosts.

 The Host View is useful only for service instances discovered using Service Mapping. This view does not offer additional information for manually created service instances.

</td><td>

The service map shows host CIs.

</td><td>

The service map shows application CIs.

</td></tr><tr><td>

**Group CIs on map** Simplify maps by grouping CIs belonging to the same type and hosted on servers sharing a prefix and domain name.

 The map still reflects the application flow correctly, because grouped CIs belong to the same tier.

 This option is relevant for service instances consisting of more than 10 CIs.

</td><td>

The service instance map shows groups of CIs. The map is more compact.

</td><td>

The service instance map shows all CIs separately. The map is larger.

</td></tr><tr><td>

**Remove Topology Cycles** Hide connections returning to the same configuration item \(CI\) that originated them to reduce map cluttering.

 Usually these returning connections are not important for analysis or troubleshooting of service instances.

</td><td>

The service instance map hides topology cycles.

</td><td>

The service instance map shows topology cycles.

</td></tr><tr><td>

**Spanning tree view** Simplify the map by organizing CIs into a tree structure and concealing some connection lines.

 This option is especially useful for very large maps.

</td><td>

The map displays a service instance as a tree.

 ![Map showing an application service in the spanning tree view.](../image/ws-map-spanning-tree-enabled.png)

</td><td>

The map reflects the actual structure of a service instance.

 ![Map showing an application service not in the spanning tree view.](../image/ws-map-spanning-tree-disabled.png)

</td></tr><tr><td>

**Show Traffic Based CIs** This option is available only for users with these roles: Service Mapping administrator \[service\_mapping\_admin\] and Service Mapping user \[service\_mapping\_user\].

 Display configuration items \(CIs\) found using traffic-based mapping.

</td><td>

The service instance map displays CIs and hosts that Service Mapping discovered using both patterns and traffic-based discovery.

 While detecting CIs inbound and outbound traffic creates an inclusive map, it may also result in mapping many redundant CIs that do not influence the service instance operation.

</td><td>

The service instance map shows only CIs and hosts discovered using patterns.

</td></tr><tr><td rowspan="2">

**Map indicators** Display additional information for a CI or service instance itself by displaying related records such as alerts, outages, incidents, and problems.

 The base system provides map indicators for the following record types:

-   Affected CIs
-   Changes: Current, past, or planned
-   Outages: Current, past, or planned
-   Problem
 For more information, see [Event Management Map Indicators \(Video\)](https://www.youtube.com/watch?v=wjtpJe8J3iA).

</td><td>

For each record type that is set to display, the corresponding indicator and the tab display. For example, the **Incidents** tab appears underneath the map and the **Incidents** indicator shows next to CIs that have incidents associated with them.

</td><td>

The service instance map shows CIs without related indicators.

</td></tr><tr><td>

If a record is associated with the application service itself, the indicator shows next to the application service name.

</td><td>

No map indicators appear next to the application service name.

</td></tr></tbody>
</table>
**Parent Topic:**[Application service analysis and maintenance using legacy Agent Workspace](../concept/service-analysis-maintenance-legacy-workspace.md)


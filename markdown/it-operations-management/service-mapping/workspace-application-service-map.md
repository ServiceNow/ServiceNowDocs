---
title: Application service maps in legacy Agent Workspace
description: Maps offer you a visualization of data on configuration items \(CIs\) comprising application services, and relations and connections between these CIs.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application service analysis and maintenance using legacy Agent Workspace, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Application service maps in legacy Agent Workspace

Maps offer you a visualization of data on configuration items \(CIs\) comprising application services, and relations and connections between these CIs.

A new map is created every time you manually create an service instance or map an service instance using Service Mapping. The system updates the map every time you add CIs to the service instance or when Service Mapping runs discovery for CIs belonging to this service instance.

## Map window

Aside from the map itself, the Service Map may also display the basic service information like the severity, status, and application owner of the service. You can also view additional service information on the Service properties pane. Click the Related items icon to display all alerts or changes associated with CIs comprising this application service or the application service itself.

The service instance map in the Event Management view reflects the severity status of CIs belonging to the service instance.

![Service Mapping Map window](../image/ws-service-map-tab.png "Service Mapping")

By default, the entire map is shown in the center of the visible map area of the window. Position the map and zoom in and out using these controls.

![Control zoom and positioning of your map.](../image/MapZoomNavigation.png "Control zoom and positioning of your map")

You can also click anywhere in the map area and drag the required segment of the map into the visible area.

## CI attributes and CI-related messages

When a map is loaded and no elements are selected, the Service properties pane shows the details of this service instance.

A selected device, application, or connector appears in green and is highlighted. Information about the selected map element is displayed in the Properties pane on the right of the map.

![The Properties pane shows attributes for connections and CIs.](../image/ws-map-connection-prop.png "The Properties pane shows attributes for connections and CIs")

The attributes for the server hosting applications and applications themselves are shown separately inside the Properties pane.

![The Properties pane shows attributes for hosts and applications separately.](../image/ws-map-app-server-prop.png "The Properties pane shows attributes for hosts and applications separately")

## Related Items

Click the **Related Items** icon to display alerts or changes associated with this application service or its CIs.

If there is any information related to the selected CI or connection, it is highlighted in the Related Items pane on the right of the window.

![Select a CI to display information related to it.](../image/ws-map-selected-ci-alert.png "Select a CI to display information related to it")

When you select information in the Related Items pane on the right of the map window, the related CI displays in yellow.

![Selecting message marks the related CI yellow.](../image/ws-map-selected-alert-ci.png "Selecting message marks the related CI yellow")

You can display other related items, such as planned changes or cases, associated with the application service. For more information, see [Modify view for an application service map in legacy Agent Workspace](../task/workspace-modify-map-view.md).

**Parent Topic:**[Application service analysis and maintenance using legacy Agent Workspace](../concept/service-analysis-maintenance-legacy-workspace.md)

**Related topics**  


[View an alert impact on CIs in a service map](../../event-management/task/t_EMViewTopology.md)


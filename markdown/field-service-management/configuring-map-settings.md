---
title: Configure the appearance of the map in Dispatcher Workspace
description: Configure map settings to define the style and appearance of the map in Dispatcher Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configure the appearance of the map in Dispatcher Workspace

Configure map settings to define the style and appearance of the map in Dispatcher Workspace.

## Before you begin

Role required: admin, wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Map Settings**.

2.  Set the system properties that control the map appearance.

<table id="table_h4y_tfj_rnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.hide\_map

</td><td>

Hide the map in Dispatcher Workspace.-   Type: Boolean
-   Default value: False


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.maximum\_auto\_zoom\_level

</td><td>

Maximum level to zoom out the map. Each map marker zooms the map while keeping the map marker stationary and restricts the map view to the maximum zoom level specified. -   Type: String
-   Default value: 12. Valid values are in between 1–20


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.refresh\_agent\_location

</td><td>

Enables the live display of agent routes from task to task on the dispatch map.-   Type: Boolean
-   Default value: True


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.refresh\_agent\_location\_interval

</td><td>

How often the map will check for an agent's updated location. If there is an update when the check is made, then the agent's location updates on the dispatch map. The value is in seconds.-   Type: String
-   Default value: 300. Don't set the value to below 60.


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.map\_type

</td><td>

Map type to use to view locations. -   Type: List
-   Default value: Roadmap

**Note:** Roadmap provides a default road map view. Choose **Satellite** for a Google Earth satellite view, **Hybrid** for a mixture of standard and satellite views, or **Terrain** for a topographical map based on terrain information.

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.map\_style

</td><td>

JSON code snippet, supported by the Google Map API to customize elements of the Google Map. Allows you to style features of maps, such as roads, water bodies, and day or night mode. -   Type: String
-   Default value: Null


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.street\_view\_enabled

</td><td>

Enables the street view service to display panoramic 360-degree views from designated roads throughout its coverage area. You can zoom and pan. Use street view on the map or panoramas directly within the map. -   Type: Boolean
-   Default value: True


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.sn\_fsm.dispatch\_ws\_map.route\_enabled

</td><td>

Enables the display of agent routes from task to task on the dispatch map. When this is enabled, the Agent route icon shows on the agent card. Selecting the Agent route icon displays the agent’s route to the work order task on the map. -   Type: Boolean
-   Default value: True


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.enable\_optimize\_route

</td><td>

Allows dispatchers to optimize agent routes from the dispatch map.-   Type: Boolean
-   Default value: True


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.cluster\_zoom\_level

</td><td>

Control the amount of zooming necessary to have icons cluster together. The lower the value, the more users have to zoom out before the markers to start clustering.-   Type: String
-   Default value: 15. Valid values are in between 1–20


</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.cluster\_label

</td><td>

Determine whether clustered pins show the number of markers \(Marker value\) or the number of items in a region \(Item value\). Markers group tasks, agents, and crews in a region into one pin. Items show tasks, agents, and crews in a region as individual pins.-   Type: List
-   Default value: Marker.


</td></tr></tbody>
</table>3.  Select **Save**.



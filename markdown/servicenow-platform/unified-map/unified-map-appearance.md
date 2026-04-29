---
title: Controlling Unified Map contents and appearance
description: Manipulating the contents and layout of a map can greatly assist with envisioning and optimizing your CMDB. You can control which elements appear on the map, isolate and analyze relationships between CIs, and simplify the map to isolate issues.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Controlling Unified Map contents and appearance

Manipulating the contents and layout of a map can greatly assist with envisioning and optimizing your CMDB. You can control which elements appear on the map, isolate and analyze relationships between CIs, and simplify the map to isolate issues.

**Important:** This topic describes changes that you can make to your view of the map. The changes do not affect other users. In contrast, administrators can configure general settings that affect all users in the workspace, as described in [Configuring Unified Map — admin settings](../concept/administer-unified-map.md).

## Save a map as a PDF document

In the toolbox, select the Export map icon ![](../image/icon-um-save-as-pdf.png) to save the current appearance of the map as a PDF document on your local drive.

## Controlling map content

<table id="table_kfz_hyf_sbc"><thead><tr><th>

Change

</th><th>

Tool and actions

</th></tr></thead><tbody><tr id="row-specify-home-node"><td>

Specify or change the home node

</td><td>

The home node is the CI that all other CIs on the map are associated with, directly or indirectly. The home node icon has a thicker border that pulsates. The map is redrawn when you specify a home node.

 Use either of the following methods:

 -   Use the **Search** box to find and select a CI.

-   Select and hold \(or right-click\) a node on the map and select **Set as home node**.

 **Note:** Connecting lines between nodes represent relationships and references, not data flow.

 -   In the vertical layout, the home node appears at the center of CI connections. Upstream connections appear at the top and downstream at the bottom. This is the default layout for displaying mapped service instances \(formerly application services\) \[cmdb\_ci\_service\_discovered\].
-   In the force layout, the home node appears at the center of CI connections.

</td></tr><tr><td>

Reload the map after a change

</td><td>

Select the Reload map icon ![](../image/icon-um-reload-map.png)

</td></tr><tr><td>

Configure a filter to display only pertinent items

</td><td>

Select the Filter icon ![](../image/icon-um-filter.png)

 When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of filter-setting precedence from the various sources is as follows:

1.  user presets
2.  shared presets
3.  shared presets that are defined in a **Unified Map shared presets** profile
4.  class profile \(Class profiles contain only layer settings and are defined in the **Node Map Profiles** related list.\)

 **Note:** Filter settings that would filter out the home node might appear in the list. You can't, however, filter out the home node even if it meets filter settings.

 For more information, see [Use filters to specify which nodes should appear on a map](../task/unified-map-configure-filters.md).

</td></tr><tr><td>

Show/hide filtered items

</td><td>

Select the Show/Hide filtered items icon ![](../image/icon-um-show-hide-filtered-items.png) to expose the filtered items on the map as dimmed view-only nodes.

 For more information, see [Use filters to specify which nodes should appear on a map](../task/unified-map-configure-filters.md).

</td></tr><tr><td>

Show complete CI details

</td><td>

Select a CI \(CI border thickens\) to display its details in the **Overview**, **Attributes**, **Service instances**,**Related items**, or **Changes** panel.

 For group CIs, such as a service instanceor a dynamic CI group, the **Attributes** panel also shows detail cards for the CIs that are members of the group.

</td></tr><tr><td>

Show relationship details

</td><td>

Two CIs might be connected by one or more relationships \(stored in the CI Relationship \[cmdb\_rel\_ci\] table\). For example, two CIs might be connected by the **Runs On::Runs**, **Depends On::Discovered From**, and by the **Owned By::Owns** relationships.

-   A solid line indicates a relationship. The arrowhead indicates the dependent node.
-   A dashed line indicates a reference.
-   A badge on a line indicates the number of relationships between the CIs.

Select a connection to display its attributes in the **Attributes** panel. For a CI with multiple relationships, select the badge to view details for all relationships.

</td></tr><tr id="row-level-setting-for-relationships"><td>

Set the number of relationship levels to display on the map

</td><td>

Use the **Levels** drop-down list to specify how many relationship levels to display on the map \(default 3\). A low setting is useful for viewing a simplified map that shows only direct connections and for limiting the overall size of a map. A higher setting enables you to review more complex CMDB structures.

 When a mapped application service \(service instance\) CI is set as the home node, the **Levels** setting has no effect and all levels of relationships appear.

 **Note:** Connecting lines between nodes represent relationships and references, not data flow.

</td></tr><tr><td>

Highlight the relationships between CIs

</td><td>

Point to a CI to animate the connections between CIs. Connected nodes are highlighted for a few seconds.

 Two CIs might be connected by one or more relationships \(stored in the CI Relationship \[cmdb\_rel\_ci\] table\). For example, two CIs might be connected by the **Runs On::Runs**, **Depends On::Discovered From**, and by the **Owned By::Owns** relationships.

 -   A solid line indicates a relationship. The arrowhead indicates the dependent node.
-   A dashed line indicates a reference.
-   A badge on a line indicates the number of relationships between the CIs.

 **Note:** Connecting lines between nodes represent relationships and references, not data flow.

</td></tr><tr id="row-view-mapped-app-svcs"><td>

View mapped application services \(service instances\)

</td><td>

The Service Mapping app might use mapped application services. Mapped application services appear as group CIs that you can expand to show members. Mapped application services \[cmdb\_ci\_service\_discovered\] are descendents of the Service Instance \[cmdb\_ci\_service\_auto\] class, such as service instances and dynamic CI groups.

 -   A badge shows the number of members in the group.
-   Select the badge to expand the group and show its member CIs. Select again to collapse.
-   In the expanded mode, move to any member CI to temporarily highlight all group members.

</td></tr><tr><td>

Show or hide the timeline

</td><td>

Select the Show/Hide timeline icon ![](../image/icon-um-toggle-timeline.png). For more information, see [Viewing related items on the Unified Map timeline](../concept/unified-map-timeline-working-on.md).

</td></tr><tr><td>

View non-operational CIs

</td><td>

-   Non-operational CIs do not appear in search results or on the map.
-   The **Open Map** button on a CI form isn't available for non-operational CIs.
-   Only CIs for which the **Life Cycle Stage** attribute is **Operational** or empty appear on maps.

 An administrator can change the default behavior to show non-operational CIs or CIs of any combination of **Life Cycle Stage** values. For more information, see [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md).

</td></tr></tbody>
</table>## Controlling map appearance

<table id="table_jt4_jxf_sbc"><thead><tr><th>

Change

</th><th>

Tool and actions

</th></tr></thead><tbody><tr><td>

Zoom in or out

</td><td>

Use any of the following methods:

-   Select + or - in the toolbox.
-   Scroll up or down in the map pane.
-   Specify a zoom value in the mini-map navigator.

</td></tr><tr><td>

Align the map to the home node

</td><td>

In the toolbox, select the Align to home node icon ![](../image/icon-um-home-node.png).

</td></tr><tr><td>

Fit all CIs on the map

</td><td>

Select the Fit to map icon ![](../image/icon-um-fit-to-map.png).

 Result: Center the map on the canvas and set the zoom level to the maximum level that enables the entire map to fit on the canvas. By default, up to 250 nodes can appear on a map. CIs in a collapsed group CI are counted.

 **Note:** Admins set the maximum node count using the **unifiedmap.map\_search.max\_nodes** property in the workspace-specific \[sn\_cmdb\_ws\_config\_property\] table. Higher values can decrease performance.

</td></tr><tr><td>

Move a CI to another location

</td><td>

Drag a CI to a different place on the map. Map elements that are connected to that CI might be moved to accommodate the new placement.

</td></tr><tr><td>

Move the entire map on the canvas and set the zoom level

</td><td>

Use either of the following methods:

-   Drag the rectangle in the mini-map navigator.
-   Select an empty area on the map and drag.

</td></tr><tr><td>

Show CI key details on the map

</td><td>

Move to a CI to show its full name and class \(or zoom into the map until those details appear\), its related items details, and the direction of the CI relationships. If there are multiple related items associated with a CI, then the CI badge contains the string 'Multiple' and a badge showing the count of related items appears on the timeline. You can move to the badge on the timeline to show all related items.

</td></tr><tr><td>

Switch the layout of the map

</td><td>

-   Vertical layout: Displays nodes in a vertical tree pattern: upstream relationships top and downstream bottom. This is the default layout for displaying mapped application services and service instances. In the toolbox, select the Vertical layout icon ![](../image/icon-um-vertical-layout.png).
-   Force layout: Displays nodes in a clustered arrangement around the home node, regardless of upstream or downstream relationships. In the toolbox, select the Force layout icon ![](../image/icon-um-force-layout.png).

 **Note:** Connecting lines between nodes represent relationships and references, not data flow.

</td></tr></tbody>
</table>
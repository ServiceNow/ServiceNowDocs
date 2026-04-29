---
title: Dependency Views map menus and controls
description: Dependency Views maps contain the following menus and controls.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Dependency Views map menus and controls

Dependency Views maps contain the following menus and controls.

![Use the various menus and controls to filter, display or hide, and place nodes on the map.](../image/DependencyViewsMapMenusControls.png "Dependency Views map")

## Map options

The following options are available across the top of the map.

<table id="table_t5r_jcx_dr"><tbody><tr><td>

![Dependency Views map context menu.](../image/MenuIcon.png)

</td><td>

Menu to save, load and export views of the map.

</td></tr><tr><td>

&lt;Root CI&gt;

</td><td>

Next to the menu icon is the name of the current root node \(CI\) of the map.

</td></tr><tr><td>

![Search field on a Dependency Views map.](../image/SearchButton.png)

</td><td>

Enter the name of a CI, application service, or business service to load into the map. Alternatively, you can start typing to have the auto-complete feature present a list of CIs and services that match your partial value.

</td></tr><tr><td>

Vertical

</td><td>

Display the map in vertical view.

</td></tr><tr><td>

Horizontal

</td><td>

Display the map in horizontal view.

</td></tr><tr><td>

Radial

</td><td>

Display the map in radial view.

</td></tr><tr><td>

Force

</td><td>

Centers the elements around the parent CI, regardless of upstream or downstream relationships.

</td></tr><tr><td>

Group

</td><td>

Groups the elements according to their CI type.

</td></tr><tr><td>

Details

</td><td>

Displays related lists such as Problems, Changes and Related Services that are associated with the selected CI.-   Click a service to highlight the CIs that are associated with that service.
-   Click **Related Services**, then double-click a service to display the map in the Event Management dashboard.

 If the Event Management plugin is active, then events and alerts are also displayed.

</td></tr><tr><td>

Settings

</td><td>

Set filters for the map.

</td></tr><tr><td>

![Navigation Tools.](../image/NavigationTool.png)

</td><td>

Use the navigation tools to increase or decrease the view of the map, rearrange the icons on the map, and move the map on the page. -   Use the plus sign \(+\) to increase magnification of the map.
-   Use the minus sign \(-\) to decrease magnification of the map.
-   Click the center dot to center the map on the page.
-   Use the direction arrows to move the page in that direction.
-   Use the selection tool under the navigation tool to toggle between moving the entire map or moving one CI on the map.

</td></tr></tbody>
</table>## Map menu

The following options are available if you right-click the map background.

<table id="table_avh_hcx_dr"><tbody><tr><td>

Run Layout

</td><td>

Redraws the map with the current layout option.

</td></tr><tr><td>

Fit To Screen

</td><td>

Resizes the map to fit all the nodes in the map window.

</td></tr><tr><td>

Reset Filters

</td><td>

Performs the same action as the **Filters** &gt; **Reset** option.

</td></tr></tbody>
</table>## Node menu

The following options are available if you right-click a node.

<table id="table_NodeMenu"><tbody><tr><td>

View Form

</td><td>

Displays the CMDB record of the selected CI in a new tab of the browser.

</td></tr><tr><td>

View Map

</td><td>

Reloads the map using the selected CI as the new root node, with the currently defined layout setting. This option does not display on the root node.

</td></tr><tr><td>

View Related Tasks

</td><td>

Displays all tasks or outages associated with the selected CI, including incidents, problems, change requests, and follow-on tasks. This option is always available, even if there are no tasks associated with the CI. This option does not appear on collapsed nodes.

</td></tr><tr><td>

View Affected CIs

</td><td>

Shows a list of all tasks that have the CI listed as an Affected CI. This option is only visible when you access the map from the map icon in a task record's Configuration item field.

</td></tr><tr><td>

View Related Outages

</td><td>

Displays all outages involving the selected CI. This option only appears when there is an outage associated with the CI. This option does not appear on collapsed nodes.

</td></tr><tr><td>

Add Relationship

</td><td>

This option displays a dotted green line that you can drag to another CI to create a relationship link. A popup dialog allows you to define the relationship type.

</td></tr><tr><td>

Expand

</td><td>

Displays all CIs and components within a clustered node, or virtual groups \(virtual nodes that appear when **glide.bsm.too\_many\_children** is reached\). This option appears only if the node is a cluster node or a virtual group node. If **Load More** was previously used, then **Expand** reverts the results of the **Load More** operation.

 The number of additional icons to display is bound by the value of the **glide.bsm.max\_nodes** property.

</td></tr><tr><td>

Collapse

</td><td>

Collapses all CIs and components within a cluster node back to a single node. Also, collapses a virtual group that has been expanded. This option only appears if the node has been expanded using the **Expand** menu item.If **Load More** was previously used, then **Expand** reverts the results of the **Load More** operation.

</td></tr><tr><td>

Run Layout From Here

</td><td>

This option re-runs the chosen layout using the current node. Use this option to get a new or clearer view on the same map.

</td></tr><tr><td>

Load More

</td><td>

Starting at the selected icon, loads the next level of the map, past the setting of **Max Levels**. Virtual grouping is not applied at the newly loaded level even if the criteria for virtual grouping is met.

 The number of additional icons to display is bound by the value of the **glide.bsm.max\_nodes** property.

</td></tr></tbody>
</table>## Relationship menu

The following options are available if you right-click a relationship link.

<table id="table_ap2_krw_dr"><tbody><tr><td>

View Relationship Form

</td><td>

Opens the **CI Relationship** form. You can modify the **Parent**, **Type**, and **Child** of the relationship from this form.

</td></tr><tr><td>

Modify Relationship

</td><td>

Searches for and selects a new relationship for this link.

</td></tr><tr><td>

Delete Relationship

</td><td>

Deletes a relationship. The relationship is deleted after prompting for confirmation.

</td></tr></tbody>
</table>
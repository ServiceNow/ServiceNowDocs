---
title: Perform actions on nodes in a Dependency Views map
description: You can view various related items for the nodes in a Dependency Views map.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Perform actions on nodes in a Dependency Views map

You can view various related items for the nodes in a Dependency Views map.

## Before you begin

Role required: None

## About this task

If the node is a collapsed node or represents a cluster, the incidents, problems and change requests are for all the collapsed nodes.

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **View Map**.

2.  Click the Node menu icon ![Node menu](../image/DependencyViewDropMenu.png) next to a node or right-click a node on the map to access the following menu items:

<table id="table_NodeMenu"><tbody><tr><td>

View Form

</td><td>

Displays the CMDB record of the selected CI in a new tab of the browser.

</td></tr><tr><td>

View Map

</td><td>

Reloads the view using the selected CI as the new root node, with the currently defined layout setting. This option does not display on the root node.

</td></tr><tr><td>

View Related Tasks

</td><td>

Displays all tasks or outages associated with the selected CI, including incidents, problems, change requests, and follow-on tasks. This option is always available, even if there are no tasks associated with the CI. This option does not appear on collapsed nodes.

</td></tr><tr><td>

View Affected CIs

</td><td>

Shows a list of all tasks that have the CI listed as an Affected CI. This option is only visible when you access the view from the view icon in a task record's Configuration item field.

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

Displays all CIs and components within a cluster node or a collapsed node. This option only appears if the node is a collapsed or cluster node.The number of additional icons to display is bound by the value of the **glide.bsm.max\_nodes** property.

</td></tr><tr><td>

Collapse

</td><td>

Collapses all CIs and components within a cluster node or a collapsed node back to a single node. This option only appears if the node has been expanded using the Expand menu item.

</td></tr><tr><td>

Run Layout From Here

</td><td>

This option re-runs the chosen layout using the current node. Use this option to get a new or clearer view on the same map.

</td></tr><tr><td>

Load More

</td><td>

Starting at the selected icon, loads the next level of the map, past the setting of **Max Levels**. The number of additional icons to display is bound by the value of the **glide.bsm.max\_nodes** property.

</td></tr></tbody>
</table>
**Parent Topic:**[Use Dependency Views](../topic/p_UseNGBSM.md)

**Related topics**  


[View a Dependency Views map](t_AccessNGBSM.md)

[Save or load a Dependency Views map](t_SaveLoadMapView.md)

[Delete a saved Dependency Views map view](t_DeleteSavedMapView.md)

[Change the layout of Dependency Views map](t_ChangeLayoutNGBSMMap.md)

[Filter the view of a Dependency Views map](t_FilterViewNGBSMMap.md)

[View metrics for CIs in a Dependency Views map](view-ci-metrics.md)

[Export a Dependency Views map](t_ExportAnNGBSMMap.md)

[View collapsed nodes in a Dependency Views map](t_ViewCollapsedNodesInNGBSM.md)


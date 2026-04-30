---
title: Working with Actions on the Investigation Canvas
description: This section describes the various actions that you can perform on the investigation canvas.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Working with Actions on the Investigation Canvas

This section describes the various actions that you can perform on the investigation canvas.

Investigation canvas includes:

1.  Form actions
2.  Graph actions
3.  Node actions
4.  Edge actions
5.  Toolbar actions

![TISC Investigation canvas view.](../image/tisc-investigation-canvas-view.png "Investigation Canvas")

|Action|Operation|
|------|---------|
|Link Case|Allows you to link case on the investigation canvas.|
|Unlink Case|Allows you to unlink the case on the investigation canvas.|
|Save|Option to save the case record.|
|Duplicate|Option to duplicate the nodes on the investigation canvas.|
|Delete|Option to delete the canvas.|

<table id="table_d1v_hlv_gdc"><thead><tr><th>

Action

</th><th>

Operation

</th></tr></thead><tbody><tr><td>

Find on map

</td><td>

Allows you to search through different nodes and edges.

</td></tr><tr><td>

Canvas Filter

</td><td>

The **Filter** functionality helps you refine your view on the investigation canvas.

For example, if you filter out a record type such as Campaign, it is temporarily removed from the canvas display.

By applying filters, you can control which types of entities or records are shown on the map, enabling a cleaner and more focused investigation experience.**Note:** Use filters to highlight only the most relevant nodes such as observables or threat actors while temporarily hiding less critical information on the canvas.

</td></tr><tr><td>

Save Canvas

</td><td>

Allows you to save the investigation canvas.

</td></tr><tr><td>

Add Data to Library

</td><td>

This option allows you to establish a new relationship between two different nodes on the investigation canvas.All the changes made on the canvas including the new nodes, new links between nodes, and any edited or modified edge labels will be saved to the library.

All nodes currently present on the canvas will be added as artifacts to the linked case.

A confirmation message will be displayed once the data is successfully saved to the library.

</td></tr><tr><td>

Add From Library

</td><td>

This action will add the threat intelligence library data and also establish the relationship between the new node imported from the threat intelligence library and the existing nodes on the investigation canvas.

</td></tr><tr><td>

Add From Case Artifacts

</td><td>

Allows you to add data from corresponding case artifacts that is linked to the canvas.

</td></tr></tbody>
</table><table id="table_yd4_wrv_gdc"><thead><tr><th>

Action

</th><th>

Operation

</th></tr></thead><tbody><tr><td>

Mark as Home Node

</td><td>

This option allows you to mark a specific node as the home node on the Investigation Canvas.When pivoting during analysis, the application automatically highlights and centers the home node, bringing it into focus at the center of the canvas.

The focused node is visually emphasized through:

-   A distinct border
-   Highlighting
-   A subtle circular motion animation

This makes it easier to identify and explore the canvas data related to the primary focus of your investigation.

</td></tr><tr><td>

Add Relationship

</td><td>

This option allows you to add custom relationships between nodes on the Investigation Canvas. You can define relationship types such as:-   One-to-many
-   Many-to-one
-   Many-to-many

This helps represent complex associations between entities.

</td></tr><tr><td>

Show Details

</td><td>

This option allows you to view detailed information about the selected node on the Investigation Canvas, including its attributes and any associated observables or relationships.

</td></tr><tr><td>

Open Record

</td><td>

This option allows you to open the selected record in a new browser tab for easier reference and multitasking.

</td></tr><tr><td>

Remove from Canvas

</td><td>

This option allows you to remove the selected node from the investigation canvas, effectively deleting it from the current view.

</td></tr><tr><td>

Fetch Related Records

</td><td>

This option allows you to fetch related records for a specific node and add them directly to the investigation canvas using the **Select Entity Types** dialogue box.Select **Add All** option to automatically includes all the object related record types into the given selection box.

For example, if there are 5 to 10 different types of related records, you will have to manually select each object type. The **Add All** feature streamlines this process by populating all the relevant records at once, improving the user experience. After adding records, you can remove them or select the **Expand** option to view the related nodes.

However to enhance the usability, you can now select **Expand All** to instantly expand all the related records linked to a node, instead of manually adding or expanding the records.

</td></tr></tbody>
</table>|Action|Operation|
|------|---------|
|Edit|This option allows you to edit and modify the label of an edge on the Investigation Canvas, enabling clearer representation of relationships between nodes.|
|Remove|This option allows you to remove an edge from the Investigation Canvas, effectively deleting the visual connection between two nodes.|

<table id="table_btj_zkv_gdc"><thead><tr><th>

Action

</th><th>

Operation

</th></tr></thead><tbody><tr><td>

Zoom in

</td><td>

Option to zoom in the investigation canvas to easily focus on specific areas of the canvas.

</td></tr><tr><td>

Zoom out

</td><td>

Option to zoom out the investigation canvas to easily focus on specific areas of the canvas.

</td></tr><tr><td>

Fit to screen

</td><td>

Option to fit the investigation canvas to the screen size.

</td></tr><tr><td>

Export map

</td><td>

Option to export the investigation canvas as a PDF for better viewing.

</td></tr><tr><td>

Refresh

</td><td>

The **Refresh** option allows you refresh and reload the data from the library onto the Investigation Canvas.**Note:** Any unsaved changes on the canvas will be lost if you refresh without saving. It is recommended to save your canvas before refreshing to avoid data loss.

</td></tr><tr><td>

Clear Canvas

</td><td>

Allows you to clear the canvas.This selection will temporarily remove the nodes from the investigation canvas.

A confirmation message is displayed, prompting you to confirm whether you want to clear the canvas. Acknowledge the message to proceed.

**Note:** After making changes on the investigation canvas, you must **Save** the canvas. If the changes are not saved and if you refresh the canvas then it will revert to its previous state, and any unsaved nodes or modifications will be lost.

</td></tr><tr><td>

Legend

</td><td>

This option provides you a visual representation of the nodes and entities currently displayed on the Investigation Canvas. The legend includes two key views:-   **Node and Link Representation**: Displays how different node types appear on the canvas and how they are connected via edges. This helps you quickly understand the structure and relationship between various elements in the investigation.
-   **Entities Representation**: Shows the types of entities currently present on the canvas \(Observables, Indicators, and objects\).

The following illustrates the legends for node, link, and entity representations:

</td></tr></tbody>
</table>![node and link representation](../image/tisc-nodes-legend.png "Node and Link representation")

![Entities representation](../image/tisc-entities-legend.png "Entities representation")

## Grouping or Ungrouping records from Investigation Canvas

The group feature allows you to group nodes for easier analysis. A grouping button has been added next to nodes that can be grouped. By default, this button displays a minus \(−\) icon on the canvas, indicating that the connected node can be collapsed or grouped.

Any outdegree node would be considered for a group.

**Note:** The group icon is introduced to reduce clutter on the canvas and simplify navigation during critical investigations. For nodes without additional edges \(connections\), the grouping button is not displayed since there are no related nodes available to group.

The following table explains the guidelines while grouping or ungrouping the nodes:

<table id="table_gd5_5r2_zfc"><thead><tr><th>

Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Grouping a Node

</td><td>

-   All child nodes with only one parent \(even across multiple levels\) will be hidden within the group.
-   Nodes with multiple parents remain visible, but connections from the group to them will be hidden.

</td></tr><tr><td>

Ungrouping a Node

</td><td>

-   Reveals all previously hidden nodes with one parent and their connections.
-   If nodes with multiple parents were already visible, their hidden connections will also be restored.

</td></tr><tr><td>

Importing Node/ Fetch Related records

</td><td>

Automatically expands a collapsed group if the new node connects to a hidden node within it.

</td></tr><tr><td>

Allowed Actions

</td><td>

Grouped nodes only support the **Show Details** action, which will show details of parent node. Other actions are disabled.

</td></tr><tr><td>

Filter

</td><td>

Filtering **non-grouped nodes** follows standard filtering behavior, while still respecting grouping rules.Filtering a **grouped node** hides the entire group and its child node.

</td></tr><tr><td>

Other Actions

</td><td>

Actions such as removing a node or modifying edges follow all grouping rules and behaviors.

</td></tr></tbody>
</table>**Parent Topic:**[Working with Investigation Canvas](tisc-investigation-canvases.md)


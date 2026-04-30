---
title: ServiceNow AI Platform configuration tree within a record screen
description: The ServiceNow AI Platform configuration tree shows all your records in a hierarchical display. Instantly locate and select any record component in the tree to display the record's field types in the configuration panel.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record screen, Mobile App Builder, Building tools, Building mobile apps, Mobile Platform]
---

# ServiceNow AI Platform configuration tree within a record screen

The ServiceNow AI Platform configuration tree shows all your records in a hierarchical display. Instantly locate and select any record component in the tree to display the record's field types in the configuration panel.

## ServiceNow AI Platform configuration tree layout

The ServiceNow AI Platform configuration tree shows your selected record as the top-level record in a hierarchical display. Underneath your selected record are all the child records belonging to the parent record. You can instantly access and select of any of the child records, at any level in the hierarchy. The content and the fields of any selected record displays in the configuration panel, where you view and edit these fields.

## Working with the ServiceNow AI Platform configuration tree

-   **Large configuration trees**

    For large configuration trees the Mobile App Builder condenses certain records. This capability ensures that the configuration tree is a more manageable size.

    These partially loaded records are recognizable because they don’t have any child records displayed beneath them. Open and edit these floored records and any records associated with it by choosing the record and then selecting the **Open record to edit** button. Once selected, the Mobile App Builder displays the chosen floored record as the root-level record. You can edit this record and all its child records. To return to the parent record, select the **Back to &lt;parent record name&gt;** button, located next to the record name in the toolbar.

-   **Display indicators**

    As you work on records, indicators display on the configuration tree. A red indicator \(![Red indicator in configuration tree](../image/mab-red-indicator.png)\) shows that there are required fields that must be populated, before saving your changes. An orange indicator \(![Orange indicator in configuration tree](../image/mab-orange-indicator.png)\) shows that records have been edited but not yet saved.

    **Note:** The red and orange indicators are displayed on the right side of the hierarchical tree. This means that for a hierarchical tree with many levels of child records, the indicators may not be immediately visible. Either use the horizontal and vertical scroll bars. Alternatively, use the resize panel controller, which exists between the ServiceNow AI Platform configuration tree panel and the configuration panel.

<table id="table_bjv_23y_ssb"><thead><tr><th>

ServiceNow AI Platform configuration tree with indicators

</th><th>

Resize panel controller

</th></tr></thead><tbody><tr><td>

![Configuration tree within the record screen.](../image/mab-config-tree.png)

</td><td>

![Panel controller for expanding and decreasing the size of configuration panel.](../image/mab-panel-controller.png)

</td></tr></tbody>
</table>

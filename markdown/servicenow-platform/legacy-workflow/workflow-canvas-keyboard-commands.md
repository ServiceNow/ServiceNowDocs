---
title: Workflow drawing canvas keyboard commands
description: Use keyboard commands to navigate and operate the Workflow Editor canvas.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow editor keyboard navigation, Workflow editor, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow drawing canvas keyboard commands

Use keyboard commands to navigate and operate the Workflow Editor canvas.

![Workflow Editor Drawing Canvas - Tab Sequences / Elements](../image/WorkflowCanvasAccesibilityArrows.png)

<table id="table_pwr_nbl_rbb"><thead><tr><th>

Task or Action

</th><th>

Keyboard Commands

</th></tr></thead><tbody><tr><td>

Select Workflow Actions menu command \(for example, **Validate Workflow** or **Publish Workflow**\)

</td><td>

1.  Press **Tab** until the context menu \(![](../image/WFEditorCanvasContextMenu.png)\) is highlighted.
2.  Press **Enter** to open the context menu.
3.  Use the down arrow key to move to the command, then press **Enter** to select it.

</td></tr><tr><td>

Set general workflow properties

</td><td>

1.  Press **Tab** until ![Information icon](../image/WorkflowPropertiesIcon.png) is highlighted.
2.  Press **Enter** to open [Workflow Properties](../../workflow-administration/reference/r_WorkflowProperties.md).

</td></tr><tr><td>

Navigate from activity box to activity box.

</td><td>

Simply press **Tab** or use the arrow keys \(right, left, up and down\) to navigate from activity to activity within the workflow. **Note:** Depending on the complexity and number of activity boxes in the workflow, the sequence of navigation is not always predictable. Depending on how you are navigating within the workflow, the navigation sequence is generally \(but not always\) row-by-row, and focus is usually placed on the nearest activity box.

</td></tr><tr><td>

Modify a selected activity.

</td><td>

1.  Navigate to the activity box, then press **Enter** to select it and place it in Edit mode. When you select an activity box, it appears as highlighted.
2.  Once in Edit mode, use **Tab** to move around within the activity box to change or access elements such as:

    -   Activity Properties \(![](../image/NodeActivityProperties.png)\)
    -   Title
    -   Node context menu
    -   Delete Node \(![](../image/DeleteNode.png)\)
    -   Condition Properties \(![](../image/ConditionProperties.png)\)
    -   Node conditional context menu \(![](../image/NodeContextMenu.png)\)
    -   Node conditional port options \(![](../image/NodeConditionalPortOptions.png)\)
**Note:** All elements in a selected activity are only accessible when working with a checked out workflow. When working with a published workflow, you can only access its activity properties and title,

3.  Press **Enter** to select an element, or press **Esc** to escape an element without making changes.

</td></tr><tr><td>

Add a condition to an activity.

</td><td>

1.  Within an activity box, select ![Condition Properties icon](../image/ConditionProperties.png) to access **Condition Properties**.
2.  In **Condition Properties**, specify the conditions for the activity.

</td></tr><tr><td>

Create a connection from a condition on one activity to the next activity that follows

</td><td>

1.  Within an activity box, select **Node conditional context menu** \(![](../image/NodeContextMenu.png)\).
2.  Select **Link to...** to create a connection to the next activity box that follows, or select **Delete** to delete an existing connection.

</td></tr><tr><td>

Add a core or custom activity

</td><td>

1.  Within an activity box, select **Node conditional port options** \(![](../image/NodeConditionalPortOptions.png)\).
2.  Select **Add Core Activity** to access Workflow Activity Definitions to add a new core activity, or select **Add Custom Activity** to add a custom activity to the workflow.

</td></tr><tr><td>

Move an activity box

</td><td>

1.  Press **Tab** to navigate to the activity box, enter press **Enter** to select it.
2.  Use the arrow keys to move the activity box. To move the activity box one pixel at a time, press **Shift** while using the arrow keys.

</td></tr><tr><td>

Validate a workflow

</td><td>

1.  Press **Tab** until ![Validate icon](../image/ValidateWorkflowIcon.png) is highlighted.
2.  Press **Enter** to validate the workflow.

 You can also select **Validate** from the Workflow Actions menu.

</td></tr><tr><td>

Run a workflow

</td><td>

1.  Press **Tab** until ![Run icon](../image/RunWorkflowIcon.png) is highlighted.
2.  Press **Enter** to run the workflow.

 **Note:** If the workflow is tied to a database table, this function is disabled. The workflow runs when the proper table conditions are activated \(for example, insertion of a new record into the table\).

</td></tr><tr><td>

Close workflow drawing canvas

</td><td>

1.  Press **Tab** until ![Close icon](../image/CloseWFEditorCanvas.png) \(on the right side of the tab that contains the name of the workflow\) appears.
2.  Press **Enter** to close the canvas.

</td></tr><tr><td>

Publish a workflow

</td><td>

1.  Press **Tab** until the context menu \(![](../image/WFEditorCanvasContextMenu.png)\) is highlighted.
2.  Press **Enter** to open the context menu.
3.  Use the down arrow key to move to the **Publish** command, then press **Enter** to select it.

</td></tr><tr><td>

Jump to Top

</td><td>

After tabbing through the entire workflow, ![The Jump to top button](../image/JumptoTop.png) appears at the bottom of the listing. Press **Enter** to jump to the top of the Workflow drawing canvas.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow editor keyboard navigation](workflow-keyboard-access.md)


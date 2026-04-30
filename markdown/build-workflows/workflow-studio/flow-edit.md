---
title: Edit a flow
description: Edit an existing flow.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Edit a flow

Edit an existing flow.

## Before you begin

Role required: flow\_designer or admin

## About this task

As of the Washington DC release, flows open in a read-only state to protect them from accidental changes. When a flow is in a read-only state, you can only review, test, deactivate, or request to edit it. You must request to edit a flow before you can make changes. While editing a flow, your changes are automatically saved each time you select **Done** to close the configuration options.

**Note:** Workflow Studio no longer displays a **Save** button while you edit a flow.

## Procedure

1.  Open the flow that you want to edit.

    If necessary, navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**, and select the flow you want to edit.

    Workflow Studio opens the flow in a read-only state, which only provides options to request to edit, review, test, or deactivate it.

2.  Select **Edit Flow**.

    Workflow Studio checks whether another person already has the flow open for edit. If the flow is already being edited, you see a message displaying the name of the user editing the flow. If the flow is available for editing, you open the flow in an editable state.

3.  Take the appropriate actions to edit the flow.

    While editing a flow, your changes are automatically saved each time you select **Done** to close the configuration options. Each time the flow is saved, the Save indicator icon is updated.

<table id="choicetable_opd_n4h_x1b"><tbody><tr><td id="d75252e116">

**Change the flow name, description, or roles**

</td><td>

In the main header, select **Properties,** enter the values you want into the appropriate fields, then select **Update**.**Note:** You can’t change the application scope of a flow after you’ve saved it.

</td></tr><tr><td id="d75252e134">

**To edit the trigger**

</td><td>

In your flow, select the trigger description, fill in the fields as desired, then select **Done**.**Note:** Modifying triggers can result in the deletion of referenced action configurations.

</td></tr><tr><td id="d75252e149">

**To edit an existing action**

</td><td>

In your flow, select the action description, fill in the fields as desired, then select **Done**.

</td></tr><tr><td id="d75252e161">

**To add a new action**

</td><td>

To add an action at the end of a flow, select the plus icon in the ACTION section. Proceed as you would for adding an action to a new flow.

 To insert an action into an existing flow, point to the vertical line between the action icons where you want to insert the action. When the plus icon appears, select it. Add the action just as you would add it to a new flow.

 **Important:** Workflow Studio displays an asterisks character beside any action, flow logic, or subflow that is missing any required field values. Open the action, flow logic, or subflow to add the required field values.

</td></tr><tr><td id="d75252e182">

**To undo the last edit**

</td><td>

Select **Undo last action** to revert your last change. ![UNdo last action icon.](../images/icon-undo.png)

 Workflow Studio stores your last 20 configuration changes. You can’t undo changes that create records. For example, converting actions into a subflow creates a subflow, and therefore can't be undone. You can select **Undo last action** multiple times to revert multiple changes.

**Important:** The undo option is only available during your current user session. Closing the flow tab or the Workflow Studio browser tab ends your current user session and clears out your undo history.

</td></tr><tr><td id="d75252e216">

**To redo the last undo**

</td><td>

Select **Redo last action** to reapply the last reverted change. ![Redo last action icon.](../images/icon-redo.png)

 Workflow Studio stores your last 20 configuration changes. You can select **Redo last action** multiple times to reapply multiple changes.

**Important:** The redo option is only available during your current user session. Closing the flow tab or the Workflow Studio browser tab ends your current user session and clears out your redo history.

</td></tr></tbody>
</table>4.  To save your changes, close the flow tab.

    Workflow Studio automatically saves changes as you add and edit items. It also saves when you test or activate a flow.


**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)


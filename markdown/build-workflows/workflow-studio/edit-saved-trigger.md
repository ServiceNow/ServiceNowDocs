---
title: Edit a saved trigger
description: Edit a saved trigger in Workflow Studio to update the trigger definitions or other options according to your business needs.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Edit a saved trigger

Edit a saved trigger in Workflow Studio to update the trigger definitions or other options according to your business needs.

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin

## About this task

You can edit a saved trigger to update any of the conditions in the trigger definition. Before you publish the changes, review the flows that are using the trigger. If necessary, you can detach the trigger from any of the flows so that the updated conditions don't affect the flow.

You can't modify the trigger type and the table.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Triggers**.

3.  Select the trigger that you want to edit.

    Workflow Studio opens the trigger definition in read-only mode.

4.  Select **Edit trigger**.

5.  Update any of the trigger conditions or the advanced options.

    **Note:** If a user has modified the advanced options while using the trigger, any modifications that you make to these options doesn't affect the user's modified settings. To view the field descriptions for the trigger forms, see [Create a saved trigger](create-saved-trigger.md).

6.  Select **Publish**.

7.  From the list of flows that are using the trigger, select each flow and evaluate if the updated trigger definitions are valid for the flow.

8.  If the updated trigger definitions aren't valid for a flow, detach the trigger from the flow.

    For instructions on how to detach a trigger, see [Detach a saved trigger from a flow](detach-saved-trigger.md).

9.  Update the trigger properties, such as the trigger name, by selecting the More Actions menu icon and then selecting **Properties**.

    ![Menu option to update the trigger properties.](../images/more-actions.png)

10. On the Trigger properties pop-up window, update the properties as needed and select **Update**.

11. Make the updated trigger available by selecting **Publish**.


**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)


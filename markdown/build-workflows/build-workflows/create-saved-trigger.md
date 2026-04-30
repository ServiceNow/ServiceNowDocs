---
title: Create a saved record trigger
description: Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Create a saved record trigger

Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin

## About this task

Create a reusable trigger definition that responds to a record based event. When a record is created or updated in a specific table, the trigger is activated and it starts the flows where the trigger is used.

For information about creating a scheduled trigger or a trigger that responds to external events, see:

-   [Create a saved scheduled trigger](create-scheduled-trigger.md)
-   [Create a saved external trigger](create-saved-external-trigger.md)

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Trigger**.

3.  Fill in the details for your trigger.

<table id="table_l5n_ytp_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger name

</td><td>

Unique name to identify the trigger.

</td></tr><tr><td>

Trigger type

</td><td>

Type of trigger to start your flow.Under **Record**, select any of the following:-   Created
-   Updated
-   Created or updated
For more information about trigger types, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Application

</td><td>

Application to create the trigger. The default is Global.The application scope determines which data your trigger can access and what data it can share.

</td></tr></tbody>
</table>4.  Select **Show additional properties**.

5.  Fill in the additional properties.

    |Field|Description|
    |-----|-----------|
    |Accessible from|Choice between whether the trigger data should be accessible only from the specified application or all application scopes.|
    |Category|Category where your trigger is displayed.|
    |Trigger annotation|Annotation for your trigger that the user can see before they select it.|

6.  Select **Build trigger**.

7.  Fill in the trigger definition.

<table id="table_wmd_rw5_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table for the flow.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that, when met, activate the trigger and start the flow.You can select if you want the users to view the conditions or add more conditions to the trigger when they use the trigger in a flow.

</td></tr><tr><td>

Advanced options

</td><td>

Additional options to choose where and when to run the flow.For more information about the advanced options, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

You can select if you want users to view and modify these options when they use the trigger in a flow.

If a user modifies the advanced options, any future modifications that you make to these options in the trigger don't affect the user modified settings.

</td></tr></tbody>
</table>    **Tip:** Your changes are saved automatically in Workflow Studio. Use the undo and redo buttons as you need.

8.  Make the trigger available by selecting **Publish**.


**Parent Topic:**[Building triggers](../concept/building-triggers.md)

**Related topics**  


[Saved flow triggers](../concept/saved-flow-triggers.md)


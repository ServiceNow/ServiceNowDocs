---
title: Define a flow logic
description: Set the triggers and actions to define a remote table flow logic.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create flow definition for remote table, Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Define a flow logic

Set the triggers and actions to define a remote table flow logic.

## Before you begin

Role required: admin

## Procedure

1.  Select the **Flow** field on the flow definitions form.

    The Flow properties dialog box shows up.

2.  Set the **Trigger** and link the required remote table.

    For the set trigger, the flow pills get created in the right nav.

3.  Set the action items in the Create Remote Table Record section.

    1.  Set the Action as Create Remote Table Record.

    2.  Drag and drop the Query ID pill from the right nav.

        **Note:** The Query ID is the id of the query that triggered the execution of the flow. It is a mandatory step to pass the Query ID to the Create Remote Table Record action to associate the Trigger to the Action.

    3.  Select **Done** to save the action.

4.  Add conditions to the flow logic if you want to create a different flow path.

    1.  Fill up the Condition Label field.

    2.  Set the condition by dragging and dropping the Query Parameter pill from the right nav.

    3.  Select the add function icon next to the Query Parameter pill to add specifics.

        The Search Transform Functions dialog box shows up.

    4.  Go to **Utilities** and select the next function depending on the Query Parameter type.

        For example, if the condition is set to search for a name, you can go to **Utilities** &gt; **Get Item from Name/Values**. Fill up the **Key** details and select **Apply**. The **Key** field needs to specify the parameter you are looking for.

        **Note:** Ensure that the **Key** is the same as the Column name and not the Label name.

5.  Add a log to the flow logic.

    1.  Select Log as the **Action** and select a **Level**.

    2.  Set the Message field by dragging and dropping the Query Parameter pill from the right nav.

    3.  Select **Done** to create logs for the set condition.


**Parent Topic:**[Create a flow definition for a remote table](create-remote-table-flow.md)


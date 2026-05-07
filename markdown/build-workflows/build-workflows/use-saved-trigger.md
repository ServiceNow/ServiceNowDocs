---
title: Use a saved trigger
description: Instead of creating a trigger, use a saved trigger in your flow. Using a saved trigger enables you to reuse standardized trigger logic across flows, reducing the effort, improving consistency, and simplifying ongoing maintenance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Use a saved trigger

Instead of creating a trigger, use a saved trigger in your flow. Using a saved trigger enables you to reuse standardized trigger logic across flows, reducing the effort, improving consistency, and simplifying ongoing maintenance.

## Before you begin

Role required: flow-designer or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Under **Flows**, select the flow you want to edit, or create a flow.

    To create a flow, specify the flow properties and select **Build flow**.

3.  Under **TRIGGER**, select **Add a trigger**.

    If the flow already contains a trigger that you want to replace with a saved trigger, hover over the existing trigger and select the delete icon.

4.  From the **Trigger** list, under **INSTALLED APPLICATIONS**, select the application under which the trigger was created.

    For example, Global. Workflow Studio displays a list of triggers present in the selected application. Select the info icon to see more details about the trigger.

    ![Select a saved trigger under the installed applications.](../images/saved-trigger-select.png)

5.  Select the trigger.

    The selected trigger is added to the flow.

6.  Depending on the trigger configurations, you can view the trigger properties and add additional conditions for the trigger.

    **Note:** Adding additional conditions affects only the flow, it doesn't alter the saved trigger.

    ![View trigger properties and optionally add more conditions for the flow.](../images/saved-trigger-properties.png)

7.  Select **Done**.


## Result

The selected saved trigger is added to the flow and will start the flow depending on how the trigger is configured.

**Parent Topic:**[Building triggers](../concept/building-triggers.md)


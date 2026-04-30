---
title: Override a UI action for an extended table
description: You can override or remove a UI action for a table that is extended from another table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [UI actions, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Override a UI action for an extended table

You can override or remove a UI action for a table that is extended from another table.

## Before you begin

This is not applicable to domain separated instances.

## About this task

When a UI action is defined for the Task table, it applies to all tasks, including incidents, changes, problems, and any other tables that extend the Task table. Similarly, a global UI action applies to every table. However, you can override a UI action for a specific table. This example demonstrates how to override or remove a UI action on the Task \[task\] table for only the Incident \[incident\] table.

## Procedure

1.  Complete the following steps to override a UI action on the Task table for just the Incident table.

    1.  Create a UI action on the Incident table with the same **Action name**.

        If the **Action name** is not defined, update both the new UI action and the UI action to be overridden with the same **Action name**.

    2.  Enter a script that is specific to the Incident table.

2.  Complete the following steps to remove a UI action on the Task table for the Incident table.

    1.  Navigate to the UI action definition for the Task table.

    2.  Add the condition **current.getRecordClassName\(\) !='incident'**.


**Parent Topic:**[UI actions](../concept/c_UIActions.md)


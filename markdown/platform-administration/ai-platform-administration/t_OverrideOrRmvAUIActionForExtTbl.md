---
title: Override a UI action for an extended table
description: You can override or remove a UI action for a table that is extended from another table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/t\_OverrideOrRmvAUIActionForExtTbl.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [UI actions, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Override a UI action for an extended table

You can override or remove a UI action for a table that is extended from another table.

## Before you begin

Role required: ui\_action\_admin or admin

**Note:** This is not applicable to domain separated instances.

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


**Parent Topic:**[Defining UI actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_UIActions.md)


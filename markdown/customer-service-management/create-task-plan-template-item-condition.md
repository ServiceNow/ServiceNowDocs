---
title: Create a template item condition
description: Create conditions for a template item after the template item has been created. These conditions determine when a template item is created when the task plan template is applied.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a template item condition

Create conditions for a template item after the template item has been created. These conditions determine when a template item is created when the task plan template is applied.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator role

## About this task

You can create conditions for template items after the items have been created and the Template Item Conditions tab appears on the Template Item record.

When you create a condition, you select a table on which the conditions are applied. The following tables are available for selection:

-   The same table as the **Target record** in the task plan template.
-   The same table as the current template item.

You can also delete a condition by selecting the condition in the Template Item Conditions list and then selecting **Delete** to remove the item from the list..

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Draft Task Plan Templates**.

2.  Select a task plan template record number to display the record.

3.  Select the Template items tab.

4.  Select a template item record.

5.  Select the Conditions tab.

6.  Select **New**.

    The template item condition record opens in a new tab. The **Template item** field displays the number of the parent template item.

    For more information about these fields, see [Template item condition form](../reference/task-plan-template-item-condition-form.md).

7.  Select a table from the **Condition table** field.

    This is the table on which the condition is applied.

8.  Select **Add Filter Condition** to choose a condition from the drop down.

    1.  Use the operators in the field to set the filtering that you want.

    2.  Select **x** to remove a condition.

9.  To add additional conditions to filter by, select **Add OR Clause**.

    1.  Use the operators in the field to set the filtering that you want.

    2.  Select **x** to remove a condition.

10. Select **Submit**.

    The system creates the template item condition record and adds it to the Template Item Conditions tab.



---
title: Create a template item condition
description: Create conditions for a template item after the template item has been created. These conditions determine when a template item is created when the task plan template is applied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-task-plan-template-item-condition.html
release: brazil
topic_type: task
last_updated: "2026-09-04"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a template item condition

Create conditions for a template item after the template item has been created. These conditions determine when a template item is created when the task plan template is applied.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator

## About this task

You can create conditions for template items after the items have been created and the Template Item Conditions tab appears on the Template Item record.

By default **Advanced** is unchecked, you select one of the following:

-   The same table as the **Target record** in the task plan template.
-   The parent template item's table.

When **Advanced** is selected, this field instead lists tables that share the reference selected in the **Base table mapping field**.

You can also delete a condition by selecting the condition in the Template Item Conditions list and then selecting **Delete** to remove the item from the list..

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Draft Task Plan Templates**.

2.  Select a task plan template record number to display the record.

3.  Select the Template items tab.

4.  Select a template item record.

5.  Select the Conditions tab.

6.  Select **New**.

    The template item condition record opens in a new tab. The **Template item** field displays the number of the parent template item.

    For more information about these fields, see [Template item condition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-template-item-condition-form.md).

7.  Select the **Advanced** check box to instead configure the condition on a table that shares a reference with the target table or parent template item table, rather than on that table directly.

    When **Advanced** is selected, the **Condition table** field lists tables that share the reference selected in **Base table mapping field**. Three additional fields appear and are mandatory: **Base table**, **Base table mapping field**, and **Condition table mapping field**.

    A **Change Advanced settings?** confirmation dialog appears. Select **Confirm** to proceed, or **Cancel** to keep the Advanced setting unchanged.

    Skip this step and the next two steps to configure a simple condition, as described in the following steps.

8.  If you selected **Advanced**, select the parent template item's table or the task plan template's target record table from the **Base table** field.

9.  If you selected **Advanced**, select a reference field on the **Base table** in the **Base table mapping field** field. The **Condition table** field then lists tables that share this same reference.

10. Select a table from the **Condition table** field.

    This is the table on which the condition is applied.

    If you selected **Advanced**, this field lists tables related to your **Base table mapping field** selection instead of the target table or parent template item table.

11. If you selected **Advanced**, select the field on the **Condition table** that matches the reference selected in **Base table mapping field**, in the **Condition table mapping field** field.

12. Select **Add Filter Condition** to choose a condition from the drop down.

    1.  Use the operators in the field to set the filtering that you want.

    2.  Select **x** to remove a condition.

13. To add additional conditions to filter by, select **Add OR Clause**.

    1.  Use the operators in the field to set the filtering that you want.

    2.  Select **x** to remove a condition.

14. Select **Submit**.

    The system creates the template item condition record and adds it to the Template Item Conditions tab.



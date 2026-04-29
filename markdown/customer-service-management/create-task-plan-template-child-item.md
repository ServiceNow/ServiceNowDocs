---
title: Create a child template item
description: Create one or more child template items, such as a task or record, for an existing template item to create a task hierarchy.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a child template item

Create one or more child template items, such as a task or record, for an existing template item to create a task hierarchy.

## Before you begin

Role required: sn\_task\_plan.admin or sn\_task\_plan.creator role

## About this task

Template items can have child template items. By creating child template items, you can create a hierarchy of template items. For example, you can create a case as a template item and then create case tasks as child template items for that case.

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Draft Task Plan Templates**.

2.  Select a task plan template record number to display the record.

3.  Select the Template items tab.

4.  Select **New**.

    The template item form opens in a new tab. The **Number** field displays the number of the child template item. The Task plan template field displays the number of the parent task plan template.

5.  Use the **Search** icon to choose a parent template item.

6.  If applicable, choose a configuration in the **Template item configuration** field.

    The corresponding field values are pre-filled. You can modify the field values if needed.

7.  Provide a brief description of the template item in the **Short description** field.

8.  Select a table from the **Table** field in which the system creates the child template item record when the task plan template is applied.

    For example, if the child template item is a case task, the system should create that item in the Task table \[sn\_customerservice\_task\].

9.  Specify the fields and the field values that the system should use to create the template item record.

10. Add an attachment to the template item.

11. Select **Submit**.

    The system creates the child template item record and adds the record to the Child Template Items tab on the template item form.


## What to do next

After creating a child template item, you can [create one or more conditions for the template item](create-task-plan-template-item-condition.md).


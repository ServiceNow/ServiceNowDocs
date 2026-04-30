---
title: Create a task plan template
description: Create a task plan template that includes template items, such as tasks, that are automatically created when the task plan template is applied.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a task plan template

Create a task plan template that includes template items, such as tasks, that are automatically created when the task plan template is applied.

## Before you begin

Role required: sn\_task\_plan.admin​ or sn\_task\_plan.creator role

## About this task

Task plan templates include conditions that determine when the template applies.

**Note:** As part of creating a task plan template, you can select a target record. If you select a target record, the task plan template is applied when a case or task matching the task plan condition is created.

After creating a task plan template, you can create the template items, such as case tasks, work order tasks, and child cases. Template items can also include conditions that determine when a template item should be created as well as attachments.

You can also [clone a task plan template](clone-task-plan-template.md).

## Procedure

1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **All Task Plan Templates**.

2.  Select **New**.

    A Task Plan Template form opens in a new tab. The template is active and is in the Draft state.

3.  Fill in the fields on the Task Plan Template form.

    1.  If there are task plan template configurations created, select one from the **Task plan template configuration** field.

        The task plan template configuration prefills the **Short description** and **Target record** field. For more information about task plan template configurations, see [Create a task plan template configuration](task_plan_template_configurations.md).

    2.  Provide a **Name** and **Short description** for the task plan template.

    3.  The **Target record** identifies the table that the task plan template is applied to.

    For more information about these fields, see [Task Plan Template](../reference/task-plan-template-form.md) form.

4.  Select **Submit**.

    The system saves the task plan template record and adds the Template items tab to the form. Use the Template Items tab to define the tasks such as case tasks or work orders that you want to be generated when the task plan template is applied.


## What to do next

After creating a task plan template, you can [create template items](create-task-plan-template-item.md) for that template.


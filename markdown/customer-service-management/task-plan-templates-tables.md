---
title: Task Plan Templates tables
description: The Task Plan Templates application includes tables that store task plan template, template item, and template item condition records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Task Plan Templates tables

The Task Plan Templates application includes tables that store task plan template, template item, and template item condition records.

The Task Plan Templates application includes the following tables.

<table id="table_k3h_r5w_lfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Plan Template\[sn\_task\_plan\_template\]

</td><td>

Stores task plan template records. A task plan template defines the plan to create the associated template items, such as case tasks and child cases.

A task plan template is a collection of independent template items which can be applied manually or automatically to an existing entity such as a case.

</td></tr><tr><td>

Template Item\[sn\_task\_plan\_template\_item\]

</td><td>

Stores template item records.Template items are the tasks or the records that are created when you apply a task plan template.

A task plan template can have multiple template items and template items can have child template items. This structure enables you to define a hierarchy of parent and child records of any task type.

You can add attachments to a template item. The attachments are available on the tasks and records created from the template item when the task plan template is applied to a case.

</td></tr><tr><td>

Template Item Condition\[sn\_task\_plan\_template\_item\_condition\]

</td><td>

Stores template item condition records.You can add conditions to a template item that determines when a template item is applicable.

</td></tr></tbody>
</table>**Related topics**  


[Task Plan Template form](../reference/task-plan-template-form.md)

[Template item form](../reference/task-plan-template-item-form.md)

[Template item condition form](../reference/task-plan-template-item-condition-form.md)


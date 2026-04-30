---
title: Configure which types of tasks can be created from Visual Task Board checklist items
description: A system property controls which types of tasks you can create from a Visual Task Board checklist item.
locale: en-US
release: xanadu
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Visual Task Board checklists, Using Visual Task Boards, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Configure which types of tasks can be created from Visual Task Board checklist items

A system property controls which types of tasks you can create from a Visual Task Board checklist item.

## Before you begin

Role required: admin

## About this task

You might want to add custom tables or remove tables you do not use.

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Locate the **glide.ui.create\_task\_type\_option\_list** property.

3.  Edit the **Value** to add or remove tables.

    You can add any table that extends Task \[task\]. Use the table name, not the label. For example, you would enter `change_request`, not Change Request. Ensure the tables listed are separated by commas, with no spaces.

    The property value populates the task type selection list users choose from when they create a task from a checklist item. Note that users can only see task types for which they have the appropriate access roles.

    ![Task type selection list](../image/CreateTaskFromChecklistItem.png)


**Parent Topic:**[Visual Task Board checklists](../concept/c_VisualTaskBoardChecklists.md)


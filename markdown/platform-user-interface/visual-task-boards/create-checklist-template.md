---
title: Create a checklist template for Visual Task Board tasks
description: A template saves time by creating checklist items automatically. You can add, edit, or remove checklist items without impacting the template.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Visual Task Board checklists, Using Visual Task Boards, Visual Task Boards, Configure UIs and portals, Configure user experiences]
---

# Create a checklist template for Visual Task Board tasks

A template saves time by creating checklist items automatically. You can add, edit, or remove checklist items without impacting the template.

## Before you begin

[Activate Visual Task Boards](t_ActivateVisualTaskBoards.md).

Role required: none

## About this task

There are two ways that you can create a checklist template:

-   In the Visual Task Board interface,
-   or in the ServiceNow AI Platform.

## Procedure

1.  Adding a checklist template in Visual Task Board
2.  In Visual Task Board, open the card details for a task.

    **Note:** You cannot give a checklist template a name when you create a checklist template in the Visual Task Board interface. To give a checklist a name, you must configure the checklist template in the ServiceNow AI Platform.

3.  Click the checklist tab \(![Checklist tab](../image/IconChecklist.png)\).

4.  Add items to the checklist that you want to save as part of the template.

5.  Click the more icon \(![More icon](../image/IconMore.png)\).

    The more icon does not display unless you have added an item to the checklist, or if you have a pre-existing checklist template.

6.  Select **Save as Template**.

7.  In the dialog box, enter a descriptive template name to identify the checklist.

    When a user creates a checklist from a template, all templates are listed in alphabetical order and there is no way to filter which templates appear. To provide a better user experience, consider implementing a naming system for checklist templates. For example, include the name of the table or another identifier to clarify how the checklist should be used.

8.  Click **Save**.

9.  Adding a checklist in the ServiceNow AI Platform
10. Navigate to **All**, and search for `checklist_template.list`.

11. Select **New** to create a new checklist template.

12. Configure the fields for your new checklist template.

<table id="choicetable_dtf_dxh_j1c"><tbody><tr><td id="d54715e200">

**Group**

</td><td>

You can use this field to limit the group of users that are allowed to use this checklist template.

</td></tr><tr><td id="d54715e209">

**Template**

</td><td>

Your template in JSON. Example:

 `{"owner":"2816f79cc0a8916401c5a33be04be443","name":"Checklist of items","items":[{"name":"Call the vendor","order":0},{"name":"Follow up email to customer","order":1},{"name":"Slack the supervisor","order":2}]}`

 The attributes of a checklist template are:

-   **Owner**

The sys\_ID of the user who owns or creates the checklist template.

-   **Name**

The name of the checklist template.

-   **Items**

The checklist items.

-   **Name**

The name of a checklist item.

-   **Order**

The order in which a checklist item appears in the checklist.

</td></tr><tr><td id="d54715e277">

**Name**

</td><td>

The name of the checklist template.

</td></tr><tr><td id="d54715e286">

**User**

</td><td>

The role required to use the checklist template.

</td></tr></tbody>
</table>13. Select **Submit**.


## Result

Your checklist template is created.

## What to do next

Create a checklist from a checklist template by selecting the template from the more icon.

**Parent Topic:**[Visual Task Board checklists](../concept/c_VisualTaskBoardChecklists.md)


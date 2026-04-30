---
title: Create a checklist
description: You can create a unique checklist for each task record. You can quickly create a checklist from a previously created template.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Checklists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a checklist

You can create a unique checklist for each task record. You can quickly create a checklist from a previously created template.

## Before you begin

The Checklist formatter must be [added to the form](https://www.servicenow.com/docs/access?context=c_FormDesign&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) by a user with the personalize\_form role.

Role required: for the write role, read role, and delete role, the logged in user must be sys\_created\_by.

**Note:** If the Explicit roles plugin is installed, the sn\_internal role is required by the Customer Service Management and the Vendor Risk Management plugins \(and possibly others.\) The Explicit roles plugin automatically creates the sn\_internal role and assigns it to all users.

## About this task

A template saves time by creating checklist items automatically. You can add, edit, or remove checklist items without impacting the template. You can use any checklist template, even if it was created on a different table.

## Procedure

1.  Navigate to a record that does not already contain a checklist.

2.  Click the down arrow beside the **Checklist** formatter.

3.  Complete one of the following steps.

<table id="choicetable_zzd_cd3_xbb"><tbody><tr><td id="d91888e88">

**To create a new checklist**

</td><td>

Select **Create new**.

</td></tr><tr><td id="d91888e100">

**To create a checklist by using a template**

</td><td>

Under **Create from template**, select a template. The checklist items in the template appear. Use any of the following steps to manage items in the checklist.

</td></tr></tbody>
</table>4.  Click **Add Item**.

5.  Enter text for the checklist item.

6.  Press the Enter key to add the checklist item.

7.  Create as many additional checklist items as desired.

8.  Click the minus \(-\) icon to delete a checklist item.

9.  Click the drag icon \(![Drag icon](../image/IconDrag.png)\) and drag a checklist item to a different position in the list.

10. Save the checklist as a template for easy reuse.

    1.  Click the down arrow beside the **Checklist** formatter.

    2.  Select **Save as Template**.

        A dialog box appears.

    3.  Enter a descriptive template name to identify the checklist.

        When a user creates a checklist from a template, all templates are listed in alphabetical order and there is no way to filter which templates appear. To provide a better user experience, consider implementing a naming system for checklist templates. For example, include the name of the table or another identifier to clarify how the checklist should be used.

    4.  From the User Group list, select a group to limit the checklist template to.

        Only members of the selected group and the user who created the checklist can use the checklist as a template. Leaving this field blank prevents anyone but the template creator from using the checklist template.

    5.  Click **Save**.

11. Save the form.


**Parent Topic:**[Checklists](../concept/c_Checklists.md)

**Related topics**  


[Activate checklists](t_ActivateChecklists.md)

[Delete checklist or a template](t_DeleteAChecklist.md)


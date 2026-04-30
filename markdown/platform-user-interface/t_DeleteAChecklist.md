---
title: Delete checklist or a template
description: You can remove a checklist from a record, and delete checklist templates you no longer need.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Checklists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Delete checklist or a template

You can remove a checklist from a record, and delete checklist templates you no longer need.

## Before you begin

Role required: for the write role, read role, and delete role, the logged in user must be sys\_created\_by.

**Note:** If the Explicit roles plugin is installed, the sn\_internal role is required by the Customer Service Management and the Vendor Risk Management plugins \(and possibly others.\) The Explicit roles plugin automatically creates the sn\_internal role and assigns it to all users.

## About this task

Deleting a checklist template has no effect on checklists created from that template.

## Procedure

1.  To delete a checklist, navigate to the record that contains the checklist.

2.  Click the down arrow beside the **Checklist** formatter.

3.  Select **Remove Checklist**.

    A confirmation dialog box appears.

4.  Click **Delete**.

5.  Complete the following steps to delete a checklist template.

    1.  In the navigation filter, enter `checklist_template.list`.

    2.  Select the check box by the checklist template you want to delete.

    3.  In the actions choice list, select **Delete**, found at the bottom of the page.

    4.  In the confirmation dialog box, click **Delete**.


**Parent Topic:**[Checklists](../concept/c_Checklists.md)

**Related topics**  


[Activate checklists](t_ActivateChecklists.md)

[Create a checklist](t_CreateAChecklist.md)


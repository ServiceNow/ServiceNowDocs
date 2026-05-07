---
title: Edit multiple records in a list using an editing form
description: You can edit multiple records at the same time using an editing form. If you want to edit multiple fields or fields that don’t appear in the list view, use an editing form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Methods for list edits, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Edit multiple records in a list using an editing form

You can edit multiple records at the same time using an editing form. If you want to edit multiple fields or fields that don’t appear in the list view, use an editing form.

## Before you begin

Role required: list\_updater

Depending on your ACL settings, some of these options might not be available even with the right role. For example, if the list is task.list and users try to select multiple incident records from that task list, the form uses the task form and not the incident form so ACLs on task are enforced instead. Since users would not have access to tasks specifically, the form wouldn’t show any fields.

## Procedure

1.  Perform one of the following actions.

<table id="choicetable_f1q_l2n_pv"><tbody><tr><td id="d79191e60">

**Update selected records**

</td><td>

1.  Select the check box by each row that you want to edit.
2.  Select and hold \(or right-click\) any column header and select **Update Selected**.


</td></tr><tr><td id="d79191e81">

**Update all records in the list**

</td><td>

1.  Filter the list so it contains only the rows you want to edit.
2.  Select and hold \(or right-click\) any column header and select **Update All**.


</td></tr></tbody>
</table>2.  Enter appropriate values in any of the fields and select **Update** to save your changes in all selected records.


**Parent Topic:**[Methods for list edits](../reference/r_MethodsForListEdits.md)

**Related topics**  


[Use the list editor](t_UseTheListEditor.md)

[Edit multiple records in a list using the list editor](t_EditMultRecUsingListEditor.md)


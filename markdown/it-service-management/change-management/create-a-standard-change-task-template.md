---
title: Create a standard change task template
description: You can create a change task template to add to a standard change proposal. If the standard change proposal is approved, the related change tasks are created when the standard change request is created.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standard change catalog, Configure, Change Management, IT Service Management]
---

# Create a standard change task template

You can create a change task template to add to a standard change proposal. If the standard change proposal is approved, the related change tasks are created when the standard change request is created.

## Before you begin

Role required: itil, change\_manager, or sn\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Standard Change** &gt; **Open Proposals**.

    **Note:** You can add standard change tasks to a standard change proposal only when the proposal is in the **New** state. Once you submit a standard change task for approval, you cannot add additional tasks.

2.  Click the **Change Task Templates** tab, and then click **New**.

3.  On the form, fill in the fields.

<table id="table_mzj_4tq_nz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the change task.

</td></tr><tr><td>

Std change proposal

</td><td>

Name of the standard change proposal for which you want to create the change task template.

</td></tr><tr><td>

Order

</td><td>

Order in which change tasks are created in the change request.The **Order** field determines the order in which you add the change tasks to the change request when you select it from the standard change catalog.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the change task template.

</td></tr><tr><td>

Change Task values

</td><td>

Field values that are populated on the change task created as part of the standard change.

</td></tr></tbody>
</table>4.  Click **Submit**.

    **Note:** Standard change catalog templates are not supported on Service Portal.


-   **[Propose a standard change template](propose-standard-chg-template.md)**  
Propose a new standard change template when you identify a need while creating a change request.

**Parent Topic:**[Standard change catalog](../concept/c_StandardChangeCatalogPlugin.md)

**Related topics**  


[Configure standard change catalog properties](t_ConfigureTheStandardChangeCatalog.md)

[Attach files to a standard change template](attach-files-change-templates.md)

[Modify or retire a standard change template](manage-standard-change-template.md)


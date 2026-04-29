---
title: Task plan templates states and actions
description: A task plan template can be in one of the following states: Draft or Published. It can also be active or inactive. Each state includes an available set of user actions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Task plan templates states and actions

A task plan template can be in one of the following states: Draft or Published. It can also be active or inactive. Each state includes an available set of user actions.

## Draft state

A task plan template is in the Draft state when it is first created.

When a task plan template is active and in the Draft state, the following actions are available.

<table id="table_bd4_t45_nfc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit

</td><td>

Select a task plan template in the list and then select **Edit** to open the task plan template record and make changes.Editing a task plan template requires the sn\_task\_plan.creator role.

</td></tr><tr><td>

Clone

</td><td>

Select a task plan template in the list and then select **Clone** to create a copy of the template, the template items and attachments, and the template item conditions.Cloning a task plan template maintains the template item hierarchy along with the attachments and conditions. The cloned task plan template is created in the Draft state and is active.

Cloning a task plan template requires the sn\_task\_plan.creator role.

**Note:** You can clone one task plan template at a time. If you select more than one task plan template in the list, the **Clone** action is not available.

</td></tr><tr><td>

Delete

</td><td>

Select one or more task plan templates in the list and then select **Delete**. Only task plan templates in the Draft state can be deleted.Deleting a task plan template requires the sn\_task\_plan.delete role.

**Note:** The system displays a confirmation message when deleting a template. When the user confirms the action, the system deletes the task plan template.

</td></tr><tr><td>

Publish

</td><td>

Selecting **Publish** moves an active task plan template from the Draft state to Published. When a task plan template is in the Published state, the fields on the Task Plan Template form are read-only.Publishing a task plan requires the sn\_task\_plan\_template.writer role.

**Note:** The system displays a confirmation message when publishing a task plan template. When the user confirms the action, the system publishes the task plan template.

</td></tr></tbody>
</table>## Published state

A task plan template is in the Published state when it is ready to be applied and a user with the writer role has published it.

When a task plan template is active and is in the Published state, the following actions are available.

<table id="table_w4y_fp5_nfc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clone

</td><td>

Select the task plan template in the list and then select **Clone** to create a copy of the template, the template items and attachments, and the template item conditions.Cloning a task plan template maintains the template item hierarchy along with the attachments and conditions. The cloned task plan template is created in the Draft state and is active.

Cloning a task plan template requires the sn\_task\_plan.creator role.

**Note:** You can clone one task plan template at a time. If you select more than one task plan template in the list, the **Clone** action is not available.

</td></tr><tr><td>

Deactivate

</td><td>

Select the task plan template in the list and then select **Deactivate** to disable the **Active** field on the Task Plan Template form.Deactivating a task plan template requires the sn\_task\_plan\_template.writer role.

**Note:** The system displays a confirmation message before deactivating a task plan template. When the user confirms the action, the system disables the **Active** field on the task plan template.

</td></tr></tbody>
</table>
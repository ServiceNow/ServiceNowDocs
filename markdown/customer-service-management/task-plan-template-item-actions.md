---
title: Template item actions
description: Template items have an available set of actions, including row-level actions that enable users to create new template items and to edit, clone, and delete template items.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Template item actions

Template items have an available set of actions, including row-level actions that enable users to create new template items and to edit, clone, and delete template items.

The Task Plan Template form includes a Template Items tab that shows the included template items in a hierarchical view. This view shows the relationship between case tasks, child cases, child case tasks, and other records.

From the Template Items tab, users can select **New** to create new template items. This action is available when the task plan template is in the Draft state.

The following row-level actions are available for template items when the task plan template is in the Draft state.

<table id="table_ldr_brx_lfc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit

</td><td>

Select the pencil icon to edit a template item inline in a pop-up window. Make the desired changes and then select **Update**.

</td></tr><tr><td>

New Child

</td><td>

Select the additional items icon next to the template item and then select **New Child**. This creates a new child record with the selected template item as the parent item.

</td></tr><tr><td>

Clone

</td><td>

Select the additional items icon next to the template item and then select **Clone**. This clones the template item to create a new template item. This includes the hierarchy of the selected template item along with the conditions and attachments of the selected template item. The cloned template item is added to the Template Items tab on the Task Plan Template form.This action requires the sn\_task\_plan.creator role.

</td></tr><tr><td>

Delete

</td><td>

Select the additional items icon next to the template item and then select **Delete**. This deletes the selected template item.This action requires the sn\_task\_plan.delete role.

**Note:** The system displays a confirmation message before deleting the template item. When the user confirms the action, the system deletes the template item, its child items, the template item conditions, and attachments.

</td></tr></tbody>
</table>## Actions for template item conditions

<table id="table_x1n_sdq_sfc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Select a template item and then select the Conditions tab to display the Template Item Condition list.Select **New** to create a new template item condition. Fill in the fields on the Template Item Condition form and then select **Save**.

</td></tr><tr><td>

Delete

</td><td>

Select a template item and then select the Conditions tab to display the Template Item Condition list.Select one or more template item conditions and then select **Delete**.

</td></tr></tbody>
</table>
---
title: Add dependencies between template item
description: Add dependencies between template items in a task plan template to control the sequence in which tasks are available to agents after the template is applied.Edit the fields of an existing dependency or remove it from the dependency map in a task plan template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/add-dependencies-between-template-item.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Task Dependencies for Task Plan Templates, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Add dependencies between template item

Add dependencies between template items in a task plan template to control the sequence in which tasks are available to agents after the template is applied.

## Before you begin

Roles required: sn\_task\_plan.viewer, sn\_task\_plan.navigation\_menu, sn\_task\_plan.admin

Plugin IDs: com.sn\_task\_plan\_templates, com.snc.task\_dependency, and com.snc.customerservice.demo.

Confirm that the following conditions are met before you start:

-   The task plan template is in Draft state. You can add or edit dependencies only while the template is in **Draft** state.
-   The template contains at least two template items to link as a predecessor and a successor.

Task dependencies define the order in which agents act on tasks generated from a task plan template. All tasks are created at the same time when the template is applied. Dependencies determine when a successor task are available based on the status of a predecessor task and any configured time constraints.

Dependencies control the order in which agents can act on those tasks after generation. You can set how strictly a dependency is enforced and add an optional time offset between tasks.

You can define the following dependency types, which determine when a successor task becomes active:

|Dependency type|Status|
|---------------|------|
|Finish to Start|The successor task is active after the predecessor task is completed.|
|Start Together|The successor task is active at the same scheduled time as the predecessor task.|
|Start after Start|The successor task is active when the predecessor task starts.|

## Procedure

1.  Navigate to **All** &gt; **Task Plan Template Workspace**.

2.  Open a task plan template you want to edit and confirm that the status field shows as **Draft**.

3.  Select the **Dependencies** tab to view the dependency map.

4.  Select **New Dependency** and complete the required fields:

<table id="table_omh_2hk_fjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predecessor

</td><td>

Select the template item that has to be acted on first.

</td></tr><tr><td>

Successor

</td><td>

Select the template item that follows the predecessor.

</td></tr><tr><td>

Dependency Type

</td><td>

Select dependency type; Finish to Start, Start Together, or Start after Start.

</td></tr><tr><td>

Assignment Criteria

</td><td>

Select the agent assignment criteria. Options are:-   None
-   Same agent
-   Same day, same agent


</td></tr><tr><td>

Minimum Lag Time

</td><td>

Enter the minimum time before the successor task is available, using the days, hours, minutes, and seconds fields.

</td></tr><tr><td>

Maximum Lag Time

</td><td>

Enter the maximum time allowed before the successor task is available, using the days, hours, minutes, and seconds fields.

</td></tr></tbody>
</table>5.  Select **Save**.

    A confirmation message indicates that the dependency is created and the dependency map updates to reflect the relationship between template items.

    **Note:** If the dependency condition is not met, a warning appears on the successor task when opened. Agents can dismiss the warning and continue.


## Edit or delete a dependency

Edit the fields of an existing dependency or remove it from the dependency map in a task plan template.

### Before you begin

Role required: sn\_task\_plan.writer.

### Procedure

1.  Navigate to **All** &gt; **Task Plan Template Workspace**.

2.  Open the template in **Draft** state.

3.  Select the **Dependencies** tab.

4.  Select the dependency you want to edit or delete.

5.  Perform one of the following actions:

    -   To edit: update the required fields and select **Save**.
    -   To delete: select **Delete** and confirm the action.
    A success message confirms the action. The dependency map updates to reflect the change.



---
title: Add task dependencies between template items
description: Add dependencies between template items in a task plan template to control the sequence in which tasks are available to agents after the template is applied.Edit the fields of an existing dependency or remove it from the dependency map in a task plan template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/add-dependencies-between-template-item.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [task plan template, task dependencies, template items, predecessor successor]
breadcrumb: [Task dependencies for task plan templates, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Add task dependencies between template items

Add dependencies between template items in a task plan template to control the sequence in which tasks are available to agents after the template is applied.

## Before you begin

Role required: sn\_task\_plan.viewer, sn\_task\_plan.navigation\_menu, or sn\_task\_plan.admin

Plugin IDs: com.sn\_task\_plan\_templates, com.snc.task\_dependency, and com.snc.customerservice.demo.

Verify that the following conditions are met:

-   The task plan template is in Draft state. You can add or edit dependencies only while the template is in **Draft** state.
-   The template contains at least two template items to link as a predecessor and a successor.

## About this task

Task dependencies define the order in which agents act on tasks generated from a task plan template. All tasks are created at the same time when the template is applied. Dependencies determine when a successor task is available based on the status of a predecessor task and any configured time constraints.

Dependencies control the order in which agents can act on those tasks after generation. You can set how strictly a dependency is enforced and add an optional time offset between tasks.

You can define the following dependency types, which determine when a successor task is set to active:

|Dependency type|When the successor task becomes active|
|---------------|--------------------------------------|
|Finish to start|The successor task is active after the predecessor task is completed.|
|Start together|The the same scheduled time as the predecessor task.|
|Start after start|The the predecessor task starts.|

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

Select item that agents act on first.

</td></tr><tr><td>

Successor

</td><td>

Select item that follows the predecessor.

</td></tr><tr><td>

Dependency type

</td><td>

Select type: Finish to Start, Start Together, or Start after Start.

</td></tr><tr><td>

Assignment criteria

</td><td>

Select assignment criteria. Options are:-   None
-   Same agent
-   Same day, same agent


</td></tr><tr><td>

Minimum lag time

</td><td>

Enter the minimum time before the successor task is available, using the days, hours, minutes, and seconds fields.

</td></tr><tr><td>

Maximum lag time

</td><td>

Enter the maximum time allowed before the successor task is available, using the days, hours, minutes, and seconds fields.

</td></tr></tbody>
</table>5.  Select **Save**.

    A confirmation message appears when the dependency is saved.

    **Note:** If the dependency condition is not met, a warning appears on the successor task when opened. Agents can dismiss the warning and continue.


## Edit or delete a dependency

Edit the fields of an existing dependency or remove it from the dependency map in a task plan template.

### Before you begin

Role required: sn\_task\_plan.writer

### Procedure

1.  Navigate to **All** &gt; **Task Plan Template Workspace**.

2.  Open the template in **Draft** state and select the **Dependencies** tab.

    Select the dependency to edit or delete.

3.  Perform one of the following actions:

    -   To edit: update the fields and select **Save**.
    -   To delete: select **Delete** and confirm.
    A success message confirms the action. The dependency map updates to reflect the change.



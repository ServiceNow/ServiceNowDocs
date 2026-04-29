---
title: Add and Manage Task Dependencies
description: Add, edit, and manage dependencies within template items so that tasks execute in the correct sequence and follow defined dependency rules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Dependencies for Task Plan Templates, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Add and Manage Task Dependencies

Add, edit, and manage dependencies within template items so that tasks execute in the correct sequence and follow defined dependency rules.

## Before you begin

Role required: admin, task plan template user

-   The template must be in **Draft** state to create or modify dependencies.
-   The user must be granted edit access permissions.

## Procedure

1.  Navigate to **All** &gt; **Task Plan Template.**.

2.  Open a task plan template.

3.  In the **Task Plan Template Dependencies** related list, select **New**, or open the **Dependencies** form.

4.  Complete the required fields, including **Predecessor**, **Successor**, and **Dependency Type**.

5.  Enter the minimum and maximum lag times, if applicable.

6.  Select **Save** to create the dependency.

    Apply the template to generate tasks with dependencies:

7.  Open the record where you want to apply the template.

8.  Select **Apply Template**.

    The system generates task records based on the template items. Using the dependency rules configured in the **Task Plan Template Dependency** table, corresponding dependency relationships are created between the generated tasks in the `sn_task_dependency_m2m` table.



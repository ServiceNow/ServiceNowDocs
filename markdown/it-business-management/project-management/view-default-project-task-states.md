---
title: View default project and project task state categories
description: View category information for the default project and project task states. In the base system, the states in project and project task inherit the states in Task table.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a project task from a project, Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# View default project and project task state categories

View category information for the default project and project task states. In the base system, the states in project and project task inherit the states in Task table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Dictionary**.

2.  Update the filter with the following AND conditions:

    1.  **\[Table\] \[is\] \[task\]**

    2.  **\[Column name\] \[is\] \[state\]**

3.  Run the filter.

4.  Select the task table, and then choose **planned\_task** table in **Dictionary Overrides** related list.


## Result

The **Attributes** field displays different states and the categories for a state as shown below. It also displays the default state value for each category.

`close_states=3;4;7,default_close_state=3,default_work_state=2,default_open_state=1,default_skipped_state=7,default_pending_state=-5,pending_states=-5,open_states=1,work_in_progress_states=2`

-   **[Customize a state for project or project task](customize-project-task-states.md)**  
Add or modify a state of project or project task using dictionary override.

**Parent Topic:**[Create a project task from a project](t_CreateATaskFromAProject.md)

**Related topics**  


[Project and project task states](../concept/project-and-project-task-states.md)


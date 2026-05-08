---
title: Customize a state for project or project task
description: Add or modify a state of project or project task using dictionary override.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View default project and project task state categories, Create a project task from a project, Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Customize a state for project or project task

Add or modify a state of project or project task using dictionary override.

## Before you begin

Role required: admin

## About this task

As an example, the steps for adding custom states for **Work in progress** state category for Project task are described. In this example,

-   the existing **Work in Progress** state is removed and following three new states are added:

    |State|Label|Category|
    |-----|-----|--------|
    |10|Design|Work in Progress|
    |11|Development|Work in Progress|
    |12|Testing|Work in Progress|

-   the default **Work in Progress** is kept as `10` \(`Design`\).

## Procedure

1.  Define a new dictionary override for `pm_project_task` table under `[Task - State](view-default-project-task-states.md)` dictionary.

2.  Specify the override attributes for the dictionary override in **Attributes** field as follows:

    `close_states=3;4;7,default_close_state=3,default_work_state=10,default_open_state=1,default_skipped_state=7,default_pending_state=-5,pending_states=-5,open_states=1,work_in_progress_states=10;11;12`


## Result

-   As specified in Step 2, the `default_work_state` is declared as 10 and the `work_in_progress_states` as 10, 11, and 12. Now whenever a project task changes to any of the new **Work in Progress** states, its parent also moves to corresponding **Work in progress** state.

    Suppose that a project task has two children records, and if the first child record moves to **Development** state, the parent also moves to **Development** state. Now if the second child record moves to **Design** state, the two children records under the project task are in two different work in progress states. In such cases, the parent record moves to the default work in progress state. In this case, the parent record moves to **Design** as the `default_work_state` is specified as `10` \(`Design`\).

-   The project states can also be customized using the same steps.

**Parent Topic:**[View default project and project task state categories](view-default-project-task-states.md)

**Related topics**  


[Project and project task states](../concept/project-and-project-task-states.md)


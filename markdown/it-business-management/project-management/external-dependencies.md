---
title: External dependencies
description: As a project manager, you can use an external dependency to set up a dependency from a task in one project to a task in another project.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# External dependencies

As a project manager, you can use an external dependency to set up a dependency from a task in one project to a task in another project.

External dependencies help you to see the impact of changes in project schedules when a predecessor project changes.

## How external dependencies work

To define the external dependency, select a project task from the predecessor project to be linked to the task in the successor project. When an external dependency is [added](../task/create-external-dependency-planning-console.md), the system adds shadow tasks in both the successor and predecessor projects.

A shadow task is a read-only task in the respective project. It has the database attribute **shadow** set to true and **orig\_sys\_id** pointing to the **sys\_id** of its original task. The shadow task is kept in sync with its original task whenever the relations are processed.

In addition to the shadow tasks, two shadow relations are also added in the planned\_task\_rel\_planned\_task table. These relations are shadows of the original relations.

For example, for two projects, project P1 is the predecessor project, and P2 is the successor project. Project P1 has a task T1, and project P2 has a task T2.

If an external dependency is created from T1 to T2, the following tasks are added in the two projects:

|Project|Task|
|-------|----|
|P1|Shadow of T2|
|P2|Shadow of T1|

After adding the external dependency, the following shadow relation records are created in the planned\_task\_rel\_planned\_task table:

|Parent|Child|Project|External|
|------|-----|-------|--------|
|T1|T2| |True|
|Shadow of T1|T2|P2|False|
|T1|Shadow of T2|P1|False|

Where:

-   `Parent` is the predecessor project.
-   `Child` is the successor project.
-   `Project` is the project where the relation is seen.
-   `External` is the external dependency.

-   **[Types of external dependencies](external-dependency-types.md)**  
The Project management application supports two types of external dependencies - hard and soft.
-   **[Add an external dependency on planning console](../task/create-external-dependency-planning-console.md)**  
Add an external dependency between two projects on the planning console. Use the work breakdown structure \(WBS\) column of the planning console to create a dependency between the different projects tasks.

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)


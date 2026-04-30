---
title: Extending the Task table with Planned tasks
description: The Planned Task plugin provides a Planned Task \[planned\_task\] table that extends the Task \[task\] table.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Task table, Table admin, Tables and data, Configure core features, Administer]
---

# Extending the Task table with Planned tasks

The Planned Task plugin provides a Planned Task `[planned_task]` table that extends the Task `[task]` table.

The Planned Task plugin cannot be activated independently. It gets activated when activating the Project Management plugin \(through PPM Standard plugin\).

Planned tasks provide additional fields for tasks pertaining to time and effort as part of a planned, multi-stage process.

**Note:** If the Planned Task\_v2 \(`com.snc.planned_taskv2`\) plugin is active when you upgrade to the Geneva or later releases, the system adds the Task column to the Planned Task \[planned\_task\] table. The Task column is of type Composite Field, and stores the Short Description and Number of the task. During the upgrade, the system updates all records in the Planned Task table.

-   **[Create a planned task](../task/t_CreateAPlannedTask.md)**  
Planned Tasks are created on planned task child tables.
-   **[Create a baseline](c_CreateABaseline.md)**  
A Planned Task Baseline is a record of the start and end times of the planned task at a particular moment in time.
-   **[Measure time and effort](c_MeasureTimeAndEffort.md)**  
The Planned Task \[planned\_task\] table provides standard fields for tracking duration and effort.
-   **[Important planned task table fields](../reference/r_ImportantPlannedTaskTableFields.md)**  
The Planned Task table has these fields.
-   **[Planned task scripts](../reference/r_PlannedTaskScripts.md)**  
Several business rules and one script include determines the dynamic calculation of crucial Planned Task fields.
-   **[Planned task hierarchy](../task/t_PlannedTaskHierarchy.md)**  
The **Task Hierarchy** tool available for Planned Task displays the relationship between parent and child planned tasks.
-   **[Configure rollup for planned task fields](../task/t_ConfiguringRollupForPlannedTask.md)**  
You can configure the planned task fields to roll up the field values in the parent entity.

**Parent Topic:**[Working with the Task table](c_TaskTable.md)


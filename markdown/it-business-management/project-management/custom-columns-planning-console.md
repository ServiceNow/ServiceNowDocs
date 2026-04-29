---
title: Custom columns in the planning console
description: In addition to the regular columns that are provided in the base system, as the PPS admin, you can configure which columns appear in the planning console.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Custom columns in the planning console

In addition to the regular columns that are provided in the base system, as the PPS admin, you can configure which columns appear in the planning console.

You can define the columns that are available in the [project planning console](c_TheProjectPlanningConsole.md), [program workbench](../../program-management/concept/c_ProgramWorkbench.md), planning and tracking views in portfolio workbench, and the release management Gantt chart. From this list of defined columns, you can select the columns that you want to view in these planning console UIs at any time.

These tables are used for custom column configuration:

-   **Planning Console \[pm\_console\]**: Stores the definition for planning consoles such as Project and Portfolio.
-   **Planning Console Display Column \[pm\_console\_display\_column\]**: Stores the planning console display columns such as Short Description, WBS, and Priority.

    A console stored in `[pm_console]` has multiple display columns that are stored in `[pm_console_display_column]`.

    **Note:** You cannot edit list of column if the column refers to a table other than the \[sys\_user\] table.

-   **Planning Console Table \[pm\_console\_table\]**: Contains a list of tables which provide data to a console.

    A console sources the data from multiple tables. For example, Project console `[pm_project]` pulls data from `pm_project` and `pm_project_task` table. This list of tables is maintained in `[pm_console_table]`.

-   **Planning Console Column \[pm\_console\_columnn\]**: Maintains the columns that should be pulled from each table and the mapping of the column in `pm_console_display_column`.

-   **[Add a custom column to the planning console](../task/add-display-column.md)**  
Define the columns that you want to make available in the project planning console, portfolio workbench, program workbench, and the release management Gantt chart.

**Parent Topic:**[Using Planning console - Legacy](c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console](../task/t_OpenPlanningConsole.md)

[Planning console tasks](../reference/r_PlanningConsoleTasks.md)

[Client side planning console](client-side-planning-console.md)

[Gantt chart](c_GanttChart.md)

[Create a parent-child relationship on the planning console](../task/t_CreateParentChildRelatConsole.md)

[Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md)

[Create a dependency from the planning console](../task/t_CreateADependency.md)

[Using Planning console - Legacy](c_TheProjectPlanningConsole.md)


---
title: Client side planning console
description: During calculation of project schedule in the planning console, it is possible to build your project structure quickly on the client side \(browser\) without having to save details in the server for each interaction. It prevents any time lags that occur after you perform any actions in the planning console, and improves the scheduling performance.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Client side planning console

During calculation of project schedule in the planning console, it is possible to build your project structure quickly on the client side \(browser\) without having to save details in the server for each interaction. It prevents any time lags that occur after you perform any actions in the planning console, and improves the scheduling performance.

For example, when a project manager changes dates on a project task in the planning console, re-calculating the dates for the dependent tasks and the project can cause time lag if each interaction is saved to the server. Similarly, when a new task or a dependency is created, there can be a time lag before the new dates are displayed if they are saved on the server side each time.

When client side planning is [enabled](../task/enable-client-side-planning.md), the changes such as re-calculation of dates are not posted to the server immediately. All the changes in planning console are kept on client side until the user explicitly saves the changes to be committed to the server.

## Exceptions

There are a few actions for which you must save your changes immediately to the server side before proceeding such as:

-   Create baseline
-   Copy project
-   Copy partial project
-   Add child tasks
-   Add external dependency
-   Edit Assigned to
-   Edit Additional Assignees

In addition, if you enable custom business rules on any of the columns, those columns are also part of exceptions.

-   **[Enable client side planning](../task/enable-client-side-planning.md)**  
Enable client side planning in planning console to enable project scheduling at the client side.

**Parent Topic:**[Using Planning console - Legacy](c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console](../task/t_OpenPlanningConsole.md)

[Planning console tasks](../reference/r_PlanningConsoleTasks.md)

[Gantt chart](c_GanttChart.md)

[Create a parent-child relationship on the planning console](../task/t_CreateParentChildRelatConsole.md)

[Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md)

[Custom columns in the planning console](custom-columns-planning-console.md)

[Create a dependency from the planning console](../task/t_CreateADependency.md)

[Using Planning console - Legacy](c_TheProjectPlanningConsole.md)


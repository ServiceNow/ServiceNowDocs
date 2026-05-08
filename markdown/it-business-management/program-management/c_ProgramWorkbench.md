---
title: Program workbench
description: The program workbench is a central location for viewing details of a program and the projects and demands that are part of the program.
locale: en-US
release: australia
product: Program Management
classification: program-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Program Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Program workbench

The program workbench is a central location for viewing details of a program and the projects and demands that are part of the program.

The program manager role can use the program workbench to view and monitor the progress of the program and the projects and demands. Program workbench provides information for only tracking the program.

You can track the progress of demands and projects, and monitor the status of cost, resource, schedule, and scope for the selected fiscal period for the program.

**Note:**

-   Program workbench is based on Service Portal which means that you can configure, customize, and extend it as per your requirements and organizational workflow. For more information, see Service Portal documentation.
-   Program workbench does not support mobile device.

The program workbench comprises of the following components:

**Fiscal period**: A choice list on the top-right to select the fiscal year for which you monitor the program.

**Timeline View**: Shows a list of all the selected demands and projects that are part of the program, and a Gantt chart of all projects and demands over time.

You can:

-   configure the colors of the program items in Gantt chart with [Dashboard Configuration](../task/t_AccessTheProgramWorkbench.md) settings.
-   select the zoom level in Gantt chart calender to **Auto Fit**. The Gantt view fits in one page to view entire timeline in one go without using the scrollbar.
-   Review the external dependencies between projects in a program.
-   click the show/hide icon \(![Show or hide columns in Gantt](../image/cogwheel-icon.png)\) to show or hide columns.

**Note:**

-   A demand is included in the timeline view only if the **Expected Start** and **Due Date** fields are populated and if the demand is in qualified or approved state.
-   Admin can [customize](../../project-management/concept/custom-columns-planning-console.md) which columns appear in the column filter list when the show/hide columns icon \(![Show or hide columns in Gantt](../image/cogwheel-icon.png)\) is clicked in the timeline view.

**Project KPI**: The tab displays the most recent status of project KPIs such as overall health, schedule, cost, resources, and scope of all the projects in the program. This information is populated from the most recent [status report](../../project-management/task/t_CreateAProjectStatusReport.md) created for the projects.

You can:

-   click the name of a project in the tab to open the latest status report created for the project.
-   point to a status indicator for a project KPI to view the comments entered for the KPI for that project.

**Cost \(Planned vs. Actual\)**: The chart displays the actual costs from all projects in the program compared to the approved budget. The actual cost for projects is derived from the [expense lines](../../project-management/task/t_CreateAExpenseLine.md).

**Note:** An expense line can be created manually for a project when a specific expense is incurred. For example, if hardware is procured for a project, an expense line can be created for the amount spent on procuring the hardware. If you receive an item using ServiceNow Procurement, an expense line is created automatically. For resource hours, the expense lines are created automatically when the time cards for the project are approved.

The display settings for the chart can be modified by selecting any of the following from the choice list:

-   **Capex**: Displays the cost chart for capital expense only.
-   **Opex**: Displays the cost chart for operating expense only.
-   **All**: Displays the cost chart for both capital and operating expenses.

**Resource \(Allocated vs. Actual\)**: The chart displays the actual resource time spent on all project tasks versus the resource hours allocated to execute the projects and demands in the program. The actual time spent is taken from processed time cards for the projects.

![Timeline view tab in program workbench](../image/ProgramWorkbenchExample1.png "Program Workbench Example 1")

![Project KPI tab in program workbench](../image/ProgramWorkbenchExample2.png "Program Workbench Example 2")

-   **[Access the program workbench](../task/t_AccessTheProgramWorkbench.md)**  
When you access the program workbench, it displays a list of all the programs.

**Parent Topic:**[Program Management](c_ProgramManagement.md)

**Related topics**  


[Create a program to manage projects and demands](../task/t_CreateAProgram.md)

[Program Dashboard](c_ProgramManagerDashboard.md)


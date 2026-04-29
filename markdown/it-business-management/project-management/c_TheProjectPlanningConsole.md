---
title: Using Planning console - Legacy
description: The planning console is a centralized interface for the Project Management application.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Using Planning console - Legacy

The planning console is a centralized interface for the Project Management application.

**Important:**

Planning console is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new [Project Workspace](../../project-workspace/concept/project-workspace-landing-page.md) with enhanced UI to help you efficiently manage your projects.

The planning console gives project managers a comprehensive view of all aspects of a project, including a hierarchical list of sub-projects, if any, project tasks that appear in a work breakdown structure \(WBS\) list, and the project Gantt chart. The console also integrates with Live Feed so your users can collaborate on projects.

## Sections in the planning console

The planning console is divided into the following sections:

-   A list of the project tasks if you open the planning console for a project.
-   The Gantt chart.
-   Banner icons and lists for performing tasks on the console.

![screenshot for Planning console](../image/planning_console.png "Example planning console")

For more information on the Gantt chart and the task relationships and dependencies that you can build, see [Gantt chart](c_GanttChart.md) and [Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md).

**Note:** The resources in the **Assigned to** column of the planning console can be constrained to be derived only from the allocated resource plans associated to the project or any of its tasks.

## Business rules

By default, the business rules are not triggered during an operation in the planning console. You can enable the business rules using [**Enable firing of Business Rules**](../reference/r_InstalledWithProjectManagement.md#project_application_properties) property.

**Note:** To enable this property, you must clear the [**Enable Client Side Planning**](../task/enable-client-side-planning.md) check box.

You can also enable business rules when [defining the columns for planning console](../task/add-display-column.md#table_irt_mrm_rx) using the **Fire BR on Save** field.

## Client side planning console

Build your project structure quickly on the client side without having to save details in the server for each interaction in planning console. Enabling [**Client side planning console**](client-side-planning-console.md) prevents any time lags that occur after you perform any actions in planning console, and improves the scheduling performance.

## Automatic and manual projects

In an **automatic** project, any change to the dates, duration, or relationships of a project task automatically updates all the tasks in the entire project, including the project record, as necessary. The automatic project icon \(![screenshot for automatic project icon](../image/automatic_project.png)\) appears adjacent to the project name.

In a **manual** project, changes to the dates, duration, or relationships of a project task do not automatically update all tasks. So parent task dates do not reflect any changes made to dependents or child tasks. The only change that is made automatically is when a task date or duration change updates dates and duration of the project record. In a manual project, any update to actual start date does not update the planned end date of the project or project task. However, enabling the [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **Enable alter of planned date with Actual for Manual Project** updates the planned end date from actual start date and planned duration. The manual project icon \(![screenshot for manual project icon](../image/manual_project.png)\) appears adjacent to the project name.

You can specify if a project is automatic or manual in the **Calculation** field on the Project form. This field becomes read-only when the project starts.

## Tutorial

A tutorial walk through is available in the console. It shows you all the features of the console and how to use them. Access the walk through within the help icon \(![screenshot for help icon](../image/help_icon.png)\).

-   **[Open the project planning console](../task/t_OpenPlanningConsole.md)**  
Access the planning console to perform the planning for the project.
-   **[Planning console tasks](../reference/r_PlanningConsoleTasks.md)**  
You can perform several tasks on the planning console that you can perform on lists and forms, such as creating project tasks and copying projects. You can also perform several tasks unique to the console.
-   **[Client side planning console](client-side-planning-console.md)**  
During calculation of project schedule in the planning console, it is possible to build your project structure quickly on the client side \(browser\) without having to save details in the server for each interaction. It prevents any time lags that occur after you perform any actions in the planning console, and improves the scheduling performance.
-   **[Gantt chart](c_GanttChart.md)**  
A Gantt chart on the planning console is a visual representation of a project timeline that shows start and end dates of tasks, and the dependencies between tasks.
-   **[Create a parent-child relationship on the planning console](../task/t_CreateParentChildRelatConsole.md)**  
The WBS section of the planning console allows you to create parent-child relationships for new tasks or move around existing tasks in a new parent-child relationship. The position of a task in the hierarchy and the level of indentation determine the parent-child relationship it has with the tasks above or below it.
-   **[Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md)**  
In the WBS section of the planning console, you can create dependencies between tasks by specifying a series of values.
-   **[Custom columns in the planning console](custom-columns-planning-console.md)**  
In addition to the regular columns that are provided in the base system, as the PPS admin, you can configure which columns appear in the planning console.
-   **[Create a dependency from the planning console](../task/t_CreateADependency.md)**  
Create a dependency between two tasks on the planning console.

**Parent Topic:**[Using Project Management](using-project-management.md)


---
title: Project Diagnostics
description: Project Diagnostics enables you to detect corrupt data in a project such as task validity, dependencies, and relationships using diagnostic scans that execute diagnostic scripts. You can also fix corrupt data using fix scripts.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project Diagnostics

Project Diagnostics enables you to detect corrupt data in a project such as task validity, dependencies, and relationships using diagnostic scans that execute diagnostic scripts. You can also fix corrupt data using fix scripts.

Data might become corrupt or invalid for various reasons, such as:

-   Incorrect field mapping during project import
-   Incorrect scheduling of tasks
-   Incorrect dependency and relationship definitions

Project Diagnostics uses diagnostic scans and fix scripts to detect and fix corrupt data in your projects. It enables you to do the following action:

-   [Create and add diagnostic features](../../project-portfolio-suite-with-financials/task/add-diagnostic-feature.md)
-   [Add diagnostic and fix scripts](../../project-portfolio-suite-with-financials/task/add-diagnostic-and-fix-script.md) to fix corrupt or invalid project data
-   [Create Diagnostic scans and map related scripts](../../project-portfolio-suite-with-financials/task/create-diagnostic-scan-map-script.md)
-   Define fields for users to create specific filter conditions. The diagnostic scripts use the results of these filter conditions as input for detecting any corrupt or invalid data.

Project Diagnostics page provides the default scans described in the following table.

<table id="table_vjn_pcp_rz"><thead><tr><th>

Diagnostic Scan Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tasks with invalid top task

</td><td>

Lists the tasks that have an invalid top task. A task is considered to have an invalid top task if the value for the top task is set to **Null** or is mapped to a different task in the hierarchy.

</td></tr><tr><td>

Tasks with invalid top portfolio

</td><td>

Lists the tasks that have an invalid top portfolio. A task is considered to have an invalid top portfolio if it belongs to a different portfolio or is not associated with any portfolio.

</td></tr><tr><td>

Tasks with invalid top program

</td><td>

Lists the tasks that have an invalid top program. A task is considered to have an invalid top program if it belongs to a different program in the same portfolio or is not associated with any program.

</td></tr><tr><td>

Invalid relations

</td><td>

Lists the invalid relations in a project.A relation is considered to be invalid if the predecessor or successor is not a part of the project \(unless it is an external relation\), or if the predecessor or successor record does not exist in the system.

</td></tr><tr><td>

Validate parent tasks

</td><td>

Lists the tasks that have empty or invalid parents.

</td></tr><tr><td>

Check for tasks with cyclic dependencies

</td><td>

Checks for any cyclic relations, which are not permitted, in a project. For example, suppose you have a project in which Task A is related to Task B. A reverse relation from Task B to Task A would be considered a cyclic dependency.

</td></tr><tr><td>

Recalculate project

</td><td>

Recalculates task dates in a project.**Warning:** Performing this action might change the dates in a project.

</td></tr><tr><td>

Check duplicate/redundant relationships

</td><td>

Lists tasks that have duplicate or redundant relations in the selected projects.

</td></tr><tr><td>

Cost plans with no start and end fiscal period

</td><td>

Checks and lists cost plans with no start and end fiscal period within the selected projects.

</td></tr><tr><td>

Validate project task constraints in project

</td><td>

Lists all tasks with invalid constraint types. For example, a task with Start no later than set as a parent or the **Constraint date** field is empty for a task with Start no earlier than and Start no later than constraint.

</td></tr><tr><td>

Validate tasks with invalid state

</td><td>

Lists all tasks with invalid WIP or Closed state based on actual dates.

</td></tr><tr><td>

Identify projects with negative planned cost for any year where the budget was not allocated to the corresponding fiscal periods

</td><td>

Checks and lists the projects that have negative fiscal year project budgets.

</td></tr><tr><td>

Identify discrepancies in project budget

</td><td>

Checks and lists the projects for which project funding does not match with the sum of task type breakdown cost or fiscal year project budget.

</td></tr><tr><td>

Identify cost plan breakdowns with invalid fiscal periods

</td><td>

Checks and lists the cost plan breakdowns with invalid fiscal periods.

</td></tr><tr><td>

Identify duplicate task type breakdowns for an expense type and a fiscal period

</td><td>

Checks and lists the duplicate task type breakdowns.

</td></tr><tr><td>

Associate orphan expense lines to the system generated cost plan

</td><td>

Lists the expense lines that are not associated to any cost plan. When you run the fix script, these orphan expense lines are associated to a [system-generated cost plan](cost-plan-breakdown.md#) and then to the respective breakdowns of the system-generated cost plan.

</td></tr></tbody>
</table>
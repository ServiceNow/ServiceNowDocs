---
title: Create a program to manage projects and demands
description: Create a program to manage related projects and demands. Define the duration, estimated cost, benefits, and ROI to the organization.
locale: en-US
release: zurich
product: Program Management
classification: program-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Program Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a program to manage projects and demands

Create a program to manage related projects and demands. Define the duration, estimated cost, benefits, and ROI to the organization.

## Before you begin

Role required: it\_program\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Programs** &gt; **Create New**.

2.  On the Program form, fill in the fields.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Program Name

</td><td>

Name of the program.

</td></tr><tr><td>

Program manager

</td><td>

Program manager assigned to the program.

</td></tr><tr><td>

Number

</td><td>

System-generated number with a configurable prefix.

</td></tr><tr><td>

Portfolio

</td><td>

Portfolio to which the program belongs.If you do not select a portfolio for the program, the program becomes a global program. You can associate the projects and demands in a global program with any portfolio.

</td></tr><tr><td>

Priority

</td><td>

Priority associated with the program.

</td></tr><tr><td>

Status

</td><td>

Status of the program. This information rolls up from the status of all the projects that are part of this program.

</td></tr><tr><td>

State

</td><td>

Current state of the program.Default states: **Pending**, **Open**, **Work in Progress**, **Closed Complete**, **Closed Incomplete**, **Closed Skipped**.

 **Note:** Set the state of the program to Closed manually. The program state does not roll up to a Closed state when program tasks, projects, and demands move to Closed state.

</td></tr><tr><td>

Phase

</td><td>

Current phase of the program such as Initiating, Planning, and Executing.

</td></tr><tr><td>

Business Unit

</td><td>

The business unit to which this program belongs.

</td></tr><tr><td>

Investment Type

</td><td>

Investment type of the program.The default available options are **Cost Reduction**, **End User Experience**, **Legal and Regulatory**, **Revenue Generating**, **Service Sustaining**, and **Strategic Enabler**.

</td></tr><tr><td>

Impacted Business Units

</td><td>

Business units of the organization that this program affects.

</td></tr><tr><td>

Strategies

</td><td>

Strategic objectives of the organization that the program fulfills. A program can fulfill multiple strategic objectives.**Note:** Leave this field empty if the program does not fulfill any strategic objective.

</td></tr><tr><td>

Goals

</td><td>

Goals associated to the selected strategy. A program can fulfill multiple goals.If you do not select a strategy, then the Goals list displays all goals in the system.

**Note:** Leave this field empty if there are no goals associated with the program.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the program.

</td></tr></tbody>
</table><table id="table_mqc_dqy_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned start date

</td><td>

Intended program start date. If the start date of associated program tasks, projects, and demands is earlier than the program start date, the start date is adjusted to an earlier date.Removal of a demand or project from the program does not affect the planned start date of the program.

</td></tr><tr><td>

Planned end date

</td><td>

Intended program end date. The end date extends based on the end date of the program tasks, projects, and demands.Removal of a demand or project from the program does not impact the planned start date of the program.

 You can adjust the program end date manually, based on the start and end date of the associated program tasks, projects, or demands.

**Note:** If a demand with end date later than the program end date is added, the Planned end date field becomes read only.

</td></tr><tr><td>

Planned duration

</td><td>

Expected duration of this program. The planned duration changes based on the changes in planned start or end date of the program.

</td></tr><tr><td>

Actual start date

</td><td>

Date on which the program actually starts.

</td></tr><tr><td>

Actual end date

</td><td>

Date on which the program actually ends.

</td></tr><tr><td>

Actual duration

</td><td>

Actual duration of the program from program start to program closure.

</td></tr></tbody>
</table><table id="table_sgm_2qy_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total planned cost

</td><td>

Estimated cost of the program. If there is operational expenditure and capital expenditure associated to the program, then planned cost is sum of operational expenditure and capital expenditure, which is in functional currency.

</td></tr><tr><td>

Planned capital

</td><td>

Capital expenditure \(Capex\) for the program. If there are no cost plans associated to the program, the **Capital expense** field is editable. Select a currency type and enter a value.

</td></tr><tr><td>

Planned operating

</td><td>

Operational expenditure \(Opex\) for the program. If there are no cost plans associated to the program, the **Operational expense** field is editable. Select a currency type and enter a value.

</td></tr><tr><td>

Budget cost

</td><td>

Budgeted cost for this program.

</td></tr><tr><td>

Actual cost

</td><td>

Actual cost of the program. The value rolls up from the cost plan breakdowns from projects and demands in the program.

</td></tr><tr><td>

Planned benefit

</td><td>

Planned benefit value for the program.This value rolls up from the benefit plan breakdowns of the program.

 You can also enter the value manually. Select a currency from the Currency Type list and enter a value.

</td></tr><tr><td>

Planned returns

</td><td>

Planned returns is based on the difference between planned benefit and planned cost.

</td></tr><tr><td>

Planned ROI%

</td><td>

The result is derived from the values in the **Planned return** and **Planned cost** fields.The formula is: planned return / planned cost x 100.

</td></tr><tr><td>

Score

</td><td>

The program score is based on the individual scores of the following attributes: **risk score**, **value score**, and **size score**, which in turn are calculated based on risk, planning ROI%, and estimated cost attributes \(on a program\) respectively.**Note:** You can configure the formula for score calculation.

</td></tr><tr><td>

Risk

</td><td>

Risk associated with the program.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

Use the following related links and lists:

|Field|Description|
|-----|-----------|
|PMO Dashboard|Access the [PMO dashboard](../../../use/dashboards/application-content-packs/pmo-dashboard.md) to view comprehensive reports of the projects and demands in the program.|
|Program Budget|Allows you to [allocate the budget](allocate-budget-to-program.md) to the program.|
|Program Workbench|Access the [Program workbench](../concept/c_ProgramWorkbench.md) to view details of the projects, demands, and program tasks associated with the program.|
|Status Report|View the most recent [program status report](view-program-status-report.md) or create a new program status report.|

<table id="table_umz_qqy_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Program Tasks

</td><td>

View the list of all associated program tasks. To create a new program task, click the **New** button. For more information, see [Create a program task](t_CreateAProgramTask.md).

</td></tr><tr><td>

Projects

</td><td>

View the list of projects included in the program. To create a new project, click **New**. For more information, see [Define a project](../../project-management/task/t_CreateAProject.md).

To add existing project to the program, click **Edit**.If you want to create parent-child relationships between projects to establish project hierarchies select the parent project in the **Parent** field. This organizes large initiatives into manageable subprojects while maintaining consolidated visibility.

The subproject now rolls up to the parent project. Progress, costs, and timelines contribute to parent project metrics.

**Tip:**

Use project hierarchies when large initiatives require multiple work streams. Parent project = program-level view; subprojects = tactical execution.

</td></tr><tr><td>

Demands

</td><td>

View the list of demands included in the program. To create a new demand, click **New**. For more information, see [Create a demand](../../planning-and-policy/task/t_CreatingDemands.md).

 To add existing demand to the program, click **Edit**.

</td></tr><tr><td>

Risks

</td><td>

View the list of risks associated with the projects and demands of the program or the program itself.To create a new risk, click **New**.

</td></tr><tr><td>

Issues

</td><td>

View the list of issues associated with the projects and demands of the program or the program itself. To create a new issue, click **New**.

</td></tr><tr><td>

Cost plans

</td><td>

View the list of all cost plans for projects and demands that are part of the program.

</td></tr><tr><td>

Benefit Plans

</td><td>

View the list of all benefit plans for projects and demands that are part of the program.

</td></tr><tr><td>

Program Budget

</td><td>

View the program budget according to fiscal years. Click the amounts in the list to revise them.

</td></tr><tr><td>

Program Status Reports

</td><td>

View the list of status reports for the program.To generate a new status report, click **New**. For more information, see [Create a program status report](create-program-status-report.md).

</td></tr></tbody>
</table>-   **[Create a program task](t_CreateAProgramTask.md)**  
You can create program tasks from the Program form related lists.
-   **[Allocate budget to a program](allocate-budget-to-program.md)**  
Set the budget of a program according to the fiscal years.
-   **[Create a program status report](create-program-status-report.md)**  
Create a program status report periodically to view a status rollup of the projects in the program. When you create a status report, the status for different aspects of the program is rolled up from the project status reports of all projects.
-   **[View program status reports](view-program-status-report.md)**  
Program status reports provide the up-to-date at-a-glance progress of all the projects in the program in several categories.

**Parent Topic:**[Program Management](../concept/c_ProgramManagement.md)

**Related topics**  


[Program workbench](../concept/c_ProgramWorkbench.md)

[Program Dashboard](../concept/c_ProgramManagerDashboard.md)


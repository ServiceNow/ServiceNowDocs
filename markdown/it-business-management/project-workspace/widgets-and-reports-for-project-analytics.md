---
title: Widgets and reports for project analytics
description: Widgets and reports that provide information for the project summary in the Analytics page of the project workspace for Agile, Waterfall, and Hybrid projects.
locale: en-US
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Analyze project analytics from Project Workspace, Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Widgets and reports for project analytics

Widgets and reports that provide information for the project summary in the Analytics page of the project workspace for Agile, Waterfall, and Hybrid projects.

## Project widgets and reports

Widgets and reports provide information that enables you to view and track the progress of your Agile, Waterfall, and Hybrid project.

**Note:** You must have the Agile Development 2.0 plugin installed to view the widgets and reports for your Agile and Hybrid projects. The Project Summary Waterfall, Hybrid, and Scrum dashboards are available in the Next experience UI framework.

Your system administrator can configure the widgets and reports in the dashboard to display project information on the **Analytics** page. The following dashboards are available:

<table id="table_twj_13x_dbc"><thead><tr><th>

Project Execution Type

</th><th>

Dashboard Displayed

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hybrid

</td><td>

Project Summary – Hybrid

</td><td>

Contains reports and widgets for hybrid projects.

</td></tr><tr><td>

Agile

</td><td>

Project Summary – Scrum

</td><td>

Contains reports and widgets for agile projects.

</td></tr><tr><td>

Waterfall

</td><td>

Project Summary – Waterfall**Note:** This dashboard was previously known as Project Manager Summary Dashboard.

</td><td>

Contains reports and widgets for waterfall projects.

</td></tr></tbody>
</table>The project execution type determines the dashboard displayed on the **Analytics** page.

You can also embed a custom dashboard in the **Analytics** page. Your system admin can modify the PMViewDataUtils script include and configure the variable value for the dashboards\_tabs in the getDashboardUrl method. As a result, you can view the custom dashboard in Project Analytics. For example:

```
var dashboards_tabs =

      {
             waterfall: {
                         dashboard_sysId: '5d4959dd878003008b9b3a0548cb0bd0',
                         tab_sysId: '1d99d5dd878003008b9b3a0548cb0bbd'
                             },
             hybrid: {
                         dashboard_sysId: '96dc46c78700330047d84c2c59cb0bf1',
                         tab_sysId: '520d4ac78700330047d84c2c59cb0bab'
                              },
             agile: {
                         dashboard_sysId: 'f3dd4ec78700330047d84c2c59cb0b93&tab',
                         tab_sysId: '52fd8ec78700330047d84c2c59cb0bae'
                              },
             any_other_executionType: {
                         dashboard_sysId: 'custom_dashboard_sys_id',
                         tab_sysId: 'custom_dashboard_tab_sys_id'
                              },
         };

```

The following widgets and reports for all project types are provided in the **Analytics** page to help the project manager analyze the project.

|Name|Description|
|----|-----------|
|Stories Missing Acceptance Criteria|Number of stories in the project without acceptance criteria information.|
|Stories Missing Points|Number of stories in the project with the **Points** field blank.|
|Stories Acceptance Overdue|Number of stories in the project that are not in the Completed or Cancelled state after the sprint end.|
|Team-wise Sprint Status|Track the sprint-wise status of various scrum teams across the release. Click the team name to view sprint details.|
|Stories by State|Donut chart showing the number of stories in different stages of development such as Draft, Ready, and WIP. Click the appropriate state to view details of the stories.|
|Progress by Points|Track the progress of the project based on points. You can group and stack stories based on any combination of Epic, Assignment group, and State.|
|Progress by Stories|Track the progress of the project based on the number of stories. You can group and stack stories based on Epic, Assignment group, and state.|

<table id="table_nbk_qqz_fdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issues

</td><td>

Number of issues in the Pending, Open, and Work In Progress states included in the project.

</td></tr><tr><td>

Actions

</td><td>

Number of action items in the Pending, Open, and Work In Progress states for the project.

</td></tr><tr><td>

Change Requests

</td><td>

Number of change requests in the Pending, Open, and Work In Progress states for the project.

</td></tr><tr><td>

Stories by State

</td><td>

Pie chart showing the number of stories in different stages of development such as Draft, Ready, and WIP. Click the appropriate state to view the details for the stories. **Note:** This widget is applicable for Hybrid projects only.

</td></tr><tr><td>

Tasks by State

</td><td>

Donut chart showing the number of project tasks in different stages of development such as Pending, Open, Work In Progress, and Closed Complete. Click the appropriate state to view the task details.

</td></tr><tr><td>

Project Member Allocation Details \(Hrs\)

</td><td>

Stacked bar chart showing allocated and actual hours of the resources assigned to the project.

</td></tr><tr><td>

Project Member Allocation Details — Monthly \(Hrs\)

</td><td>

Pivot chart showing the monthly allocated and actual hours for the resources assigned to the project.

</td></tr><tr><td>

Task Assignments

</td><td>

Track the state of various project tasks across the release based on the assigned users or group. Click the user or group name to view the details of the assigned tasks.

</td></tr><tr><td>

Resource Plans by State

</td><td>

Donut chart showing the number of resource plans grouped according to their current state.

</td></tr><tr><td>

Overdue Tasks and Milestones

</td><td>

List of overdue project tasks and milestones, which are the tasks that satisfy either of the following conditions in the Project Task \[pm\_project\_task\] table: -   The value of the **Planned start date** is before today's date and the **State** value is Open or Pending.
-   The value of the **Shadow** field is set to false.

</td></tr><tr><td>

Upcoming Tasks \(next 2 weeks\) with no assignee

</td><td>

List of unassigned Open or Pending project tasks that are planned to start 14 days from the current date.

</td></tr></tbody>
</table><table id="table_jmk_kqz_fdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Current state of the project such as Initiating or Planning.

</td></tr><tr><td>

Status

</td><td>

Color indicator that signifies the status of the project.

</td></tr><tr><td>

Percent Complete

</td><td>

Percentage of the project that has been completed.

</td></tr><tr><td>

Time Elapsed

</td><td>

Amount of time that has passed while working on the project from the actual start date to the planned end date.If the project is in the Open or Pending state, then the time elapsed is calculated based on the Planned start date and the current date.

</td></tr><tr><td>

Risks

</td><td>

Number of risks in the Pending, Achieved, and Not Achieved states concerning the project.

</td></tr><tr><td>

Cost Trend Analysis

</td><td>

Line graph showing a comparison between the planned costs and actual costs on a monthly basis.

</td></tr><tr><td>

Monetary Benefit Trend Analysis

</td><td>

Line graph showing a trend of planned financial benefits on a monthly basis.

</td></tr><tr><td>

Non-monetary Benefit Plans

</td><td>

Breakdown of the number of non-monetary benefit plans for active projects along with its associated benefit plans.

</td></tr><tr><td>

Non-monetary Planned vs Actual Benefits

</td><td>

Comparison of total planned and actual non-financial benefits for active projects grouped by fiscal period.

</td></tr><tr><td>

Confirmed vs Allocated vs Actual Hours

</td><td>

Comparison of total confirmed, allocated, and actual hours for the project.

</td></tr><tr><td>

Time Cards — Pending Approval

</td><td>

Time cards for the selected project that are submitted but not yet approved.

</td></tr><tr><td>

Time Card — Exception Report

</td><td>

List of users who did not submit their time cards for the selected project, and time cards that are not yet approved for the selected project. The exception report is generated for users who are assigned to a task in progress, or hard-allocated to the project or task.

</td></tr></tbody>
</table>**Parent Topic:**[Analyze project analytics from Project Workspace](../task/analyze-project-analytics-in-project-workspace.md)


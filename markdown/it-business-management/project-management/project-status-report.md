---
title: View project status reports
description: Project status reports provide the most recent, at-a-glance progress of a project displayed in several categories.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Create a project status report, Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# View project status reports

Project status reports provide the most recent, at-a-glance progress of a project displayed in several categories.

## Before you begin

Role required: it\_project\_manager

## About this task

The project status report acts as a snapshot, meaning the report preserves the status of various parameters for the date and time when the status report is generated and does not display the status of various parameters dynamically. For example, the project status report created last week retains the same status as it was for that week and does not update the status dynamically.

You can use the project status reports to compare the progress of your project. Generate a new project status report for your recent changes to reflect on the report.

The project status report shows snapshot status of RIDAC \(Risk, Issues, Decisions, Actions, and Request Changes\) records, key milestones, and charts only.

## Procedure

1.  Open a project status report.

<table id="choicetable_ft2_dt1_wbb"><thead><tr><th align="left" id="d57046e74">

Option

</th><th align="left" id="d57046e77">

Steps

</th></tr></thead><tbody><tr><td id="d57046e83">

**From project workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Project Workspace**.
2.  From Projects page, select a project to open.
3.  Select the **Status Report** tab.
4.  Select a status report from the list to view its contents.


</td></tr><tr><td id="d57046e119">

**From project record**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.
2.  In the project list, open a project record.
3.  Select the **Status Report** related link.
4.  Select a status report from the list.


</td></tr><tr><td id="d57046e161">

**From Project Status form**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.
2.  In the project list, open a project record.
3.  Select the **Status Report** related list.
4.  Select **New** and create a project status report.
5.  Select **Save**.
6.  Select **View**.


</td></tr></tbody>
</table>    **Note:** You can also open a project status report from the portfolio workbench. Open a portfolio in the portfolio workbench and select **Track Portfolio**. Right-click a project in the **Timeline View** and select **Status Report** from the context menu.

2.  Review project status in the following sections.

<table id="table_status_report_project"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Provides a general overview about the project such as:-   **Project Name**: Name of the project.
-   **Project Manager**: Project manager assigned to the project.
-   **Portfolio**: Primary portfolio to which the project belongs.
-   **State**: Current state of the project.
-   **Phase**: Current phase of the project such as Initiating, Planning, and Executing.
-   **% Complete**: Percentage of the project completed.
-   **Planned Start Date**: Intended date the project begins.
-   **Planned End Date**: Intended date the project ends.
-   **Planned Cost**: Estimated cost of the project.
-   **Actual Start Date**: Date on which the project began.
-   **Actual End Date**: Actual end date of the project.
-   **Actual Cost**: Actual cost of the project.
 This information is rolled up from the project form.

 If you had set your preference as project currency in the **Status report currency** field of the Project form, then the **Overview** tab displays the following project currency fields:

-   **Planned Cost in Project Currency**: Estimated cost of the project in project currency.
-   **Actual Cost in Project Currency**: Cost of the project in project currency.
**Note:** The above fields appear when you enable the PPM Standard Multicurrency plugin \(com.snc.ppm\_multicurrency\) and switch to the Project Currency view. For more information, see [Multi-currency in project financials](../../project-portfolio-suite-with-financials/concept/multicurrency-pps.md).

</td></tr><tr><td>

Summary

</td><td>

Provides information about the overall health of the project.-   **Executive Summary**: Brief summary and analysis of the project.
-   **Last Week's Achievements**: Progress of the project in the previous week.
-   **Key Activities Planned**: Next planned activities for the project.


</td></tr><tr><td>

Cost \(Planned vs. Actual\) chart

</td><td>

If you have enabled the Project Currency view, then the Cost in Project Currency \(Planned vs. Actual\) section provides information about the actual cost versus the planned cost in project currency.This information is rolled up from the [cost plan](t_CreateAProjectCostPlan.md) for the project.

-   **Planned**: Approved cost for the project.
-   **Actual**: Actual cost for the project is derived from the expense line created for the project cost plan and from the time cards created for the project.


</td></tr><tr><td>

Resource \(Allocated vs. Actual\) chart

</td><td>

Provides information about the actual resource hours used versus the allocated hours. This information is rolled up from the [resource plan](../../resource-management/task/t_CreateResourcePlanProjectTask.md) for the project.-   **Allocated**: Resource hours that have been allocated to execute the project.
-   **Actual**: The actual time spent is taken from the processed time cards created for the project.


</td></tr><tr><td>

Current Status

</td><td>

Provides the status related to overall health, schedule, cost, resources, and scope of the project. This information is populated from the most recent status entered by the project manager for the project.-   **Status**: Color indicator to signify the status.
-   **Comments**: Comments for the status.


</td></tr><tr><td>

Status History

</td><td>

Provides the trend of overall health, schedule, cost, resources, and scope of the project. The Status reports can have maximum 9 entries in the status history tab. This information is populated up from the last 9 [status report](t_CreateAProjectStatusReport.md) created for the project.

 **Date**: Status date of the status reports. The color indicators signify the status of the project on these dates.

</td></tr><tr><td>

Key Milestones

</td><td>

Provides information about key milestones in the project. This information is populated from the [project tasks](t_CreateATaskFromAProject.md) identified as key milestones.-   **Pending**: List of key milestone tasks in the Pending, Open, and Work in Progress state.
-   **Completed**: List of key milestone tasks in the Closed state.


</td></tr><tr><td>

Risks

</td><td>

Provides information about risks concerning the project. This information is rolled up from the risks that are part of the project.-   **Pending**: List of risks in the Pending state.
-   **Completed**: List of risks in the Achieved and Not Achieved state.
 The following information from the Risk record is displayed:

-   Short description
-   Probability
-   Risk status
-   State
-   Assigned to
-   Due date
 For more information, see [Add risks for a project](add-risks-for-project.md).

</td></tr><tr><td>

Issues

</td><td>

Provides information about issues included in the project. This information is rolled up from the issues reported for the project.-   **Pending**: List of issues in the Open and Work in Progress state.
-   **Completed**: List of issues in the Closed state.
 The following information from the Issue record is displayed:

-   Short description
-   Priority
-   State
-   Assigned to
-   Due date
 For more information, see [Add issues for a project](add-issues-for-project.md).

</td></tr><tr><td>

Decisions

</td><td>

Provides information about decisions included in the project. This information is rolled up from the decisions reported for the project.-   **Pending**: List of issues in the Open and Work in Progress state.
-   **Completed**: List of issues in the Closed state.
 The following information from the Decision record is displayed:

-   Short description
-   Priority
-   Decision status
-   State
-   Assigned to
-   Due date
 For more information, see [Add decisions for a project](add-decisions-for-project.md)

</td></tr><tr><td>

Actions

</td><td>

Provides information about action items for the project. This information is rolled up from the actions reported for the project.-   **Pending**: List of actions in the Open and Work in Progress state.
-   **Completed**: List of actions in the Closed state.
 The following information from the Action record is displayed:

-   Short description
-   Priority
-   State
-   Approval
-   Assigned to
-   Due date
 For more information, see [Add actions for a project](add-actions-for-project.md).

</td></tr><tr><td>

Request Changes

</td><td>

Provides information about a [change request](create-project-change-request.md) for the project. This information is rolled up from the change requests created for the project.-   **Pending**: List of project change requests in the Pending, Open, and Work in Progress state.
-   **Completed**: List of project change requests in the Closed state.
 The following information from the Request Change record is displayed:

-   Title
-   Priority
-   State
-   Category
-   Approval
-   Assigned to
-   Due date
 For more information, see [Create a request change](create-project-change-request.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Create a project status report](t_CreateAProjectStatusReport.md)

**Related topics**  


[Create a project status report](t_CreateAProjectStatusReport.md)


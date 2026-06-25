---
title: View program status reports
description: Program status reports provide the up-to-date at-a-glance progress of all the projects in the program in several categories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/program-management/view-program-status-report.html
release: australia
product: Program Management
classification: program-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a program to manage projects and demands, Program Management, Project Portfolio Management, Strategic Portfolio Management]
---

# View program status reports

Program status reports provide the up-to-date at-a-glance progress of all the projects in the program in several categories.

## Before you begin

Role required: it\_program\_manager

## About this task

Use the **Program Status Report** related list to view the program status reports created for the program. If no report is listed, [create a program status report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-management/create-program-status-report.md).

## Procedure

1.  Navigate to **Project** &gt; **Programs** &gt; **All**.

2.  In the program list, open a program record.

3.  Select the **Status Reports** related link.

4.  Select a status report from the top-left corner of the page to view its contents.

5.  Review the program status in the report.

<table id="table_status_report_project"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

Provides general overview information about the program:-   **Program Name**: Name of the program.
-   **Program Manager**: The program manager.
-   **Portfolio**: The portfolio to which the program belongs.
-   **Business Unit**: The business unit to which the program belongs.
-   **Investment Type**: Investment type of the program.
-   **Impacted BU**: Business units of the organization that this program affects.
-   **State**: Current state of the program.
-   **Phase**: Current phase of the program, for example, Initiating, Planning, and Executing.
-   **% Complete**: Percentage of the program completed.
-   **Planned Start Date**: Planned start date of the program.
-   **Planned End Date**: Planned end date of the program.
-   **Planned Cost**: Estimated cost of the program.
-   **Actual Start Date**: Actual start date of the program.
-   **Actual End Date**: Actual end date of the program.
-   **Actual Cost**: Actual cost of the program.
 This information rolls up from the [Program form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-management/t_CreateAProgram.md).

</td></tr><tr><td>

Summary

</td><td>

Information about the overall health of the program from the most recent [status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-management/create-program-status-report.md) entered by the program manager for the project.-   **Executive Summary**: Brief summary and analysis of the program.
-   **Last Week's Achievements**: Progress of the program in the previous week.
-   **Key Activities Planned**: Next planned activities for the program.


</td></tr><tr><td>

Current Status

</td><td>

Status of program related to overall health, schedule, cost, resources, and scope that is rolled up from the latest project status reports of all projects in the program. If there are multiple project status reports for each of these projects, the values from the latest project status report of each project are aggregated and rolled up to the program status. For more information, see [Program Status Report form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-management/create-program-status-report.md).

 Different colors indicate the status of above aspects. The rolled-up color for the final status is in the order red, yellow, and green by default. If there are projects in red, yellow, and green, then the program status is red. If there are projects only in yellow and green, then the program status is yellow.

 The following image illustrates the color codes for the program status rolled up from the project.\[Omitted image "program-status-roll-up.png"\] Alt text: Program status roll-up from the project status

**Note:** A grey X icon \(\[Omitted image "none\_icon.png"\] Alt text: None icon\) for any program aspect means that the program manager has excluded that aspect from the status report.

</td></tr><tr><td>

Project KPI

</td><td>

Status of the Key Performance Indicators for overall health, schedule, cost, resources, and scope for each project in the program. Only projects for which the **Show on Program Status Report** option in the project form is selected are listed.

The value of these KPIs roll up and are shown in the Current Status section of the program status report. **Note:** A grey X icon \(\[Omitted image "none\_icon.png"\] Alt text: None icon\) next to any project KPI means that the project manager has excluded that aspect from the status report.

</td></tr></tbody>
</table>6.  If you need a printed copy of the report, select the print icon \(\[Omitted image "PrintIcon.png"\] Alt text: Print icon\) in the header of **Status Report** tab.


## Program status report

\[Omitted image "program-status-report-example.gif"\] Alt text: Program status report example

**Parent Topic:**[Create a program to manage projects and demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-management/t_CreateAProgram.md)

**Related topics**  


[Create a program task]()

[Allocate budget to a program]()

[Create a program status report]()


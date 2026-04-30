---
title: Create a program status report
description: Create a program status report periodically to view a status rollup of the projects in the program. When you create a status report, the status for different aspects of the program is rolled up from the project status reports of all projects.
locale: en-US
release: zurich
product: Program Management
classification: program-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a program to manage projects and demands, Program Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a program status report

Create a program status report periodically to view a status rollup of the projects in the program. When you create a status report, the status for different aspects of the program is rolled up from the project status reports of all projects.

## Before you begin

Ensure that the **Show on Program Status Report** option in the Project form for all the projects that you want to include in the status report is selected.

Role required: it\_program\_manager

## Procedure

1.  Navigate to **Project** &gt; **Programs** &gt; **All**.

2.  In the program list, open a program record.

3.  In the **Program Status Reports** related list, click **New**.

4.  On the form, fill in the fields.

    **Note:**

    Changing the status for any aspect in the Program Status Report form also updates the corresponding fields in the Program form.

<table id="status_report_form_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Program

</td><td>

Name of the program.

</td></tr><tr><td>

Status Date

</td><td>

Date until which you want to generate the status report.Default value is the current date.

</td></tr><tr><td>

Number

</td><td>

System-generated ID number for the status report with a configurable prefix.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |State|Current state of the program such as Pending, Open, or Work in Progress.|
    |Percent complete|Percentage of the program completed.|
    |Planned start date|Planned start date of the program.|
    |Planned end date|Planned end date of the program.|
    |Actual start date|Actual start date of the program.|
    |Actual end date|Actual end date of the program.|
    |Planned cost|Estimated cost of the program.|
    |Actual cost|Actual cost of the program.|

    |Field|Description|
    |-----|-----------|
    |Overall health|Overall health of the program rolled up from the latest status report of each project in the program. The status is indicated using red, green, and yellow colors as the default.|
    |Executive Summary|Brief summary and analysis of the program.|
    |Comments|Comments about the overall status.|
    |Last Week's Achievements|Description of key tasks completed or any significant progress in the program in the last week.|
    |Key Activities planned|Next planned activities for the program.|

    |Field|Description|
    |-----|-----------|
    |Schedule|Status of the program schedule rolled up from the latest project status report of each project in the program. The status is indicated using red, green, and yellow colors by default.|
    |Comments on Schedule|Information related to the program schedule.|

    |Field|Description|
    |-----|-----------|
    |Cost|Status of the program cost rolled-up from the latest project status report of each project in the program. The status is indicated using red, green, and yellow colors by default.|
    |Comments on cost|Information related to the program cost.|

    |Field|Description|
    |-----|-----------|
    |Resources|Status of resources rolled-up from the latest project status report of each project in the program. The status is indicated using red, green, and yellow colors by default.|
    |Comments on Resources|Additional information related to program resources.|

    |Field|Description|
    |-----|-----------|
    |Scope|Status of the program scope rolled up from the latest project status report of each project in the program. The status is indicated using red, green, and yellow colors by default.|
    |Comments on Scope|Information related to the program scope.|

5.  Select a different status color to override the rolled-up color for various aspects of the program or select **None** if you do not want the status of an aspect to appear in the program status report.

    Selecting **None** displays a grey X icon \(![None icon](../image/none_icon.png)\) for that program aspect on the program status report.

    The override color that you set is not retained from one report to next. When the next program status report is generated, it takes the color from the associated projects.

6.  Select **Submit**.


**Parent Topic:**[Create a program to manage projects and demands](t_CreateAProgram.md)

**Related topics**  


[Create a program task](t_CreateAProgramTask.md)

[Allocate budget to a program](allocate-budget-to-program.md)

[View program status reports](view-program-status-report.md)


---
title: Create a status report in Project Workspace
description: Create a status report in Project Workspace for your projects. Your team can view the report and be updated on project health, metrics, risks, issues, and milestones.
locale: en-US
release: xanadu
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2024-09-10"
reading_time_minutes: 4
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a status report in Project Workspace

Create a status report in Project Workspace for your projects. Your team can view the report and be updated on project health, metrics, risks, issues, and milestones.

## Before you begin

Role required: it\_pps\_admin, it\_project\_manager

## About this task

## Procedure

1.  Open a project from the planning page of Project Workspace.

    For information on how to navigate to the planning page, see [Access the new Project Workspace](access-new-project-workspace.md).

2.  Open the Status reports page of the project by selecting **Status Reports** from the list.

3.  From the Pages section, select **Create status report**.

    ![Create new status report from template.](../image/create-status-report-from-template.png)

4.  If you want to base your status report on a template, then select **Create status report from template**.

5.  In the "Welcome to your Template Center!" screen, select **Use** for the template that you want to use.

6.  On the Create status report form, fill in the fields.

    For a description of the field values, see [Create status report form](../reference/create-status-report-form.md).

7.  Select **Submit**.

    The status report appears with the data and information that you entered populated.![Sample status report.](../image/status-report-ACME.png)

8.  Select the **More actions** icon and then perform these steps.

    1.  Select **Export as PDF** to share and archive a PDF version of the report.

    2.  Select **Edit status report** to open and edit the status report.

    3.  Select **Hide Live Presence** to hide the live presence.

    4.  Select **Copy** to create a copy of status report.

        ![Export as PDF](../image/status-report-export-as-PDF.png)

        You can’t edit the status report. To edit the status report, you can disable the status report read-only system property \(sn\_pw.status\_report\_doc\_read\_only\). By default, it is set to true, and the status report is read only. This property can be enabled or disabled at both the instance and record levels.

9.  Make changes to the report by editing the data, formatting, organizing the content, and entering additional data.

    The changes you make to the status report here are saved to the status report in the project workspace but don’t get saved to the underlying status report record, which you access from the status report related list in Projects form.

10. Observe and monitor the report.

    For more information on viewing and analyzing status reports, see [Analyze the status report in Project Workspace](view-status-report-in-project-workspace.md).

    If you don’t have old status reports, you can't see the import option. For more information on importing existing status report, see [Import old project status report to Project Workspace](import-old-status-reports.md).


-   **[Analyze the status report in Project Workspace](view-status-report-in-project-workspace.md)**  
Observe a status report in Project Workspace for your project to learn about project health, metrics, risks, issues, and milestones.
-   **[Update the status report in Project Workspace](update-status-report-pw.md)**  
Create and update the status report for your projects in Project Workspace.
-   **[Duplicate a status report in Project Workspace](duplicate-status-report-pw.md)**  
Save time by duplicating an existing status report to copy all the project details without having to copy the information manually in the Project Workspace.
-   **[Import old project status report to Project Workspace](import-old-status-reports.md)**  
Migrate your old status reports from the classic Project Workspace to the new Project Workspace and optimize reporting process of your projects.
-   **[Add dynamic content to status report in Project Workspace](add-dynamic-content-to-status-report-in-pw.md)**  
Add dynamic content to a status report in Project Workspace for your projects. The dynamic content gets updated automatically in the status report as a change is made to the record.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Add dynamic content to status report in Project Workspace](add-dynamic-content-to-status-report-in-pw.md)

[Status reporting in Project Workspace](../concept/status-reporting-in-pw.md)

[Analyze the status report in Project Workspace](view-status-report-in-project-workspace.md)

[Import old project status report to Project Workspace](import-old-status-reports.md)

[Create a status report template in Project Workspace](create-a-status-report-template-project-workspace.md)


---
title: Update status report in Project Workspace
description: Modify a status report in Project Workspace for your project to update project health, metrics, risks, issues, and milestones.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a status report in Project Workspace, Managing projects with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Update status report in Project Workspace

Modify a status report in Project Workspace for your project to update project health, metrics, risks, issues, and milestones.

## Before you begin

Role required: it\_pps\_admin, it\_project\_manager

## About this task

By default, the status report is read-only and the **sn\_pw.status\_report\_doc\_read\_only** system property is set to true. To edit the status report, you can disable this system property by setting it to false. Once you change the property to false, you can edit or update the report. You can also navigate to the Details page and set **Allow edit status report** field to true.

Any updates made on the status report form are reflected in the status report, regardless of whether the property is set to true or false.

## Procedure

1.  Open a project from the home page of Project Workspace.

    For information, see [Access the new Project Workspace](access-new-project-workspace.md).

2.  Open the Status reports page of the project by selecting **Status Reports** from the list.

3.  From the Pages section, select the name of the status report you want to update.

4.  Select the me of the stat icon and select **Edit status report** to edit the status report.

    -   When editing is disabled, all fields in the status report are read-only.
    -   When editing is enabled, only dynamic fields in the status report remain read-only and you can add any static or manual information in the report.
    -   You can still edit the dynamic fields in both the scenarios using Edit Status Report option.
5.  Make changes to the report by editing the data, formatting, organizing the content, and entering additional data.

    To edit the **sn\_pw.status\_report\_doc\_read\_only** property, enter `sys_properties.list`. In the list, search for **sn\_pw.status\_report\_doc\_read\_only**. You can modify the **Value** field and select **Update**.

    If the existing status reports are incompatible with the new changes, following actions are taken. These actions are applicable on both status report and project status form:

    -   If a report is read-only, it automatically updates to the new format without notification.
    -   If a report is editable, a message appears prompting you to copy the static data and regenerate the report.
    -   A Regenerate button is provided, which allows you to regenerate the report and ensure compatibility with the new updates.

**Parent Topic:**[Create a status report in Project Workspace](create-a-status-report-in-project-workspace.md)

**Related topics**  


[Import old project status report to Project Workspace](import-old-status-reports.md)

[Add dynamic content to status report in Project Workspace](add-dynamic-content-to-status-report-in-pw.md)


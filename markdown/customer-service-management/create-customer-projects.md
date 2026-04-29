---
title: Create customer projects
description: Create customer projects at internal or external business locations to manage location openings, renovations, closings, or other location-specific initiatives.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create customer projects

Create customer projects at internal or external business locations to manage location openings, renovations, closings, or other location-specific initiatives.

## Before you begin

To access customer projects and to enable required roles, make sure that you enable the Customer Project Management \(com.snc.csm\_ppm\) plugin.

Role required: admin, it\_project\_manager, sn\_service\_org.project\_manager

## About this task

A customer project can be initiated by applying templates, or by importing and exporting projects. Furthermore, cases can be created to address issues either at the project or project task level.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  Initiate a project by selecting **New**.

    Under **My projects**, a list of projects associated with your role is displayed. Under **All projects**, a list of all projects is displayed.

3.  On the form, fill in the fields.

    The following table outlines the unique fields of the form. To learn more about other fields, refer [Starting a project](https://www.servicenow.com/docs/access?context=t_CreateAProject&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

    |Field|Description|
    |-----|-----------|
    |Project class|Class of the project. Select **Customer Project**.|
    |Project template|Template of a project. To create a project from template, select a template from the list displayed. Based on the template, project tasks are created.|
    |Project name|Name for the project.|

4.  Select **Confirm**.

5.  Select a project to see all the related tabs.

    ![Project workspace displaying related tabs of a project.](../image/project-workspace.png)

<table id="table_jzx_dmn_tdc"><thead><tr><th>

Related tabs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planning

</td><td>

In this section, you can:-   create or add tasks
-   update task details
-   create case for the project and project tasks
-   set deadlines using graph
-   apply template
-   delete, move, import, and export project
-   launch help videos
-   calculate completion estimates
-   copy partial project


</td></tr><tr><td>

Details

</td><td>

In this section, you can view and update all project tasks and details of the project.

</td></tr><tr><td>

Financials

</td><td>

Displays cost plans of the project

</td></tr><tr><td>

RIDAC

</td><td>

Displays risks of the project

</td></tr><tr><td>

Analytics

</td><td>

Enables you to track project phases, plans, assignments, issues, time elapsed, resources, benefits, and other details of the project graphically.

</td></tr><tr><td>

Docs

</td><td>

Docs of the project

</td></tr><tr><td>

Status Reports

</td><td>

Reports of the project

</td></tr></tbody>
</table>6.  Under the **Details** tab, fill in the other fields.

    The following table outlines the unique fields of the customer project. To learn more about other fields, see [Starting a project](https://www.servicenow.com/docs/access?context=t_CreateAProject&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

<table id="table_h33_rpn_tdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Account for the project. Select an account from the displayed list.**Note:**

-   On selecting an account, the **Service Organization** field disappears.
-   The customer project manager can’t access projects or project tasks associated with service organization project manager.


</td></tr><tr><td>

Service Organization

</td><td>

Service organization for the project. Select an internal business location \(IBL\) or external business location \(EBL\) from the displayed list.**Note:**

-   On selecting a service organization, the **Account** field disappears.
-   The service organization project manager can’t access projects or project tasks associated with customer project manager.


</td></tr></tbody>
</table>
## What to do next

[Create a project task from a project](https://www.servicenow.com/docs/access?context=t_CreateATaskFromAProject&version=australia&pubname=australia-it-business-management&ft:locale=en-US)


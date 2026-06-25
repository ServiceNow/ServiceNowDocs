---
title: Migrate budget of active projects to Next Experience
description: Migrate the project budget to Next Experience to manage the financials using Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/fin-migrate-budget-project-ppm.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate budget of active projects to Next Experience

Migrate the project budget to Next Experience to manage the financials using Project Workspace.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d181504e85">

Choice

</th><th align="left" id="d181504e88">

Description

</th></tr></thead><tbody><tr><td id="d181504e94">

**Using list actions**

</td><td>

1.  Select the required projects from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Budget**.
3.  On the migrate budget confirmation window, select **OK**.


</td></tr><tr><td id="d181504e124">

**Using related links**

</td><td>

1.  Open the required project.
2.  Select the **Migrate Budget** related link.
3.  On the migrate budget confirmation window, select **OK**.


</td></tr><tr><td id="d181504e151">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate budget for active demands and projects** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/scheduled-script-execution-form.md).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Note:** After migration, you won't be able to view the budget on Classic UI. You're encouraged to manage budget using the Financials in Next Experience.


**Parent Topic:**[Starting a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md)

**Related topics**  


[Create a project task from a project]()

[Create a parent-child relationship on the Project Task form]()

[Create a monetary benefit plan for a project]()

[Create a non-monetary benefit plan for a project]()

[Associate monetary and non-monetary benefit plans]()

[Create a project cost plan]()

[Recalculating costs of all resource plans in a project]()

[Create an expense line]()

[Create and manage waterfall projects]()

[Update a project]()

[Copy a project]()

[Assign a project schedule]()

[Create baseline of a project]()

[Create a milestone]()

[Activate project task email notifications]()

[Change the planned start date of a project]()

[Create a cost type definition]()

[Costing add-on in Project Management]()

[Generate labor costs]()

[Create a project status report]()

[Allocate budget to a project]()

[Migrate financial baselines of projects to Next Experience]()

[Migrate financial baselines of projects to Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/migrate-fin-baselines-projects.md)


---
title: Copy a project
description: Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/t\_CopyAProject.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Copy a project

Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  On the Project form, select additional actions icon \(\[Omitted image "additional-options.png"\] Alt text: additional actions icon.\) and select **Copy Project**.

2.  On Copy the selected project modal, enter the **New Project Name**.

3.  Select a **Start date** and select **OK**.

    Copy partial project, which is available from the Project Task form, provides similar functionality. It copies all task or project relationships and children from the selected project and inserts them into the current project. In this case, a new project record is not created.


## Result

Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to **0**.

By default only the short description, planned dates and duration fields are copied from source project to the target project. If additional columns must be copied, they should be declared in the [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **List of attributes that will be copied from the originating project task**.

-   **[Change default values of copied project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_ModifyTheCopyProjectUIPage.md)**  
Reset or change the default values for copied fields in the new copied partial or complete project.

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

[Migrate budget of active projects to Next Experience]()

[Migrate financial baselines of projects to Next Experience]()

[Change default values of copied project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_ModifyTheCopyProjectUIPage.md)


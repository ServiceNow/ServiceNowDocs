---
title: Activate project task email notifications
description: The following email notifications for the Project Management application are available by default, but are inactive. You must activate them manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/t\_ActivateProjTaskEmailNot.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Activate project task email notifications

The following email notifications for the Project Management application are available by default, but are inactive. You must activate them manually.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Activate the following notifications:

    |Notification|Table|Field|Condition|Description|
    |------------|-----|-----|---------|-----------|
    |Project task assigned|pm\_project\_task|Assigned to|Inserted or updated|Sends an email notification when a task is assigned to a resource or the assigned resource is changed.|
    |Project task started|pm\_project\_task|State|Changes to **Work in Progress**|Sends an email notification when the project task starts.|
    |Project task commented|pm\_project\_task|Additional comments|Any changes occur|Sends an email notification when the comment field is updated.|


-   **[Set up project notifications with the workflow tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_SetUpProjNotifiWorkflowTool.md)**  
Use the workflow tool, for example, to set up a workflow that sends an email notification when the state of a project task becomes **Work in Progress**.

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

[Change the planned start date of a project]()

[Create a cost type definition]()

[Costing add-on in Project Management]()

[Generate labor costs]()

[Create a project status report]()

[Allocate budget to a project]()

[Migrate budget of active projects to Next Experience]()

[Migrate financial baselines of projects to Next Experience]()


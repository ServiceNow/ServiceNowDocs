---
title: Activate project task email notifications
description: The following email notifications for the Project Management application are available by default, but are inactive. You must activate them manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-business-management/project-management/t\_ActivateProjTaskEmailNot.html
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
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


-   **[Set up project notifications with the workflow tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/project-management/t_SetUpProjNotifiWorkflowTool.md)**  
Use the workflow tool, for example, to set up a workflow that sends an email notification when the state of a project task becomes **Work in Progress**.

**Parent Topic:**[Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/project-management/c_ProjectApplicationOverview.md)


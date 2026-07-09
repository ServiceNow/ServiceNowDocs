---
title: Configure the form view for CWM tasks and connected work items
description: Configure which fields appear when you open a CWM task or connected work item by customizing the default form view for the relevant table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/configure-form-view-for-cwm-tasks.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
breadcrumb: [Configure, Collaborative Work Management, Strategic Portfolio Management]
---

# Configure the form view for CWM tasks and connected work items

Configure which fields appear when you open a CWM task or connected work item by customizing the default form view for the relevant table.

## Before you begin

Role required: admin

## About this task

CWM displays fields from the default view of a table's record form in the task side panel for CWM tasks and connected work items. For stories, CWM uses the CWM view of the form instead of the default view.

## Procedure

1.  Navigate to the list view of the table whose form you want to configure.

    For example, navigate to `incident.list` for the Incident table, `sn_cwm_task.list` for CWM tasks, or `rm_story.list` for stories.

2.  Open any record in the table.

3.  Right-click the form to open the form context menu, and select **View** &gt; **Default view**.

    For stories \(`rm_story`\), select **View** &gt; **CWM view** instead.

4.  Configure the form using Form Builder.

    For instances without Form Builder, use Form Design or Form Layout instead. For more information, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md).

5.  Add or remove the fields you want to display, and save your changes.


## Result

The updated fields appear in the task side panel when you open tasks or connected work items from CWM Boards.

**Related topics**  


[Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md)

[Show or hide fields on a form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md)

[Update details of connected work items in CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/update-details-of-connected-work-items-in-cwm-boards.md)


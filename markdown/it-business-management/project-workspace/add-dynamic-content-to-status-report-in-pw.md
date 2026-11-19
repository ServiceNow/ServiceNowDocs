---
title: Add dynamic content to a status report or docs template
description: Add dynamic content to a status report or a Project Docs template in Project Workspace. The dynamic content gets updated automatically as a change is made to the underlying record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/add-dynamic-content-to-status-report-in-pw.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a status report in Project Workspace, Manage projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Add dynamic content to a status report or docs template

Add dynamic content to a status report or a Project Docs template in Project Workspace. The dynamic content gets updated automatically as a change is made to the underlying record.

## Before you begin

Role required: it\_pps\_admin, it\_project\_manager

## Procedure

1.  Open a project from the home page of Project Workspace.

    For information, see [Access the Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/access-new-project-workspace.md).

2.  Open the Docs template page of the project by selecting **Docs template** from the list.

3.  From **Docs template** page, select the template to open it.

4.  Select **Doc** tab and select at the appropriate place and then type `/` \(forward slash\) to open a list of actions, including **Mention a user** or **Mention a record** or **Insert dynamic content** as required.

    1.  You can type in `/` \(forward slash\) and select **Mention a user** to tag a user.

    2.  You can type in `/` \(forward slash\) and select **Mention a record** to insert a record.

        \[Omitted image "status-report-add-dynamic-content.png"\] Alt text: Mention a record in status report.

        Once you insert a record, it is embedded as a link, which you can click to open the related record and see its details.

    3.  You can type in `/` \(forward slash\) and select **Insert a dynamic content** to insert dynamic content into your status report or Project Docs template.

        \[Omitted image "insert-dynamic-content.gif"\] Alt text: Insert dynamic content option.

        Using the insert dynamic content option, you can configure and view dynamic data such as the status date, project details, and other project fields. This option is only available if the **Is dynamic** field in the Category list for PWS Docs is selected in the Doc template form.

        For example, in a Project Docs template, you can insert a dynamic **Project manager** field. When the template is applied to create a doc, the field is automatically populated with the project manager from that project's details. You can select formatting options such as headings, bullets, and others.

5.  Observe and monitor the report.

    For more information on viewing and analyzing status reports, see [Analyze the status report in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/view-status-report-in-project-workspace.md).


**Parent Topic:**[Create a status report in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/create-a-status-report-in-project-workspace.md)

**Related topics**  


[Status reporting in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/status-reporting-in-pw.md)

[Create a status report or docs template in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/create-a-status-report-template-project-workspace.md)

[Create a status report in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/create-a-status-report-in-project-workspace.md)

[Analyze the status report in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/view-status-report-in-project-workspace.md)

[Duplicate a status report in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/duplicate-status-report-pw.md)

[Import old project status report to Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/import-old-status-reports.md)

[Create document template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/create-new-document-template-form.md)


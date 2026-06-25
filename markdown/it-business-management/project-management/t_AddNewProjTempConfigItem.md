---
title: Add a project template configuration item
description: Add a project template configuration item to include in a template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/t\_AddNewProjTempConfigItem.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Project template configuration, Applying templates to projects, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add a project template configuration item

Add a project template configuration item to include in a template.

## Before you begin

Role required: it\_pps\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Template Config**.

2.  Select **New**.

3.  Fill in the fields on the Project Template Configuration form.

    For more information, see [Project template configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/project-template-form.md).

4.  Select **Submit**.

    For example, to add a requirement object to the project template configuration, fill in the fields as follows:

    -   **Table**: Requirement \[dmn\_requirement\]
    -   **Parent table**: Project \[pm\_project\]
    -   **Link element**: Parent
    -   **Active**: Enable this check box
    -   **Elements**: short\_description, description, priority, type, state

**Parent Topic:**[Project template configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTemplateConfiguration.md)

**Related topics**  


[Applying templates to projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTemplates.md)

[Project template configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTemplateConfiguration.md)


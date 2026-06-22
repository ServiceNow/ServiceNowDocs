---
title: Configure project type fields and layouts
description: Define custom fields and a unique form layout to support configuration independence across different types of projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/configure-project-type-pw.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
keywords: [project type, dynamic category, custom form view, enterprise-wide deployment, EWD]
breadcrumb: [Configure, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure project type fields and layouts

Define custom fields and a unique form layout to support configuration independence across different types of projects.

## Before you begin

-   Identify the dynamic category that defines custom project records fields associated with project type.

    **Note:** If the dynamic category doesn't exist or to create a dedicated dynamic category for a project type, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/configure-form-layout.md).

-   Identify the form view that defines form layout for project records associated with project type.

    **Note:** If the form view doesn't exist or you want to create a dedicated form view for a project type use the **Default SPM Dynamic Namespace** only when defining a dynamic category. For more details, see [Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/create-dynamic-category.md).


Role required: pps\_admin

## About this task

Each project type configuration consists of a dynamic category and a custom form view. The dynamic category defines the custom fields scoped to that project type. The custom form view defines the form layout rendered when that project type is assigned to a record. Custom fields don't appear on records of other project types and don't affect default fields.

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Project types**.

2.  Select **New** to open the project type form.

3.  Fill in the fields on the form.

    For a description of the field values, see [Project type form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/project-type-form-pw.md).

4.  Select **Save** to create and save the project type configuration.


## Result

The project type configuration is saved and activated. Project records assigned to a project type display the custom form view and associated fields. Records assigned to other project types aren't affected.

**Parent Topic:**[Configuring Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/configure-pw.md)


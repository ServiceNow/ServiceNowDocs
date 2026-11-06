---
title: Project type form
description: Learn about the fields on the Project type form of the Project Workspace. Use this form to create a project type for your projects and choose which modules the project type shows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/project-workspace/project-type-form-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 2
breadcrumb: [Form field information for Project Workspace, Project Workspace reference, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Project type form

Learn about the fields on the Project type form of the Project Workspace. Use this form to create a project type for your projects and choose which modules the project type shows.

## Access the project type form

The project type form is separate from the project form. Use it to define your own project type, choose which modules the project shows in Project Workspace, and choose the form view to apply. To open the form, navigate to **All** &gt; **Project Administration** &gt; **Project types** and select **New**. You can also open the Project Type \[project\_type\] table directly.

After you create a project type, select it in the **Project type** field when you create a project. The project opens in Project Workspace with only the modules selected for that type. For more information, see [Project form in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/project-form-pw.md).

|Field|Description|
|-----|-----------|
|Label|Name of the project type configuration.|
|Name|ID of the project type. This field is automatically set to the label value.|
|Description|Enter a brief description explaining the configuration for project type.|
|Table|Project type to configure. Select the type for which you want to define custom fields and a form layout.|
|Dynamic category|Name of the dynamic category associated with this project type. The dynamic category defines the additional fields that appear on the project table alongside the default fields, and is automatically populated when the configuration is saved.|
|Form view|Name of the form view to render when this project type is assigned to a record. The form view is dynamically applied based on the project type. If you don't select a form view, the default view is used.|

|Field|Description|
|-----|-----------|
|Planning|Option to show the Planning module in the Project Workspace menu for projects of this type.|
|Details|Option to show the Details module in the Project Workspace menu for projects of this type.|
|Financials|Option to show the Financials module in the Project Workspace menu for projects of this type.|
|RIDAC|Option to show the RIDAC module in the Project Workspace menu for projects of this type.|
|Resource|Option to show the Resource module in the Project Workspace menu for projects of this type.|
|Analytics|Option to show the Analytics module in the Project Workspace menu for projects of this type.|
|Docs|Option to show the Docs module in the Project Workspace menu for projects of this type.|
|Status Report|Option to show the Status Report module in the Project Workspace menu for projects of this type.|

**Parent Topic:**[Form field information for Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/form-field-information-for-project-workspace.md)


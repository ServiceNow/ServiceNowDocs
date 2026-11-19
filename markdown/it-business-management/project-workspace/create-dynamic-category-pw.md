---
title: Create a dynamic category for a project type
description: Create a dynamic category to define the custom fields that appear on project records of a specific project type in Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/create-dynamic-category-pw.html
release: brazil
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 2
keywords: [dynamic category, dynamic attribute, custom fields, project type, enterprise-wide deployment, EWD]
breadcrumb: [Configuring project types in Project Workspace, Configuring Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a dynamic category for a project type

Create a dynamic category to define the custom fields that appear on project records of a specific project type in Project Workspace.

## Before you begin

The custom fields that projects of the project type require, and the data type of each field, must be identified.

Role required: admin

## About this task

A dynamic category groups the dynamic attributes that appear as custom fields on project records. When you assign the dynamic category to a project type, project managers can view and update those fields in Project Workspace and in playbooks for projects of that type. A category can have a parent category, and it inherits the attributes of its parent.

## Procedure

1.  Navigate to **All** &gt; **Enterprise-Wide Deployment** &gt; **SPM Dynamic Categories**.

    The Default SPM Dynamic Namespace record opens.

2.  Select the Dynamic Categories related list.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Namespace|Namespace that the dynamic category belongs to. This field is automatically set to Default SPM Dynamic Namespace.|
    |Label|Display name of the dynamic category. Use a name that identifies the project type that the category supports.|
    |Parent|Parent category whose attributes this category inherits. Leave this field empty to create a top-level category.|
    |Name|Unique system name of the dynamic category.|
    |Description|Brief description of the custom fields that the dynamic category provides.|

5.  Select **Submit**.

6.  Open the dynamic category and add the dynamic attributes that define its custom fields.

    Supported data types are String, Boolean, Date, Date/Time, Integer, Decimal, Floating point, Choice, and Reference. For a Choice attribute, select the choice set that provides its values. To create a dynamic attribute, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md).


## Result

The dynamic category is available for project type configurations. Projects assigned to a project type that uses this category show its custom fields in Project Workspace and in playbooks.

## What to do next

Associate the dynamic category with a project type. For more information, see [Configure project type fields and layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configure-project-type-pw.md).

**Parent Topic:**[Configuring project types in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configuring-project-types-pw.md)

**Related topics**  


[Project types in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/project-types-in-pw.md)

[Configure project type fields and layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configure-project-type-pw.md)


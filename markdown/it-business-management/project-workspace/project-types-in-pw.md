---
title: Project types in Project Workspace
description: Administrators can define custom fields, a form view, and visible modules for each project type in Project Workspace without affecting default settings or other project types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/project-workspace/project-types-in-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Explore, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Project types in Project Workspace

Administrators can define custom fields, a form view, and visible modules for each project type in Project Workspace without affecting default settings or other project types.

Project types require the SPM Enterprise-Wide Deployment \(EWD\) application \(sn\_spm\_ewd\). Starting with Project Workspace version 7.3.0, the application is installed automatically.

Each project type configuration consists of three components: dynamic category, form view, and module visibility.

-   **Dynamic category**

    Defines the custom fields for a specific project type. A dynamic category belongs to the Default SPM Dynamic Namespace and groups the dynamic attributes that appear as custom fields on project records of that type. Custom fields are scoped to a specific type and don't appear on records of other types or affect default fields.

    -   A dynamic category can have a parent category. A child category inherits the attributes of its parent, so you can define shared fields once and add type-specific fields in each child category.
    -   Custom fields support the String, Boolean, Date, Date/Time, Integer, Decimal, Floating point, Choice, and Reference data types.
    -   Project managers view and update custom fields in Project Workspace and in playbooks for projects of that type.
    For details, see .

-   **Form view**

    Defines a unique form layout for each project type. The form view is dynamically rendered based on the project type assigned to a record.

-   **Module visibility**

    Defines which modules appear in the Project Workspace menu for projects of a specific type. You can show or hide the Planning, Details, Financials, RIDAC, Resource, Analytics, Docs, and Status Report modules. All modules are shown by default, and projects without a project type show all modules. Role-based access still applies: users need the required role to access a shown module.


You can set the project type of a project only once. After the project type is set, you can't change it.

## Project types and partitions

EWD partitions and project types are two independent, complementary layers. Partitions control who can see a project and its dashboards. Project types control what a project looks like and how it's navigated after you have access to it. Partitions don't determine the form fields, form layout, or modules of a project. Those are controlled by the project type. For the full EWD concept, see [Exploring SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/explore-ewd.md).

The Project \[pm\_project\] table is one of the tables EWD supports for partitioning. You define a partition criteria field on the Project table, such as **Department**, and create a partition for each value. When a project is created, it's automatically assigned to the partition that matches its criteria field. A user then sees only the projects that belong to a partition their role grants them access to, across Project Workspace, list views, search results, and dashboards. For the full list of supported tables, see [Supported tables for partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/supported-tables-for-partition-ewd.md).

When partitions and project types are both configured, a user sees:

-   Only the projects that belong to their assigned partitions, in list views, search results, and dashboards.
-   For each of those projects, only the modules that are shown for the project's type, subject to role-based access.
-   The custom fields and form layout defined for the project's type.

**Parent Topic:**[Exploring Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/exploring-project-workspace.md)

**Related topics**  


[Configure project type fields and layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-workspace/configure-project-type-pw.md)

[create-dynamic-category-pw]

[Install SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/install-ewd.md)


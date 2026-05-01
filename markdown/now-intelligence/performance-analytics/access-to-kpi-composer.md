---
title: Access to KPI Composer
description: The level of access to KPI Composer determines whether a user can create, edit, or only view a KPI Composer project. It also determines which projects a user can access and whether they can access the underlying records or only the UI.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Access to KPI Composer

The level of access to KPI Composer determines whether a user can create, edit, or only view a KPI Composer project. It also determines which projects a user can access and whether they can access the underlying records or only the UI.

Access to KPI Composer depends on the following things, singly or in combination:

-   User role
-   Responsibility
-   Access granted during sharing

## Role-based access

An admin can grant a user the role of a KPI Composer admin or user. A KPI Composer admin has the same privileges as a ServiceNow AI Platform admin for KPI Composer. A KPI Composer user does not automatically have access to all projects and cannot associate indicator or breakdown definitions with actual Performance Analytics entities.

<table id="table_wcd_bly_vjb"><thead><tr><th>

Role

</th><th>

Contains

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_kpi\_composer.admin or admin

</td><td>

pa\_viewer

</td><td>

-   Full access to all components of KPI Composer, including records.
-   Full access to all projects.
-   Can share or assign responsibility for projects.
-   Can associate indicator and breakdown definitions with Performance Analytics indicators and breakdowns.

</td></tr><tr><td>

sn\_kpi\_composer.user

</td><td>

None

</td><td>

-   Can access only projects that they have created.
-   Can share or assign responsibility for projects they create.
-   Can access only the design tabs, artifact properties, indicator definitions, and breakdown definitions of those projects.
-   Cannot add Performance Analytics indicators or breakdowns to the respective definitions.

 A user with this role may have access to more projects based on responsibility or on projects being shared with them.

</td></tr></tbody>
</table>The appropriate Performance Analytics roles are also necessary to implement KPI Composer designs in Performance Analytics.

## Responsibility for projects

A responsible user has the following access to the projects they are responsible for:

-   Can view and edit the projects.
-   Can share or assign responsibility for the projects.
-   Can access only the design tabs, artifact properties, indicator definitions, and breakdown definitions of those projects.
-   Cannot add Performance Analytics indicators or breakdowns to the respective definitions.

This level of access is equivalent to what the sn\_kpi\_composer.user role grants. It is also equivalent to having a project shared with edit rights. Responsibility differs first in being independent of any role. The second difference is procedural, not technical: Responsible users are understood to be in charge of oversight and implementation of the project. Even the creator of a project is therefore not automatically responsible for it.

Responsible users are named in the project properties. Any user with edit rights can name responsible users. For more information about naming responsible users, see [Define properties for a project](../task/define-properties-project.md).

## Shared projects

Any user with edit rights can share a project. When you share a project, you grant one of two levels of access:

-   **Edit access**

    This level of access is technically the same as the access of a responsible user, or a user with the sn\_kpi\_composer.user role. The first difference is that no role is required. The second difference is that there is no implication of responsibility to oversee or implement the project.

-   **View access**

    A user with view access can read the design tabs, artifact properties, indicator definitions, and breakdown definitions of the shared project. They can use all viewing utilities, like search and filter. However, they cannot change anything in the project. The only thing they can add is a journal entry.


For more information, see [Share a KPI Composer project](../task/share-a-kpi-composer-project.md).

**Parent Topic:**[Design your Performance Analytics solution with KPI Composer](designing-pa-solution.md)


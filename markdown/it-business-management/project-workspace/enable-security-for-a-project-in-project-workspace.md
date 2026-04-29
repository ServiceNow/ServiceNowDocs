---
title: Enable security for a project in Project Workspace
description: Enable security in a project to make the project confidential to ensure that only authorized users can access the project and its related sub projects and entities.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring security for a project in Project Workspace, Configuring Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Enable security for a project in Project Workspace

Enable security in a project to make the project confidential to ensure that only authorized users can access the project and its related sub projects and entities.

## Before you begin

Install the Project Advanced Security plugin.

Role required: admin

## Procedure

1.  Open a project from the home page of Project Workspace.

    For information, see [Access the new Project Workspace](access-new-project-workspace.md).

2.  Open the Details page of the project by selecting **Details** from the list.

3.  Scroll down all the way to locate **Confidential** and select it.

4.  In the following fields, specify the users and user groups that can access the project.

    |Field|Description|
    |-----|-----------|
    |**Allowed users**|Enter names of specific users you want to allow access to the project.|
    |**Allowed groups**|Enter user groups you want to allow access to the project.|

    You need to specify at least one user or user group for access.

    The confidential project can be accessed by **Allowed users**, **Allowed groups**, the **Assigned to** user, **Additional assignee**, the **Project Manager**, and the administrator.

5.  Select **Save**.

    Once you make the project confidential, the confidentiality setting is applied to the project, all sub projects, and entities such as cost plans, cost plan breakdowns, benefit plans, benefit plan breakdowns, expense lines, time cards, status reports, baselines, story, investment object, project tasks, resource plan, resource assignments, and RIDAC.

    These will only be accessible to individuals who have been explicitly added to the project.

    This setting applies to all associated workspaces. If the project is marked confidential in one workspace, it is automatically made confidential across all other workspaces, including:

    -   Project Management Workspace
    -   Resource Management Workspace
    -   Strategic Portfolio Workspace

**Parent Topic:**[Configuring security for a project in Project Workspace](../concept/configuring-security-for-a-project-in-pw.md)

**Related topics**  


[Configuring security for a project in Project Workspace](../concept/configuring-security-for-a-project-in-pw.md)


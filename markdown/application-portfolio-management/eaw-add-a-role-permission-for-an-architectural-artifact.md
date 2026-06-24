---
title: Add a role permission for an architectural artifact
description: Role permissions refer to the access rights assigned to different roles to create, view, or edit architectural artifacts. These permissions enable only users having the authorized role to perform any actions on architectural artifacts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-portfolio-management/eaw-add-a-role-permission-for-an-architectural-artifact.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage architectural artifacts, Working with information portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add a role permission for an architectural artifact

Role permissions refer to the access rights assigned to different roles to create, view, or edit architectural artifacts. These permissions enable only users having the authorized role to perform any actions on architectural artifacts.

## Before you begin

**Important:** Starting from Xanadu Patch 4 release, the **Role Permissions** tab has been deprecated from Enterprise Architecture Workspace. However, you can still manage access permissions for architectural artifacts using the **Share** feature. For more information, see [Manage access to architectural artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/eaw-manage-access-to-architectural-artifacts.md).

Role required: All users with **Writer** permission assigned.

## About this task

You can create role permissions and associate them with architectural artifacts. Based on your existing role, you can provide certain role permissions.

-   If you’re the owner of the architectural artifact, you can provide **Reader**, **Writer**, and **Owner** role permission to other users.
-   If you’re assigned the **Writer** role permission to an architectural artifact, you can provide **Writer** or **Reader** role permission to other users.
-   If you’re assigned the **Reader** role permission to an architectural artifact, you can’t provide any role permission to other users.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon \[Omitted image "portfolio-icon.png"\] Alt text: Portfolio icon.

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Information Portfolio**.

4.  Select **Architectural Artifacts**.

5.  Select the architectural artifact that you want to associate role permissions with.

    A new page appears and the details of the architectural artifact are displayed.

6.  Select the **Role Permissions** tab.

7.  Select **New**.

8.  On the form, fill in the fields.

    For a description of the field values, see [Create new role permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/eaw-create-new-role-permissions.md).

9.  Select **Save**.


**Parent Topic:**[Manage architectural artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-portfolio-management/eaw-managing-architectural-artifacts.md)


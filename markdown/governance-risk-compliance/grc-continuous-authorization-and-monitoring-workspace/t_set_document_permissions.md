---
title: Set document permissions
description: Grant users and roles access to documents by assigning permissions at the role, user, group, or criteria level. Permissions control whether users can view, edit, or own documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_set\_document\_permissions.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [document permissions, access control, role permissions, user permissions]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Set document permissions

Grant users and roles access to documents by assigning permissions at the role, user, group, or criteria level. Permissions control whether users can view, edit, or own documents.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_user

In general, any role with write access to the record can add, edit, or modify the docs.

**Note:** You can add documents only when the record is in an active state. Inactive records don't allow changes to linked documents.

## About this task

Assign access to documents at the level that fits your organization. You can grant permissions to everyone in a role or a group. Alternatively, you can assign access to specific team members, or anyone who meets particular requirements.

## Procedure

1.  In the **Documents** panel, select the document and select **Manage Permissions**.

    The Manage permissions dialog opens, showing sections for role permissions, user permissions, group permissions, and user criteria permissions.

2.  To assign permissions by role, expand the **Role Permissions** section and select **New**.

    Complete the following steps in the New Role Permission section:

    1.  In the **User Role** field, enter or search for the role that should have access to the document.

        Available roles appear as you type. Select the role from the dropdown list.

    2.  In the **Permission** dropdown, select the access level: **Reader**, **Writer**, or **Owner**.

        Permission levels control what users with the specified role can do with the document:

        -   **Reader:** View the document only
        -   **Writer:** View the document and create new versions
        -   **Owner:** Full control including viewing, editing, versioning, and managing permissions
    3.  Select **Save** to grant this role access to the document.

3.  To grant permissions to specific users instead of roles, expand the **User Permissions** section and select **New**.

    Complete the following steps in the New User Permission section:

    1.  In the **User** field, enter or search for the user that should have access to the document.

    2.  In the **Permission** dropdown, select the access level: **Reader**, **Writer**, or **Owner**.

    3.  Select **Save** to grant this role access to the document.

4.  To grant permissions to a specific group, expand the **Group Permissions** section and select **New**.

    Complete the following steps in the New Group Permission section:

    1.  In the **Group** field, enter or search for the role that should have access to the document.

    2.  In the **Permission** dropdown, select the access level: **Reader**, **Writer**, or **Owner**.

    3.  Select **Save** to grant this group access to the document.

5.  To grant permissions based on criteria \(for example, all members of a group or employees in a department\), expand the **User Criteria Permissions** section and select **New**.

    Complete the following steps in the New User Criteria Permission section:

    1.  In the **User Criteria** field, search for the criteria.

    2.  In the **Permission** dropdown, select **Reader**, **Writer**, or **Owner**.

    3.  Select **Save** to apply this criteria-based permission.

        The criteria permission is added. Any user matching the specified criteria now has the assigned permission level for the document.


## Result

Document permissions are now configured. Users and roles can access the document according to their assigned permission levels. Role-based permissions apply to all users with that role, user permissions apply to specific individuals, and criteria-based permissions apply to users matching the specified conditions.

**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)


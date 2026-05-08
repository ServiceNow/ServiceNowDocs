---
title: Collaborate with other developers
description: In App Engine Studio \(AES\), you can add or remove users and groups to be collaborators on an application.Give users or groups permission to collaborate with other developers in App Engine Studio \(AES\) using the Collaboration feature.Change the permissions that are assigned to a collaborator or create a custom collaboration permission to enable what people can do in App Engine Studio \(AES\).Collaboration permissions define what users can do in App Engine Studio \(AES\).Remove users and groups from collaboration to restrict them from owning or editing an app.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Collaborate with other developers

In App Engine Studio \(AES\), you can add or remove users and groups to be collaborators on an application.

Users have varying levels of permissions for actions on the Collaboration feature. At a high level:

<table id="table_lyw_dms_5qb"><thead><tr><th>

Users with these permissions

</th><th>

Can perform these actions

</th></tr></thead><tbody><tr><td>

Manage Collaborators delegated development permission to the application

</td><td>

Can:

-   See a list of collaborators and their descriptors
-   Search for users or groups
-   Select or change the collaboration descriptor for a user or group \(but users can't change customized users or groups\)
-   Add collaborators by sending invitations
-   Remove users or groups \(but users can't remove customized users or groups\)

 Can't:

-   Customize permissions for a user or group
-   Deploy via update sets

</td></tr><tr><td>

Invite Collaborators delegated development permission to the application

</td><td>

Can:

-   See a list of collaborators and their descriptors
-   Search for users or groups
-   Add collaborators by sending invitations

 Can't:

-   Select or change the collaboration descriptor for a user or group
-   Remove users or groups
-   Customize permissions for a user or group

</td></tr><tr><td>

No Collaborator-related roles to the application

</td><td>

Can see a read-only list of collaborators and their descriptors.

 Can't:

-   Search for users or groups
-   Select or change the collaboration descriptor for a user or group
-   Add collaborators by sending invitations
-   Remove users or groups
-   Customize permissions for a user or group

</td></tr><tr><td>

Administrators

</td><td>

Admins must elevate to a security\_admin role to work with collaboration features. For more information, see Elevated privilege roles.

Administrators can:

-   See a list of collaborators and their descriptors
-   Show/hide members of a group
-   Search for users or groups
-   Select or change the collaboration descriptor for a user or group \(includes changing customized users or groups and changing the owner\)
-   Add collaborators by sending invitations
-   Remove users or groups \(includes removing customized users and groups and removing the owner even if there is only one owner\)
-   Customize permissions for a user or group

</td></tr></tbody>
</table>**Note:** You should create collaboration descriptors in addition to Owner and Editor in the global scope. If you want collaboration descriptors to appear and be used in AES, you should also set them to `standard = TRUE`. AES doesn't support collaboration descriptors that are created in custom scopes, and non-standard collaboration descriptors don't render in AES.

When you add a user or group, a collaboration task is generated and an approval flow kicks off. To find all collaboration tasks, navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Collaboration Tasks**. The collaboration task provides information on which application a developer is being added to, and what permissions are granted. Approvers sometimes need to review these task records before they add developers to the application.

If you're an admin, you can modify the Collaboration Request flow. The base system Collaboration Request flow handles collaboration requests as follows:

-   If the user has AES or delegated developer permissions and isn't new to the platform, the collaboration request approval record is auto-approved.
-   If the user does not have AES or delegated developer permissions and is new to the platform, approval is required.

If you're an admin, you can modify the collaboration descriptors that developers use to assign delegated development permissions. The base table provides Owner and Editor collaboration descriptors. By default, Owners have the manage collaborator delegated development permission set, and Editors have the invite collaborator delegated development permission set.

**Note:** If you’re using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app that’s linked to Git, the new flow won’t be available in the app for other AES users until the admin checks the flow into Git.

**Parent Topic:**[Building apps in App Engine Studio](aes-app-creation.md)

## Add a user or group to collaboration

Give users or groups permission to collaborate with other developers in App Engine Studio \(AES\) using the Collaboration feature.

### Before you begin

Role required: admin, manage collaborator delegated development role, or invite collaborator delegated development role

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select the Manage collaborators ![Manage Collaborators button](../image/aes-manage-collaborators-purple.png) button.

    ![Add collaborators in App Engine Studio](../image/aes-add-collaborator-purple.png "Collaborate with others")

4.  To add another user or group as a collaborator, enter the user name or group name in the **Invite people by name or group** field.

5.  Search for a specific user or group by entering the first few characters of the name.

    A drop-down list with matching user names and groups appears where you can select the user or group you want to add. If a user or group appears in the drop-down list but you can't select it, it's already been added as a collaborator and can't be re-selected.

6.  Select the collaboration descriptor for the user or group that you're adding.

    For a list of collaboration permissions, see [Delegated development and collaboration permissions](aes-collaboration-feature-overview.md#).

    **Note:** Users with Invite Collaborators permissions can't do this, and will default to the Editor option.

    Only App Collaboration Descriptors that are defined in the global scope and have the standard option selected appear in the list.

7.  Select **Send**.

    -   If the user has AES or delegated developer permissions and is new to the platform, the user is listed under the pending requests section and approval is required. After the request is approved, both the requester and the user receive an email indicating that the user has been added to the application. ![Collaboration approval email example](../image/aes-approval-email-purple.png)
    -   If the user has AES or delegated developer permissions and is not new to the platform, the collaboration request is auto-approved. Both the requester and the user receive an email indicating that the user has been added to the application.
    **Note:** If a valid controller has been configured on the instance from which the collaboration request originated, a collaboration request task is created on the controller instance. If the originating instance isn't configured on the controller, work notes are automatically added to the request record indicating that the instance must be configured before approval is granted. If the originating instance is the controller or a valid controller has not been configured, the collaboration request task is created on the requesting instance. For more information, see [Configure your controller instance](../../pipelines-and-deployments/task/config-controller-instance.md).


## Change collaborator permissions

Change the permissions that are assigned to a collaborator or create a custom collaboration permission to enable what people can do in App Engine Studio \(AES\).

### Before you begin

Role required: admin or manage collaborator delegated development role

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select the Manage collaborators ![Manage Collaborators button](../image/aes-manage-collaborators-purple.png) button.

4.  For the user or group you want to change, select a different collaborator descriptor from the drop-down list.![Select a new collaboration descriptor for this user](../image/aes-collaborator-set-permissions-purple.png)

    Customized users and groups are not editable by non-admins.

5.  Admin only: Create custom collaboration permissions for specific users in an application.

    1.  In AES, select **Customize Permissions** from the drop-down list across from the user's name.

    2.  Select or clear delegated development permissions for the user or group.

        For a list of collaboration permissions, see [Delegated development and collaboration permissions](aes-collaboration-feature-overview.md#).

    If the selection matches that of another standard Collaboration descriptor, the system will provide a prompt before proceeding. For details on each delegated development permission, see [Delegate development and deployment permissions to personnel](../../applications/task/t_AddADeveloper.md).

6.  Select **Save**.


## Delegated development and collaboration permissions

Collaboration permissions define what users can do in App Engine Studio \(AES\).

### File type access permissions

File type access permissions grant access to application file types.

<table id="table_zyz_3tl_bwb"><thead><tr><th>

Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All file types

</td><td>

Grants access to collaborate on all file types.**Note:** This option includes access to additional file types not listed in separate permissions.

</td></tr><tr><td>

Integrations

</td><td>

Grants access to web service APIs, REST APIs, data sources, and Integration Hub - Import.

</td></tr><tr><td>

Reporting

</td><td>

Grants access to reports and scheduled reports.

</td></tr><tr><td>

Mobile builders

</td><td>

Grants access to build mobile experiences, such as with Mobile App Builder.

</td></tr><tr><td>

UI Builder

</td><td>

Grants access to work with UI Builder to build more complex interfaces.

</td></tr><tr><td>

Workflow

</td><td>

Grants access to the Workflow Editor and Activity Creator.

</td></tr><tr><td>

Service Portal

</td><td>

Grants access to work with Service Portal editors and tools.

</td></tr><tr><td>

Workflow Studio

</td><td>

Grants access to the Flows design environment in Workflow Studio to create flows and actions. Script action steps require the **Allow Scripting** permission.

</td></tr><tr><td>

Service Catalog

</td><td>

Grants access to work with catalog-related file types such as catalog items, record producers, and variables to add catalog items to apps.

</td></tr><tr><td>

Tables and forms

</td><td>

Grants access to model and layout-related file types such as table columns, form layout, and list layout.

</td></tr><tr><td>

Playbooks

</td><td>

Grants access to work with the Playbooks design environment to create processes. Editing activity subflows or actions requires the **Flow Designer** permission.

</td></tr><tr><td>

Decision Tables

</td><td>

Grants access to work with Decision Tables to create decision logic based on multiple if-then rules.

</td></tr><tr><td>

Notifications

</td><td>

Grants access to create automatic email notifications in apps.

</td></tr></tbody>
</table>### Security/Entitlement permission

The **Manage ACLs and Roles** permission grants access to security management files, such as Access Control Lists and roles.

### Programming tools permission

The **Allow scripting** permission grants access to script fields, such as scripting in business rules, UI actions, and client scripts.

### Application management permissions

The application management permissions grant access to basic app management functions, like managing collaborators.

|Permission|Description|
|----------|-----------|
|Delete application|Grants the collaborator within a scoped app rights to delete the application.|
|Manage collaborators|Grants access to manage and invite collaborators for apps.|
|Source control|Grants full access to use source control.|
|Invite collaborators|Grants access to invite developers to collaborate on an app.|

### Deployment permissions

The deployment permissions grant access to installing, upgrading, and publishing apps.

|Permission|Description|
|----------|-----------|
|Upgrade app|Grants access to upgrade the associated application after it has been installed in the current instance.|
|Submit for deployment|Grants access to submit the associated application for review and deployment.|
|Publish to app repo|Grants access to publish the associated application to the application repository in the current instance.|
|Publish to app store|Grants access to publish the associated application to the ServiceNow Store in the current instance.|

## Remove a user or group from collaboration

Remove users and groups from collaboration to restrict them from owning or editing an app.

### Before you begin

Role required: admin or manage collaborator delegated development role

### About this task

You can remove the final owner and editor for an app. If an app doesn't have any owners and needs one, an admin must add them.

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select the Manage collaborators ![Manage Collaborators button](../image/aes-manage-collaborators-purple.png) button.

    The Collaborate with others modal appears with a list of the current collaborators.

4.  To remove a user or group as a collaborator, select **Remove** from the drop-down list. ![Remove a collaborator](../image/remove-collaborator-purple.png)



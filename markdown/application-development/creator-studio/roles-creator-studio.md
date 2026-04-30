---
title: Creator Studio roles and personas
description: Roles control what everyone you work with can do in Creator Studio. Administrators assign roles to give team members permission to configure or use Creator Studio.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio roles and personas

Roles control what everyone you work with can do in Creator Studio. Administrators assign roles to give team members permission to configure or use Creator Studio.

The two roles for Creator Studio are used to restrict access from creating new apps, which helps make sure your instance isn't overfilled with redundant, unplanned, or unused apps.

## Personas that use Creator Studio

Personas aren’t explicitly part of Creator Studio, but administrators assign roles to give team members permission to configure or use Creator Studio.

-   **Low-code/citizen developer**

    Low-code/citizen developers are tech savvy and interested in creating apps. Though they might not have formal coding or app development training, citizen developers can submit ideas for new apps and, if approved, build them using Creator Studio.

    Low-code/citizen developers have either the sn\_creatorstudio.user or sn\_creatorstudio.restricted\_user role.

-   **App Engine admin**

    App Engine admins manage all processes related to app development in Creator Studio. They review new app ideas, handle app deployment, and manage collaborators, usually in the App Engine Management Center.

    App Engine admins have the app\_engine\_admin role and must be in the app\_engine\_admin group.

-   **Security admin**

    The security admin creates and modifies roles and access control lists for apps. This role is set on the platform level, and it is required for making updates to roles in Creator Studio.

-   **System administrator**

    The system administrator has access to all system features, functions, and data, regardless of security constraints. Grant this privilege carefully. If you have sensitive information, such as HR records, that you must protect, create a custom admin role for that area and train a person who is authorized to see those records to act as the administrator.


## Roles and what they can do in Creator Studio

In addition to the roles in the following table, users with the admin and delegated\_developer roles can also access Creator Studio.

For complete details on which roles each role contains, see [Components installed with Creator Studio](creator-studio-components-installed.md).

<table id="table_zbp_qgq_h1c"><thead><tr><th>

Role

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creator Studio User

</td><td>

sn\_creatorstudio.user

</td><td>

-   Users can create apps in Creator Studio.
-   The user is automatically delegated as the app owner. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).
-   Contains sn\_g\_app\_creator.app\_creator.

 **Note:** This role gets assigned the delegated\_developer role when they create or get access to an app.

</td></tr><tr><td>

Creator Studio Restricted User

</td><td>

sn\_creatorstudio.restricted\_user

</td><td>

-   Users can't create apps in Creator Studio.
-   Users can request apps to be created for them, and to work on an app.
-   Users can work on apps that they've been designated as developers for.
-   When assigned to work on an app, this user gets the delegated\_developer role for that app.

</td></tr><tr><td>

App Engine Admin

</td><td>

app\_engine\_admin

</td><td>

-   Approve requests from restricted users to create an app.
-   Approve collaboration requests.
-   Contains sn\_creator\_studio.admin\_write and sn\_creator\_studio.basic\_write to enable admins to see the apps they need to approve.

</td></tr></tbody>
</table>**Note:**

To ensure that users can use the Collaboration Approval Workflow regardless of instance versions, admins must assign the catalog \_builder\_editor role to Creator Studio user groups.

## User groups and what they can do in Creator Studio

Groups are a standard functionality that help you quickly control people's access to Creator Studio by adding them to a group.

<table id="table_dgw_vjq_h1c"><thead><tr><th>

Group

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creator Studio Users

</td><td>

-   Users are automatically approved to create apps in Creator Studio.
-   Contains sn\_creatorstudio.user.

</td></tr><tr><td>

Creator Studio Restricted Users

</td><td>

-   Users in this group need to request applications be created in Creator Studio on their behalf.
-   Contains sn\_creatorstudio.restricted\_user.

</td></tr></tbody>
</table>## Developer roles and testing apps on instances

If you have a Creator Studio role of sn\_creatorstudio.user or sn\_creatorstudio.restricted\_user, you won't be able to test the apps you build on the non-production instance's Request App Workspace. You should be able to test the app on the non-production instance using Creator Studio's app previews. You will be able to test the apps as a fulfiller in the workspace on the app that's been deployed to production.

**Use case:**

Let's say that a user is in the Creator Studio Users group, so when that user builds an app, that user gets delegated development permissions for that app. That user can then publish a request form, and if there are no roles required for the form, that user can submit requests with the form.

However, that user won't be able to fulfill requests or access the Request App Workspace because that user won't have the x\_acme\_user\_app.agent role, and that user can't give that role to themself. Administrators must assign additional roles as necessary.

## Collaboration roles and instances on different versions

As admins implement Creator Studio, they may have it installed on a non-production instance while their production instance is on a previous version of the ServiceNow AI Platform that doesn't have Creator Studio. This mis-match of instance versions affects the Collaboration Approval Workflow, which specifies the non-production instance as the source and the production instance as the controller. If the controller doesn't have the version of the collaboration plugin that supports Creator Studio, collaboration is unsupported.

To ensure that users can use the Collaboration Approval Workflow regardless of instance versions, admins must assign the catalog \_builder\_editor role to Creator Studio user groups.

## Roles and app development collaboration

Roles define user access to Creator Studio. Permission to work on individual apps is controlled on an app-by-app basis. That is, you must manage the collaborators for each app by inviting other citizen developers to work on the app with you, or request to join someone else's app. For more information, see [Collaboration in Creator Studio](creator-studio-collaboration-roles.md).

**Parent Topic:**[Configuring Creator Studio](../concept/configuring-creator-studio.md)


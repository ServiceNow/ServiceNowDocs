---
title: Collaborating on apps using ServiceNow Studio
description: You can collaborate, or share app development in ServiceNow Studio with other people in your company.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Collaborating on apps using ServiceNow Studio

You can collaborate, or share app development in ServiceNow Studio with other people in your company.

## Collaboration is delegated development

Collaboration, also referred to as delegated development, builds on the existing delegated development feature set in the ServiceNow AI Platform. It enables developers to invite other developers into apps so that they can co-create and develop the app together. Depending on your permissions, you can invite others to collaborate on an app with you, or request to join someone else's app. For more information on delegated development, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

There are two standard types of collaborators when you co-develop an app with other people: owners and editors. Admins can create a custom collaboration role by adjusting permissions.

## Requirements for collaboration

ServiceNow Studio supports the collaboration plugin for properly licensed customers.

**Note:**

1.  You must have an App Engine Enterprise license to take full advantage of collaboration.
2.  If you already have the collaboration plugin installed, you can continue to use collaboration.
3.  Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

## Apps that you can access

The two ServiceNow Studio roles that can access ServiceNow Studio, admin and delegated\_developer, have different access to apps:

-   Users with the admin role automatically have access to all apps in ServiceNow Studio.
-   Users with the delegated\_developer role have access to:
    -   Apps they create.
    -   Apps they've been invited to edit \(as an editor on the app\).
    -   All apps within the scope you have access to. For more information on scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

If you know of an app that you want to work on but don't see it in ServiceNow Studio, contact your admin and ask that they give you permission to work on the app using the Collaboration app. The ServiceNow AI Platform Collaboration app is automatically installed with ServiceNow Studio. For more information about the Collaboration app, see [Application collaboration](../../applications/concept/application-collaboration.md).

## What app owners and editors can do

There are two default collaborator roles for working on apps with other developers: owner and editor.

-   If you create an app, you're the owner of that app.
-   If you see an app in ServiceNow Studio that you've been delegated to work on, you can open it and begin working on it with whatever collaboration role the owner assigned you. That role is usually editor.

<table id="table_p2r_v4r_m1c"><thead><tr><th>

Descriptor

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner

</td><td>

Owner of the application.-   If you created the app, you're automatically the owner.
-   Owners can manage other collaborators for the app.
-   Owners can delete apps because they have the delete app permission.
-   Owners automatically get the delegated\_developer role for the app.

</td></tr><tr><td>

Editor

</td><td>

-   Editors can invite collaborators.
-   Editors have a more limited ability to edit the app.

</td></tr></tbody>
</table>**Note:** For the full list of default owner and editor collaborator collaboration type permissions, see [Collaboration permissions for ServiceNow Studio](../reference/servicenow-studio-collab-permissions.md).

## Custom collaboration descriptors and permissions

The collaboration descriptor that someone is assigned determines if they can assign, manage, and monitor delegated development permissions. For example, people who are owners can do more than people with the editor collaboration descriptor.

If you want to create a customized collaboration role for help building your app, you can create a custom collaboration descriptor, which is a customized collaboration role. You then use collaboration permissions to control what developers \(or users who deploy applications\) can do in the app.

If needed, admins can define custom collaboration descriptors to select when managing collaborators using the Collaboration app. For more information on custom descriptors, see [Create collaboration descriptors to assign permissions](../../applications/task/create-collaboration-descriptors.md).

## Managing collaboration permissions for other developers

If you invite someone to collaborate on an app and they don't have the Delegated developer \(delegated\_developer\) role, an App Engine admin must approve the collaboration request. For more information, see [Delegated development and deployment](../../applications/concept/c_DelegatedDevelopment.md).

When you add a user or group to collaborate on an app, a collaboration task is generated behind the scenes, which initiates an approval flow. If you have App Engine Management Center \(AEMC\) installed, your admin can review and approve/deny these collaboration request tasks there. The collaboration task that goes to your admin provides information on which app a developer is being added to, and what permissions they get. Admins and approvers sometimes need to review these task records before they add developers to the application.

If you don’t have AEMC installed, admins can navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Collaboration Tasks**.

-   **[View collaborators on an app in ServiceNow Studio](../task/view-app-collabs-servicenow-studio.md)**  
View the collaborators for an app to see who is co-developing the app in ServiceNow Studio.
-   **[Add collaborators to an app in ServiceNow Studio](../task/add-collabs-app-servicenow-studio.md)**  
Invite other people to work on an app with you in ServiceNow Studio, collaborating as co-developers.
-   **[Modify or customize collaboration permissions for a user or group in ServiceNow Studio](../task/modify-collab-descriptor-servicenow-studio.md)**  
Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.
-   **[Remove collaborators from an app in ServiceNow Studio](../task/remove-collaborators-servicenow-studio.md)**  
Restrict a user or group from working on an app in ServiceNow Studio by removing them as a collaborator.

**Parent Topic:**[Configuring ServiceNow Studio](configuring-servicenow-studio.md)


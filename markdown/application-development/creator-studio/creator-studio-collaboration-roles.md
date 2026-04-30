---
title: Collaborating with others to build apps in Creator Studio
description: Sometimes you need help with building out your app, and that’s OK! And sometimes other people need your help building their apps, which is great! This point is where collaboration comes into play.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [app collaboration, collaboration, delegated development]
breadcrumb: [Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Collaborating with others to build apps in Creator Studio

Sometimes you need help with building out your app, and that’s OK! And sometimes other people need your help building their apps, which is great! This point is where collaboration comes into play.

You can collaborate on apps you don't own by requesting permission to edit them, and invite other people you work with to collaborate on your apps with you.

Collaboration, also referred to as [delegated development](../concept/creator-studio-glossary.md#), builds on the existing delegated development feature set in the ServiceNow AI Platform. It enables developers to invite other developers into apps so they can co-create and develop the app together. Depending on your permissions, you can invite others to collaborate on an app with you, or request to join someone else's app.

**Note:** You must have an App Engine Enterprise license to take full advantage of collaboration.

The ServiceNow AI Platform Collaboration app is automatically installed with Creator Studio. For more information about the Collaboration app, see [Application collaboration](../../applications/concept/application-collaboration.md).

## Collaboration descriptors: Owners and Editors

So, you realize you either need help with your app, or you want to help someone else build their app. What’s next? You need the appropriate collaboration role.

There are two standard types of collaborators when you co-develop an app with other people: Owners and Editors. These two roles are called [collaboration descriptors](../concept/creator-studio-glossary.md#). The collaboration descriptor that someone is assigned determines if they can assign, manage, and monitor delegated development permissions. For example, people who are Owners can do more than people with the Editor collaboration type.

If needed, your admin can define custom collaboration descriptors to select when managing collaborators, either in the Creator Studio Guided Setup or in the Collaboration app. For more information on custom descriptors, see [Configure Creator Studio using Guided Setup](../task/config-creator-studio-guided-setup.md#) and [Create collaboration descriptors to assign permissions](../../applications/task/create-collaboration-descriptors.md).

<table id="table_p2r_v4r_m1c"><thead><tr><th>

Descriptor

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner

</td><td>

Owner of the application.-   If you created the app, you're automatically the owner.
-   Owners can manage other collaborators for the app.
-   Owners have the delete app permission, which enables them to edit app settings, such as name, description, and icon.
-   Owners automatically get the delegated\_developer role for the app.

</td></tr><tr><td>

Editor

</td><td>

-   Editors can invite collaborators.
-   Editors have limited ability to edit the app.

</td></tr></tbody>
</table>## Collaboration development permissions

You’ve designated Owners and Editors in your app, now what? You must invite other collaborators to work in your app.

Collaboration permissions enable you to control who's building apps in Creator Studio. You assign permissions to developers \(or users who deploy applications\) so that they can develop and deploy applications.

If you invite someone to collaborate on an app and they don't have the Delegated developer \(delegated\_developer\) role, an App Engine admin must approve the collaboration request. For more information, see [Exploring Delegated Development](../../applications/concept/c_DelegatedDevelopment.md).

When you add a user or group, a collaboration task is generated behind the scenes, and an approval flow kicks off. If you have App Engine Management Center \(AEMC\) installed, your admin can review and approve/deny these collaboration request tasks there. If you don’t have AEMC installed, admins can navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Collaboration Tasks**.

The collaboration task that goes to your admin provides information on which application a developer is being added to, and what permissions are granted. Approvers sometimes need to review these task records before they add developers to the application.

## What can owners and editors do?

If you’re in the Creator Studio users group, you can see all users and groups collaborating on an app, as well as their collaboration descriptors.

If you can’t see the users and groups, you may have a different permission with more restrictions. But fear not! You can always contact your admin if you have any questions about who's working on an app.

The following table provides a list of general defaults for what owners and editors can do in Creator Studio.

**Note:** For the full list of default Owner and Editor collaborator collaboration type permissions, see [Customized app collaboration permissions in Creator Studio](creator-studio-collab-custom-permissions.md).

|Creator Studio feature|Owner|Editor|
|----------------------|-----|------|
|Invite collaborators|Yes|Yes|
|Manage collaborators|Yes|No|
|Edit app settings, such as name, description, and icon|Yes|No|
|Create, edit, and delete forms|Yes|Yes|
|Create, edit, and delete automation|Yes|Yes|
|Manage the fulfiller workspace list configurations and records|Yes|Yes|
|Submit app for deployment|Yes|No|
|Delete app|Yes|No|

## Collaboration roles and instances on different versions

As admins implement Creator Studio, they may have it installed on a non-production instance while their production instance is on a previous version of the ServiceNow AI Platform that doesn't have Creator Studio. This mis-match of instance versions affects the Collaboration Approval Workflow, which specifies the non-production instance as the source and the production instance as the controller. If the controller doesn't have the version of the collaboration plugin that supports Creator Studio, collaboration is unsupported.

To ensure that users can use the Collaboration Approval Workflow regardless of instance versions, admins must assign the catalog \_builder\_editor role to Creator Studio user groups.

-   **[Ask to work on an app in Creator Studio](../task/creator-studio-request-join-app.md)**  
Want to work on an app but don't have access to it? No problem. We'll show you how to ask for access.
-   **[Manage collaborators for an app in Creator Studio](../task/creator-studio-manage-collaborators.md)**  
Add or remove people who can work on an app, or change their permissions for the app using the **Manage collaborators** option.

**Parent Topic:**[Building apps with Creator Studio](../concept/building-apps-with-creator-studio.md)


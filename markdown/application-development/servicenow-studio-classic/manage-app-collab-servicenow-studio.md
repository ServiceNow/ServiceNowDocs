---
title: Collaborating on apps using ServiceNow Studio
description: Collaborate with other developers on app development in ServiceNow Studio by inviting them to co-create and develop apps with you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Collaborating on apps using ServiceNow Studio

Collaborate with other developers on app development in ServiceNow Studio by inviting them to co-create and develop apps with you.

## What is collaboration in ServiceNow Studio?

Collaboration, also referred to as delegated development, builds on the existing delegated development feature set in the ServiceNow AI Platform. It enables developers to invite other developers into apps to co-create and develop together. Depending on your permissions, you can invite others to collaborate on an app or request to join another developer's app. For more information, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

There are two standard collaborator roles when co-developing an app: owner and editor. Admins can create a custom collaboration role by adjusting permissions.

## What are the requirements for collaboration?

ServiceNow Studio supports the collaboration plugin for properly licensed customers.

**Note:**

1.  An App Engine Enterprise license is required to use collaboration fully.
2.  If you already have the collaboration plugin installed, you can continue to use collaboration.
3.  Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

## Which apps can you access in ServiceNow Studio?

The admin and delegated\_developer roles have different levels of app access in ServiceNow Studio:

-   Users with the admin role have access to all apps in ServiceNow Studio.
-   Users with the delegated\_developer role have access to:
    -   Apps they create.
    -   Apps they have been invited to edit.
    -   All apps within the scope they have access to. For more information about scopes, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/c_ApplicationScope.md).

To request access to an app that is not visible in ServiceNow Studio, contact your admin and ask them to grant you permission using the Collaboration app. The Collaboration app is automatically installed with ServiceNow Studio. For more information about the Collaboration app, see [Application collaboration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/application-collaboration.md).

## What can owners and editors do?

There are two default collaborator roles for working on apps with other developers: owner and editor.

-   If you create an app, you are the owner of that app.
-   If an app is visible in ServiceNow Studio and you have been delegated to work on it, open it and begin working with the collaboration role the owner assigned you. That role is usually editor.

<table id="table_p2r_v4r_m1c"><thead><tr><th>

Descriptor

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner

</td><td>

Owner of the application.-   If you create the app, you are automatically the owner.
-   Owners can manage other collaborators for the app.
-   Owners can delete apps because they have the delete app permission.
-   Owners automatically receive the delegated\_developer role for the app.

</td></tr><tr><td>

Editor

</td><td>

-   Editors can invite collaborators.
-   Editors have more limited editing permissions than owners.

</td></tr></tbody>
</table>**Note:** For the full list of default owner and editor permissions, see [Collaboration permissions for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.md).

## What are custom collaboration descriptors?

The collaboration descriptor assigned to a developer determines what they can do in the app — including assigning, managing, and monitoring delegated development permissions. Owners have more permissions than editors by default.

To create a customized collaboration role, create a custom collaboration descriptor and use collaboration permissions to control what developers can do in the app.

Admins can define custom collaboration descriptors to select when managing collaborators using the Collaboration app. For more information about custom descriptors, see [Create collaboration descriptors to assign permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/create-collaboration-descriptors.md).

## How does the collaboration approval process work?

If you invite someone to collaborate on an app and they do not have the delegated\_developer role, an App Engine admin must approve the collaboration request. For more information, see [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

When you add a user or group to collaborate on an app, the platform generates a collaboration task that initiates an approval flow. The task includes details about which app the developer is being added to and what permissions they receive. If App Engine Management Center \(AEMC\) is installed, admins can review and approve or deny collaboration requests there.

If AEMC is not installed, admins can navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Collaboration Tasks** to review collaboration tasks.

-   **[View collaborators on an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/view-app-collabs-servicenow-studio.md)**  
View the collaborators on an app in ServiceNow Studio to see who has access and what role each person has.
-   **[Add collaborators to an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/add-collabs-app-servicenow-studio.md)**  
Add collaborators to an app in ServiceNow Studio so other developers can co-develop the app with you.
-   **[Modify or customize collaboration permissions for a user or group in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/modify-collab-descriptor-servicenow-studio.md)**  
Modify or customize the collaboration permissions for a user or group in ServiceNow Studio to control what they can do in an app.
-   **[Remove collaborators from an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/remove-collaborators-servicenow-studio.md)**  
Remove a user or group as a collaborator in ServiceNow Studio to revoke their access to an app.

**Parent Topic:**[Configuring ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/configuring-servicenow-studio.md)


---
title: Manage collaborators for an app in Creator Studio
description: Add or remove people who can work on an app, or change their permissions for the app using the Manage collaborators option.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Collaborating with others to build apps in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Manage collaborators for an app in Creator Studio

Add or remove people who can work on an app, or change their permissions for the app using the **Manage collaborators** option.

## Before you begin

Your system administrator needs to assign you the Manage collaborators permission. Admins can also manage collaborators.

## About this task

You can invite collaborators or manage collaborators depending on your permissions for each app. For example, if you have the Invite collaborators permission, you can't change the collaborator type of existing collaborators, such as Editor or Owner.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Find the app you want to manage collaborators for.

3.  Access the Collaborators with others modal in one of two ways:

    -   From the Creator Studio home page, select the app's more actions icon \(![Option to manage collaborators](../image/cs-more-options-icon.png)\) and select **Manage collaborators** from the menu that appears.
    -   Open the app, select the more actions icon \(![](../../servicenow-studio/image/sn-studio-more-options-icon.png)\) in the navigation panel, and select **Manage collaborators** from the menu that appears.

        ![Select the more options menu to manage collaborators](../image/crs-manage-collab.png "Open Manage collaborators")

4.  Change the permission of existing collaborators in the Collaborator section using the **Select descriptor** field.

    -   **Owner** changes the user or group to be an owner for the app.
    -   **Editor** changes the user or group to be an editor for the app.
    -   **Customize permissions** enables you to select specific things that users can do with the app. For more information, see [Customized app collaboration permissions in Creator Studio](../reference/creator-studio-collab-custom-permissions.md).
    -   **Remove** revokes the user or group's access to work on the app.
    **Note:** The collaboration descriptor must be in the global scope for it to be used by others.

    ![Option to customize collaboration permissions](../image/cs-collab-custom-1.png "Customize collaboration permissions")

5.  Customize collaboration permissions by selecting **Customize permissions** and selecting the permissions the user should have.

    ![Select custom collaboration permissions](../image/cs-collab-custom-2.png "Customize collaboration permissions")

6.  Add any additional collaborators.

    1.  Start typing the people or groups you want to invite in the **Invite people by name or group** field.

    2.  Specify the collaboration level in the **Select descriptor** field.

    3.  Select the **Send** button to start the approval process.

    You can specify as many users and groups as needed.


## Result

Unless you customized permissions, which requires the **Save** button, your changes are automatically saved when you close the Collaborate with others modal.

## What to do next

Your App Engine admin must then approve the changes to collaborators.

**Parent Topic:**[Collaborating with others to build apps in Creator Studio](../reference/creator-studio-collaboration-roles.md)


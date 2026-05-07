---
title: Modify or customize collaboration permissions for a user or group in ServiceNow Studio
description: Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaborating on apps, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Modify or customize collaboration permissions for a user or group in ServiceNow Studio

Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the app that you want to modify collaborators for, and select **App details**.

3.  Access collaboration settings by selecting the more options icon ![](../image/sn-studio-more-options-icon.png) and selecting **Invite**.

    ![Invite collaborators to work on your app using the more options menu on the app details page.](../image/sn-studio-collab-select-zs2.png)

4.  Choose the new permission level for the user or group in the Collaborators section of the modal.

5.  Customize what the collaborator can do by creating custom permissions.

    1.  Select **Customize permissions** for the user or group in the Collaborators section.

        ![Option to customize collaboration permissions](../../creator-studio/image/cs-collab-custom-1.png "Customize collaboration permissions")

    2.  Choose the permissions you want the group or user to have.

        For more information on permissions and descriptions, see [Collaboration permissions for ServiceNow Studio](../reference/servicenow-studio-collab-permissions.md).

        ![Select custom collaboration permissions](../../creator-studio/image/cs-collab-custom-2.png "Customize collaboration permissions")

    3.  Select **Save**.


## Result

Your changes are automatically saved when you close the Collaborate with others modal.

## What to do next

Your App Engine admin must then approve the changes to collaborators. For more information, admins should see [Approve a collaboration request](../../creator-studio/task/approve-collaboration-request.md).

**Parent Topic:**[Collaborating on apps using ServiceNow Studio](../concept/manage-app-collab-servicenow-studio.md)


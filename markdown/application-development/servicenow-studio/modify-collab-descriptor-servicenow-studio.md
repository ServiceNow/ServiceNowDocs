---
title: Modify or customize collaboration permissions for a user or group in ServiceNow Studio
description: Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Collaborating on apps using ServiceNow Studio, Configuring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Modify or customize collaboration permissions for a user or group in ServiceNow Studio

Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Find and select the app where you want to modify permissions for collaborators.

3.  Access collaboration settings by selecting the collaborators icon \(![collaborators icon](../image/sn-studio-collab-icon.png)\).

    ![Collaboration icon near the Publish button](../image/sn-studio-collab-select.png "Access collaboration in ServiceNow Studio")

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


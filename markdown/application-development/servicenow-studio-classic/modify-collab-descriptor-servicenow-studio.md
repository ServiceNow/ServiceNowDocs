---
title: Modify or customize collaboration permissions for a user or group in ServiceNow Studio
description: Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/modify-collab-descriptor-servicenow-studio.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collaborating on apps, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Modify or customize collaboration permissions for a user or group in ServiceNow Studio

Change the collaboration access that a user or group has to work on an app in ServiceNow Studio by modifying or customizing their collaboration descriptor.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the app that you want to modify collaborators for, and select **App details**.

3.  Access collaboration settings by selecting the more options icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text: and selecting **Invite**.

    \[Omitted image "sn-studio-collab-select-zs2.png"\] Alt text: Invite collaborators to work on your app using the more options menu on the app details page.

4.  Choose the new permission level for the user or group in the Collaborators section of the modal.

5.  Customize what the collaborator can do by creating custom permissions.

    1.  Select **Customize permissions** for the user or group in the Collaborators section.

        \[Omitted image "cs-collab-custom-1.png"\] Alt text: Option to customize collaboration permissions

    2.  Choose the permissions you want the group or user to have.

        For more information on permissions and descriptions, see [Collaboration permissions for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.md).

        \[Omitted image "cs-collab-custom-2.png"\] Alt text: Select custom collaboration permissions

    3.  Select **Save**.


## Result

Your changes are automatically saved when you close the Collaborate with others modal.

## What to do next

Your App Engine admin must then approve the changes to collaborators. For more information, admins should see [Approve a collaboration request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/approve-collaboration-request.md).

**Parent Topic:**[Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md)


---
title: Add collaborators to an app in ServiceNow Studio
description: Add collaborators to an app in ServiceNow Studio so other developers can co-develop the app with you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/add-collabs-app-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Collaborating on apps, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Add collaborators to an app in ServiceNow Studio

Add collaborators to an app in ServiceNow Studio so other developers can co-develop the app with you.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the app you want to add collaborators to, then select **App details**.

3.  Access collaboration settings by selecting the more options icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text: and selecting **Invite**.

    \[Omitted image "sn-studio-collab-select-zs2.png"\] Alt text: Invite collaborators to work on your app using the more options menu on the app details page.

4.  In the **Invite people by name or group** field, enter the name of the user or group you want to invite.

    A list of matching users and groups appears. If a user or group appears in the list but is not selectable, they have already been added as a collaborator.

5.  In the **Select descriptor** field, select the collaboration role for the user or group.

    If you are an editor for the app, you can select only the editor descriptor.

    -   For more information about collaboration descriptors, see [Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md).
    -   For a list of all collaboration permissions, see [Collaboration permissions for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.md).
6.  Select **Send** to invite the collaborator.

    -   If the user is new to the ServiceNow AI Platform, an admin must approve the request. After approval, both the requester and the user receive an email confirming that the user has been added to the application.
    -   If the user is not new to the ServiceNow AI Platform, the collaboration request is auto-approved. Both the requester and the user receive an email confirming that the user has been added to the application.

**Parent Topic:**[Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md)


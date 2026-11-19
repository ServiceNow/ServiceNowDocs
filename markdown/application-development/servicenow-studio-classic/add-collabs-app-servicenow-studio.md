---
title: Add collaborators to an app in ServiceNow Studio
description: Invite other people to work on an app with you in ServiceNow Studio, collaborating as co-developers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/servicenow-studio-classic/add-collabs-app-servicenow-studio.html
release: yokohama
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Collaborating on apps using ServiceNow Studio, Configuring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Add collaborators to an app in ServiceNow Studio

Invite other people to work on an app with you in ServiceNow Studio, collaborating as co-developers.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Find and select the app you want to invite people to collaborate on.

3.  Open collaboration settings for the app by selecting the collaborators icon \(\[Omitted image "sn-studio-collab-icon.png"\] Alt text: collaborators icon\).

    \[Omitted image "sn-studio-collab-select.png"\] Alt text: Collaboration icon near the Publish button

4.  Search for the user or group that you want to invite to work on the app by entering the name in the **Invite people by name or group** field.

    A drop-down list displays the matching people and groups. If a user or group appears in the drop-down list but you can't select it, it's already been added as a collaborator and can't be re-selected.

5.  Select the collaboration role for the user or group that you're adding from the **Select descriptor** field.

    If you're an editor for the app, you can select only the editor descriptor.

    -   For more information on collaboration descriptors, see [Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md).
    -   For a list of all the collaboration permissions, see [Collaboration permissions for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.md).
6.  Finish inviting the collaborator by selecting **Send**.


## Result

-   If the user has ServiceNow Studio or delegated developer permissions and is new to the ServiceNow AI Platform, they must be approved by an admin. After the request is approved, both the requester and the user receive an email indicating that the user has been added to the application.

    \[Omitted image "aes-approval-email-purple.png"\] Alt text: Collaboration approval email example

-   If the user has ServiceNow Studio or delegated developer permissions and is not new to the ServiceNow AI Platform, the collaboration request is auto-approved. Both the requester and the user receive an email indicating that the user has been added to the application.

**Parent Topic:**[Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md)


---
title: Modify or customize collaboration permissions for a user or group in ServiceNow Studio
description: Modify or customize the collaboration permissions for a user or group in ServiceNow Studio to control what they can do in an app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/modify-collab-descriptor-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Collaborating on apps, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Modify or customize collaboration permissions for a user or group in ServiceNow Studio

Modify or customize the collaboration permissions for a user or group in ServiceNow Studio to control what they can do in an app.

## Before you begin

Customers that don't have Collaboration installed will not be able to manage delegated development permissions in ServiceNow Studio. Existing delegated development permissions will still be respected within ServiceNow Studio.

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the app you want to modify collaborators for, then select **App details**.

3.  Access collaboration settings by selecting the more options icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text: and selecting **Invite**.

    \[Omitted image "sn-studio-collab-select-zs2.png"\] Alt text: Invite collaborators to work on your app using the more options menu on the app details page.

4.  In the **Collaborators** section of the **Collaborate with others** dialog, select the new permission level for the user or group.

5.  To create custom permissions for the collaborator, select **Customize permissions** for the user or group in the **Collaborators** section.

    1.  Select **Customize permissions** for the user or group.

        \[Omitted image "cs-collab-custom-1.png"\] Alt text: Option to customize collaboration permissions

    2.  Select the permissions you want the user or group to have.

        For more information about permissions, see [Collaboration permissions for ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.md).

        \[Omitted image "cs-collab-custom-2.png"\] Alt text: Select custom collaboration permissions.

    3.  Select **Save**.


## Result

Changes are saved automatically when you close the **Collaborate with others** dialog.

## What to do next

Your App Engine admin must approve the changes to collaborators. For more information, see [Approve a collaboration request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/approve-collaboration-request.md).

**Parent Topic:**[Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md)


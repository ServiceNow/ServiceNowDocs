---
title: Upload manifest file in Microsoft Teams
description: Upload the manifest file in Microsoft Teams to integrate Microsoft Teams with your ServiceNow instance.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Upload manifest file in Microsoft Teams

Upload the manifest file in Microsoft Teams to integrate Microsoft Teams with your ServiceNow instance.

## Before you begin

Make sure that you have the manifest file for pre-published apps. For more information, see [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md).

Role required: admin

## Procedure

1.  Launch Microsoft Teams application.

2.  Navigate to **Apps** &gt; **Manage your apps**, then select **Upload a customised app**.

    **Note:**

    Ensure that ServiceNow for Microsoft Teams is allowed as a third-party app in Microsoft Teams. For information about allowing apps in Microsoft Teams, see the [Microsoft Teams documentation](https://learn.microsoft.com/en-us/microsoftteams/app-policies).

3.  Navigate to the location where the manifest file is downloaded and select the zip file.

4.  Click **Open**.

    The **ServiceNow for Teams** appears in **Apps** screen.

    ![ServiceNow for Teams app in Microsoft Teams.](../images/sn-ms-teams.png)

5.  Click **ServiceNow for Teams** app.

6.  Click **Add**.

    ![ServiceNow for Teams app.](../images/sn-ms-teams-app-1.png)

    The ServiceNow for Teams app appears in Microsoft Teams.

    -   **Chat**: Begin your conversation with the Virtual Agent to get help.

        ![Chat tab in Microsoft Teams.](../images/chat-tab-ms-teams02.png)

    -   **Employee Center**: Click **Employee Center** tab to view the organization updates and the status on your tasks and requests.

        ![Employee Center tab in Microsoft Teams.](../images/emp-center-ms-teams02.png)

    **Note:** If you don't want to create a manifest file, you can edit an existing manifest file as required. Upon updating the existing manifest file, you can download and upload the manifest file in Microsoft Teams to make the changes effective.


**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)


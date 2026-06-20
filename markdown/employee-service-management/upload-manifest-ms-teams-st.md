---
title: Upload manifest file in Microsoft Teams
description: Upload the manifest file in Microsoft Teams to integrate Microsoft Teams with your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/upload-manifest-ms-teams-st.html
release: xanadu
product: Employee Service Management
classification: employee-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Upload manifest file in Microsoft Teams

Upload the manifest file in Microsoft Teams to integrate Microsoft Teams with your ServiceNow instance.

## Before you begin

Make sure that you have the manifest file for self-configured apps. For more information, see [Create and download the manifest file for self-configured apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/download-manifest-file-st.md).

Role required: admin

## Procedure

1.  Launch the Microsoft Teams application.

2.  Navigate to **Apps** &gt; **Upload a customised app**.

    **Note:**

    Ensure that ServiceNow for Microsoft Teams is allowed as a third-party app in Microsoft Teams. For information about allowing apps in Microsoft Teams, see the [Microsoft Teams documentation](https://learn.microsoft.com/en-us/microsoftteams/app-policies).

3.  Navigate to the location where the manifest file is downloaded and select the zip file.

4.  Select **Open**.

    The **ServiceNow for Teams** appears in the **Apps** screen.

    \[Omitted image "sn-ms-teams.png"\] Alt text: ServiceNow for Teams app.

5.  Select the **ServiceNow for Teams** app.

6.  Select **Add**.

    \[Omitted image "sn-ms-teams-app-1.png"\] Alt text: ServiceNow for Teams app in Microsoft Teams.

    The ServiceNow for Teams app appears in Microsoft Teams.

    -   **Chat**: Begin your conversation with the Virtual Agent to get help.

        \[Omitted image "chat-tab-ms-teams02.png"\] Alt text: Chat tab in Microsoft Teams.

    -   **Employee Center**: Select the **Employee Center** tab to view the organization updates and the status on your tasks and requests.

        \[Omitted image "emp-center-ms-teams02.png"\] Alt text: Employee Center tab in Microsoft Teams.

    **Note:** If you don't want to create a manifest file, you can edit an existing manifest file as required. After updating the existing manifest file, you can download and upload the manifest file in Microsoft Teams to make the changes effective.


**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/c_employee_ex_s_tnt.md)


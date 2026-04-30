---
title: Authorize pre-published Azure apps to grant required permissions
description: Authorize the pre-published apps to enable ServiceNow to make API calls to Microsoft to enable each of the ServiceNow for Teams application workflows.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate Notify connector pre-published app with Microsoft Teams, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Authorize pre-published Azure apps to grant required permissions

Authorize the pre-published apps to enable ServiceNow to make API calls to Microsoft to enable each of the ServiceNow for Teams application workflows.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

## About this task

To connect your ServiceNow instance to your M365 tenant and to Authorize apps, the user must have both the external\_app\_install\_admin role as well as the application administrator role in M365. Application administrator is a Microsoft driven role, for more information on roles, refer [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#available-roles).

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

    ![Install apps on ServiceNow instance.](../image/notify-ms-teams-app-02.png)

2.  Click **Authorize** for Notify Connector.

3.  Provide the admin consent by selecting **Accept**.

    **Note:** Additional permissions such as 'Manage Teams apps for all chats' and 'Allow the Teams app to manage all tabs for all chats' are required to create an app for meeting extensibility, and to create a new tab for a major incident meeting from the major incident workbench in Microsoft Teams.

    ![Admin consent for the app.](../image/notify_connector_admin_consent.png)

    Upon successful authorization, the app is shown as **Installed**.

    ![Notify connector app is installed.](../image/notify-app-installed-02.png)


**Parent Topic:**[Integrate Notify connector pre-published app with Microsoft Teams](../concept/setup-notify-ms-teams-multi-tenant.md)


---
title: Authorize pre-published Azure apps to grant required permissions
description: Authorize the pre-published apps to enable ServiceNow to make API calls to Microsoft to enable each of the ServiceNow for Teams application workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/authorize-multi-tenant-apps.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Authorize pre-published Azure apps to grant required permissions

Authorize the pre-published apps to enable ServiceNow to make API calls to Microsoft to enable each of the ServiceNow for Teams application workflows.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

## About this task

To connect your ServiceNow instance to your M365 tenant and to Authorize apps, the user must have both the external\_app\_install\_admin role as well as the application administrator role in M365. Application administrator is a Microsoft driven role, for more information on roles, refer [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#available-roles).

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

    \[Omitted image "notify-ms-teams-app-02.png"\] Alt text: Install apps on ServiceNow instance.

2.  Click **Authorize** for Notify Connector.

3.  Provide the admin consent by selecting **Accept**.

    **Note:** Additional permissions such as 'Manage Teams apps for all chats' and 'Allow the Teams app to manage all tabs for all chats' are required to create an app for meeting extensibility, and to create a new tab for a major incident meeting from the major incident workbench in Microsoft Teams.

    \[Omitted image "notify\_connector\_admin\_consent.png"\] Alt text: Admin consent for the app.

    Upon successful authorization, the app is shown as **Installed**.

    \[Omitted image "notify-app-installed-02.png"\] Alt text: Notify connector app is installed.


**Parent Topic:**[Integrate Notify connector pre-published app with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/setup-notify-ms-teams-multi-tenant.md)


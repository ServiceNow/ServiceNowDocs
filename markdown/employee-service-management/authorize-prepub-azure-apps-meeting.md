---
title: Authorize pre-published SSO and Activity Notification Azure apps to grant required permissions
description: Authorize the pre-published SSO and Activity Notification apps to enable ServiceNow to make API calls from a personal tab in Microsoft Teams.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions pre-published app with Microsoft Teams, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Authorize pre-published SSO and Activity Notification Azure apps to grant required permissions

Authorize the pre-published SSO and Activity Notification apps to enable ServiceNow® to make API calls from a personal tab in Microsoft Teams.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

## About this task

To connect your ServiceNow instance to your Microsoft 365 tenant and to Authorize apps, the user must have both the external\_app\_install\_admin role and the application administrator role in Microsoft 365. Application administrator is a Microsoft driven role, for more information on roles, refer [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#available-roles).

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

2.  Select **Authorize** for SSO and Activity Notification.

3.  Provide the admin consent by selecting **Accept**.

    **Note:** Additional permissions such as 'Manage Teams apps for all chats' and 'Allow the Teams app to manage all tabs for all chats' are required to create an app for meeting extensibility, and to create a new tab for a major incident meeting from the major incident workbench in Microsoft Teams.

    Upon successful authorization, the app status is displayed as Installed.


**Parent Topic:**[Integrate Meeting Extensions pre-published app with Microsoft Teams](../concept/setup-meeting-extensibility-multi-tenant.md)


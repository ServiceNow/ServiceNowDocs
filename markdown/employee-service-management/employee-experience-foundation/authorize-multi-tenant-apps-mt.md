---
title: Grant permissions to required Microsoft Azure apps
description: Authorize the required pre-published apps to enable your ServiceNow instance to make API calls to Microsoft Azure to enable ServiceNow for Teams application workflows.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Grant permissions to required Microsoft Azure apps

Authorize the required pre-published apps to enable your ServiceNow instance to make API calls to Microsoft Azure to enable ServiceNow for Teams application workflows.

## Before you begin

Install Virtual Agent Lite or Virtual Agent. For more information see [Virtual Agent integration with messaging apps](https://www.servicenow.com/docs/access?context=va-integration-messaging-apps&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

To connect your ServiceNow instance to your Microsoft 365 tenant and to authorize apps, you must have both the external\_app\_install\_admin role and the Global Administrator role in Microsoft 365. For information about the related Microsoft roles, see [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#available-roles).

Role required: External admin \(external\_app\_install\_admin\). This role is installed on the base system as part of the installation of the Channel Proxy plugin.

## About this task

The ServiceNow for Teams pre-published apps are:

-   Notify Connector: Install Notify Connector for Microsoft Teams to enable the chat to call feature. For more information, see [Notify connector for Microsoft Teams](../../notify2/concept/notify-connector-ms-teams.md).
-   Request-based Chats
-   SSO and Activity Notifications

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

2.  Authorize the relevant app.

    1.  Click **Authorize** in the row of the app entry.

    2.  Provide the admin consent by selecting **Accept**.

        For information on API permissions used in ServiceNow for Microsoft Teams integration, refer [ServiceNow for Microsoft Teams integration API permissions for Request-based chat and SSO](../reference/request-based-chat-api-permissions.md).

    Upon successful authorization, a green check mark appears next to the app name and the **Authorize** button changes to **Installed**.


## What to do next

If the upn is different from email ID in your environment, go to [Enable connecting to meetings from Microsoft Teams](create-oauth-oidc-record.md). If the upn is same as the email ID, go to [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md).

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)


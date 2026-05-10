---
title: Integrating Request-based chat with Microsoft Teams for GCC-H or DoD
description: You can integrate request-based chat with Microsoft Teams for Government Community Cloud - High \(GCC-H\) or US Department of Defense \(DoD\) customers to auto import the chat conversations between the agents and the employees.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Integrating Request-based chat with Microsoft Teams for GCC-H or DoD

You can integrate request-based chat with Microsoft Teams for Government Community Cloud - High \(GCC-H\) or US Department of Defense \(DoD\) customers to auto import the chat conversations between the agents and the employees.

## Prerequisites

Before integrating Employee Center with your Microsoft Teams tenant, ensure that the following prerequisites are met:

-   Your ServiceNow instances have been upgraded to the Vancouver release.
-   You have not previously attempted installing the Conversational Integration with Microsoft Teams app on your instances.
-   You have the admin permissions on ServiceNow and Microsoft Azure instances.

## Integration process

1.  Activate the IT Service Management integration with Microsoft Teams plugin \(sn\_now\_teams\_it\).

    **Note:** For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

2.  [Register and configure the Request-based chat application on the Microsoft Azure portal](../task/register-app-req-based-chats.md).
3.  [Add permissions to the Microsoft Azure application](../task/authenticate-users-req-based-chat.md).
4.  [Configure Application Registry on the ServiceNow instance](../task/app-registry-chat-single-tenant.md#).

    **Note:** For GCC-H and DoD, use the `https://login.microsoftonline.us/` domain for token and authorization URLs on the application registry page.

5.  [Update chat credentials with Azure GCC URL](../task/update-chat-credentials-azure-gcch.md).
6.  [Create record with Azure GCC details](../task/create-record-azure-gcch.md).

-   **[Update chat credentials with Azure GCC URL](../task/update-chat-credentials-azure-gcch.md)**  
Update the Azure URL in the chat credentials of GCC customers. Enable GCC customers to start chat and import chat conversations from Microsoft Teams to the ServiceNow instance.
-   **[Create record with Azure GCC details](../task/create-record-azure-gcch.md)**  
Create and update a new record in the sys\_properties.list table with the details of the Azure account of GCC customers.

**Parent Topic:**[Integrating ServiceNow with Microsoft Teams for GCC-H or DoD](setup-sn-ms-teams-gcch.md)


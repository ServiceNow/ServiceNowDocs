---
title: Authenticate guest users to initiate and import chat from Microsoft Teams
description: Assign permissions to guest users to initiate and import chat conversations with employees from Microsoft Teams to a ServiceNow instance for a self-configured app.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request-based chat access for a guest user, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Authenticate guest users to initiate and import chat from Microsoft Teams

Assign permissions to guest users to initiate and import chat conversations with employees from Microsoft Teams to a ServiceNow® instance for a self-configured app.

## Before you begin

Ensure you have completed the Request-based chat app configuration for a self-configured app. For more information, see:

1.  [Register and configure the Request-based chat application on the Microsoft Azure portal](register-app-req-based-chats.md)
2.  [Configure Application Registry on the ServiceNow instance](app-registry-chat-single-tenant.md#)
3.  [Add permissions to the Microsoft Azure application](authenticate-users-req-based-chat.md)

Role required: admin

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Select the Request-based chat app to enable agents to initiate and import the conversations from Microsoft Teams to the ServiceNow instance.

4.  Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph**.

5.  Select **Application permissions**.

6.  In the Select permissions search field, enter `User.Read.All` and select that permission.

    This permission obtains the Microsoft Azure user type value. This value is stored on the ServiceNow instance to enable the creation and importing of chats on the user's behalf.

7.  Select **Add permissions**.

8.  In the **API permissions** screen, select the **Grant admin consent for \{tenant\}** link.

9.  Select **Yes** in the pop-up dialog box to save the settings.


**Parent Topic:**[Request-based chat access for a guest user](../concept/guest-user-chat-access-st.md)


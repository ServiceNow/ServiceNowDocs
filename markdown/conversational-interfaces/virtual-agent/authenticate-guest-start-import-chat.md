---
title: Authenticate guest users to initiate and import chat from Microsoft Teams
description: Assign permissions to guest users to initiate and import chat conversations with employees from Microsoft Teams to a ServiceNow instance for a self-configured app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/authenticate-guest-start-import-chat.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Authenticate guest users to initiate and import chat from Microsoft Teams

Assign permissions to guest users to initiate and import chat conversations with employees from Microsoft Teams to a ServiceNow® instance for a self-configured app.

## Before you begin

Ensure you have completed the Request-based chat app configuration for a self-configured app. For more information, see:

1.  
2.  
3.  

Role required: Microsoft Azure admin

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


**Parent Topic:**[Exploring other Virtual Agent features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/exploring-other-vad-features.md)


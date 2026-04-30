---
title: Manage permissions and authenticate the Notify connector app/bot in Microsoft Azure portal
description: Assign permissions to users to be able to authenticate successfully and participate in conference calls in Microsoft Teams.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2023-03-08"
reading_time_minutes: 1
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Manage permissions and authenticate the Notify connector app/bot in Microsoft Azure portal

Assign permissions to users to be able to authenticate successfully and participate in conference calls in Microsoft Teams.

## Before you begin

Role required: Microsoft Azure admin

## About this task

You can manage the permissions required by the Notify connector app/bot to perform required actions for conference calls.

## Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/).

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Search and open the Notify connector bot created in step 3 in the section [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md) by name or by Application \(client\) ID.

4.  Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph** and select **Application Permissions**.

5.  Search and select the following values using **Select permissions**, and then select **Add permissions** to grant the permission.

    -   **User.Read.All** from User list.
    -   **OnlineMeetings.ReadWrite.All** from OnlineMeetings list.
    -   **Calls.InitiateGroupCall.All**, **Calls.JoinGroupCall.All**, **Calls.JoinGroupCallAsGuest.All** from Calls list.
6.  Grant admins access to the Microsoft Azure applications that require admin approval.

    1.  Select **Grant admin consent for &lt;tenant&gt;** in the API permissions page.

    2.  Select **Yes** in the Grant admin consent confirmation pop-up page.


**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)


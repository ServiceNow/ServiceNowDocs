---
title: Configure the Notify connector app to use Meeting Extensions in the Microsoft Azure portal
description: Configure the existing Notify connector app/bot to use Meeting Extensions in Microsoft Azure portal to fetch the incident details during the conference call in Microsoft Teams.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure the Notify connector app to use Meeting Extensions in the Microsoft Azure portal

Configure the existing Notify connector app/bot to use Meeting Extensions in Microsoft Azure portal to fetch the incident details during the conference call in Microsoft Teams.

## Before you begin

Role required: Microsoft Azure admin

## About this task

No need to create a separate Meeting Extensions bot as the Meeting Extensions app depends on the Notify connector for Microsoft Teams app. You can configure the existing Notify connector app/bot in the Microsoft Azure portal for Meeting Extensions to have a seamless conference call experience in Microsoft Teams.

**Note:** Ensure that API permissions are configured for the Notify connector for Microsoft Teams app in the Microsoft Azure portal. For more information, see [Manage permissions and authenticate the Notify connector app/bot in Microsoft Azure portal](../../notify2/task/manage-permissions-notify.md). You must update the following changes to the existing Notify connector app in the Microsoft Azure portal.

## Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/) as Microsoft Azure admin.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Open the app created for Notify connector in Microsoft Teams in the section [Create an app in Microsoft Teams to enable making calls](../../notify2/task/create-app-ms-teams.md).

4.  Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph** and select **Application permissions**.

5.  Search and select the following values using **Select permissions**, and then select **Add permissions**.

    -   **TeamsTab.ReadWriteForChat.All** from TeamsTab list.
    -   **TeamsAppInstallation.ReadWriteForChat.All** from TeamsAppInstallation list.
6.  Grant admins access to the Microsoft Azure applications that require admin approval.

    1.  Select **Grant admin consent for &lt;tenant&gt;** in the API permissions page.

    2.  Select **Yes** in the Grant admin consent confirmation pop-up page.

7.  Authenticate app to receive the incoming requests from Microsoft Teams into ServiceNow® instance.

    1.  Navigate to **Manage** &gt; **Authentication** &gt; **Platform configurations** &gt; **Add a platform** &gt; **Web applications** &gt; **Web**.

    2.  On the form, fill in the fields.

<table id="table_cfc_hsg_pnb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Redirect URIs

</td><td>

Enter the meeting login URL.

 URL should be in the following format:

 `https://<instance-name>.service-now.com/sn_now_teams_ext_meeting_login.do`

</td></tr><tr><td>

Implicit grant

</td><td>

Select **Access tokens** and **ID tokens**

</td></tr></tbody>
</table>    3.  Click **Configure**.


**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)


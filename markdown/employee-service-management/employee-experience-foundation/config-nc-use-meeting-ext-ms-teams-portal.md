---
title: Create and configure an app for Meeting Extensions in the Microsoft Teams Developer Portal
description: Create and configure an app for Meeting Extensions in Microsoft Teams Developer Portal to fetch incident details during the conference call in Microsoft Teams.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create and configure an app for Meeting Extensions in the Microsoft Teams Developer Portal

Create and configure an app for Meeting Extensions in Microsoft Teams Developer Portal to fetch incident details during the conference call in Microsoft Teams.

## Before you begin

Ensure you have installed Notify connector and other required plugins on your ServiceNow® instance. For more information, see [Install Meeting Extensions for Microsoft Teams](install-meeting-ext-ms-teams.md).

Role required: Microsoft Teams admin

## Procedure

1.  Log in to the Microsoft Teams portal at [https://dev.teams.microsoft.com](https://dev.teams.microsoft.com).

2.  Create an app.

    1.  Navigate to **Apps** &gt; **New app**.

    2.  Enter a valid name for the app in the Add app dialog box and select **Add**.

    3.  On the App details page, fill in the fields.

<table id="table_dnd_rwv_rwb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Name of your application. For example, ServiceNow Meeting Extensions for Microsoft Teams.

</td></tr><tr><td>

Full name

</td><td>

Full name of your application.

</td></tr><tr><td>

Application \(client\) ID

</td><td>

Unique identification number for the app.**Note:** This App ID is different from the generated Bot ID/App ID.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the app.

</td></tr><tr><td>

Long description

</td><td>

Detailed description of the app.

</td></tr><tr><td>

Version

</td><td>

Version for the app.

 For example, 1.0.

</td></tr><tr><td>

Developer or company Name

</td><td>

Name of your company.

</td></tr><tr><td>

Website

</td><td>

Link to your company website.

</td></tr><tr><td>

Privacy policy

</td><td>

Link to the privacy statement for your app.

</td></tr><tr><td>

Terms of use

</td><td>

Link to the terms and conditions for your app.

</td></tr></tbody>
</table>    4.  Select **Save**.

3.  Configure the Group and Channel app.

    1.  Navigate to **Configure** &gt; **App features** &gt; **Group and Channel app**.

    2.  On the Group and channel app details page, fill in the fields.

<table id="table_xg2_dgw_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration URL

</td><td>

The configuration URL in the following format:

 `https://<instance_name>.service-now.com/sn_now_teams_ext_meeting_configuration.do`

</td></tr><tr><td>

Scope

</td><td>

The meeting types **Team** or **GroupChat**,depending on where users can use your app.

</td></tr><tr><td>

Context

</td><td>

Select all context items from the list.

</td></tr><tr><td>

Users can reconfigure the app

</td><td>

Option to allow users to reconfigure the Meeting Extensions app.

</td></tr></tbody>
</table>    3.  Select **Save**.

4.  Assign the chat and meeting permissions.

    1.  Navigate to **Permissions** &gt; **Chat/Meeting permissions**.

    2.  Select **MeetingStage.Write.Chat**.

    3.  Select **Save**.

5.  Go to **Single sign-on** and enter the Application ID URI in the format `api://<instance_name>.service-now.com/<client ID in Microsoft Azure>`.

    For information about the Client ID, see [Create an app in Microsoft Teams to enable making calls](../../notify2/task/create-app-ms-teams.md).

6.  Add a domain.

    1.  Navigate to **Domains** &gt; **Create your first domain**.

    2.  Enter `*.service-now.com` in the Add domain dialog box to allow authorizations for ServiceNow URLs.

7.  Select **Publish/Distribute**.


## What to do next

[Upload the app manifest in Microsoft Teams](upload-app-manifest-ms-teams.md).

**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)


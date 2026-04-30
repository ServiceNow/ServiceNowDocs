---
title: Upload the app manifest in Microsoft Teams
description: Enable users to interact with agents from Microsoft Teams application by copying the Notify connector App ID value.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2023-03-08"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Upload the app manifest in Microsoft Teams

Enable users to interact with agents from Microsoft Teams application by copying the Notify connector App ID value.

## Before you begin

Role required: Microsoft Teams admin

## Procedure

1.  Log in to [Microsoft Teams admin portal](https://admin.teams.microsoft.com/).

2.  Navigate to **Teams apps** &gt; **Manage apps** &gt; **Upload new app** &gt; **Upload**.

3.  Search, select, and open \(in the Upload a custom app dialog-box\) the app package you downloaded in the section [Create and configure an app for Meeting Extensions in the Microsoft Teams Developer Portal](config-nc-use-meeting-ext-ms-teams-portal.md).

4.  Go to **Manage Apps**, search for the uploaded app, open and copy the **App ID** value in a notepad from the app details page.

    This App ID is used for Meeting Extensions and so, this App ID must be updated in System Properties in ServiceNow® instance.


**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)


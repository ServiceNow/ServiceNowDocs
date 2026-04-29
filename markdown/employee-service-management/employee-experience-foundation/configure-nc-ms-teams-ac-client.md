---
title: Configuring Notify connector for Microsoft Teams app in Microsoft Teams
description: Configure the manifest file in Microsoft Teams client or admin center to use Notify connector for Microsoft Teams app.Configure the manifest file in Microsoft Teams client to use Notify connector for Microsoft Teams app.Configure the manifest file in Microsoft Teams admin center to use Notify connector for Microsoft Teams app.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions pre-published app with Microsoft Teams, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configuring Notify connector for Microsoft Teams app in Microsoft Teams

Configure the manifest file in Microsoft Teams client or admin center to use Notify connector for Microsoft Teams app.

You can upload the manifest file in Microsoft Teams using one of the following procedures.

-   [Configure Notify connector for Microsoft Teams app in Microsoft Teams](configure-nc-ms-teams-ac-client.md#)
-   [Configure Notify connector for Microsoft Teams app in Microsoft Teams](configure-nc-ms-teams-ac-client.md#)

**Parent Topic:**[Integrate Meeting Extensions pre-published app with Microsoft Teams](setup-meeting-extensibility-multi-tenant.md)

## Configure Notify connector for Microsoft Teams app in Microsoft Teams

Configure the manifest file in Microsoft Teams client to use Notify connector for Microsoft Teams app.

### Before you begin

Role required: Microsoft Teams admin

### Procedure

1.  Launch Microsoft Teams application.

2.  Navigate to **Apps** &gt; **Manage your apps** &gt; **Upload an app**.

3.  Upload manifest file on Microsoft Teams client using one of the following procedures.

    -   Select **Upload an app to your org's app catalog** if you are an admin.
    -   Select **Submit an app to your org** if you are not an admin and for a Microsoft Teams admin to approve.
        1.  Search, select, and open the downloaded app manifest file. An acknowledgement of request submission to your admin is displayed.
        2.  Log in to the [Microsoft Teams admin portal](https://admin.teams.microsoft.com/) as Microsoft Teams admin.
        3.  Navigate to **Teams apps** &gt; **Manage apps**.
        4.  Search the app by name and select to open. The app default status is Blocked.
        5.  Select **Publish** and select **Publish** on the Publish your custom app? pop-up page. The app status is changed to Allowed.
    It may take some time for the uploaded app to appear on the Microsoft Teams admin center.


### Result

The **ServiceNow Meetings Bot** card appears in Microsoft Teams.

## Configure Notify connector for Microsoft Teams app in Microsoft Teams

Configure the manifest file in Microsoft Teams admin center to use Notify connector for Microsoft Teams app.

### Before you begin

Role required: external\_app\_install\_admin, admin

### Procedure

1.  Log in to [Microsoft Teams admin portal](https://admin.teams.microsoft.com/).

2.  Navigate to **Teams apps** &gt; **Manage apps** &gt; **Upload new app** &gt; **Upload**.

3.  Search, select, and open \(in the Upload a custom app dialog-box\) the manifest file you downloaded.


### Result

The **ServiceNow Meetings Bot** card appears in Microsoft Teams.


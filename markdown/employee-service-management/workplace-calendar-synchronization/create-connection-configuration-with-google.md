---
title: Create a Connection and credential record for Google
description: Connect Google with the ServiceNow using the flow designer to synchronize reservations.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create a Connection and credential record for Google

Connect Google with the ServiceNow using the flow designer to synchronize reservations.

## Before you begin

Ensure the following:

-   [Authenticate Google for calendar synchronization](authenticate-google-for-calendar-sync.md).
-   Ensure that you have the Super admin role in Google.

Role required: admin

## About this task

Configure the Google connection and credential record. Perform steps in the flow designer. Configure the default Google Calendar spoke. You can also create your own connection and credential alias, if you don't want to configure the default Google Calendar spoke using the flow designer. To create your own alias, refer to [Configure your own Google connection and credential alias](../concept/configure-your-own-google-connection-and-credential-alias.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  In the **Search all connections** bar, search for Google.

4.  Select **Google\_calendar \(sn\_gcalendar\_spoke\)**.

5.  On the Google\_Calendar card, select **View Details**.

6.  Select **Configure** next to the **Google\_Calendar** connection.

7.  On the Configure Connection window, enter the following credentials:

    -   **Connection URL**: Enter `https://www.googleapis.com`.
    -   **API Version**: Enter `v3`. The field is auto-filled.
    -   **OAuth Client ID**: Enter the client ID that you copied while authenticating Google with ServiceNow in [Authenticate Google for calendar synchronization](authenticate-google-for-calendar-sync.md).
    -   **OAuth Client Secret**: Enter the client secret that you copied while authenticating Google with ServiceNow in [Authenticate Google for calendar synchronization](authenticate-google-for-calendar-sync.md).
    -   **OAuth Redirect URL**: Enter `https://<instance-name>.service-now.com/oauth_redirect.do`
    -   **OAuth Authorization URL**: Enter `https://accounts.google.com/o/oauth2/v2/auth`
    -   **OAuth Token URL**: Enter `https://www.googleapis.com/oauth2/v4/token`
8.  Select **Configure and Get OAuth Token**.

9.  In the Google window, log in to the Google Workspace and get the OAuth Token.

    Enter your Google Super admin credentials.


## Result

The Google connection and credential record is created. To view the connection and credential alias record, navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and select **Google\_Calendar**.

## What to do next

[Configure Google as calendar provider](configure-google-as-calendar-provider.md)


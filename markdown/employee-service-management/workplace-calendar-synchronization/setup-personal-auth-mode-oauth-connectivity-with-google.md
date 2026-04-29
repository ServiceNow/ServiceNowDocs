---
title: Set up personal authentication mode OAuth connectivity with Google
description: Create a personal authentication mode application registry for Google Calendar with your instance for OAuth authorization.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a personal authentication mode connection for Google, Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Set up personal authentication mode OAuth connectivity with Google

Create a personal authentication mode application registry for Google Calendar with your instance for OAuth authorization.

## Before you begin

[Authenticate Google for calendar synchronization](../task/authenticate-google-for-calendar-sync.md)

Ensure that the application scope is set to **Google Calendar Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope to set the scope of your application.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Google Calendar Spoke**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Google Calendar** OAuth Provider from the list of Application Registries.

3.  On the form, fill in the fields with the specified details.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, Google Calendar.|
    |Client ID|Client ID created during the app authentication in Google.|
    |Client Secret|The password you generated when creating the app in Google.|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |Token URL|OAuth server token endpoint. Enter `https://www.googleapis.com/oauth2/v4/token`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, Google Calendar.


## Result

The OAuth connectivity is added for Google.


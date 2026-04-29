---
title: Setup OAuth connectivity with Google Calendar
description: Create an application registry for Google Calendar with ServiceNow to synchronize reservations. Perform this app registration if you want to create your own connection and credential alias for Google Calendar.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 2
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Setup OAuth connectivity with Google Calendar

Create an application registry for Google Calendar with ServiceNow to synchronize reservations. Perform this app registration if you want to create your own connection and credential alias for Google Calendar.

## Before you begin

[Authenticate Google for calendar synchronization](authenticate-google-for-calendar-sync.md)

Ensure that the application scope is set to **Google Calendar Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope to set the scope of your application.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Google Calendar Spoke**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  Select **Connect to a third party OAuth Provider**

4.  On the form, fill in the fields with the specified details.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, Google calendar Own.|
    |Client ID|Client ID created during the app authentication in Google.|
    |Client Secret|The password you generated when creating the app in Google.|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization mode**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://accounts.google.com/o/oauth2/v2/auth`.|
    |Token URL|OAuth server token endpoint. Enter `https://www.googleapis.com/oauth2/v4/token`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

5.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, Google Calendar Own default profile.

6.  Create a OAuth Entity Scope.

    1.  In the OAuth Entity Scopes related list, select **Insert a new row...**

    2.  Enter the name as `Calendar` for the scope.

    3.  Enter the OAuth scope as `Calendar`.

    4.  Select the Save icon.

    5.  Similarly, create another scope and enter the following details:

        -   **Name**: calendar.events
        -   **OAuth scope**: calendar.events
    6.  Right-click the Application Registry form header and select Save.

        The system creates the scope records.

7.  Select **Update**.

8.  On the Application registry form, select the **OAuth Entity Profiles** related list.

    In the following steps, add the OAuth Entity Scopes that you created in Step 6 to the default profile.

    1.  Select the default entity profile, for example, Google Calendar Own default profile.

    2.  On the OAuth Entity Profile form, do the following:

        1.  In the OAuth Entity Profiles Scopes section, double-click **Insert a new row**.
        2.  Select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\).
        3.  Select `calendar` that is assigned to the OAuth provider that you created in Step 6.
        4.  Repeat the previous steps and also add `calendar.events`.
9.  Select **Update**.


## Result

The OAuth connectivity is added for Google.

## What to do next

[Create your own connection and credential alias for Google](create-own-connection-credential-alias-for-google.md)


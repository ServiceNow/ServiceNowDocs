---
title: Create your own connection and credential alias for Google
description: Instead of using the default Google\_Calendar alias, you can create your own connection and credential alias to use it with your Google Calendar provider.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 2
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create your own connection and credential alias for Google

Instead of using the default **Google\_Calendar** alias, you can create your own connection and credential alias to use it with your Google Calendar provider.

## Before you begin

[Setup OAuth connectivity with Google Calendar](setup-oauth-connectivity-with-google.md)

Ensure that the application scope is set to **Google Calendar Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Google Calendar Spoke**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the connection and credential alias.|
    |ID|The field is automatically generated after you save the form based on the specified **Name**.|
    |Application|Ensure that the application is set as **Google Calendar Spoke**|
    |Parent alias|Select **sn\_gcalendar\_spoke.Google\_Calendar**.|

4.  Select **Submit**.

    The Connection and Credential alias record is created. As the next step, you must create a OAuth 2.0 credential record.

5.  Create an OAuth 2.0 credential to use in the newly created connection and credential alias record.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **OAuth 2.0 Credentials**.

    4.  On the form, fill in the fields.

        |Field|Descriptions|
        |-----|------------|
        |Name|Name of the credential. Provide a unique name to differentiate from the default credentials provided by the application.|
        |Active|Option to activate the credential.|
        |OAuth Entity Profile|Select the default OAuth entity profile that was generated when you performed the app registry in [Setup OAuth connectivity with Google Calendar](setup-oauth-connectivity-with-google.md).|
        |Applies to|Specify how you want to apply to the MID servers.|
        |Order|Order for the credential.|

    5.  Select **Submit**.

        The credential record is created.

    6.  Open the credential record.

    7.  On the form, select **Get OAuth Token**.

        On the Google window that opens, enter your credentials.

    8.  Select **Update**.

6.  Configure connection for the connection and credential alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

    2.  Select the connection and credential record that you created in the initial steps.

    3.  On the form, in the Connections related list, select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the connection.|
        |Credential|Select the credential record that you created in Step 5.|
        |Connection alias|The field is automatically set with the connection and credential alias.|
        |Connection URL|Enter [https://www.googleapis.com](https://www.googleapis.com).|

    5.  Select **Submit**.


## Result

The connection and credential record is created with specified credentials and connections.

## What to do next

[Configure Google as calendar provider](configure-google-as-calendar-provider.md)


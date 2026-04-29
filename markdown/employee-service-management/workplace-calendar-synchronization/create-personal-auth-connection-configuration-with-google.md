---
title: Configure a personal authentication mode Connection and Credential alias for Google
description: Establish a personal authentication mode connection and credential alias for Google Calendar. Confirm that the values for the connection and credentials alias are set as specified.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a personal authentication mode connection for Google, Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure a personal authentication mode Connection and Credential alias for Google

Establish a personal authentication mode connection and credential alias for Google Calendar. Confirm that the values for the connection and credentials alias are set as specified.

## Before you begin

Confirm that the application scope is set to Google Calendar Spoke.

Role required: admin

## About this task

Configure the default connection and credential alias to use the default entity profile created during the personal authentication mode application registry.

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select **Google Calendar Personal Auth** connection and credential child alias type created for personal authentication.

3.  Perform the following to check the HTTP Connection details:

    1.  On the Connection &amp; Credential Aliases form, under the **Connections** tab, select **Google Personal Auth Connection** connection name.

    2.  In the **Connection alias** field, verify that the child alias inherits the properties from the parent alias.

    3.  Verify that the Connection URL is set to [https://www.googleapis.com](https://www.googleapis.com)https://www.googleapis.com.

    4.  Select **Update**.

4.  Perform the following to check the OAuth Credentials details:

    1.  On the Connection &amp; Credential Aliases form, under the **Connections** tab, select the credential name.

    2.  On the OAuth 2.0 Credentials form, verify that the **OAuth Entity Profile** is set with the default OAuth entity profile that was created when creating the personal authentication mode app registry.

    3.  On the OAuth 2.0 Credentials form, verify that the **Integration Type** is set to Personal.


## Result

The Connection and Credential alias is set.


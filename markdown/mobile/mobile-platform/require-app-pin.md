---
title: Require an app PIN for the mobile app
description: Require users to enter a PIN when the application has been inactive for five minutes. To require the mobile user to set and enter a local application PIN, add the system property glide.sg.require\_mobile\_application\_pin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/require-app-pin.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Require an app PIN for the mobile app

Require users to enter a PIN when the application has been inactive for five minutes. To require the mobile user to set and enter a local application PIN, add the system property **glide.sg.require\_mobile\_application\_pin**.

## Before you begin

Role required: admin

## About this task

Users generate a six-digit code for the app PIN. The PIN must be entered when they log in to an instance from their mobile device, or after the application has been inactive for more than five minutes. If your users have faceID, touchID, or similar biometric security configured on their phone, they can use biometric authentication in place of the PIN.

\[Omitted image "app-pin.png"\] Alt text: App PIN.

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.require\_mobile\_application\_pin**.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.require\_mobile\_application\_pin**|
    |Type|true \| false|
    |Value|true|

    **Note:** The mobile app is automatically locked after five minutes of inactivity. Users accessing the mobile app after a period of inactivity must enter their PIN code.


**Parent Topic:**[Mobile system property configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/additional-mobile-configuration.md)


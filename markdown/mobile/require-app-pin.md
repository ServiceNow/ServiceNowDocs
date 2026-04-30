---
title: Require an app PIN for the mobile app
description: Require users to enter a PIN when the application has been inactive for five minutes. To require the mobile user to set and enter a local application PIN, add the system property glide.sg.require\_mobile\_application\_pin.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Require an app PIN for the mobile app

Require users to enter a PIN when the application has been inactive for five minutes. To require the mobile user to set and enter a local application PIN, add the system property **glide.sg.require\_mobile\_application\_pin**.

## Before you begin

Role required: admin

## About this task

Users generate a six-digit code for the app PIN. The PIN must be entered when they log in to an instance from their mobile device, or after the application has been inactive for more than five minutes. If your users have faceID, touchID, or similar biometric security configured on their phone, they can use biometric authentication in place of the PIN.

![App PIN.](../image/app-pin.png)

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


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


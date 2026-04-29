---
title: Configure the blur app option to improve security
description: As a security feature, administrators can configure the mobile app to blur or appear blackened, depending on the operating system, when not in focus on a mobile device. When you double-click the home button on your mobile device to close apps or navigate back to where you left off, the ServiceNow app appears blurred or blackened.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the blur app option to improve security

As a security feature, administrators can configure the mobile app to blur or appear blackened, depending on the operating system, when not in focus on a mobile device. When you double-click the home button on your mobile device to close apps or navigate back to where you left off, the ServiceNow app appears blurred or blackened.

## Before you begin

Role required: admin

## About this task

Before you enable the **glide.sg.blur\_ui\_when\_backgrounded** system property, consider the following information.

**Important:**

-   **For both iOS and Android, as of the the 20.1.0 mobile client release**
    -   The **glide.sg.blur\_ui\_when\_backgrounded** system property is supported on both iOS and Android devices.
    -   By default, the value for this property is set to `false`, which turns it off.
    -   The screen share feature isn't supported.
    -   Users are prevented from taking screen shots and screen recordings.
-   **iOS specific**

    ServiceNow mobile apps appear blurred when not in focus on a mobile device.

    **Note:** For BlackBerry and Microsoft Intune variants, screen recordings and screenshots remain enabled.

-   **Android specific**

    ServiceNow mobile apps appear blackened when not in focus on a mobile device.


## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the record for **glide.sg.blur\_ui\_when\_backgrounded**.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.blur\_ui\_when\_backgrounded**|
    |Type|true \| false|
    |Value|true|


## Result

With the property in place, the app is blurred when not in focus.

![App is blurred when not in focus](../image/BlurApp.png)

**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


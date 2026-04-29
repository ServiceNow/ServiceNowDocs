---
title: Configure the mobile app to clear the copy/paste clipboard and block ability to share content
description: To have the mobile app clear the pasteboard when the app enters the background, as well as block the ability to share content, add the system property glide.sg.clear\_pasteboard\_when\_backgrounded.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System properties, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the mobile app to clear the copy/paste clipboard and block ability to share content

To have the mobile app clear the pasteboard when the app enters the background, as well as block the ability to share content, add the system property **glide.sg.clear\_pasteboard\_when\_backgrounded**.

## Before you begin

Role required: admin

## About this task

By default, content that you copy in the mobile app remains on your device's clipboard even after you close the mobile app. In addition, you can share copied content to an external app and to a non-native virtual agent. Use the system property **glide.sg.clear\_pasteboard\_when\_backgrounded** to change this default behavior.

**Important:**

-   Users can share content from text edit menus on Android devices.
-   iOS, Android, and third-party keyboards might allow pasting, sharing, or viewing clipboard history even when this property is set.
-   Content that is opened in an external browser is not part of a ServiceNow mobile app although it may appear to be on Android devices depending on the configuration. The clipboard is cleared when a user moves to an external browser. This means that users are able to copy data from the external browser to elsewhere on their phone.

In summary, setting this property discourages moving data out of the ServiceNow mobile apps, but does not prevent it. For a robust security solution, use a Mobile Application Management \(MAM\)/Mobile Device Management \(MDM\) with your mobile apps. For more information, see [Enterprise mobility management \(EMM\)](../concept/enterprise-mobility-management.md).

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.clear\_pasteboard\_when\_backgrounded**.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.clear\_pasteboard\_when\_backgrounded**|
    |Type|true \| false|
    |Value|true|


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


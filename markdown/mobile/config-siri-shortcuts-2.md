---
title: Configure a Siri shortcut
description: Change the destination screen of your Siri shortcuts to direct your users to a different screen than the default.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Siri shortcuts, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure a Siri shortcut

Change the destination screen of your Siri shortcuts to direct your users to a different screen than the default.

## Before you begin

Role required: admin

As an admin, you can change the destination screen of the three of default Siri shortcuts listed below. Creating new Siri shortcuts is currently not supported.

## Procedure

1.  In the web-based UI, enter `sys_sg_screen_shortcut.list` in the filter navigator.

2.  Open the record for the shortcut you want to modify.

    |Shortcut|Definition|
    |--------|----------|
    |com.servicenow.requestor.sc|Browse items and services|
    |com.servicenow.requestor.tasks|Open my tasks|
    |com.servicenow.requestor.request|Open my requests|

    **Important:**

    -   You can update the screen your user will navigate to when using a shortcut, however you cannot change the text of the shortcut.
    -   Open the record by clicking on the **Shortcut** field. Clicking on the **Screen** field will open the screen record rather than the shortcut record.
3.  In the screen shortcut record, update the **Screen** field by clicking the reference icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and selecting a screen. This screen displays to your users when they access the associated Siri shortcut.


**Parent Topic:**[Siri shortcuts](../concept/siri-shortcuts.md)


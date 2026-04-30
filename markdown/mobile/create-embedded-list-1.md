---
title: Configure an embedded list for a record screen
description: Create an embedded list that you can include as in a record screen.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Embedded lists for a record screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an embedded list for a record screen

Create an embedded list that you can include as in a record screen.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder appears in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select a record screen.![Record screen segments section of a record screen](../image/record-screen-seg-section.png)

    **Note:** You can also create a new screen segment for your list by clicking the **New** button.

4.  In the **Record screen segments** section of the record screen control panel, select the screen segment where you want to add an embedded list.

5.  In the **Embedded screen** section, click **Choose** to select a screen to embed.![Embedded screen section](../image/embedded-screen-section.png)

    **Note:** You can also click the **New** button create a new screen. For details on creating screens, see [Create a screen](sg-studio-configure-applet-screens.md).

6.  Find the screen to embed in the **Choose an item** pop-up and click **Apply**.

    **Warning:** A list section can only have one embedded screen. If one is already assigned, the **Choose** and **New** buttons appear disabled. To add a new embedded list, you must remove the existing one by clicking the remove \(![Remove icon](../image/remove-icon.png)\) icon to the right of the current embedded list.

7.  Click **Save** in the upper right corner of the screen to save your record screen.


## Result

Your form is configured with an embedded list. Your users can access this list on the form by tapping the tab with the name of this list.

## What to do next

To learn more about relationship data items used for embedded lists, see [Configure a relationship data item for an embedded list](sg-data-item-relationship.md).


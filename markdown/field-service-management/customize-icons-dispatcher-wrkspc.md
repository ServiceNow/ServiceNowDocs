---
title: Change the graphic for calendar event icons
description: Customize the icons that show on calendar events to clarify their purpose or match your organization's look and feel. You can substitute your existing icons from a different application so your interfaces match.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure settings for Dispatcher Workspace, Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Change the graphic for calendar event icons

Customize the icons that show on calendar events to clarify their purpose or match your organization's look and feel. You can substitute your existing icons from a different application so your interfaces match.

## Before you begin

Role required: wm\_admin

Make sure that **Enable icon display on calendar event** is enabled. For more information, see [Configure settings for Dispatcher Workspace](configure-workspce-settings.md).

## About this task

For a list of icons that show on calendar events, see [Calendar event icons in Dispatcher Workspace](../reference/calendar-event-icons.md).

**Warning:** You must understand JSON code to perform this procedure.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Calendar Event Body Iconography**.

2.  In the **Value** field, note the file name of the icon to be changed.

    The icon positions and default generating field types are:

    -   topIcon - The icon at the top left indicates the work type
    -   bottomFirstIcon - The first icon at the bottom right indicates whether a task is a crew task
    -   bottomSecondIcon - The second icon at the bottom right indicates whether a task is locked
    For information on changing the fields that determine whether the icon is displayed, see [Change the fields that display calendar event icons](add-event-icons.md).

3.  Select **All** search for **Images,** and select **Images** under **System UI**.

4.  Search for the file name of the icon to be customized.

5.  Open the image record.

6.  Select **here** if you see a message about editing the Global application.

7.  Select **Update**.

8.  Select **Choose File**.

9.  Open the new image file.

    Make sure that the name of the file you're adding matches the one that you're replacing.

10. Select **OK**.


## Result

The icon is updated and appears on calendar events in Dispatcher Workspace.


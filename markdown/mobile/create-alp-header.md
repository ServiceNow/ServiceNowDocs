---
title: Configure a launcher screen header
description: Create a launcher screen header to define how the title of the screen appears.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a launcher screen header

Create a launcher screen header to define how the title of the screen appears.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** in the menu.

4.  From the Record type list, select **Launcher screen \[sys\_sg\_applet\_launcher\]**, and then select one of the following options:

    -   **New**
    -   An existing launcher screen record
    Configuring the header title is required. You can also configure the header function instance, which is optional.

5.  To configure the header title, locate the Settings pane, and then select **New**.

    The launcher header screen appears where you can create a header title.

6.  Enter a new header title in the **Properties** field and select **Save**.

    To use a variable in the header title such as combining `Hello` with the variable `{username}`, use an existing header title record:

    1.  Instead of selecting **New** in the Settings pane, select **Choose**.
    2.  Select one of the base system header titles.
7.  To configure the header function instance, select **Launcher screen** in the menu on the left. In the Launcher screen page, locate the Header function instance section.

    When you configure a header function instance, an icon appears in the header:

    ![Screen capture of the mobile screen with the header function.](../image/header-function-instance.png "Header function instance icon")

    Tapping the icon takes a user to the destination screen that is configured with the header function.

8.  In the Header function instance section of the page, select **New**.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the header function instance. This name is internal and isn't visible to end-users.|
    |Display label|Label that is visible to end-users.|
    |Order|Optional field that you can use to set the order that the UI functions appear. If you have multiple functions, set **Order**.|
    |Active|Toggle that turns the header function on and off. If the toggle is enabled, the header function is enabled.|
    |Icon|Icon that appears in the header of the launcher screen.|
    |Function|Function that runs when a user taps on the icon in the header of the launcher screen.|

10. Select **Save**.



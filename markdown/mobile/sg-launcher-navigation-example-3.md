---
title: Use your navigation function as a top menu selection
description: Use your navigation function as a top menu selection to give your users access to the screen launcher from within a screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure navigation to a launcher screen, Navigation functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Use your navigation function as a top menu selection

Use your navigation function as a top menu selection to give your users access to the screen launcher from within a screen.

## Before you begin

Role required: admin

Your users can access the top menu function by tapping the icon in the upper right corner of a launcher screen. In these steps you add your navigation function to a top menu function of an existing screen. If you have not configured any screens, you need to do that first. For detail on that process, see [Create a screen](sg-studio-configure-applet-screens.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select the screen where you want to add the top menu function.

4.  In the **Top menu function instances** section of the screen record, select **New**.

5.  Complete the following fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your top menu function. This name is internal and isn't visible to end users.|
    |Description|Additional information about the top menu function.|
    |Display label|The label for this top menu function. Use a value to inform your users of what the action does. In this case, you could use the name of the destination screen launcher.|
    |Order|Optional field that you can use to set the order that the UI functions appear. If you have multiple functions, set **Order**.|
    |Active|Toggle that turns the top menu function on and off. If the toggle is enabled, the navigation function will be enabled as an option in the top menu.|
    |Disable offline|Toggle that turns the top menu function off when the device is offline.|
    |Icon|The icon that appears for the top menu function.|
    |Function placement|The function used by this top menu function. These fields are automatically populated.|
    |Button Emphasis|The button emphasis for the top menu function. This selection affects the color of the button. For a navigation function, select **Primary** or **Secondary**. These colors are determined by your mobile theme. For more information on configuring a legacy mobile theme, see [Create a theme for your mobile applications](sg-configure-theme.md).|
    |Function|The function used by this top menu function. Select the function you wish to use.|

6.  Select **Save**.


## What to do next

Test the top menu action using your mobile app. After completing the steps, you can see a menu icon in the upper right corner of your screen. Tapping the menu icon displays the items in the menu. Your navigation function appears in this list using the name you provided in the **Display label** field.

**Parent Topic:**[Configure navigation to a launcher screen](../concept/sg-launcher-nav-example.md)


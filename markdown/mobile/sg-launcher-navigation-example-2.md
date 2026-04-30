---
title: Use your navigation function as a quick action
description: Use your navigation function as a quick action if users need to frequently access the launcher.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure navigation to a launcher screen, Navigation functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Use your navigation function as a quick action

Use your navigation function as a quick action if users need to frequently access the launcher.

## Before you begin

Role required: admin

Quick actions appear on screen launcher pages and serve as a quick way to provide shortcuts to commonly used screens and actions. Add your navigation function as a quick action to give your users an easily accessible shortcut to the launcher defined in your navigation function.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select the screen where you want to add the quick action function.

4.  In the **Quick action function instance** section of the screen record, select **New**.

5.  Complete the following fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your quick action. This name is internal and isn't visible to end users.|
    |Description|Additional information about the quick action.|
    |Display label|The label for this quick action. Use a value to inform your users of what the action does. In this case, you could use the name of the destination screen launcher.|
    |Order|Optional field that you can use to set the order that the UI functions appear. If you have quick actions, set **Order**.|
    |Active|Toggle that turns the quick action on and off. If the toggle is enabled, the quick action will be enabled.|
    |Disable offline|Toggle that turns the quick action off when the device is offline.|
    |Icon|The icon that appears for the quick action in the UI.|
    |Function placement|The function used by this quick action. These fields are automatically populated.|
    |Button Emphasis|The button emphasis for the quick action. This selection affects the color of the button. For a navigation function, select **Primary** or **Secondary**. These colors are determined by your mobile theme. For more information on configuring a legacy mobile theme, see [Create a theme for your mobile applications](sg-configure-theme.md).|
    |Function|The function used by this quick action. Select the navigation function you wish to assign to this quick action.|

6.  Select **Save**.


## What to do next

Test the navigation using your mobile app. After completing the steps, you can see a quick action in your screen launcher with the label and icon you defined in these steps. Tapping the quick action will direct you to the screen launcher you defined in your navigation function.

**Parent Topic:**[Configure navigation to a launcher screen](../concept/sg-launcher-nav-example.md)


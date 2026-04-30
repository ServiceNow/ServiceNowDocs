---
title: Use your navigation function as a footer function
description: Footer functions enable your end users to take an action on a details segment of a form. You can use the navigation function you created to give your users access to the application launcher from within the details segment of your forms. Unlike the top menu function, the form footer button is visible at the bottom of the form.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure navigation to a launcher screen, Navigation functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Use your navigation function as a footer function

Footer functions enable your end users to take an action on a details segment of a form. You can use the navigation function you created to give your users access to the application launcher from within the details segment of your forms. Unlike the top menu function, the form footer button is visible at the bottom of the form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select the screen where you want to add the footer function.

4.  In the **Footer function instances** section of the screen record, select **New**.

5.  Complete the following fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your footer function.|
    |Description|Additional information about the function.|
    |Display label|The label for this footer function. Use a value to inform your users of what the action does. In this case, you could use the name of the destination screen launcher.|
    |Order|Optional field that you can use to set the order that the UI functions appear. If you have multiple functions, set **Order**.|
    |Active|Toggle that turns the footer function on and off. If the toggle is enabled, the header function is enabled.|
    |Disable offline|Toggle that turns the footer function off when the device is offline.|
    |Icon|The icon that appears for the footer function.|
    |Function placement|The function used by this footer function. These fields are automatically populated.|
    |Button Emphasis|The button emphasis for the footer function. This selection affects the color of the button. For a navigation function, select **Primary** or **Secondary**. These colors are determined by your mobile theme. For more information on configuring a legacy mobile theme, see [Create a theme for your mobile applications](sg-configure-theme.md).|
    |Function|The function used by this footer function. Select the function you created in previous steps.|

6.  Select **Save**.


## What to do next

Test the footer function using your mobile app. After completing the steps, you can see a footer function button at the bottom of your details segment. Tap the button to navigate to the screen launcher you defined in the previous steps.

**Parent Topic:**[Configure navigation to a launcher screen](../concept/sg-launcher-nav-example.md)


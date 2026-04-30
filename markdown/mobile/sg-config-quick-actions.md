---
title: Quick actions
description: Define quick actions for your launcher screen so that your users can access commonly used functions, such as transferring records or using a template in the mobile app.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Quick actions

Define quick actions for your launcher screen so that your users can access commonly used functions, such as transferring records or using a template in the mobile app.

## Before you begin

Role required: admin

## About this task

<table id="table_pll_qnn_rhb"><tbody><tr><td>

Define quick actions for a launcher screen so that your users can access commonly used functions.

 Users access quick actions by tapping the quick action icon.

 For Android users, this icon appears as a plus symbol \(![Android quick action icon](../image/quick-action-icon-ios.png)\) at the upper right corner of the launcher screen.

 For iOS users this icon appears as an ellipsis symbol \(![iOS quick action icon](../image/quick-action-icon.png)\)

</td><td>

![Quick actions screen.](../image/quick-actions-screenshot2.png)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category from the menu.

4.  Search for and select the launcher screen where you want to add a quick action.

5.  In the Launcher screen form, scroll down to the **Quick action function instance** section, and select **New**.

6.  In the form, complete the fields as needed.

<table id="table_rtm_514_5jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Enter a name for the quick action. This name does not display to end users.

</td></tr><tr><td>

Description

</td><td>

Enter a description that helps you identify the quick action.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Display label

</td><td>

Enter a descriptive label for the quick action. End users can view this label in the device screen.

</td></tr><tr><td>

Order

</td><td>

Enter a numerical value for the order of this quick action compared to other quick actions in this launcher screen. Quick actions with lower numberical values set for **Order** display first in the device screen.

 To view the relative order of all the quick actions in the launcher screen, select the launcher screen in the navigation menu. Then review the other quick actions in the **Quick action function instance** section of the form.

</td></tr><tr><td>

Active

</td><td>

Make sure the **Active** toggle is turned on so the quick action is enabled.

</td></tr><tr><td>

Disable offline

</td><td>

Enable this toggle to turn off the quick action when the device is offline. By default, this toggle is turned off, which means the quick action is enabled when the device is offline.

</td></tr><tr><td>

Icon

</td><td>

Icon that displays for the quick action. Select **Choose** to use an existing icon or select **New** to add one. For more information about creating an icon, see [Mobile icons](../reference/sg-mobile-icon.md).

</td></tr></tbody>
</table>7.  In the **Function placement** section, for **Button emphasis color**, select the emphasis color for the button from the following options.

    |Option|Description|
    |------|-----------|
    |None|No emphasis color is used on the button.|
    |Primary|The emphasis color is the color that is set as the primary color in the mobile theme that you are using.|
    |Destructive|The emphasis color is the color that is set as the destructive color in the mobile theme that you are using.|

    **Note:** For more information about mobile themes, see [Mobile theme color guidelines](../reference/sg-theme-colors.md). If you have enabled Next Experience theming for mobile, see [Next Experience theming for mobile](../concept/explore-ne-theming.md).

8.  In the **Function** section, select **Choose** to use an existing function or select **New** to create one.

    For information about creating a new function, see [Mobile functions](../concept/sg-studio-mobile-button-types.md).

9.  Select **Save**.



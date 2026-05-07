---
title: Configure the navigation bar and navigation tabs
description: Configure the navigation bar that appears at the bottom of the mobile app. Use navigation bar tabs to navigate to screens, launcher screens, as well as saved records, settings, and notifications pages.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Navigation bar, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure the navigation bar and navigation tabs

Configure the navigation bar that appears at the bottom of the mobile app. Use navigation bar tabs to navigate to screens, launcher screens, as well as saved records, settings, and notifications pages.

## Before you begin

Role required: admin

## About this task

Add a navigation bar to your mobile app, and add various types of navigation tabs relevant to your users’ requirements. You can either choose preconfigured tabs or create a tab based on an existing template. There are slightly different configurations for the launcher screen and screen tabs in comparison to the saved, notifications, and the settings tabs.

Screen and launcher screen navigation tabs can also contain a badge count. This badge is a number that displays next to the navigation tab, according to defined conditions. For example, the badge count can display information like the number of records in a list, or records in a record section.

The following is a short summary of each of the navigation tab types:

-   Launcher: Use this option to navigate to a launcher screen.
-   Screen: Use this option to navigate to a screen that shows record data or UI sections.
-   Saved: This option opens a page showing the user’s saved records.
-   Notifications: This option opens the Notifications page showing user-related notifications within the mobile app experience.
-   Settings: This option opens the Settings page where the user controls their mobile experience.

**Note:** Your navigation bar should only contain one of each of the following tab types, saved, notifications, and settings tabs. For more information, see the General guidelines for the navigation bar section in the topic [Navigation bar](../concept/sg-mobile-tab-bar.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select Navigation bar \[sys\_sg\_navigation\], and then select **New**.

5.  Enter a name for your navigation bar.

6.  Select or create navigation tab types to add to your navigation bar.

<table id="choicetable_opn_3z2_ccc"><thead><tr><th align="left" id="d75897e156">

Method to add navigation tabs

</th><th align="left" id="d75897e159">

Procedure

</th></tr></thead><tbody><tr><td id="d75897e165">

**Select existing navigation tabs**

</td><td>

1.  Select **Choose** in the Navigation tabs section.
2.  Select a navigation tab and then select **Apply**.
3.  Repeat steps a. and b. for each navigation tab you want to add.
4.  Select **Save**.


</td></tr><tr><td id="d75897e198">

**Create either a saved, notifications, or settings navigation tab type**

</td><td>

1.  Select **New** in the Navigation tabs section.
2.  Select either the Saved, Notifications, or Settings tab type, and then select **Continue**.
3.  In the new tab screen for the option you selected, do the following.
    1.  Enter a name for the tab in the **Label** field.
    2.  Select whether the tab should display in the navigation bar, by using the **Active** toggle.
    3.  In the Icon field, select whether to choose an existing icon or to create an icon for your navigation tab. Either do one of the following.
        1.  Select **Choose**, then choose an icon and then select **Apply**.
        2.  Select **New** to display the New icon form and then do the following:
            1.  Enter a name for the icon.
            2.  From the **Type** field, select `Image`.
            3.  In the Set appearance section, in the **Style** field, enter `Name`.
            4.  In the Set appearance section, in the **Value** field, enter the name of an image icon. For a list of image icon names, see [Image icons](../reference/image-icons.md).
4.  Select **Save**.


</td></tr><tr><td id="d75897e301">

**Create either a launcher or screen navigation tab type**

</td><td>

1.  Select **New** in the Navigation tabs section.
2.  Select either the Launcher or Screen tab type, and then select **Continue**.
3.  In the new tab screen for the option you selected, do the following.
    1.  Enter a name for the tab in the **Label** field.
    2.  Select whether the tab should display in the navigation bar, by using the **Active** toggle.
    3.  Depending whether you selected the launcher or screen navigation tab types, do one of the following.
        -   If you selected Launcher, then in the Launcher area either select **Choose**, select a launcher screen, and then select **Apply**. Alternatively, select **New** to create a launcher screen. This is the launcher screen users are directed to when they tap this navigation tab. For more information about creating a launcher screen, see [Create a launcher screen](launcher-screen-template.md).
        -   If you selected Screen, then in the Screen area, select **Choose**, select a screen, and then select **Apply**. This is the screen users are directed to when they tap this navigation tab.
    4.  In the Icon field, select whether to choose an existing icon or create an icon. Either do one of the following.
        -   Select **Choose**, then choose an icon and then select **Apply**.
        -   Select **New** to display the New icon form and then do the following:
            1.  Enter a name for the icon.
            2.  From the **Type** list, select `Image`.
            3.  In the Set appearance section, in the **Style** field, enter `Name`.
            4.  In the Set appearance section, in the **Value** field, enter the name of an image icon. For a list of image icon names, see [Image icons](../reference/image-icons.md).
            5.  Select **Save**.
    5.  Add a badge count to indicate the number of records that await your users’ attention for this tab.
        1.  Select **New** in the Badge count section.
        2.  Enter a name for the badge count in the **Name** field.
        3.  Select whether the badge should display in the navigation tab, by using the **Active** toggle.
        4.  In the Data section, select the table you want to apply your condition filter.
        5.  In the Conditions section, create conditions used to count records that match the condition to determine the badge count. The records that match the condition are displayed as a count on the navigation tab. For more information on configuring badge counts in the web-based UI, see [Configure badge counts on navigation bars](config-badge-counts-nav-bars.md).
        6.  In the Badge placement section, the fields **Location**, **Mobile component**, and **Component** all contain predefined values.
        7.  Select **Save**.
    6.  Add user criteria permissions to determine what criteria a user must meet in order to see this tab in their navigation bar. For more information,see [User roles and user criteria permissions for mobile apps](../concept/roles-user-criteria.md).
4.  Select **Save**.


</td></tr></tbody>
</table>7.  Select **Save**.

8.  Select the Navigation bar record from the Navigation tree, to view the navigation tabs you selected.

9.  Set the order of the navigation tabs to display in the navigation bar, by doing the following.

    1.  Select the value in the Order column for the navigation tab that you want to define.
    2.  Enter an order value.

        **Note:** Navigation tabs with lower values display to the left of the navigation bar.

    3.  Select the check option
    4.  Repeat these steps for each of the navigation tabs that you want to order.
10. Select **Save**.



---
title: Create a launcher screen
description: Use launcher screens in a dashboard layout, for users to access mobile screen types, as selected by you.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a launcher screen

Use launcher screens in a dashboard layout, for users to access mobile screen types, as selected by you.

## Before you begin

Role required: admin

## About this task

The launcher screen configuration page contains all the sections that make up a launcher screen. This topic details how to create a basic launcher screen page and subsequent topics detail the features you can configure for this feature. For example sections like the launcher screen header, search bar, UI sections, and quick actions.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Create a launcher screen by using one of the following methods.

<table id="choicetable_e2v_z3s_s1c"><thead><tr><th align="left" id="d81524e92">

Method

</th><th align="left" id="d81524e95">

Procedure

</th></tr></thead><tbody><tr><td id="d81524e101">

**Using the Screens menu option**

</td><td>

1.  Select the **Screens** option from the menu, and then select **New**.
2.  Select the Launcher screen type, and then select **Continue**.


</td></tr><tr><td id="d81524e128">

**Using the All mobile records menu option**

</td><td>

1.  Select the **All mobile records** option from the menu.
2.  From the **Record type** field, select Launcher screen \[sys\_sg\_applet\_launcher\], and then select **New**.


</td></tr></tbody>
</table>4.  Complete the following fields as needed.

<table id="table_fdm_zcv_33b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name for the launcher screen.

</td></tr><tr><td>

Title

</td><td>

Title of the launcher screen as listed on the mobile device.

</td></tr><tr><td>

Active

</td><td>

Toggle that sets whether the launcher screen is available or not.

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Available offline

</td><td>

Determine whether this launcher screen is available when the user is offline.

</td></tr><tr><td>

Header function instance

</td><td>

Determine if this launcher section contains a header section. For more information, see [Configure a launcher screen header](create-alp-header.md).

</td></tr><tr><td>

Search configuration

</td><td>

Determine if this launcher section contains a search area. For more information, see [Global search for mobile](../concept/mobile-search-config.md).

</td></tr><tr><td>

Launcher sections

</td><td>

Determine what UI sections are contained in this launcher screen. For more information, see [Launcher screen UI sections](../concept/alp-ui-sections.md).

</td></tr><tr><td>

Quick action function instance

</td><td>

Determine if this launcher section contains any quick action functions. For more information, see [Quick actions](sg-config-quick-actions.md).

</td></tr><tr><td>

Access control type

</td><td>

Option to assign either user role permissions or user criteria permissions for this launcher screen. For more information, see [User roles and user criteria permissions for mobile apps](../concept/roles-user-criteria.md).

</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this launcher screen. If you have selected no roles, users with any role have access to the launcher screen.**Note:** This field is available when User roles is selected in the **Access control type** field.

</td></tr><tr><td>

User criteria access

</td><td>

Determine which user criteria can access this launcher screen. If you have not selected any user criteria, all user have access to the launcher screen.**Note:** This field is available when User criteria is selected in the **Access control type** field.

</td></tr></tbody>
</table>5.  Configure the relevant sections for your launcher screen.

    You can add any of the following sections to a launcher screen, as detailed in these links: [Configure a launcher screen header](create-alp-header.md), [Global search for mobile](../concept/mobile-search-config.md), [Launcher screen UI sections](../concept/alp-ui-sections.md), and [Quick actions](sg-config-quick-actions.md).

6.  Select **Save**.



---
title: Configure an icon UI section
description: Use the icon UI section type to navigate to screens, launcher screens, and functions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an icon UI section

Use the icon UI section type to navigate to screens, launcher screens, and functions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the Record type list, select **Icon section \[sys\_sg\_navigation\_section\]**, and then select **New**.

5.  On the form, fill in the fields.

<table id="table_wdr_lhm_qrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Title

</td><td>

Name for the UI section.

</td></tr><tr><td>

Active

</td><td>

Toggle \(on or off\) that sets whether the icon section is usable.

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Hide header

</td><td>

UI section header visibility. If this option is enabled, the UI section header isn't visible.

</td></tr><tr><td>

Orientation

</td><td>

Orientation of the UI section. You can select either **Horizontal** or **Vertical**.-   Horizontal layout:

Use this section type to display icons for many screens or launcher screens in one horizontal view. Limit the name character count to 20 or fewer characters so it doesn't get cut off. Use the horizontal layout to group related screen or launcher screens that don't require counts.

-   Vertical layout:

Use the vertical layout for actionable items such as approvals or requests.

</td></tr><tr><td>

Display type

</td><td>

Option that defines whether the icon section contains images, icons, or cards with text \(basic\).

 Use the basic option if you want to emphasize the count number.

</td></tr><tr><td>

Display feed count

</td><td>

Displays a count of records within each screen. Use this option with both vertical and horizontal orientation.**Note:** Only icons that point to list and map screens display a count value.

</td></tr><tr><td>

Icon section destination

</td><td>

Destination where the user is redirected after clicking an icon. A destination can be a launcher screen, a screen, or a function.

 Select **Choose** to select an existing icon section destination or select **New** to configure one.

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
</table>6.  Select **Save**.

7.  To configure the number and format of columns in icon sections, select the more options menu \(![more options menu icon](../image/button-more-ios.png)\) at the top of the form, and then select **Open in platform**.

    The record opens in your instance web UI, where you can make the following configurations:

<table id="table_srm_cp5_rfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Column count

</td><td>

Number of columns displayed in each icon section. You can display from 1 to 3 columns. Selecting **None** displays one column.

 This field is available when you select **Vertical** in the **Orientation** field.

</td></tr><tr><td>

Wide column count

</td><td>

Number of columns displayed in each icon section for larger devices like tablets or phones in landscape mode. You can display from 1 to 4 columns. Selecting **None** displays one column.

 This field is available when you select **Vertical** in the **Orientation** field.

 **Note:** The selection made in the **Wide** column count field must be greater than the number in the **Column count** field.

</td></tr></tbody>
</table>8.  Right-click the banner and select **Save**.


## What to do next

After creating icon UI sections, you must associate the UI sections to a launcher screen so they're displayed. For more information, see [Add a UI section to the launcher screen](ui-section-to-launcher-screen.md).

To personalize your icon sections, see [Adding images to an icon section](add-image-icon-section.md).


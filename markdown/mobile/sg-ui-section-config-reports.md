---
title: Configure an analytics UI section
description: Use the analytics UI section to display previews of your data visualization charts. Use it to show different visualizations for data sources and provide access to a specific chart or list screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an analytics UI section

Use the analytics UI section to display previews of your data visualization charts. Use it to show different visualizations for data sources and provide access to a specific chart or list screen.

## Before you begin

Role required: admin

For an analytics UI section to display data visualizations you need both a mobile analytics preview and a chart screen with navigation functions. For more information, see [Create a mobile analytics preview](sg-mobile-dashboard-preview.md) and [Chart screen](../concept/chart-screen.md). A maximum of six analytics previews can be displayed in an analytics UI section.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **Analytics section \[sys\_sg\_chart\_section\]**, and then select **New**.

5.  On the form, fill in the required fields.

<table id="table_uks_1bf_dmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name for the analytics section.

</td></tr><tr><td>

Active

</td><td>

Whether the analytics section is displayed in the app.

</td></tr><tr><td>

Type

</td><td>

Type of analytics section. Select either Data Visualization Chart or Data Visualization Single Score. **Note:** The Chart and Single Score options are set to be replaced by Data Visualization Chart and Data Visualization Single Score.

</td></tr><tr><td>

Orientation

</td><td>

Orientation of the analytics section. You can select either**Horizontal** or **Vertical**. Orientation must be **Vertical** for the Data Visualization chart section type.**Note:** For Data Visualization Single Score:

-   Use a vertical view when you want all scores to be visible on the screen without scrolling or your titles or values are long.

-   Use a horizontal view when you want to display several scores in a scrollable section.

</td></tr><tr><td>

Define custom size

</td><td>

Enables you to define the card's dimensions within the analytics section.**Note:** This option only displays when you select Data Visualization Single Score in the **Type** field and Horizontal in the **Orientation** field.

</td></tr><tr><td>

Custom height

</td><td>

The height of cards in the record section. The range is from 42 through 296 pixels. This field is available when you select the field  **Define custom size**.**Note:** This option only displays when you select Data Visualization Single Score in the **Type** field and Horizontal in the **Orientation** field.

</td></tr><tr><td>

Custom width

</td><td>

The width of cards in the record section. The range is from 64 through 304 pixels. This field is available when you select the field  **Define custom size**.**Note:** This option only displays when you select Data Visualization Single Score in the **Type** field and Horizontal in the **Orientation** field.

</td></tr><tr><td>

Analytics previews

</td><td>

Determines the analytics preview to display in the section.

**Note:** You can display up to six analytics previews.

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
</table>6.  From the **Type** field, select either Data Visualization Chart or Data Visualization Single Score.

    **Note:** According to the selection made, different fields are available or unavailable.

7.  In the Analytics preview section, select the analytics previews you want to display.

    These are the analytics previews created in the Analytic Center.

    **Note:** You can display up to six analytics previews.

8.  Select **Save**.


## What to do next

After creating an analytics UI section, you must add the UI sections to a launcher screen so they're displayed. For more information, see [Add a UI section to the launcher screen](ui-section-to-launcher-screen.md).


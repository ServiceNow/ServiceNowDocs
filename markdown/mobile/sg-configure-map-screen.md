---
title: Configure a map screen
description: Configure a map screen so that your users can see location-based information on a map from their mobile app. The map highlights points of interest, and users can switch between a map view and list view to help them understand the information displayed on a map.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Map screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a map screen

Configure a map screen so that your users can see location-based information on a map from their mobile app. The map highlights points of interest, and users can switch between a map view and list view to help them understand the information displayed on a map.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the  **Screens**  category, and then select  **New**.

4.  Select the  **Map** option in the Create a screen page, and then select  **Continue**.

5.  In the New map screen record, complete the fields as needed.

<table id="table_qh2_dqv_wtb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name for the map screen. This name is displayed as the screen header and the name of the screen in the UI section.

</td></tr><tr><td>

Description

</td><td>

Additional information about your map screen.

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Fetch type

</td><td>

Fetch type settings determine when data is loaded into your screen. The following fetch types are available: `prefetch`, `on-demand`, `background`, and `dynamic`. For more information, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

Available offline

</td><td>

Option to determine whether the map screen is available in offline mode.

</td></tr><tr><td>

Hide screen name

</td><td>

Option to determine whether the screen name is not shown as the screen header. For example, this option is useful if the text already appears in the header name or if it does not provide any value to the user.

</td></tr><tr><td>

Hide filters and sorting

</td><td>

Option to determine whether to disable the filter and sorting option on the map screen.

</td></tr><tr><td>

Filter

</td><td>

Option to determine whether users can filter record types by category. Use this option to help users view specific sets of records.

</td></tr><tr><td>

Empty state

</td><td>

You can indicate to users, with the aid of a visual display, that the map does not contain any points of interest. For more information, see [Empty state display](../concept/empty-state-handling.md).

</td></tr><tr><td>

Top menu function instances

</td><td>

Option to determine whether to use top menu functions to display additional options.

</td></tr><tr><td>

UI parameters

</td><td>

Option to determine whether to use UI parameters for this screen.The UI parameter is a variable that affects how a field or UI element behaves. Use it to determine how a value can be entered or if it will be auto-populated for a UI element, based on what the user has done.

</td></tr><tr><td>

Role access

</td><td>

Option to determine the roles that a user requires to access the map screen on their mobile device. If no role is selected, then all user roles have access to the map screen.

</td></tr></tbody>
</table>6.  From the Icon section either create a new icon or choose an existing icon. This icon displays if you add your map screen to a launcher screen UI section.

7.  Create a screen segment to continue adding look-and-feel map elements to the screen. You can only create a single segment within each map screen.

    1.  From the **Screen segment** field, select the **+New** button.

        The New screen segment form displays.

    2.  In the New screen segment record, complete the fields as needed.

<table id="table_wsj_1gg_ytb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name for screen segment used in the map screen.

</td></tr><tr><td>

Order

</td><td>

The order where the property is displayed. **Note:** An entry in this field is not required as only a single segment is supported.

</td></tr><tr><td>

Screen

</td><td>

This field is not available.

</td></tr><tr><td>

Interleave sort

</td><td>

Option to determine whether the sort and order of a list is displayed in an ascending or descending order. This selection is relevant when you have multiple item streams.

</td></tr></tbody>
</table>8.  Create a stream of records that connect data items and list item configuration records to the screen.

    **Note:** Streams are records that connect data items and list item configuration records to the screen. You can configure multiple item streams within a map. Use this option to define different attributes within a map. For example, you can define different pin colors for each item stream, one for incidents and one for work order tasks.

    1.  From the Streams section, select the **+New** button.

        The location item stream displays.

    2.  In the **Name** field, enter a name of the location item stream.

    3.  In the settings section, do the following steps:

        1.  From the **Table** field, select the table to define location-based map pins and cards.
        2.  \(Optional\) In the **Interleaved** field, select the field that determines how to order your data items. This option is relevant if you have more than one item stream.

            **Note:** You select the data item later in this procedure.

        3.  From the **Location** field, select a reference to the location table. The selected option shows as a location on the map.
        4.  Select a pin color by either selecting a color from the grid or enter a hexadecimal value, and then select **Save**.
9.  Choose an existing data item or create a new data item. To create a new data item, see [Data items](../concept/sg-data-item.md).

    The data item returns data from a single table to be used for the map location item stream.

10. Choose an existing list item configuration that determines how each record appears in the list and the actions associated with it.

11. Select **Save**.


## Result

The configured map screen displays information from your data item plotted on a map, along with a list view to display details on each item.

![Map screen displaying the map view with highlighted items](../image/SGMapScreen.png "Map screen displaying the map view with highlighted items")

## What to do next

You can add your map screen within a record section and an icon section. When a user taps on the relevant icon, they are navigated to the configured map screen. For more information, see [Configure a record UI section](sg-ui-section-config-item.md) and [Configure an icon UI section](sg-ui-section-config-navig.md).


---
title: Configure a record screen for use with a list screen
description: Use a record screen as part of a list so that your users can see the details of a record from their mobile app.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a record screen for use with a list screen

Use a record screen as part of a list so that your users can see the details of a record from their mobile app.

## Before you begin

Role required: admin

## About this task

Your instance creates screen records automatically for calendar, list, and map screens. You can also create your own record screens manually.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder

3.  Select the **Screens** category, and then select the list screen where you want to configure a record screen.

4.  In the navigation menu, scroll down to the **Embedded Screen** section, and then select an existing Record screen or select **New** to create a new Record Screen.

5.  Under the **Embedded screen** section, select **New** to create a new embedded screen.

6.  Select the **Record** option in the Create a screen page, and then select **Continue**.

7.  Fill in the following fields as needed.

<table id="table_wrg_24n_lwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

The record screen name. This name is not visible to end users.

</td></tr><tr><td>

Description

</td><td>

Additional information about the record screen.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Fetch type

</td><td>

Settings that determine when data is loaded in your screens. Select from the following fetch types:

-   **Prefetch**: This option pre-loads record screen data when an end user accesses a list, calendar, or record screen.
-   **Background**: The app makes a background network request to load embedded screens or record screen segments.
-   **Dynamic prefetch**: Screens for the first 10 rows load as described for the **Prefetch** fetch type. After the 10 first rows load, additional rows of screens load with the **On-demand** fetch type.
-   **On-demand**: The app sends a network request to load the app only when end users navigate to it.
 For more information about fetch types, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

Dynamic prefetch count

</td><td>

You can change the number of rows loaded with prefetch by changing the value of the Dynamic prefetch count field.

</td></tr><tr><td>

Hide screen name

</td><td>

Option to determine whether the screen name is not shown as the screen header. This is useful if the text already appears in the header name or if it does not provide any value to the user.

</td></tr><tr><td>

View using \(Legacy Card/Card\)

</td><td>

A Card used for the header section of the record screen. Use the Mobile Card Builder to change the appearance of your mobile card or the fields displayed on the card. For more detail on using the Mobile Card Builder, see [Configure a record screen for use with a list screen](sg-configure-form-applet.md).The best practice is using **Card**.

</td></tr><tr><td>

Card

</td><td>

This is an element that visually displays information from different records. You can style this information by setting specific conditions for each information type

</td></tr><tr><td>

Icon

</td><td>

The icon that displays for your record screen. Select **Choose** to use an existing icon, or select **New** to configure one.

</td></tr><tr><td>

Alert

</td><td>

This is a mobile alert overlay for a record screen. Use it to inform users of an important message and to redirect them to a specific screen. Only one mobile alert is available per instance.

</td></tr><tr><td>

Data item

</td><td>

This defines what table you want data from and what conditions must be met for the data to be displayed.

</td></tr><tr><td>

Record screen segments

</td><td>

This is a UI element for switching between different lists on a single record screen. Use it to divide content into different areas on the screen.

</td></tr><tr><td>

Dynamic segments height

</td><td>

Sets the height for dynamically sized segments.

</td></tr><tr><td>

Dynamic segments minimum width

</td><td>

Sets the minimum width for dynamically sized segments.

</td></tr><tr><td>

Top menu function instances

</td><td>

Add additional functions to the top menu. Your users access the top menu function by tapping the icon in the upper right corner of a screen

</td></tr><tr><td>

UI parameters

</td><td>

UI parameters are variables that affect how a field or UI element behaves. Use UI parameters to determine how a value can be entered or whether it is automatically populated for the UI element based on the end user's action. Select an existing UI parameter or select **New** to add one. For more information about adding a UI parameter, see [Configure a parameterized record screen](configure-param-form-applet.md).

</td></tr><tr><td>

Dynamic screen title

</td><td>

Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen.

</td></tr><tr><td>

Role access

</td><td>

Allows you to create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include in the title of the destination screen.

</td></tr></tbody>
</table>8.  Under the **Card** section, select **New**.

9.  Fill in the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Properties|
    |Name|The card name. This name is not visible to end users.|
    |Description|Additional information about the card.|
    |Active|Toggle that determines whether this card will be displayed.|
    |Table|The table where the card gets its data from.|
    |Card template|The template that determines the card's UI element layout.|
    |UI rules|Determines how the mobile interface will change or which fields will update when certain conditions are met.|

10. In the Data section, select the table you wish to use.

11. Under **Card template**, either select **Choose** to use an existing card template, or select **New** to create a new one.

    Card templates can be customized further in Mobile Card Builder. For more information see [Customize a screen using Mobile Card Builder](mcb-customize-item-view.md).

    **Note:**

    To open your new card template in Mobile Card Builder you first need to save. An error will appear and notify you should any required fields be missing values.

12. Configure an activity stream screen for your record.

    For details on adding an activity stream, see [Configure an activity stream screen for a record screen](configure-activity-stream.md).

13. Select **Save**.



---
title: Configure a parameterized record screen
description: Configure a record screen to query a user for a parameter. The screen then uses this parameter to determine the record that appears on the screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a parameterized record screen

Configure a record screen to query a user for a parameter. The screen then uses this parameter to determine the record that appears on the screen.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder

3.  Select the **Screens** category, and then select **New**.

4.  Select the **Record** option in the Create a screen page, and then select **Continue**.

5.  Complete the following fields as needed.

<table id="table_qnm_qbk_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your screen. This name appears as a tile in the mobile application.

</td></tr><tr><td>

Description

</td><td>

Additional information about your screen.

</td></tr><tr><td>

Fetch type

</td><td>

Settings that determine when data is loaded in your screen. Select from the following fetch types:

 -   **Prefetch:** This option pre-loads record screen data when an end user accesses a list, calendar, or record screen.
-   **On-demand:** The app sends a network request to load the app only when end users navigate to it.
-   **Background**: The app makes a background network request to load embedded screens or record screen segments.
-   **Dynamic prefetch:** Screens for the first 10 rows load as described for the Prefetch fetch type. After the 10 first rows load, additional rows of screens load with the On-demand fetch type.


</td></tr><tr><td>

Dynamic prefetch count

</td><td>

You can change the number of rows loaded with prefetch by changing the value of the Dynamic prefetch count field.

</td></tr><tr><td>

Hide screen name

</td><td>

Option to hide the record's screen name.

</td></tr><tr><td>

View using \(Legacy Card/Card\)

</td><td>

A Card used for the header section of the record screen. Use the Mobile Card Builder to change the appearance of your mobile card or the fields displayed on the card. For more detail on using the Mobile Card Builder, see [Customize a screen using Mobile Card Builder](mcb-customize-item-view.md).

 The best practice is using **Card**.

</td></tr><tr><td>

Card

</td><td>

This is an element that visually displays information from different records. You can style this information by setting specific conditions for each information type.

</td></tr><tr><td>

Icon

</td><td>

Icon that appears in the header of the launcher screen.

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

Functions placed in the top menu of the record screen.

</td></tr><tr><td>

UI parameters

</td><td>

This is a variable that affects how a field or UI element behaves. Use it to determine how a value can be entered or if it will be autopopulated for a UI element based on what the user has done.

</td></tr><tr><td>

Dynamic screen title

</td><td>

This is how you can create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include it in the title of the destination screen.

</td></tr><tr><td>

Role access

</td><td>

Option to limit user access to the screen by role.

</td></tr></tbody>
</table>6.  On the Record screen form, select an existing data item or create a new one.

<table id="table_q1r_x2k_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data item.

</td></tr><tr><td>

Description

</td><td>

Additional information about your data item.

</td></tr><tr><td>

Table

</td><td>

Table where the data item gets its data from.

</td></tr><tr><td>

Group by

</td><td>

Determine what values the table will be grouped by.

</td></tr><tr><td>

Condition Type

</td><td>

Whether the conditions for the data item are declarative, scripted, or use an encoded query. Leave this field at its default setting.

</td></tr><tr><td>

Offline condition

</td><td>

Conditions to apply when the user sets the app to offline mode.

</td></tr><tr><td>

Parameters

</td><td>

Data Parameter used for filtering the data item. Use parameters to accept values passed from screens or other sources.

</td></tr></tbody>
</table>7.  In the Data item screen, create a new data parameter by selecting the **New** button in the Parameters field.

8.  In the New Data Parameter screen, enter a name for your parameter in the **Name** field, and select the parameter **Type**.

    The available types are Integer, String, Decimal, Boolean, Datetime, or Date. For more detail on available options when creating parametrized data items, see [Configure a parametrized data item](sg-config-parametrized-data-item.md).

9.  Use the left panel hierarchy tree to return to the data item you just created a data parameter for.

    In the **Condition** field, create a query that uses your parameter to filter your records.

10. Use the left panel hierarchy tree to return to the Record Screen and select **New** in the **UI Parameters field** to create a new parameter.

11. In the **Properties** section, enter a name for the UI parameter.

12. In the **Setting** section, fill in the following fields.

<table id="table_ilk_qhk_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input type

</td><td>

How your users enter a value for this parameter. Select from the following options:

 -   Text
-   Choice List
-   Search List
-   QR/Barcode


</td></tr><tr><td>

Table name

</td><td>

Table used for the choice list where users select a parameter value.**Note:** This field is visible only when **Input type** is set to **Choice list** or **Search list**.

</td></tr><tr><td>

Field name

</td><td>

The field used for the choice list where users select a parameter value.**Note:** This field is visible only when **Input type** is set to **Choice list** or **Search list**.

</td></tr><tr><td>

Default value

</td><td>

Default value for your parameter.**Note:** This field is only visible when **Default value type** is set to **Manual**.

</td></tr><tr><td>

Input style

</td><td>

Input style for your parameter. Select from **Inline** or **Popup**.

</td></tr><tr><td>

Default value type

</td><td>

Whether the parameter has a default value. Select **None** to have no default value, or **Manual** to enter a manual value in the **Default value** field.

</td></tr><tr><td>

Mandatory

</td><td>

Determines whether user input for the parameter is mandatory.

</td></tr><tr><td>

Placeholder text

</td><td>

Text that appears in the parameter entry field before the users enters a value.

</td></tr><tr><td>

Multi-select

</td><td>

Whether the user can select multiple values from the choice list.**Note:** This field is visible only when **Input type** is set to **Choice list**.

</td></tr><tr><td>

Search type

</td><td>

The type of search used when finding a parameter value.**Note:** This field is visible only when **Input type** is set to **Search list**.

</td></tr><tr><td>

Carried

</td><td>

Whether this parameter a carried parameter. Use carried parameters to move information between different screens and actions.

</td></tr></tbody>
</table>13. In the **Data Parameter Mapping** section, select the **Choose** button to create a new parameter mapping.

14. Select the data parameter you created for the data item.

15. Select **Apply**.

16. Select **Save**.


## Result

The UI parameter in your form is associated with the data parameter in your data item. When a user accesses this form, the screen prompts the user for a value for the parameter. The data item uses that value to filter the record displayed in the form.


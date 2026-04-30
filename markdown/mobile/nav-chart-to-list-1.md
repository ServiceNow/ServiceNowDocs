---
title: Create a parameterized list for your chart
description: Create the list that users see when they tap on your chart screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configure a navigation from a chart to a list screen, Chart screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a parameterized list for your chart

Create the list that users see when they tap on your chart screen.

## Before you begin

Role required: admin

Create a parameterized list to provide your users with the option to view the records that make up sections of your data visualization. The user taps on an area of the data visualization to drill down to a list of records. Creating a parameterized list is similar to creating a standard list. In addition to the steps used to create a standard list, you must create.

-   A parameterized data item for your list. This data item uses your parameter to filter what data is displayed in your list. In this case, the records from your chart screen.
-   A parameter on your list screen. This parameter stores the value passed into your list.
-   A screen UI parameter mapping to associate the parameter in your list with the parameter in your data item.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **List** option in the Create a screen page, and then select **Continue**.

5.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your list screen. This name appears as a tile in the mobile application.|
    |Description|Additional information about your list screen.|
    |Available offline|Option to determine whether the screen is available in offline mode or not.|
    |Hide screen name|Option to determine whether the screen name isn't shown as the screen header. This option is useful if the text already appears in the header name or if it doesn't provide any value to the user.|
    |Hide filters|Option to avoid the list from displaying a list filter.|
    |Icon|Icon used to represent your list screen when added to a launcher screen.|
    |Custom filter|Option to add a custom filter for filtering record types by category.|
    |Empty state|Configure what displays in an empty space when no data is available to show.|
    |Screen segments|Configure additional screen segments for the list screen.|
    |Top menu function instances|Add additional functions to the top menu. Your users access the top menu function by tapping the icon in the upper right corner of a screen.|
    |Footer function instances|Add additional functions to the footer. The form footer button is visible at the bottom of the form, usually on a details segment.|
    |UI parameters|Change how a field or UI element behaves.|
    |Dynamic screen title|Allows you to create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include in the title of the destination screen.|
    |Role access|Determine which user roles can access this screen. If you've selected no roles, users with any role will have access to the screen.|

6.  In the **Screen segments** section, select **New** to create a new screen segment.

7.  In the new Screen segment record, complete the following fields as needed.

<table id="table_k23_l5t_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Screen segment screen.

</td></tr><tr><td>

Order

</td><td>

The order in which the segment appears on the screen.

 Segments display from the lowest to the highest value.

</td></tr><tr><td>

Screen

</td><td>

Displays the list name from the list screen record.

</td></tr><tr><td>

Max number of offline rows

</td><td>

The maximum number of rows that is saved for offline viewing.

</td></tr><tr><td>

Streams

</td><td>

Records that connect data items and list item config records to the list screen.

</td></tr><tr><td>

Sort list stream interleave field

</td><td>

Determine whether the list stream interleave field is sorted in ascending or descending order.

</td></tr></tbody>
</table>8.  In the **Streams** section, select **New** to create a new stream section.

9.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the Stream.|
    |Table|Choose the relevant table.|
    |Interleaved field|Select the field that you want to use to interleave your data item.|
    |Data item|Define the table you want data from and what conditions must be met for the data to be displayed.|
    |List item config|Determine how each record appears and what actions are associated with it.|

10. In the **Data item** section, select **New** to create a new data item.

11. Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the Data item.|
    |Description|Additional information about the data item.|
    |Table|Choose the relevant table for the data item.|
    |Group by|Option to group table items.|
    |Condition type|Type of condition to use. For this example, choose **Append encoded query**.|
    |Append encoded query|Set the parameter that will carries the data from a chart to a list. This field only appears if **Append encoded query** is selected as the condition type.|
    |Parameters|Configure parameters to accept values passed from screens or other sources.|

12. In the **Parameters** section, select **New** to create a new parameter.

13. Complete the following fields as needed.

<table id="table_gw4_svt_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the data parameter.

</td></tr><tr><td>

Parent table

</td><td>

Table from where the data item gets its data. This table should be the same one as the records on your chart.

</td></tr><tr><td>

Parent

</td><td>

The parent data item.

</td></tr><tr><td>

Type

</td><td>

The type of data values being passed. In this example, choose **String**.

</td></tr><tr><td>

Default value

</td><td>

Optional default value.

</td></tr></tbody>
</table>14. Select **Save**.

15. Return to the main list screen from the top of the ServiceNow AI Platform configuration panel.

16. In the **UI parameters section**, select **New** to create a new parameter.

17. Complete the following fields as needed.

<table id="table_chc_1wt_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the UI parameter screen.

</td></tr><tr><td>

Display name

</td><td>

The display name for the UI parameter. It is the same as the Name property.

</td></tr><tr><td>

Parameter type

</td><td>

Choose whether this parameter affects a screen or a function.

</td></tr><tr><td>

Screen

</td><td>

Choose the relevant chart screen that the parameter is populated from

</td></tr><tr><td>

Input style

</td><td>

Whether the input styles for the UI parameter are None, inline or popup. In this case select **Inline**.

</td></tr><tr><td>

Mandatory

</td><td>

Determine if this variable is mandatory.

</td></tr><tr><td>

Placeholder text

</td><td>

Optional placeholder text

</td></tr><tr><td>

Input source

</td><td>

Whether the input styles for the UI parameter are auto-fill or user input. In this example, select **Auto fill**.

</td></tr><tr><td>

Input type

</td><td>

Whether the input styles for the UI parameter are None, GPS location, Date, Constant, Source field, User or Append encoded query. In this example, select **Append encoded query**.

</td></tr><tr><td>

Screen data parameter mapping

</td><td>

Determine which specific values you want to pass to this screen.

</td></tr></tbody>
</table>18. In the **Screen data parameter mapping** section, choose the relevant data parameter.

19. Select **Save**.


## What to do next

Configure the List item config for your list screen to choose the cards and fields that will appear on this list. For more information, see [List screen](../concept/list-screen.md).

If you're adding an analytics preview to the launcher screen UI section. See, [Configure an analytics UI section](sg-ui-section-config-reports.md).

**Parent Topic:**[Configure a navigation from a chart to a list screen](../concept/nav-chart-to-list.md)


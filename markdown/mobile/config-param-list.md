---
title: Configure a parameterized list screen
description: Configure a list screen to query a user for a parameter, which the screen uses to filter the records that appear on the screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Parametrized list screens, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a parameterized list screen

Configure a list screen to query a user for a parameter, which the screen uses to filter the records that appear on the screen.

## Before you begin

Role required: admin

Creating a parameterized list is similar to creating a standard list. In addition to the steps used to create a standard list, you must create:

-   A parameterized data item for your list. This data item uses your parameter to filter what data is displayed in your list.
-   A parameter on your list screen. This parameter stores the value passed into your list.
-   A screen UI parameter mapping to associate the parameter in your list with the parameter in your data item.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder

3.  Select the **Screens** category, and then select **New**.

4.  Select the **List** option in the Create a screen page, and then select **Continue**.

5.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|The name of your list screen. This name appears as a tile in the mobile application.|
    |Description|Additional information about your list screen.|
    |**Screen Settings**|
    |Available offline|Option to determine whether the screen is available in offline mode or not.|
    |Hide screen name|Option to determine whether the screen name is not shown as the screen header. This is useful if the text already appears in the header name or if it does not provide any value to the user.|
    |Hide filters|Option to prevent the list from displaying a list filter.|
    |Icon|Icon used to represent your list screen when added to a launcher screen.|
    |Custom filter|Option to add a custom filter for filtering record types by category.|
    |Empty state|Configure what displays in an empty space when no data is available to show.|
    |Screen segments|Configure additional screen segments for the list screen.|
    |Top menu function instances|Option to determine whether to use top menu functions to display additional options.|
    |Footer function instances|Option to determine whether to use footer functions to display additional options.|
    |UI parameters|Change how a field or UI element behaves.|
    |Dynamic screen title|Allows you to create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include it in the title of the destination screen.|
    |Role access|Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen. |

6.  In the **Icon** section either select an existing icon or create an icon.

    This icon displays in the launcher screen when you add it to your list screen. For more information about creating icons, see [Mobile icons](../reference/sg-mobile-icon.md).

7.  In the **Screen segments**section, select **New**.

8.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the screen segment screen.|
    |Order|The order in which the segment appears on the screen. Segments display from the lowest to the highest value.|
    |Screen|Displays the list name from the list screen record.|
    |Max number of offline rows|The number of rows displayed for offline viewing.|
    |Streams|Records that connect data items and list item config records to the list screen.|
    |**Interleave sort**|
    |Sort list stream interleave field|Determine whether the list stream interleave field is sorted in ascending or descending order.|

9.  In the **Streams** section, select **New**.

10. Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the stream.|
    |Table|Choose the relevant table that contains data to display in your list.|
    |Interleaved field|Select the field you want to use to interleave your data item.|
    |Data item|Data items are queries on a selected table that provide the data presented in a screen.|
    |List item config|Determine how each record appears and the actions associated with it.|

11. In the **Data item** section, select **New**.

12. Complete the **Properties** and **Data** sections as needed.

    For more information about creating a data item, see [Configure a standard data item](sg-studio-create-data-item.md).

13. In the **Parameters** section, select **New**.

14. In the **Data parameter** screen, in the **Name** field, enter a name for the parameter.

    Parameter names correlate most often with fields on a form. For example, type `Priority` as the parameter name when the field refers to priority.

15. From the **Type** field, select a data type for the parameter.

    The type determines how the user interacts with the mobile UI. For example, a type of Decimal or Integer tells the mobile device to open a numbers-only keypad. Select from the following types:

    -   **Integer**: Opens a numbers-only keypad
    -   **String**: Uses a full keyboard for input. Use the String type for list parameters, such as priority or state, or for reference fields, such as assigned to or caller.
    -   **Decimal**: Opens a numbers-only keypad
    -   **Boolean**: Opens a true or false selection option
    -   **DateTime**: Opens a calendar with an exact time selector
    -   **Date**: Opens a calendar
16. In the **Data item** form, in the Condition section, add a query condition for your parameter.

    The condition field should match the parameter for which you are querying the database. For example, if you are creating a data item to query the Priority field, create a condition for Priority called `{{data parameter}}`. Make sure that you select the data parameter that you created by selecting it in the condition builder.

    You now have a parameterized data item to use in your parameterized list. This example shows a parameterized data item that uses a parameter named Priority to filter the data items for a priority matching that parameter's value.

17. Navigate back to your list stream using the hierarchal configuration tree.

18. In the **Data item** field, select the parameterized data item you created in the previous steps.

19. Return to your list screen and select **New** under the **UI Parameters** to create a new UI parameter.

20. Complete the following fields as needed.

<table id="table_p4g_1mj_1xb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your UI parameter.

</td></tr><tr><td>

Display name

</td><td>

Automatically populated with the same text used for the **Name** field.

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Parameter type

</td><td>

This field is automatically populated.

</td></tr><tr><td>

Screen

</td><td>

This field is automatically populated.

</td></tr><tr><td>

Input style

</td><td>

Input style for your parameter. Select from **Inline, Popup,**or**None**.

</td></tr><tr><td>

Mandatory

</td><td>

Determines whether user input for the parameter is mandatory.

</td></tr><tr><td>

Placeholder text

</td><td>

Text that appears in the parameter entry field before the users enters a value.

</td></tr><tr><td>

Order

</td><td>

Optional field that you can use to set the order that the UI parameters appears. If you have multiple parameters, set **Order**.

</td></tr><tr><td>

Input source

</td><td>

Select whether the parameter input is from **User input**or **Auto fill**. Select **User input** for this example.

</td></tr><tr><td>

Input type

</td><td>

How your users enter a value for this parameter. Select from the following options:

 -   Text
-   Choice List
-   Search List
-   QR/Barcode
 Select **Choice list** for this example.

</td></tr><tr><td>

Carried

</td><td>

Whether this parameter a carried parameter. Use carried parameters to move information between different screens and actions.

</td></tr><tr><td>

Multi-select

</td><td>

Whether the user can select multiple values from the choice list. This field is visible only when the**Input type** field is set to **Choice list.**

</td></tr><tr><td colspan="2">

**Data**

</td></tr><tr><td>

Table

</td><td>

Table used for the choice list where users select a parameter value. This field is visible only when the **Input type** field is set to **Choice list** or **Search list**.

</td></tr><tr><td>

Field

</td><td>

The field used for the choice list where users select a parameter value. This field is visible only when the **Input type** field is set to **Choice list** or **Search list**.

</td></tr><tr><td>

Screen data parameter mapping

</td><td>

Determine what specific values you want to pass to this screen.

</td></tr></tbody>
</table>21. In the **Screen data parameter mapping** section, choose the data parameter you created in your data item.

22. Select **Save**.

23. We have added support for parameterized data item with an input form screen. For more details refer to [Parametrized data item support for input form screens](config-paramtrzed-data-item-screen.md).

    These steps will allow you to configure an input form screen that contains the inputs and variables that you want to use as part of the data item query condition. This feature is configured in the web-based UI instead of Mobile App Builder.

    **Note:**

    The input form screen can contain only inputs, only variables, or both inputs and variables for use as part of the data item query condition. For information about creating an input form screen, see [Configure an input form screen](parameter-screen-config.md).

    1.  Navigate to the target list, For example, if you want to configure a parameterized data item list screen:

        1.  Enter `sys_sg_list_screen.list` in the filter
        2.  Select the list screen that you want to be parameterized.
        3.  In the **Input Form Screen** field, search for the input form screen that you created.
        4.  Select **Update**.
    2.  Map the inputs or variables created in the input form screen to the data parameter as shown in the following table.

        |Field|Description|
        |-----|-----------|
        |Variable|Input form screen variable|
        |Screen|Target screen. This field automatically populates.|
        |Application|Application scope. This field automatically populates.|
        |Input|Input label from the input form screen|
        |Data parameter|Data parameter from the target screen data item|



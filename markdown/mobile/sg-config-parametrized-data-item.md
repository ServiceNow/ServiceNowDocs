---
title: Configure a parametrized data item
description: Configure a parametrized data item to filter and view just the relevant data according to the selected parameters.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a parametrized data item

Configure a parametrized data item to filter and view just the relevant data according to the selected parameters.

## Before you begin

Role required: admin

## About this task

Use the included examples to create a data item that allows users to open an incident list filtered by priority. The parameter created in the example is for priority. .

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Data** category from the menu, and then select **New**.

4.  From the Create a data item dialog box, select the type of data item you want to create, and then select **Continue**.

    Both the standard and relationship data items can include parameters.

5.  Complete the Properties and Data sections as needed.

    For more information about creating a data item, see [Configure a standard data item](sg-studio-create-data-item.md). For example, create a data item for open incidents.

    **Note:** To configure the Condition section you must first complete and save the parameter configuration.

6.  In the Parameters section, select **New**.

7.  In the Data Parameter screen, in the **Name** field, enter a name for the parameter.

    Parameter names correlate most often with fields on a form. For example, type `Priority` as the parameter name when the field refers to priority.

8.  From the Type field, select the data type of the parameter.

    The type determines how the user interacts with the mobile UI. For example, a type of Decimal or Integer tells the mobile device to open a numbers-only keypad. Select from the following types:

    -   **Integer**: Opens a numbers-only keypad
    -   **String**: Uses a full keyboard for input. Use the String type for list parameters, such as priority or state, or for reference fields, such as assigned to or caller.
    -   **Decimal**: Opens a numbers-only keypad
    -   **Boolean**: Opens a true or false selection option
    -   **DateTime**: Opens a calendar with an exact time selector
    -   **Date**: Opens a calendar
9.  Select **Save**.

10. In the Data item form, in the Condition section, add a query condition for your parameter.

    The condition field should match the parameter for which you are querying the database. For example, if you are creating a data item to query the Priority field, create a condition for `Priority is {{*priority*}}`. Make sure that you select the parameter that you created by selecting the search icon \( ![Search icon in Mobile App Builder](../image/mab-search-icon.png)\) in the condition builder.



    ![Mobile App Builder data item form showing paramerterized data configuration.](../image/mab-data-item-form.png)

    **Note:** Mobile App Builder indicates that an item is a parameter with curly brackets **\{\{…\}\}**.

11. Select **Save**.


## What to do next

After you create a data item, assign it to a screen. Data items with parameters require additional configuration in the screen. For more information on assigning a data item with parameters to a screen, see [Assign a data item with parameters to a list screen](sg-assign-param-data-item-screen.md).


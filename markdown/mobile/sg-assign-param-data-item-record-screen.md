---
title: Assign a data item with parameters to a record screen
description: When you associate a parametrized data item with a record screen, additional fields appear in the screen configuration that you must complete for the parameter to be applied.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure a parametrized data item, Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Assign a data item with parameters to a record screen

When you associate a parametrized data item with a record screen, additional fields appear in the screen configuration that you must complete for the parameter to be applied.

## Before you begin

Make sure that you have configured a data item that has parameters. For more information, see [Configure a parametrized data item](sg-config-parametrized-data-item.md).

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the Record option in the Create a screen page, and then select **Continue**.

5.  In the **Data item** field, select **Choose**.

6.  From the Choose an item menu, select the parameterized data item that you created, and select **Apply**.

7.  In the UI parameters section of your record screen, select **New**.

8.  In the New UI parameter screen, complete the following fields as needed. Some fields only appear when you select a specific input type.

    Use the fields on this form to determine how the user interacts with the UI.

<table id="table_vys_xqx_2fb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td colspan="2">

**Properties** section

</td></tr><tr><td>

Name

</td><td>

Name for the UI parameter. You can have multiple UI parameters with the same name so make sure you choose something you can easily discover later. The name you select appears in the mobile app. For this example, use Priority as the name.

</td></tr><tr><td>

Display name

</td><td>

Name that displays. This name automatically matches the input name.

</td></tr><tr><td colspan="2">

**Settings** section

</td></tr><tr><td>

Parameter type

</td><td>

Type of parameter. In Mobile App Builder, this field is automatically set to **Screen** when a new parameter is created from a screen record.

</td></tr><tr><td>

Screen

</td><td>

Screen record. In Mobile App Builder, this field is automatically set to the parent screen record.

</td></tr><tr><td>

Input style

</td><td>

How the user interacts with the UI. Choose from **Inline** or **Popup**. For this example, choose **Inline**.

</td></tr><tr><td>

Mandatory

</td><td>

Whether the user is required to enter information for that field. For this example, leave this check box cleared.

</td></tr><tr><td>

Placeholder text

</td><td>

Text that appears below the field type. This option does not appear if you have a default value selected.

</td></tr><tr><td>

Order

</td><td>

Field used for input ordering.

</td></tr><tr><td>

Input source

</td><td>

Determines whether the input is populated by the end user or automatically by the system. For this example, choose **User input**.

</td></tr><tr><td>

Input type

</td><td>

How the end-user input is added to the system. For example, if you want to add a parameter for the Assigned to field, select **Choice list** so that users have a list of options to choose from. Select from one of the following options:

 -   **None**: There is no input type.
-   **Text**: Provides a simple text field. This option works best for fields that require free text input. For example, work notes or resolution details. This is the default input type.
-   **Choice list**: Opens a list for the end user to select from. This option works well for reference fields that require specific information.

**Note:** The choice list input type returns a maximum of 1,000 results. For references that require more than 1,000 results, use the **Search list** input type.

-   **Search list**: Provides a search bar so that end users can search in a list.
-   **QR/Barcode**: Provides the option to search by QRC or barcode.


</td></tr><tr><td>

Carried

</td><td>

Use carried parameters to move information between different screens and actions.

</td></tr><tr><td colspan="2">

**Data** section

</td></tr><tr><td>

Table

</td><td>

The table name for which you want to create a UI parameter. For example, Incident.

 This field only appears if you select **Choice list** or **Search list** as the input type.

</td></tr><tr><td>

Field

</td><td>

The field name for which you want to create a UI parameter. For example, Priority.

 This field only appears if you select **Choice list** or **Search list** as the input type.

</td></tr><tr><td>

Default value type

</td><td>

The value that appears by default in the UI field. The Default value type field only appears for Function type parameters. Select one of the following options.-   **None**: There is no default text. This option works well for a list input type.
-   **Manual**: An additional field appears for you to enter a default term. For example, **Search for a field**. The manual default works well for search or text input types.


</td></tr></tbody>
</table>9.  In the Screen data parameter mapping section, select **Choose**,

10. From the Choose an item menu, select the data parameter you created with the data item, and then select **Apply**.

11. Select **Save**.

12. If you want the field on the mobile screen to be automatically populated with a value, configure the auto-fill parameters.

    1.  In the **Input source** field for the UI parameter record, select **Auto fill**.

    2.  In the **Input type** field, select from the following options.

        -   **GPS location**: Automatically inputs the location of the mobile device.
        -   **Date**: Automatically inputs the current date for the mobile device.
        -   **Constant**: Automatically inputs a constant value.
        -   **Source field**: Automatically inputs a value from a table field.
        -   **User**: Automatically inputs the currently logged in user.
        -   **Append encoded query**: Automatically inputs data from an encoded query.
    3.  Select **Save**.

13. Complete any additional screen fields as needed. For more information, see [Create a screen](sg-studio-configure-applet-screens.md).

14. Select **Save**.



---
title: Create an action function with parameters
description: Request additional information from your end users when they interact with an action. For example, you can allow your end users to provide a reason for rejecting an approval by adding a text input parameter to a Reject button. When you create an action item that has parameters, you must also configure the UI parameters for the action function.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create an action function with parameters

Request additional information from your end users when they interact with an action. For example, you can allow your end users to provide a reason for rejecting an approval by adding a text input parameter to a Reject button. When you create an action item that has parameters, you must also configure the UI parameters for the action function.

## Before you begin

Role required: admin

## About this task

The UI parameter fields don’t appear on the action function unless you’ve associated an action item with parameters to the action function.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** in the menu, and then select **New**.

    Complete the action function fields as needed. For more information on completing the fields for the action function, see [Configure an action function](sg-studio-config-action-function.md).

4.  Scroll down to the UI Parameters section of the form, select **New**, and complete the fields as needed.

<table id="table_vys_xqx_2fb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name for the UI parameter. You can have multiple UI parameters with the same name so make sure that you choose something you can easily discover later. If the parameter requires user input, use a user-friendly name.

</td></tr><tr><td>

Display name

</td><td>

UI label that displays on the app. This label is auto populated with the value from the **Name** field.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Parameter type

</td><td>

Select **Screen** or **Function**.

</td></tr><tr><td>

Screen/Function

</td><td>

Depending on whether you select **Screen** or **Function**, select the screen or function you want to use.

</td></tr><tr><td>

Input style

</td><td>

How the user interacts in the UI. Choose from **inline** or **pop-up**.

</td></tr><tr><td>

Mandatory

</td><td>

Whether the user is required to enter information for that field.

</td></tr><tr><td>

Placeholder text

</td><td>

Text that appears below the field type.

</td></tr><tr><td>

Order

</td><td>

The order in which the UI parameters are rendered on the screen.

</td></tr><tr><td>

Default value type

</td><td>

The value that appears by default in the UI field. Select one of the following options.-   **None**: There’s no default text. This option works well for a list input type.
-   **Manual**: A **Default value** field appears for you to enter a default term. For example, **Search for a field**. The manual default type works well for search or text input types.
-   **Source field**: Pulls in information from the field selected in the Field name section. If you select this option, a table name and field are required.


</td></tr><tr><td>

Input source

</td><td>

The source for the parameter input. Choose **User Input** or **Auto fill**.

</td></tr><tr><td>

Input type

</td><td>

The UI used to complete the variable. The available options in this field depend on the choice entered in the **Input source** field. Choose from one of the following options.-   **User input options:**
    -   **Text**

Provides a simple text field. This option works best for fields that require text, such as work notes or resolution details.

    -   **Choice list**

Opens a list for the user to select from. This option works well for reference fields that require specific information.

**Note:** The **Choice list** input returns a maximum of 1000 results. For references that require more than 1000 results, use the **Search list** input type.

    -   **Search list**

Provides a search bar so that users can search in a list. Select a reference field on a table for users to search on.

    -   **QR/Barcode**

Provides the option to search by QRC or barcode. Learn more about this feature in [Mobile barcode scanning](../concept/sg-mobile-scanning.md).

-   **Auto fill options**
    -   **GPS Location**

Auto-fills with the mobile user's location when the action is used. For details on this feature, see [Mobile location tracking configuration](https://www.servicenow.com/docs/access?context=mobile-location-tracking&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

    -   **Date**

Auto-fills with the date and timestamp of when the action is used.

    -   **Constant**

Auto-fills with a constant value. The **Constant value** field appears on the form when this choice is selected.

    -   **Source field**

Auto-fills from a specified field. The**Button parent table** and **Source field** fields appear on the form when this choice is selected.

    -   **User**

Auto-fills with the mobile user's user record.

    -   **Append encoded query**

Used to connect a chart screen to a list or record screen.

</td></tr><tr><td>

Carried

</td><td>

Whether this parameter is a carried parameter. Use carried parameters to move information between different screens and actions.

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Button parent table

</td><td>

Table used when using **Source field** as the default value type.

 This field is only visible when **Default value type** is set to **Source field**, **Input source** is set to **Auto fill**, and **Input type** is set to **Source field**.

</td></tr><tr><td>

Source field

</td><td>

The field used from the source field table.

 This field is only visible when **Default value type** is set to **Source field**, **Input source** is set to **Auto fill**, and **Input type** is set to **Source field**.

</td></tr></tbody>
</table>5.  In the **Action data parameter mapping** section, select **Choose** to select the data parameter that was created under the action item.

6.  Select **Save**.


## What to do next

Associate the function with a specific screen. For more information on how to associate the action, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).


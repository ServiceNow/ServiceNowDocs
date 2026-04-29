---
title: Configure an action item with parameters
description: Parameters determine the information you are passing into the action to ensure you are changing the correct record and to enforce required fields as needed. Create an action item with parameters to define the changes being made to an action and how the changes get made.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure an action item, Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an action item with parameters

Parameters determine the information you are passing into the action to ensure you are changing the correct record and to enforce required fields as needed. Create an action item with parameters to define the changes being made to an action and how the changes get made.

## Before you begin

Role required: admin

## About this task

Use action items to define what an action function does when a user uses that function. The following steps detail creating an action with parameters.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Functions** category and then select **New**.

4.  In the **Action item** area of the form, select **New** and complete the fields for the action item as needed.

    For more information on creating an action item, see [Configure an action item](sg-studio-create-action-item.md).

5.  In the **Data parameters** area of the Action Item form, select **New**.

6.  In the **Name** field of the Data Parameter field, enter the name of the data parameter.

    You can have multiple parameters with the same name, so choose a name that you can distinguish easily. Because the data parameter is created from the action item form, Mobile App Builder automatically populates the parent table and parent fields.

7.  From the **Type** list, select the type of parameter.

    The type determines how the user interacts with the mobile UI. For example, a type of Decimal or Integer tells the mobile device to open a numbers-only keypad. Select from the following types:

    -   **Integer**: Uses a numbers-only keypad for input.
    -   **String**: Uses a full keyboard for input. Use the String type for list parameters, such as priority or state, or for reference fields, such as **Assigned to** or **Caller**.
    -   **Decimal**: Uses a numbers-only keypad for input.
    -   **Boolean**: Uses a true or false selection option.

        **Note:** Making a **Boolean** mandatory has no effect. **Boolean** fields are always considered to have a value. A selected check box has a value of true and an unselected check box has a value of false. Either of these values satisfies the requirement of a mandatory field.

    -   **DateTime**: Uses a calendar with an exact time selector.
    -   **Date**: Uses a calendar.
8.  Enter a **Default value** if needed.

    This is the default value of the action item parameter. When a default value is entered, users do not need to enter a value.

9.  Select **Save**.

10. Navigate back to the action item using the menu.

    Confirm that the Data Parameter you created in Steps 5-9 appears in the **Data parameters** section of the Action item form.



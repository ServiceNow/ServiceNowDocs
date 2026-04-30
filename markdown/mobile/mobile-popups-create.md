---
title: Create a mobile pop-up
description: Learn how to display configurable mobile pop-ups based on real-time conditions. You can display these pop-ups at the mobile app login phase or after a button tap.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Mobile pop-ups, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create a mobile pop-up

Learn how to display configurable mobile pop-ups based on real-time conditions. You can display these pop-ups at the mobile app login phase or after a button tap.

## Before you begin

Role required: admin

Before configuring your mobile pop-ups, consider the following:

-   Mobile cards are used in the display of pop-ups. You can either design one of your own mobile cards or use one of the template cards provided. For more information, see [Mobile Card Builder](../concept/mobile-card-builder.md).
-   Supported button types that trigger pop-ups are action item and navigation. For more information, see [Action functions](../concept/mobile-actions.md).
-   All button locations are supported. For example, swipe, top menu action, and footer function.
-   Buttons are supported in the following UI sections, record, icon, media, and content. For more information, see [Launcher screen UI sections](../concept/alp-ui-sections.md).
-   Mobile pop-ups aren't supported in offline.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** drop-down list, select **Mobile event \[sys\_sg\_event\]**, and then select **New**.

5.  Complete the following fields as needed:

<table id="table_xrm_xw1_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

The name for your mobile event, which activates the mobile pop-up.

</td></tr><tr><td>

Description

</td><td>

Additional information about the mobile event.

</td></tr><tr><td>

Active

</td><td>

Whether the mobile event is activated.

</td></tr><tr><td>

Type

</td><td>

Type of event that triggers the pop-up.

</td></tr><tr><td>

Source table

</td><td>

The source table for this mobile event.

</td></tr><tr><td>

Source record

</td><td>

Determine either the mobile app config or the mobile function as the record that this event occurs on. The options are dependent on the selection made from the **Source table** field.

</td></tr><tr><td>

Event action

</td><td>

The action that occurs when the mobile event is triggered.**Note:** There can only be one action per event.

</td></tr></tbody>
</table>6.  Select from the **Type** field whether the triggered event occurs when the user logs in or when a button is selected.

    Select either:

    -   `OnLogin`: The mobile pop-up displays after a user enters their credentials and logs in.
    -   `OnButtonClick`: The mobile pop-up displays when the user selects a specified button function.
7.  Select from the **Source table** field the table that relates to the mobile event type you selected.

    **Note:** If you select `OnLogin` as the **Type**, the source table is Mobile app config \[sys\_sg\_native\_client\].

    If you select `OnButtonClick` as the **Type**, the source table is Function \[sys\_sg\_button\].

8.  Select **New** in the Event Action area, to define what happens when an event is triggered.

9.  Complete the following fields as needed, to create conditions in the event action form, for showing or not showing a mobile pop-up.

<table id="table_igw_my1_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

The name for your mobile event action.

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Type

</td><td>

The type of event action. Select **ShowPopup**.

</td></tr><tr><td>

Condition type

</td><td>

The conditions applied to this mobile event action.

 -   Declarative: Adds a condition builder to the form. For more information, see [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
-   Script: Adds a script condition field to the form.


</td></tr><tr><td>

Query condition script

</td><td>

Use scripts to determine the records to be returned. **Note:** This field only displays when you choose Script in the **Condition Type** field

</td></tr><tr><td>

Table

</td><td>

The table that contains the records to be returned.

**Note:** This field only displays when you choose Declarative in the **Condition Type** field.

</td></tr><tr><td>

Condition

</td><td>

Set conditions to determine what records are returned from the selected table. If a condition isn’t set, the query returns all records.**Note:** This field only displays when you choose Declarative in the **Condition Type** field.

</td></tr><tr><td>

Popups

</td><td>

Select the mobile pop-up to use and how it displays.

</td></tr></tbody>
</table>10. Select **ShowPopup** in the **Type** field.

11. Select either **Declarative** or **Scripted** in the **Condition type** field.

    Different fields display when you select either Declarative or Scripted conditions that apply to this mobile event.

12. Select **New** in the **Popups** field, to determine what the mobile pop-up looks like.

13. Complete the following fields as needed.

<table id="table_gxp_sz1_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

The name of the mobile pop-up.

</td></tr><tr><td>

Tap outside to close

</td><td>

Option to tap on your mobile screen outside of the pop-up area, to close the mobile pop-up.**Note:** If this option isn't selected, your pop-up card must contain a button to close the pop-up. Otherwise, this setting is ignored.

</td></tr><tr><td>

Blur background

</td><td>

Option to blur the background of your mobile screen. This option gives more emphasis to the pop-up.

</td></tr><tr><td>

Active

</td><td>

Whether the mobile event is activated.

</td></tr><tr><td>

Card

</td><td>

The card to be used for the pop-up.

</td></tr></tbody>
</table>14. Select either **Choose** to use an existing card or select **New** to create one from the **Card** field.

    For more information about creating cards, see [Mobile Card Builder](../concept/mobile-card-builder.md).

    **Note:** Two mobile pop-up card templates are provided with the base system. These templates are called Pop-up 01 and Pop-up 02.

15. Assign configurable functions or predefined functions to a button on a mobile pop-up card.

    **Note:** For more information about configurable functions, see [Mobile functions](../concept/sg-studio-mobile-button-types.md) and [Configure a card action using Mobile Card Builder](create-mca-with-mcb.md). Also, see the What to do next section in this topic.

16. Select **Save**.


## What to do next

You can add two types of functions to a button on a mobile pop-up card, configurable functions and predefined functions. Configurable functions enable developers to customize function behavior and functionality. Predefined functions have dedicated functionality, purpose built for mobile pop-ups. The following predefined functions are available:

-   Cancel: Dismisses the pop-up without performing any additional action.
-   Continue: Submits or proceeds with the original function from which the pop-up was triggered.
-   Logout: Logs out the user from the current instance and is navigated to the instance list page.

For more information, see [Mobile functions](../concept/sg-studio-mobile-button-types.md) and [Configure a card action using Mobile Card Builder](create-mca-with-mcb.md).

-   **[Assign predefined functions to mobile pop-ups](popups-system-button.md)**  
Use predefined functions within mobile pop-ups to perform actions like dismiss the pop-up, proceed with the suggested instruction, or log out of the instance.

**Parent Topic:**[Mobile pop-ups](../concept/mobile_popups.md)


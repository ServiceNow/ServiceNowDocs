---
title: Assign predefined functions to mobile pop-ups
description: Use predefined functions within mobile pop-ups to perform actions like dismiss the pop-up, proceed with the suggested instruction, or log out of the instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a mobile pop-up, Mobile pop-ups, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Assign predefined functions to mobile pop-ups

Use predefined functions within mobile pop-ups to perform actions like dismiss the pop-up, proceed with the suggested instruction, or log out of the instance.

## Before you begin

Role required: admin

## About this task

You can add two types of functions to a button on a mobile pop-up card, configurable functions and predefined functions. Configurable functions enable developers to customize function behavior and functionality. For more information, see [Mobile functions](../concept/sg-studio-mobile-button-types.md) and [Configure a card action using Mobile Card Builder](create-mca-with-mcb.md). Predefined functions have dedicated functionality, purpose built for mobile pop-ups. The following predefined functions are available:

-   Cancel: Dismisses the pop-up without performing any additional action.
-   Complete: Submits or proceeds with the original function from which the pop-up was triggered.
-   Log out: Logs out the user from the current instance and is navigated to the instance list page.

**Note:** You perform the assignment of mobile pop-up predefined functions in the web-based UI.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_view\_config.list** to display all available cards.

2.  Search for the card that you defined as a mobile pop-up and select the card.

3.  Select a card button element attribute listed within the **Card elements** tab.

    The Card element form displays.

4.  Select **New** in the Card element attribute area.

    The Card element attribute form displays.

5.  Enter `SystemButtonType` in the **Type** field.

6.  Enter a value for this system button in the **Value** field.

    The value can either be `Cancel`, `Proceed`, or `Logout`.

7.  Select **Submit**.

8.  Repeat steps 4 through 8 to add additional predefined functions to a mobile pop-up card.


**Parent Topic:**[Create a mobile pop-up](mobile-popups-create.md)


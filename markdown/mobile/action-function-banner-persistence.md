---
title: Define banner display persistence
description: Define if a message or banner displayed on a mobile device requires the user to acknowledge the receipt of the message.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Define banner display persistence

Define if a message or banner displayed on a mobile device requires the user to acknowledge the receipt of the message.

## Before you begin

Role required: admin

## About this task

Configure specific messages to remain on a screen until the user actively dismisses the message. By default, messages fade after a few seconds.

When a function button has multiple messages associated to it, then all associated messages are consolidated into a single message. If one of these messages contains a persistence attribute, then the single consolidated message adopts the persistence behavior.

Only one banner message is displayed at a time. Newer banner messages replace existing banner messages. This replacement occurs even if the original existing banner contains persistent attributes.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application sope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu.

4.  Select a function where you want to add the persistence banner behavior.

5.  In the Function record, make sure **Action item** is selected for the **Type** field.

6.  Scroll down to the **Messages** section, and enter text in the **Success Message** field.

7.  Scroll down to the **Button attributes** section and select an existing button attribute record or select **New** to add one.

8.  In the Button Attribute record, complete the following fields as needed to add the persistent behavior attribute.

    |Field|Description|
    |-----|-----------|
    |Button|Name of the button record. This information is automatically populated from the function record.|
    |Name|The button attribute. Select **alerts\_require\_dismissal**.|
    |Value|Whether the attribute is turned on. Enter `true` to turn on the attribute. By default, the Value is set to true.|

9.  Select **Save**.


## Result

A banner remains on the screen until the user actively dismisses it.

![Mobile screen with banner displayed awaiting user to tap the dismiss button.](../image/banner-persistence.png)


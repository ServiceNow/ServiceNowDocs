---
title: Implementing notification action with a script
description: Use the Script field in the Notification Action form to update and implement a notification action.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create provider notification, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Implementing notification action with a script

Use the **Script** field in the Notification Action form to update and implement a notification action.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

    A list of notifications shows up.

2.  Select an existing notification.

3.  Scroll down to the Notification Actions related list.

4.  Open the Notification Action form and choose between the following options to reach the Notification Action form:

    -   If there are no existing notification actions under Notification Actions related list, do the following.
        1.  Click **New Provider Action** under Notification Actions related list.
        2.  Select the type of notification action you would like to create from the Notification Action wizard.

            **Note:** Scriptable Action, Flow Action and Virtual Agent are the only types of notification actions available.

    -   If there is an existing notification action, select one from the list under Notification Actions related list.
    The Notification Action form shows up.

5.  On the form, update the fields as required.

    |Fields|Description|
    |------|-----------|
    |Name|Name of the actionable notification.|
    |Application|Scope of the actionable notification record.|
    |Notification|Name of the notification containing the actionable notification record.|
    |Active|Option to activate the actionable prompt record.|
    |Script|Script to implement the actionable notification.|

6.  Click **Update**.


**Parent Topic:**[Create provider notification](../concept/create-provider-notification-using.md)


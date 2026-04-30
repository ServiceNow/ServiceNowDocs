---
title: Send SMS workflow activity
description: The send SMS workflow activity to send short text messages using Notify to users' phones. This workflow activity can be added to any table.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send SMS workflow activity

The **send SMS** workflow activity to send short text messages using Notify to users' phones. This workflow activity can be added to any table.

## Notify requirements

To send SMS messages, you must add and configure a provider in Notify. For more information about configuring a provider, see [Configure a provider in Notify](../../../product/notify2/task/configure-providers-for-provider-selectors.md).

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_pgm_tfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From

</td><td>

Select the Notify phone number to use to send the SMS message.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to use JavaScript to determine which numbers to send the message to, and the Notify number to use to send the message.

</td></tr><tr><td>

To

</td><td>

Select any number of users to send the message to. The user record must have a E.164-compliant phone number or notification device configured for SMS messages.

</td></tr><tr><td>

To \(groups\)

</td><td>

Select any number of groups to send the message to. All members of that group with an E.164-compliant phone number or SMS notification device receive the message.

</td></tr><tr><td>

Message

</td><td>

Enter the message to send. You can add field values from the current record by using the **Select variables** box. You can also add values from the workflow scratchpad. If a field and a scratchpad variable have the same name, the field value is used. Because you can use variables in this message, it is not possible to determine the length of the message at design time. If the activity sends a message that is longer than supported by the telephony provider, the message is truncated and the instance logs a warning.

</td></tr><tr><td>

To \(script\)

</td><td>

Enter a script to determine which numbers to send the message to, and the Notify number to use to send the message. The script should return a JavaScript object with the format `{notify_number: \'...sys_id...\', users: [...], groups: [...], numbers: [...]}`. Specify the users or groups to send the message to as an array of sys\_id values. Specify other numbers as an array of E.164-compliant phone numbers.

 This field appears only if **Advanced** is selected.

</td></tr></tbody>
</table>## Conditions

The conditions determine which transition comes after this activity. This activity does not specify any conditions by default.

You can add an error condition to this activity. The activity transitions through the error condition if the Notify number used to make the call is not configured correctly or unable to send SMS messages, or if an error occurs while sending the SMS.


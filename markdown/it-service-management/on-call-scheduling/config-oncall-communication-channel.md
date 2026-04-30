---
title: Configure On-Call communication channel
description: Configure notification messages sent from a communication channel for on-call escalations. You can customize the notification content, the response keywords, table and the domain they apply, for a specific channel available in the base system such as Email and Microsoft Teams or a custom channel that is created.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure On-Call communication channel

Configure notification messages sent from a communication channel for on-call escalations. You can customize the notification content, the response keywords, table and the domain they apply, for a specific channel available in the base system such as Email and Microsoft Teams or a custom channel that is created.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter **on\_call\_communication\_channel\_config.list**.

    The **On-Call Communication Channel Configs** \[On-Call Communication Channel Configs\] table opens up on a new browser tab.

2.  Select **New**.

3.  On the form, fill in the details:

<table id="table_yr1_tqf_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Channel type

</td><td>

Type of channel associated with the communication channel configuration.

</td></tr><tr><td>

Channel default

</td><td>

Option to make this channel configuration serve as default configuration for the specified channel.

</td></tr><tr><td>

Channel subflow

</td><td>

Subflow that is triggered to send escalation notifications for the specified channel type.

</td></tr><tr><td>

Order

</td><td>

Priority for this configuration when multiple configurations exist for the same channel type and table.

</td></tr><tr><td>

Table

</td><td>

Table and its child tables on which the configuration is applicable.**Note:**

-   This field is visible only if the **Channel default** check box is cleared.
-   If no configuration is available or matched for the child table then the configuration that is available or matched for the parent table is considered for the child table.
-   If no configuration is available or is matched for both the parent and the child table, then the configuration for the specified channel with the **Channel default** check box selected, is considered.


</td></tr><tr><td>

Conditions

</td><td>

Conditions based on which the channel configuration is applied to the table or it's child tables.

</td></tr><tr><td class="sub-head" colspan="2">

Response Keywords

</td></tr><tr><td>

Accept keyword

</td><td>

Text or number keyword that is used to accept the escalation sent from channel type such as email or voice.**Note:** This field is read-only for SMS channel type.

</td></tr><tr><td>

Reject keyword

</td><td>

Text or number keyword used to reject the escalation sent from channel type such as email or voice.**Note:** This field is read-only for SMS channel type.

</td></tr><tr><td class="sub-head" colspan="2">

Messages - User

</td></tr><tr><td>

Title

</td><td>

Subject line that is displayed in escalation notifications to users for various channels, such as Email or Microsoft Teams.**Note:** This field is not available for SMS channel type.

</td></tr><tr><td>

Message

</td><td>

Message content included in escalation notifications sent to users through channels such as Email, SMS, and others.

</td></tr><tr><td>

Accept instruction

</td><td>

Instruction that is used to accept escalation sent to the user from channel type such as email or voice.

</td></tr><tr><td>

Reject instruction

</td><td>

Instruction that is used to reject escalation sent to the user from channel type such as email or voice.

</td></tr><tr><td class="sub-head" colspan="2">

Messages - Device

</td></tr><tr><td>

Title

</td><td>

Subject line that is displayed in escalation notifications to devices for various channels, such as Email or Microsoft Teams.**Note:** This field is not available for SMS channel type.

</td></tr><tr><td>

Message

</td><td>

Message content included in escalation notifications sent to devices through channels such as Email, SMS, and others.

</td></tr><tr><td class="sub-head" colspan="2">

Messages - Catch All

</td></tr><tr><td>

Title

</td><td>

Subject line that is displayed in escalation notifications sent to catch all users through various channels, such as Email or Microsoft Teams.**Note:** This field is not available for SMS channel type.

</td></tr><tr><td>

Message

</td><td>

Message content included in escalation notifications sent to catch all users through various channels such as Email, SMS, and others.

</td></tr><tr><td>

Accept instruction

</td><td>

Instruction that is used to accept escalation sent to the catch all users from channel type such as email or voice.

</td></tr><tr><td>

Reject instruction

</td><td>

Instruction that is used to reject escalation sent to the catch all users from channel type such as email or voice.

</td></tr></tbody>
</table>    **Note:** The following variables are used and applicable in the content for messages, titles, accept and reject instructions:

    -   Dynamic Variables: Placeholders like `{number}` represent field values from the source record. For example, you can reference fields such as `{caller_id.user_name}` for incidents.
    -   Reserved Variables: Functional placeholders, including Response keywords \(`{accept_keyword}`, `{reject_keyword}`\) and Notify variables \(`{message_number}`, `{on_call_group_notify_number}`\), are critical and cannot not be modified.
    -   Hyperlink Variables: `{URI}` and `{URI_REF}` generate clickable links in the notifications to the source record. `{URI}` appear as LINK, clicking which opens the source record while `{URI_REF}` appears as the clickable source record number, clicking which also opens the source record.
4.  Select **Submit**.


**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)


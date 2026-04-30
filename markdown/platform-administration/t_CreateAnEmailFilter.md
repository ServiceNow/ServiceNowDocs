---
title: Create an email filter
description: You can create email filters to apply a custom action script or filter actions when email matches your filter's conditions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email filters, Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email filter

You can create email filters to apply a custom action script or filter actions when email matches your filter's conditions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Filters**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the email filter.|
    |Application|Application scope of the email filter.|
    |Order|Priority that the email filter takes over other filters for the same table. To give the filter higher priority over other filters, enter a lower number.|
    |Active|Option to activate the email filter.|
    |Short description|Description of what the filter does.|
    |Conditions|Conditions to define which emails to filter.|
    |Condition script|Script to define which emails to filter. Use this script to access other tables, variables, or methods. For example, the condition script for the Ignore VCAL filter looks for the results of the EmailUtils script include, which detects vCalendar attachments.|
    |Action script|Script to define additional behavior to be performed when the filter condition evaluates to true. This might include an email action not included in the default filter actions. In the base system, the action script is used to produce the error string that is published to the email log \(**System Logs** &gt; **Email**\).|

4.  Right-click in the header bar and select **Save** from the context menu.

    The Filter Actions related list appears.

5.  Click **New** in the related list.

6.  Select how the system should react when the conditions of this filter evaluate to true.

    The two choices in the base system are: Mark as Ignored and Move to Junk. You can use the Action script to perform additional email tasks.

    **Note:** Before creating additional email actions with a script, see [Inbound Email Actions](../concept/c_InboundEmailActions.md). Like business rules, inbound email actions use both conditions and scripts and can provide a number of useful actions on emails the instance receives.


**Parent Topic:**[Email filters](../concept/c_EmailFilters.md)


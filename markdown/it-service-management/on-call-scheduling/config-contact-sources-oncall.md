---
title: Specify the sources of contact information for schedule notifications
description: Configure the communications methods that shift managers can choose from to send on-call schedule notifications. For example, add email and phone contact sources.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure or update an On-Call schedule, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Specify the sources of contact information for schedule notifications

Configure the communications methods that shift managers can choose from to send on-call schedule notifications. For example, add email and phone contact sources.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Contact Sources**.

2.  Click **New** and then fill in the form.

<table id="table_zcs_fn4_zhb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful display label for the type of contact source.

</td></tr><tr><td>

Table

</td><td>

Table that contains the contact source.

</td></tr><tr><td>

User Field

</td><td>

Reference field to the user table. This field appears only for some tables.

</td></tr><tr><td>

Active

</td><td>

Option to activate the contact source for use.

</td></tr><tr><td>

Source Type

</td><td>

Type of communication method.

</td></tr><tr><td>

Source

</td><td>

-   For email, the source of the email address.
-   For phone numbers, the source of the phone number.


</td></tr></tbody>
</table>    For all major on-call schedule email notifications, you can now decide where the links to an on-call schedule record are redirected. Instead of an on-call schedule record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call schedule record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
    -   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
    The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

3.  Click **Submit**.


**Parent Topic:**[Configure or update an On-Call schedule](create-update-schedule-oncall.md)


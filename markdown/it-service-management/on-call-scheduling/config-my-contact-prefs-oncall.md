---
title: Configure my availability and contact preferences
description: You specify your availability and the methods to use to contact you for On-Call escalations. The instance notifies you if an admin overrides your settings for some reason.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing schedules and request time-off, On-Call Scheduling, IT Service Management]
---

# Configure my availability and contact preferences

You specify your availability and the methods to use to contact you for On-Call escalations. The instance notifies you if an admin overrides your settings for some reason.

## Before you begin

Role required: itil or admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **My Preferences**

2.  On the **Contact Attempts** tab, click the + icon and fill in the **Availability** form.

<table id="table_l4t_lkz_whb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and meaningful name for this record of your availability settings.

</td></tr><tr><td>

User

</td><td>

The user for whom you are creating the availability \(typically yourself\).

</td></tr><tr><td>

Active

</td><td>

Option to enable this availability record. Select the check box to activate your availability.

</td></tr><tr><td>

Schedule type

</td><td>

Select an existing availability schedule or create a custom schedule.

</td></tr><tr><td colspan="2">

Use these fields to create a custom availability schedule:

</td></tr><tr><td>

Start time

</td><td>

If this shift is not an all-day shift, then specify the start time of your availability.

</td></tr><tr><td>

End time

</td><td>

The end time of your availability.

</td></tr><tr><td>

Repeat on

</td><td>

The time of a single duration. For example, if you select weekly repetitions, specify the days of the week when you are available.

</td></tr><tr><td>

Time zone

</td><td>

The time zone of your availability. **Note:** The time zone is not editable and is taken from your user's profile.

</td></tr></tbody>
</table>3.  Click **Submit.**

4.  On the **Contact Preferences** tab, click the contact **Attempt** method to configure.

    The **Contact Preferences** dialog box appears.

5.  Select the contact methods that the instance should use to contact you while you are on-call.

    The methods you select are the contact methods that the instance should use for this contact attempt. Depending on your instance configuration, you can specify any or all of the following notification methods:

    -   SMS text
    -   Email
    -   Slack
    -   Voice
    -   Microsoft Teams. For information on setting up this channel, see [Set up Microsoft Teams as a contact method for an on-call escalation](set-up-msteams-oncall.md).
    -   Mobile push. For information on setting up this channel, see [Set up mobile push as a contact method for an on-call escalation](set-up-mobile-push-oncall.md).
6.  Repeat the process for each contact attempt.

    **Note:** Admins can specify overrides of your contact methods for all members of your group. Override settings appear on the **Contact Overrides** tab.


**Parent Topic:**[Viewing schedules and request time-off](../../user-administration/concept/viewing-schedules-and-escalation.md)


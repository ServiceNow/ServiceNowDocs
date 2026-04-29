---
title: Override contact preferences for a shift
description: Override all shift members' contact preferences to enforce a communication channel, for example, in case of an emergency.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Override contact preferences for a shift

Override all shift members' contact preferences to enforce a communication channel, for example, in case of an emergency.

## Before you begin

Role required: rota\_admin, rota\_manager

## Procedure

1.  Use one of the following methods to open the Edit Escalation and Contact Preferences page:

    -   1.  Navigate to **On-Call Scheduling** &gt; **On-Call Schedules**. The On-Call Schedules page opens to the All On-Call Schedules tab.
2.  Click a schedule card.
3.  On the **Shifts** tab, click the Actions icon \(![Actions icon](../image/icon-actions.png)\) for the shift and select **Edit Escalation and Contact Preferences**.
    -   1.  Navigate to **On-Call Scheduling** &gt; **My Group Schedules**.
2.  Select the shift.
3.  Click **Edit Escalation and Contact Preferences**
2.  On the **Contact Preferences** tab, click the contact **Attempt** method to configure.

    The **Contact Preferences** dialog box appears.

3.  Select the contact methods that the instance should use for all shift members for the selected contact attempt.

    Depending on your instance configuration, you can specify any or all of the following notification methods:

    -   SMS text
    -   Email
    -   Slack
    -   Voice
    -   Microsoft Teams. For information on setting up this channel, see [Set up Microsoft Teams as a contact method for an on-call escalation](set-up-msteams-oncall.md).
    -   Mobile push. For information on setting up this channel, see [Set up mobile push as a contact method for an on-call escalation](set-up-mobile-push-oncall.md).
    **Note:** SMS and voice require that Notify is active.

4.  Enable the **Override user preference** option.


**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)


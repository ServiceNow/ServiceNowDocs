---
title: Escalation and reminder settings for rosters
description: Use the escalation settings to specify how and when escalations occur and when reminder notifications are sent.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Escalation and reminder settings for rosters

Use the escalation settings to specify how and when escalations occur and when reminder notifications are sent.

## Escalation and reminder settings

You can specify unique settings for each roster. When you configure a roster, you can specify

-   **Forced communication channel**: You can specify a mandatory communication channel: SMS, voice, Slack, email, Microsoft Teams, or mobile push.

    -   SMS and voice require that Notify is active.
    -   An on-call member must have an SMS device to receive SMS notifications. If the member does not have an SMS device, then no further attempts are made and the lack of an SMS device is logged.
    For information on setting up MS Teams as a notification channel, see [Set up Microsoft Teams as a contact method for an on-call escalation](../task/set-up-msteams-oncall.md).

    For information on setting up mobile push as a notification channel, see [Set up mobile push as a contact method for an on-call escalation](../task/set-up-mobile-push-oncall.md).

-   **Number of reminders**: The number of times the instance sends reminders to a person who does not reply within the time frame specified by **Time between reminders**.
-   **Time between reminders**: The time interval between sending reminders.

    **Note:** If an escalation trigger rule is defined for the On-Call: Conference Call Escalation workflow, then the time between reminders is set to 60 seconds irrespective of the **Time between reminders** field value in the associated escalation policy.

    For information about escalation policy, see [Create an escalation policy](../task/create-custom-esc-policy-oncall.md).

    For information about escalation trigger rule, see [Create an escalation trigger rule](../task/create-trigger-rule-oncall.md).

-   Values in the **Number of reminders** and **Time between reminders** fields determine the value in the **Time before escalation** field. For example, if **Number of reminders** is 2 and **Time between reminders** is 10 minutes, then the **Time before escalation** is 30 minutes. That is, the time that passes between the first notification of a non-responsive roster member and the first notification of the next member in the escalation path.

## Instructions

For detailed instructions, see [Configure a roster](../task/config-roster-oncall.md).

**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)


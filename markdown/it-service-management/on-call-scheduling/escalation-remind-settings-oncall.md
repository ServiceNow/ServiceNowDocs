---
title: Escalation and reminder settings for rosters
description: Use the escalation settings to specify how and when escalations occur and when reminder notifications are sent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/on-call-scheduling/escalation-remind-settings-oncall.html
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Define escalation process, On-Call Scheduling, IT Service Management]
---

# Escalation and reminder settings for rosters

Use the escalation settings to specify how and when escalations occur and when reminder notifications are sent.

## Escalation and reminder settings

You can specify unique settings for each roster. When you configure a roster, you can specify

-   **Forced communication channel**: You can specify a mandatory communication channel: SMS, voice, Slack, email, Microsoft Teams, or mobile push.

    -   SMS and voice require that Notify is active.
    -   An on-call member must have an SMS device to receive SMS notifications. If the member does not have an SMS device, then no further attempts are made and the lack of an SMS device is logged.
    For information on setting up MS Teams as a notification channel, see [Set up Microsoft Teams as a contact method for an on-call escalation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/on-call-scheduling/set-up-msteams-oncall.md).

    For information on setting up mobile push as a notification channel, see [Set up mobile push as a contact method for an on-call escalation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/on-call-scheduling/set-up-mobile-push-oncall.md).

-   **Number of reminders**: The number of times the instance sends reminders to a person who does not reply within the time frame specified by **Time between reminders**.
-   **Time between reminders**: The time interval between sending reminders.
-   Values in the **Number of reminders** and **Time between reminders** fields determine the value in the **Time before escalation** field. For example, if **Number of reminders** is 2 and **Time between reminders** is 10 minutes, then the **Time before escalation** is 30 minutes. That is, the time that passes between the first notification of a non-responsive roster member and the first notification of the next member in the escalation path.

## Instructions

For detailed instructions, see [Configure a roster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/on-call-scheduling/config-roster-oncall.md).

**Parent Topic:**[Designing an escalation process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/on-call-scheduling/designing-escalation-process-oncall.md)


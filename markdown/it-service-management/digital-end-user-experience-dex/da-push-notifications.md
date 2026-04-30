---
title: Desktop Assistant notifications
description: Desktop Assistant notifications enable your organization to communicate important updates to end users instantly, regardless of their device activity. This feature enables delivering critical information, supporting Major Incident Management and Proactive Engagement
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Desktop Assistant notifications

Desktop Assistant notifications enable your organization to communicate important updates to end users instantly, regardless of their device activity. This feature enables delivering critical information, supporting Major Incident Management and Proactive Engagement

**Note:** The administrators can now use Desktop Assistant as a channel to send notifications for any update or activity. This can be done by configuring the API \(Application Programming Interfaces\) with required parameters. For more information, see [API parameters to customize Desktop Assistant notifications](../reference/api-parameters-to-customize-desktop-assistant-notifications.md)

Desktop Assistant notifications provide a reliable way to inform end users of critical updates with minimal effort. These notifications provide updates for awareness but aren’t directly actionable.

Notifications are sent as system push notifications on Windows and macOS devices. You can also access notifications through the Desktop Assistant notification panel.

To learn more about viewing notifications in your Desktop Assistant, see [View notifications](../task/view-notifications.md).

Desktop Assistant supports notifications from the following applications in these ways:

-   Major Incident Management sends real-time updates about critical incidents to all configured recipients, with each notification delivered once per logged-in device. Major Incident Management provides updates to two recipient lists out of the box:
    -   All users in affected location\(s\): Major Incident Management sends the updates all the configured recipients in the affected locations. For example, a Major Incident Management notification informs all employees in affected locations of a sudden network outage, ensuring they’re aware of the issue.
    -   All users based on the application usage in the affected location\(s\): Major Incident Management sends the updates only to the configured recipients based the application usage in the affected locations. The recipient list consists of only users whose aggregated application usage is greater than zero during the selected aggregation period and aggregation frequency. The aggregation period and aggregation frequency can be any of the following:

        -   Daily: 1-7 days
        -   Weekly: 1-4 weeks
        -   Monthly: 1-12 months
        For example, if the aggregation frequency is set to daily and the aggregation period is 7, a message is sent to users in the affected location\(s\) whose aggregation application usage is greater than 0 over the last 7 days. Similarly, if the aggregation frequency is set to weekly and the aggregation period is 4, the message is sent to users in the affected location\(s\) whose aggregated application usage is greater than 0 over the last 4 weeks.

        By default, the aggregation frequency is set to **Daily**, and the aggregation period is **7**.

        This ensures that only relevant users receive useful updates, avoiding unnecessary notifications.

        To customize this out of box recipient list, **All users based on the application usage in the affected location\(s\)**, see [Update the recipient list for Major Incident Management updates based on application usage](../task/recipient-lists-for-mim.md).

        To create a notification for a particular incident using this recipient list, see [Compose communications for incidents and major incidents](../../service-operations-workspace/task/compose-communication-mim-sow.md).

-   Proactive Engagement uses Desktop Assistant to alert users about:

    -   Actions that users must take to maintain device health
    -   Issues detected on devices
    -   Steps to remediate issues by following the self-help instructions or using the URL that Desktop Assistant recommends
    For example, users receive alerts to restart their devices if they have not done so in the recommended duration.


You can define how long the system attempts to deliver notifications by configuring the Time-to-Live \(TTL\) value using the **sn\_dex\_desktop.sn\_desktop\_assistant.notification\_time\_to\_live** property. Older notifications exceeding the TTL are discarded.

**Note:** The Time-to-Live \(TTL\) value can be set to a maximum of seven days.

You can also disable notifications by following the steps in [Enable or disable notifications](../task/enable-notification.md).

**Note:** Notifications should appear on the end user’s devices within two minutes after generation.


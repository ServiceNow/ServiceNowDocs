---
title: Desktop Assistant notifications
description: Desktop Assistant notifications enable your organization to communicate important updates to end users instantly, regardless of their device activity. This feature enables delivering critical information, supporting Major Incident Management and Proactive Engagement.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Desktop Assistant notifications

Desktop Assistant notifications enable your organization to communicate important updates to end users instantly, regardless of their device activity. This feature enables delivering critical information, supporting Major Incident Management and Proactive Engagement.

Desktop Assistant notifications provide a reliable way to inform end users of critical updates with minimal effort. These notifications provide updates for awareness but aren’t directly actionable.

Desktop Assistant supports an optimum number of 400,000 notifications per day, with a maximum rate of 10,000 notifications per minute.

## Accessing notifications

Access Desktop Assistant notifications as system push notifications on Windows and macOS devices, or from the Desktop Assistant notifications list. For more information, see [View Desktop Assistant notifications](../task/view-notifications.md).

Notifications should appear on end users’ devices within two minutes of generation.

## Supported applications

Desktop Assistant supports notifications from Major Incident Management and Proactive Engagement.

-   Major Incident Management: Major Incident Management sends real-time updates about critical incidents to recipients in the following base system recipient lists.
    -   All users in affected locations: Updates are sent to all configured recipients in affected locations. For example, a Major Incident Management notification informs all employees in an affected location of a sudden network outage, ensuring they’re aware of the issue.
    -   Impacted application users in affected locations: Updates are sent only to impacted recipients in affected locations. To make sure only relevant users receive updates, the recipient list includes users with application usage above zero during a specified aggregation period and frequency. The aggregation period and frequency can be configured to one of the following options:

        -   Daily: 1–7 days
        -   Weekly: 1–4 weeks
        -   Monthly: 1–12 months
        By default, the aggregation frequency is set to **Daily**, and the aggregation period is **7** days.

        For example, if the aggregation frequency is set to daily and the aggregation period is seven days, notifications are sent to users in affected locations who have application usage above 0 over the last seven days. Similarly, if the frequency is set to weekly and the aggregation period is four weeks, notifications are sent to users in affected locations who have application usage above 0 over the last four weeks.

        Each notification is delivered once to every logged-in device.

        You can customize the **Impacted application users in affected location\(s\)** recipient list or create a notification for an incident using this list. For more information, see [Customize recipient list for Major Incident Management updates](../task/recipient-lists-for-mim.md) and [Compose communications for incidents and major incidents](../../service-operations-workspace/task/compose-communication-mim-sow.md).

-   Proactive Engagement: Proactive Engagement uses Desktop Assistant to notify users about the following device-related events:

    -   Actions that users must take to maintain device health.
    -   Issues detected on devices
    -   Steps to remediate issues by following the self-help instructions or using the linked resources.
    For example, end users receive alerts to restart their devices if they haven’t done so in the recommended duration.


## Configuring notifications

As a DEX administrator, you can configure and manage Desktop Assistant notifications.

You can configure API parameters to enable Desktop Assistant to send notifications for any update or activity. For more information, see [API parameters to customize Desktop Assistant notifications](../reference/api-parameters-to-customize-desktop-assistant-notifications.md).

You can define how long the system attempts to deliver notifications by configuring the time-to-live \(TTL\) value using the **sn\_dex\_desktop.sn\_desktop\_assistant.notification\_time\_to\_live** property. The TTL can be set to a maximum of seven days. Older notifications exceeding the TTL are automatically discarded.

You can also enable and disable Desktop Assistant notifications. For more information, see [Enable or disable Desktop Assistant notifications](../task/enable-notification.md).


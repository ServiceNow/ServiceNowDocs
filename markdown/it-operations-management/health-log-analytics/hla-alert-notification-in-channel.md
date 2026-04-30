---
title: Health Log Analytics alert notification in Slack or Microsoft Teams channels
description: Health Log Analytics sends notifications for new anomaly alerts in real time to Slack or Microsoft Teams channels. This built-in functionality frees you from having to continuously monitor logs to prevent incidents.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics alert notification in Slack or Microsoft Teams channels

Health Log Analytics sends notifications for new anomaly alerts in real time to Slack or Microsoft Teams channels. This built-in functionality frees you from having to continuously monitor logs to prevent incidents.

The notifications include the number of the alert, its description, severity, configuration item, state, and priority group. You can filter the alerts for which notifications are sent to your channel. For example, you may only want to receive alerts of a Major severity or a High priority group. By default, no notifications are sent on secondary alerts.

To support channel notification, the channel must be configured to receive Health Log Analytics notifications.

Starting with Version 33.0.27 - August 2024, Health Log Analytics uses the Microsoft Teams Graph spoke application to send notifications on new anomaly alerts. The application replaces the Microsoft Teams spoke plugin, which will be deprecated. If you're using an HLA version earlier than 33.0.27, follow the setup procedure in [Set up Health Log Analytics alert notifications in channels](../task/hla-notifications-in-channel.md). Otherwise, see [Set up Health Log Analytics alert notifications in a Microsoft Teams channel](../task/hla-notifications-in-ms-teams.md).

![Sample HLA alert notification in Microsoft Teams.](../image/hla-alert-notification-teams.png "Sample HLA alert notification in Microsoft Teams")

-   **[Set up Health Log Analytics alert notifications in channels](../task/hla-notifications-in-channel.md)**  
Set up notifications for new Health Log Analytics anomaly alerts in either a Slack or Microsoft Teams channel.
-   **[Set up Health Log Analytics alert notifications in a Microsoft Teams channel](../task/hla-notifications-in-ms-teams.md)**  
Set up notifications for new Health Log Analytics anomaly alerts in a Microsoft Teams channel.

**Parent Topic:**[Administering Health Log Analytics](hla-administer.md)


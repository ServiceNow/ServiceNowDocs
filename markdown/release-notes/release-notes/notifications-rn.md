---
title: Notifications release notes
description: The ServiceNow Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Notifications release notes

The ServiceNow® Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Yokohama release.

## Notifications highlights for the Yokohama release

-   Use the new email notifications dashboard with key metrics.
-   Use filter notifications that are based on categories, delivery channels, subscriptions, and digests for notification preferences.
-   Use the enhanced assignment group, advanced condition, and mandatory notifications for a provider framework.
-   Use the standard forms for custom notification preferences and delivery channels.

See [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/notifications.md) for more information.

## New in the Yokohama release

-   **[Email notifications dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/email-notifications-dashboard.md)**

    Use the new notifications dashboard with key metrics. This dashboard is available to administrators by default. You can configure this dashboard to enable access to other users.


## UI changes

-   **[Advanced filters options for notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/advanced-notification-prefrences.md)**

    Added categories, delivery channels, active or inactive notifications, subscriptions, and digest-enabled filter options for notification preferences.

-   **[Standard forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/advanced-notification-prefrences.md)**

    Enabled standardized forms across custom notification preferences and delivery channels.

-   **[Assignment group field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-add-assignment-group.md)**

    Extended the provider framework to add support for assignment groups.

-   **[Advanced condition field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/noti-new-update-notification.md)**

    Extended the provider framework to add an advanced condition.


## Changed in this release

-   **[Advanced filters in notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/advanced-notification-prefrences.md)**

    Use notifications filters for categories, delivery channels, active or inactive notifications, subscriptions, and digest enabled notifications.

-   **[Support for assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-add-assignment-group.md)**

    Send provider notifications for assignment groups and to users that are part of groups stored in sys\_user\_group table.

-   **[Advanced condition for provider framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/noti-new-update-notification.md)**

    Use an advanced condition to send a notification that is based on the current email record, changing field values, or system properties.

-   **[Mandatory notifications for provider framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/make-notification-mandatory-provider.md)**

    Make critical notifications mandatory for the provider framework.

-   **[Email bounce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/email-bounce.md)**

    Prevent resending bounced emails to the addresses that are known to generate bounces.


## Activation information

Notifications is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)


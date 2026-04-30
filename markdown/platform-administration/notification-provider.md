---
title: Provider notification
description: Send notifications directly to recipients via the provider on supported channels. Notifications can be simple messages for review, or actionable messages with buttons that users can select to perform certain actions.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Provider notification

Send notifications directly to recipients via the provider on supported channels. Notifications can be simple messages for review, or actionable messages with buttons that users can select to perform certain actions.

## Important terms

-   **Provider**

    A provider is an implementation that delivers notifications to destinations of a specific channel.

-   **Channel**

    A channel represents a particular communication mechanism with a recipient.

-   **Destination Type**

    A destination type represents a logical way of categorizing a destination for the underlying channel and is required to send via a channel, as well as set a preference. As an admin, you can modify the notification **Auto Opt-in** behavior for a destination type.

-   **Destination**

    A destination is a specific contact information of a recipient for a channel. It includes a destination type and an identifier suitable for use in the channel.

    Destination Type sent by default is either set to true or false during the adapter installation. This determines if the destination type is opt-in or opt-out.

    -   If sent by default is set to true, notifications are delivered to the recipients if they have not explicitly opted-in/out to receive a notification on the destination type.
    -   If sent by default is set to false, notifications are not delivered to the recipients if they have not explicitly opted in to receive the notification on the destination type.

## Destination preference precedence

Notifications are delivered to the destinations that honor the following preference precedence:

1.  Notification preference of the recipient
2.  Destination preference of the recipient
3.  Destination Type send by default. You also have the option to modify **Auto Opt-in** behavior for a destination type.

**Note:** Groups are not supported as recipients.

## Common content for a notification

Provide common notification content so that different notification channels can use the same generic content.

## Actionable notification

Enable provider admins to define an actionable notification and send it to users. You can also enable response actions.

**Note:** A notification should either have Common Content or Provider Content in order to be delivered to the recipients.

All the above-mentioned capabilities are applicable only for [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) providers.


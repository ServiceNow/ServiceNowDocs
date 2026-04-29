---
title: Configure a delivery channel for Virtual Agent notification
description: Configure a delivery channel for Virtual Agent notifications by specifying the messaging channel information to send notifications to users.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Virtual Agent notifications, Configure, Virtual Agent, Conversational Interfaces]
---

# Configure a delivery channel for Virtual Agent notification

Configure a delivery channel for Virtual Agent notifications by specifying the messaging channel information to send notifications to users.

## Before you begin

Ensure that a messaging channel is configured in your instance. Virtual Agent admins can only select one or more chat channels for the notification from the list of chat channels associated with the instance.

Role required: virtual\_agent\_admin

## About this task

Use the delivery channel to support multiple channels for the same notification content. The procedure to configure delivery channels depends on the channel type. There are two notification channel types: Messaging channels and chat channels. For more information about channels, see [Channels in Conversational Interfaces](../../conversational-interfaces/concept/ci-channels-overview.md).

Delivery channels are also part of multiple active conversations in Virtual Agent. See [Route Virtual Agent NLU notifications through multiple portals](t_route-va-notifications-multiple-portals.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select the notification for which you want to define or update content.

3.  In the notification Contents related list, open the notification content.

4.  Follow the procedure according to the channel type for the notification that you're configuring.

    -   To update delivery channels for messaging content, select **New** in the Delivery Channels related list.
    -   To update delivery channels for chat content, select the **Add/Remove multiple** option in the Delivery Channels related list.

        ![The Add/Remove multiple icon is highlighted next to Delivery channels on the Channels tab.](../images/VA-channels-button.png)

        Use the arrows to add or remove specific delivery channels from your Selected Delivery Channels list. When you've defined all applicable delivery channels, select **Save**.

        **Note:** The mweb channel is for the web client and the NASS channel is for enhanced chat. If no specific chat channel is defined, notifications are triggered to all available chat channels by default. Virtual Agent admins can modify the chat channels associated with a notification at any time.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Notification Content|Reference of the notification content pre-populates for the delivery channel.|
    |Active|Option to activate the delivery channel.|
    |Connection|Connection record for the messaging channel configured in the instance.|
    |Send From|Provider application for the selected messaging channel.|
    |Send To \(Table\)|Name of the table that you want to send the notifications to.|
    |Send To \(Field\)|Name of the field that you want to send the notifications to. This field is optional.|

6.  Select **Submit** \(new notification records\) or **Update** \(existing notification records\).


**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)


---
title: Enable Virtual Agent notifications
description: Enable Virtual Agent notifications so that your end users can receive notifications in supported Virtual Agent channels.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Virtual Agent, notifications, channels]
breadcrumb: [Configuring Virtual Agent notifications, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable Virtual Agent notifications

Enable Virtual Agent notifications so that your end users can receive notifications in supported Virtual Agent channels.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Enable notifications for your users in the appropriate channel:

<table id="table_zgd_scv_bdc"><thead><tr><th>

Channel

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enhanced chat

</td><td>

The **sn\_nowassist\_va.nass\_notification\_enabled** system property defaults to `true` in System Properties \(sys\_properties.list\). This property enables Virtual Agent notifications to appear to users within the enhanced chat. For more information on setting up Virtual Agent notifications, see [Configure a delivery channel for Virtual Agent notification](configure-delivery-channel.md).

</td></tr><tr><td>

Chat widget \(mweb\)

</td><td>

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.
2.  Select **Virtual Agent**.
3.  Under **Notifications**, slide the **Use notifications** toggle switch to enable notifications.

![Virtual Agent setting showing Use notifications toggle switch in inactive state.](../images/va-settings-notif-enabled-switch.png)

**Note:** You can also change the notification text color and background in chat branding configurations. For details, see [Set up your Virtual Agent bot's branding](../../conversational-interfaces/task/ac-configure-chat-branding.md).

</td></tr><tr><td>

Slack, Microsoft Teams, or Workplace messaging integrations

</td><td>

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and Integrations**.
2.  For the appropriate messaging integration, select **Enable notifications for all users**.

![Messaging Apps Integration page with the Enable notifications for all users field for Microsoft Teams option highlighted.](../images/va-enable-notif-adapter.png)

</td></tr><tr><td>

Custom chat integration

</td><td>

1.  Navigate to **All** and in the filter navigator, enter `sys_cs_channel.list`.
2.  In Messaging Channels, select the custom integration record to update.
3.  Select **Enable Notifications** to activate notifications.
4.  Select **Update**.
 For more information on configuring custom chat integrations, see[Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md).

</td></tr></tbody>
</table>    Notifications are sent to recipients via the Virtual Agent bot in the channels that you enabled.


**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)


---
title: Route Virtual Agent NLU notifications through multiple portals
description: Send notifications and other Virtual Agent messages through as many portals as desired.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual Agent, notifications, portals, multiple active conversations, notifications]
breadcrumb: [Using multiple active conversations in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Route Virtual Agent NLU notifications through multiple portals

Send notifications and other Virtual Agent messages through as many portals as desired.

## Before you begin

The multiple active conversations feature includes the ability to send notifications on incidents. You can configure your notifications to go to only one conversation on a specific portal, or to any number of concurrent conversations.

[Activate multiple active conversations in Virtual Agent](t_activate-multiple-active-conversations-va.md)

[Configure a delivery channel for Virtual Agent notification](configure-delivery-channel.md)

Role required: virtual\_agent\_admin or admin

**Note:** These instructions are for configuring Natural Language Understanding \(NLU\) conversations. Large Language Model \(LLM\) conversations are configured for multiple active conversations based on portals, with no configuration necessary.

## Procedure

1.  Navigate to **All** &gt; **sys\_notification\_va\_content.list**.

    A list of Virtual Agent Notification Contents appears.

2.  Select the Notification Content that you want to send through multiple portals.

    For example, to receive comments on Incidents, select the Incident commented Notification Content.

3.  Under the **Channels** tab, confirm that the Consumer account contexts pane is available after activating multiple active conversations for the chat widget.

    The Default Consumer Account Context will be visible in the pane.

    **Note:** This string should also match the portal where the conversation will be directed. For example, the SP portal will also be the name of the Consumer account context.

4.  To add a context, on the **Select target record** line, input the string matching the desired Consumer account context.

    **Note:** This string should also match the portal where the conversation will be directed. For example, the SP portal will also be the name of the Consumer account context.

5.  To remove a context, select it in the Consumer account contexts pane, then select the **X**.

6.  Select **Update**.


## Result

Messages with multiple contexts will now be sent through Virtual Agent to users at their matching portals.

**Parent Topic:**[Using multiple active conversations in Virtual Agent](../concept/c_multiple-active-conversations-va.md)


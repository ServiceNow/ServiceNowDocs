---
title: Activate multiple active conversations in Virtual Agent
description: Use the multiple active conversations system, in combination with defined context values and a default portal, to handle concurrent conversations with Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 1
keywords: [Multiplke active conversations, Virtual Agent, context values, default portal]
breadcrumb: [Multiple active conversations for Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Activate multiple active conversations in Virtual Agent

Use the multiple active conversations system, in combination with defined context values and a default portal, to handle concurrent conversations with Virtual Agent.

## Before you begin

A default context is necessary to start out with the multiple active conversations system. See [Set a default NLU context value for multiple active conversations](t_set-default-context-value-multiple-active-conversations.md) for more information.

Role required: virtual\_agent\_admin or admin

## About this task

Virtual Agent includes settings that let multiple conversations be carried out with the same user across multiple portals. Users can also receive updates and notifications sent to any number of portals \(determined by an administrator\) anywhere in their instance on ServiceNow AI Platform.

The multiple active conversations feature is inactive by default in Virtual Agent until toggled on. As of the Vancouver release, multiple active conversations are available through the chat widget; other channels may be incorporated in future.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  Under **multiple active conversations**, select **Manage settings**.

3.  Select **Activate**.

4.  Select **Save**.


## What to do next

With multiple active conversations activated, you can also send notifications from Virtual Agent to portals using the feature. See [Route Virtual Agent NLU notifications through multiple portals](t_route-va-notifications-multiple-portals.md) for more information.

**Parent Topic:**[Multiple active conversations for Virtual Agent](../concept/c_multiple-active-conversations-va.md)


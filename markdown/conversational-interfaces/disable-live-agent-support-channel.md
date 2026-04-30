---
title: Disable live agent support for a channel
description: Add the disable\_live\_agent property to the Channel Properties related list to exclude it from live agent support.
locale: en-US
release: xanadu
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Channels in Conversational Interfaces, Exploring Conversational Interfaces Console, Conversational Interfaces Console, Conversational Interfaces]
---

# Disable live agent support for a channel

Add the **disable\_live\_agent** property to the Channel Properties related list to exclude it from live agent support.

## Before you begin

Role required: admin

## About this task

The **disable\_live\_agent** property is replacing the **com.glide.cs.exclude.liveagent.support** system property to indicate that the channel doesn't support a live agent. If the **disable\_live\_agent** parameter is not set for the channel, the older system property will still be honored for the time being.

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the filter.

2.  Select a channel name in the table.

    For example, select **Alexa**.

3.  In the **Channel Properties** related list, select **New**.

4.  On the Custom Adapter Property New record form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter `disable_live_agent`.|
    |Value|Enter `true`.|

5.  Select **Submit**.


## Result

The **disable\_live\_agent** parameter displays in the Channel Properties related list.

![Alexa messaging channel record page, with disable_live_agent parameter highlighted.](../image/disable-live-agent-channel-param.png)

**Parent Topic:**[Channels in Conversational Interfaces](../concept/ci-channels-overview.md)


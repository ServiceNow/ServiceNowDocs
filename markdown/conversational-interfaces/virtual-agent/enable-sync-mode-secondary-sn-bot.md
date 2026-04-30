---
title: Enable synchronous mode on the secondary ServiceNow Virtual Agent instance
description: Enable synchronous mode on the secondary ServiceNow Virtual Agent instance to use ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Synchronous or asynchronous mode, Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable synchronous mode on the secondary ServiceNow Virtual Agent instance

Enable synchronous mode on the secondary ServiceNow Virtual Agent instance to use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect.

## Before you begin

**Note:** Now Assist capabilities are supported only in asynchronous mode. For more information, see [Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance](enable-async-mode-secondary-sn-bot.md).

Role required: admin

## Procedure

1.  On the secondary instance, navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.

2.  Select the Bot to Bot record.

3.  Select the **Synchronous** check box.

4.  Click **Update**.


**Parent Topic:**[Use ServiceNow Virtual Agent as a secondary bot in synchronous or asynchronous mode](../concept/use-servicenow-virtual-agent-as-a-secondary-bot-in-synchronous-or-asynchronous-mode_0.md)


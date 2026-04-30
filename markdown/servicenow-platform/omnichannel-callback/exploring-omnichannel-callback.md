---
title: Exploring Omnichannel Callback
description: Learn more about Omnichannel Callback and review its benefits.
locale: en-US
release: yokohama
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exploring Omnichannel Callback

Learn more about Omnichannel Callback and review its benefits.

## Omnichannel Callback overview

The Omnichannel Callback app is a ServiceNow AI Platform® capability that offers enhanced user experience by providing an option for agents to call users back rather than waiting in the queue for an available agent. For example, you can use the callback functionality to call users back when the agent wait time is long or when there are no agents available.

Callbacks are a well-received addition to any interactive voice response \(IVR\). You can invoke callbacks on any supported conversational integration channels.

## Omnichannel Callback workflow

In this workflow:

1.  Users seeking help from a live agent request for a callback when the live agent is either unavailable or the wait time to get to a live agent is long.
2.  Omnichannel Callback determines the availability of agents via ServiceNow® Advanced Work Assignment \(AWA\) and places a callback work item for an available agent.
3.  AWA picks up the callback task and places it in the callback queue.
4.  The agent receives a **Callback** accept card. If the agent decides to close the interaction or requeue the callback manually, the agent can do so from the workspace.

## Omnichannel Callback benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Omnichannel Callback creates callback work items for available agents via AWA. Callback requests are placed in the AWA queue immediately upon submission. If the customer does not answer the initial callback, the agent has the option to manually initiate a retry. In such cases, the callback is re-queued according to the retry mechanism defined in the system.|Recurring Callback|Agents|
|Users requesting a callback can schedule by date and time based on the available time slots. Omnichannel Callback provides the framework for the scheduled callback. Consumer use cases for scheduled callback are currently supported via Customer Service Management \(CSM\) application only.|Scheduled callback|Customers|
|The user can request for a video callback at an appointed time. Currently, video callback is supported only via the Zoom service and requires the Zoom extension for Omnichannel Callback Store app. For more information, see [Zoom extension for Omnichannel Callback](../../zoom-channel-omni-callback/Concept/zoom-extension-omni-callback.md).|Video callback|Customers|


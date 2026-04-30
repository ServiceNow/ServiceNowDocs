---
title: Exploring Omnichannel Callback
description: Learn more about Omnichannel Callback and review its benefits.
locale: en-US
release: xanadu
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: concept
last_updated: "2024-08-01"
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

<table id="table_ldh_glm_jyb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Omnichannel Callback creates callback work items for available agents via AWA. Callback requests are placed in the AWA queue immediately upon submission. If the customer does not answer the initial callback, the agent has the option to manually initiate a retry. In such cases, the callback is re-queued according to the retry mechanism defined in the system.

</td><td>

Recurring Callback

</td><td>

Agents

</td></tr><tr><td>

The agent can directly call the end user. **Note:** When an agent dials the end user through **Click to Call**, the auto-scheduled callback logic does not count the attempt toward the remaining callback attempts.

</td><td>

Click to Call

</td><td>

Agents

</td></tr><tr><td>

Users requesting a callback can schedule by date and time based on the available time slots. Omnichannel Callback provides the framework for the scheduled callback. Consumer use cases for scheduled callback are currently supported via Customer Service Management \(CSM\) application only.

</td><td>

Scheduled callback

</td><td>

Customers

</td></tr><tr><td>

The user can request for a video callback at an appointed time. Currently, video callback is supported only via the Zoom service and requires the Zoom extension for Omnichannel Callback Store app. For more information, see [Zoom extension for Omnichannel Callback](../../zoom-channel-omni-callback/Concept/zoom-extension-omni-callback.md).

</td><td>

Video callback

</td><td>

Customers

</td></tr></tbody>
</table>
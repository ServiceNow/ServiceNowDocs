---
title: Unified routing of email interactions via CCaaS
description: Leverage a unified routing solution through Contact Center as a Service \(CCaaS\) to streamline email interactions using consistent routing logic across voice, chat, and other digital channels. This centralized approach eliminates the need for disparate systems, instead routing all interactions through a single, unified engine.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Unified routing of email interactions via CCaaS

Leverage a unified routing solution through Contact Center as a Service \(CCaaS\) to streamline email interactions using consistent routing logic across voice, chat, and other digital channels. This centralized approach eliminates the need for disparate systems, instead routing all interactions through a single, unified engine.

## CCaaS routing benefits

CCaaS routing offers the following benefits:

-   Unified routing across channels: CCaaS uses a single routing engine to manage channels like email and voice, making customer interactions easier to handle. This unified system provides a smooth omnichannel experience for agents and customers.
-   Reduced configuration and administrative effort: CCaaS unified routing streamlines operations by automating interaction assignments, minimizing the need for complex setup and ongoing management, and reducing manual workload.

## Managing email interactions on hold and rerouting

Agents can place email interactions on hold while they wait for customer responses. When an interaction is placed on hold, CCaaS is notified of this status change, which enables the system to reassign the agent’s capacity to other tasks.

When a customer responds to the On Hold email, the interaction status is automatically changed to Work in progress. At this point, if the agent to whom the interaction is assigned isn't available, the email interaction can be optionally rerouted to the next available agent. This feature can be enabled by setting the system property **sn\_eaai\_csm.email.reroute.enabled** to true. By default, it is set to false. When enabled, the **Assigned to** field is cleared, and an event is triggered in CCaaS, enabling it to redirect the email to an available agent. This process verifies that customer inquiries are addressed promptly, even if the initial agent is no longer available.

**Related topics**  


[System properties for configuring Email Interaction](../reference/system-properties-for-configuring-email-as-an-interaction.md)

[Routing and assigning an email interaction to agents](routing-assigning-email-interaction-agents.md#)


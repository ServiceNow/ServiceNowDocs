---
title: Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks
description: The callback interaction feature built on the Interaction Controls Component \(ICC\) supports callback voice interactions directly within the ServiceNow configurable workspace. The workspace provides agents with callback voice interaction and callback control features in a unified view, resulting in improved productivity and enhanced customer experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Callback, CCaaS callback, ICC Callback, Callback requests]
breadcrumb: [Integrating with contact centers, Integrate, Customer Service Management]
---

# Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks

The callback interaction feature built on the Interaction Controls Component \(ICC\) supports callback voice interactions directly within the ServiceNow configurable workspace. The workspace provides agents with callback voice interaction and callback control features in a unified view, resulting in improved productivity and enhanced customer experience.

## Callback feature overview

Contact Center platforms provide a callback feature that lets callers keep their place in line and receive a callback when an agent is available. The callback requests are assigned to agents based on the order they are received. Alternatively, callers may select a specific date and time for a scheduled callback. The Callback functionality enables contact centers to reduce hold times and enhance customer experience by enabling customers to request a return call instead of waiting in the queue. This asynchronous communication model helps balance contact center load and improves both customer satisfaction and agent efficiency. The callback routing can be implemented in two different modes, depending on operational goals and infrastructure: Customer-first and Agent-first. These modes dictate how and when a call is established between the customer and the agent during a callback request.

-   **Customer-first mode**

    In this mode, CCaaS first dials the customer and connects them to an available agent after the customer answers the call.

    Callback flow: The callback request is queued. When the callback request reaches the top of the queue and an agent becomes available, the CCaaS dials the customer first. If the customer answers, the CCaaS dials and connects to an agent by routing the call to the agent's inbox in the configurable workspace. If the agent accepts, the call is bridged. This mode reduces unnecessary agent idle time and ensures that an agent is only engaged when a customer answers.

    The following image shows the customer-first mode with an immediate \(ASAP\) callback request on IVR where a customer is dialed before agent is connected. Agent views the callback interaction as any other normal voice interaction in the CSM Configurable Workspace.

    ![Customer-first mode: Immediate callback request on IVR – Customer dialed before agent is connected](../image/ccaas-callback-customer-first.png "Customer-first mode - Immediate callback request")

-   **Agent-first mode**

    In this mode, CCaaS routes the interaction first to an available agent. The Agent previews the callback context and dials the customer.

    Callback flow: The callback request is queued. When the callback request reaches the top of the queue and an agent becomes available, CCaaS routes the interaction to an available agent. The agent accepts the interaction and opens it in ServiceNow configurable workspace. The agent previews the callback context card and then dial the customer. Dialing the customer can be manual or automatic based on a configuration in CCaaS. If the customer doesn’t answer, the agent can redial or close the callback interaction.

    The following image shows the agent-first mode with immediate \(ASAP\) callback request on IVR where an agent is dialed before the customer is connected.

    ![Agent-first mode: Immediate callback request on IVR – Agent preview before dialing the customer](../image/ccaas-callback-agent-first.png "Agent-first mode - Immediate callback request")


The Interaction Controls Component \(ICC\) for callbacks feature enables CCaaS providers to display callback interactions so agents can manage customer calls directly from their configurable workspace. For more information on how to handle CCaaS callback requests, see [Manage a CCaaS callback request in the Configurable Workspace](../task/ccaas-address-callback-requests.md) and [Manage a CCaaS callback request using Global Voice Control](../task/handle-ccaas-callback-gvc.md).

**Note:**

To manage and activate the ICC integration for callbacks, see [Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integrations](../task/enable-icc-for-ccaas.md) and [Plugin requirements for voice and callback integrations with contact centers](../task/plugin-requirements-for-external-call-routing-integration-for-contact-centers.md).

**Related topics**  


[Manage a CCaaS callback request in the Configurable Workspace](../task/ccaas-address-callback-requests.md)

[Manage a CCaaS callback request using Global Voice Control](../task/handle-ccaas-callback-gvc.md)


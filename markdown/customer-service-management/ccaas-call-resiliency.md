---
title: Call resiliency
description: Call resiliency for Contact Center as a Service \(CCaaS\) delivers phone calls to Agent Workspaces without creating an Interaction in the ServiceNow instance. This capability verifies uninterrupted and reliable call management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Call resiliency

Call resiliency for Contact Center as a Service \(CCaaS\) delivers phone calls to Agent Workspaces without creating an Interaction in the ServiceNow instance. This capability verifies uninterrupted and reliable call management.

## Call resiliency for contact center integration overview

Call resiliency for CCaaS voice call integration ensures that inbound calls are delivered to agents. Inbound calls are delivered even if there are issues with creating Interactions in the ServiceNow instance. This feature routes phone calls to agents without requiring an Interaction.

When an agent accepts a call, an Interaction and a phone log record are created. If an agent rejects the call or the call times out, the contact center redirects the call to the next available agent. The integrated contact center, using the Interaction Controls Component \(ICC\) capability, displays call data such as the phone number and call duration, and provides basic functions such as mute, hold, and disconnect. Agents can open interactions by clicking the **Open interaction** link, although call transfer isn’t possible without an Interaction record. This approach ensures seamless call handling and minimizes service disruptions.

The following call resiliency visual gives you a snapshot of the end-to-end workflow.

![Contact center call resiliency workflow](../image/ccaas-call-resiliency-architecture-updated.png "Call resiliency flow")

Refer to the following table for annotation description of the preceding image.

|Annotation|Description|
|----------|-----------|
|1|Incoming call|
|2|Create voice interaction|
|3|Offer voice call option to the agent|
|4|Agent can accept/reject a call|
|5|When agent accepts a call, a voice interaction is created|
|6|Notification is sent to OpenFrame for the successful creation of an interaction|
|7|Global call screen displays|
|8|Synchronized call occurs continuously from steps 6 to 9. Once the agent accepts a call, any action the agent takes gets synced between ServiceNow and CCaaS|
|9|Conversation gets updated in the interaction|
|10|Interaction record gets updated|

## Call resiliency workflow use cases

Let’s go over some use cases to understand how call resiliency works for an integrated contact center.

In the call resiliency mode, calls are delivered to the Agents without interruption to call control options such as accept, hold, mute, or move calls to queues.

-   **Accept/Auto-accept calls**

    Agents can accept or auto-accept calls seamlessly in the call resiliency mode even without creating an Interaction. If an Interaction record doesn't get created, the agent has the option to create one by manually clicking the **Open interaction** link during the live call.

-   **Reject call**

    When a customer makes an inbound call, in the resiliency mode, CCaaS delivers the call to the agent's workspace. If the agent clicks **Reject**, the system generates an event. The event is communicated to the contact center, which in turn redirects the call to the next available agent. The contact center takes necessary actions to ensure seamless service delivery. This process verifies that the system is aware of the agent's action and can respond appropriately to maintain efficient call handling.

-   **Call timeout**

    If a call times out, call resiliency promotes ensures efficient interaction management by automatically creating an interaction and a work item. This process guarantees that, even if a call times out, the necessary interactions and work items are generated and managed effectively that enables contact centers to maintain seamless service delivery.


## Key Benefits of call resiliency

The call resiliency workflow improves the efficiency and reliability of handling incoming calls in a contact center. The following are some benefits:

-   **Enhanced reliability**

    Calls are delivered to agents even if interaction creation fails, promoting prompt handling and continuous service.

-   **Efficient call handling**

    The 'Offer API' creates interactions after the agent accepts the call, reducing wait time.

-   **Call management flexibility**

    Agents can reject or let calls time out, and the system redirects them to the next available agent, promoting no call is missed.

-   **Comprehensive call data**

    The ICC call controls display essential call information, such as phone numbers and duration, aiding effective call management.

-   **Limited functionality for seamless operations**

    Agents can perform basic functions such as mute, hold, and disconnect, maintaining smooth call operations even in resiliency mode.

-   **On-demand interaction creation**

    Interactions are created after the agent accepts the call, promoting all necessary records are generated without delay.

-   **Improved Agent experience**

    A clear and efficient workflow enhances the agent's experience, making call and interaction management easier.



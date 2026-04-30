---
title: Interaction Controls Component \(ICC\) call interaction features
description: The Contact Center Integration framework integrates traditional contact center capabilities, including telephony, intelligent routing, and workforce engagement management \(WEM\), with the CSM Configurable Workspace. This integration consolidates tools and workflows into a single, intuitive platform for both customers and agents.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 3
keywords: [ICC features for NVC]
breadcrumb: [Integrating contact centers with Interaction Controls Component \(ICC\) for voice calls, Integrating with contact centers, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Interaction Controls Component \(ICC\) call interaction features

The Contact Center Integration framework integrates traditional contact center capabilities, including telephony, intelligent routing, and workforce engagement management \(WEM\), with the CSM Configurable Workspace. This integration consolidates tools and workflows into a single, intuitive platform for both customers and agents.

The voice interaction feature is available for integration via Interaction Controls Component \(ICC\) for contact centers.

**Note:** See [Implement the Interaction Controls Component \(ICC\) for contact center integration](../task/enable-icc-for-ccaas.md) to manage the integration dependencies before using the feature.

![Screenshot showing the embedded voice controls in agent workspace with call transfer](../image/csm-nvc-call-transfer.png)

The following features are available from ICC call interactions to promote streamlined operations and an enhanced agent experience:

-   **Inbound call**

    Manages inbound calls by accepting or rejecting them directly from the Agent Workspace. During an active call, you can use buttons to hold, start, or stop recording, mute yourself or other parties, and transfer calls to a queue, other agents, or external numbers.

-   **Outbound call**

    Initiates outbound calls to contact customers, using the phone keypad to dial manually or by selecting the call icon on the record phone field to call directly.

-   **Call transfer**

    Transfers calls using either consult or blind transfer methods. In a consult transfer, you share the call context with the external contact before completing the transfer. A blind transfer immediately transfers the call to the external contact.


## How does it work

As an agent, you log in to the Configurable Workspace and the integrated contact center to start handling interactions from both of them. The agent inbox acts as a universal workspace where you receive and manage interactions for cases, emails, and chats, creating a consistent experience across all communication channels.

You can accept an incoming call to view the voice interactions page and verify the customer. The voice interaction page includes the following main components:

-   **Call control panel**

    Provides all call control buttons, such as record, mute, hold, and transfer \(consult or blind\).

-   **Customer details section**

    Offers an overview of the customer and their interaction history.

-   **Call transcript section**

    Displays a history of the live conversation between the agent and the customer.

    **Note:** CCaaS providers must turn on the Call Transcript feature.

    An interaction record is automatically created for each call. Opening the interaction record expands any voice interaction to show additional call details, including call transcript, wrap-up options, and customer context. The agent can view and update this record during the call and in the wrap-up interaction.

    **Note:** You can use an identity property and extension point to hide the conversation panel when real-time transcription is turned on or off. See: [Show or hide the conversation panel](show-hide-conversation-panel.md).


When an agent receives a customer call, they can verify the customer's details, view the interaction history, and see suggested knowledge articles for the customer's issue. They can also determine if the issue requires escalation to a specialized team.

For a smooth handoff, the agent can opt for a consult transfer to a specialized agent, providing context before transferring the call. Alternatively, the agent can transfer the call to an existing queue or an available agent.

During the transfer, the agent's call is automatically placed on hold. Once the consult transfer is complete, the first agent finalizes the transfer and leaves the call with the new agent. After the call transfer is complete, the agent's initial call is automatically placed in wrap-up mode, where they can finalize the interaction.

In wrap-up mode, ServiceNow® Now Assist automatically generates a call summary and adds it to the interaction. The agent can review the summary, select a suggested wrap-up code from Now Assist, generate their own code, add additional notes, and then end the interaction.

**Note:** The call transcription capability must be enabled to implement this feature.


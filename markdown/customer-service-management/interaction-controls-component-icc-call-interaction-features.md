---
title: Interaction Controls Component \(ICC\) call features
description: Streamline call handling and enhance the agent experience in the Agent Workspace. Integrate voice call capabilities and the core contact center features with Interaction Controls Component \(ICC\).
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [ICC for voice calls, Integrating with contact centers, Integrate, Customer Service Management]
---

# Interaction Controls Component \(ICC\) call features

Streamline call handling and enhance the agent experience in the Agent Workspace. Integrate voice call capabilities and the core contact center features with Interaction Controls Component \(ICC\).

The core features and capabilities of the contact center include:

-   Voice interaction feature
-   Intelligent routing
-   Workforce engagement management \(WEM\)

**Note:**

To use voice call capabilities available with Interaction Controls Component \(ICC\) integration, see [Interaction Controls Component \(ICC\) for voice calls](contact-center-integration-with-icc.md).

Use the ICC call control features with the existing contact center core features to promote streamlined operations and an enhanced agent experience. The following features are available within call interactions, and are numbered alongside the image as follows.

## Overview of ICC call interaction features within CSM Configurable Workspace

![Interaction Controls Component call interaction features within the CSM Configurable Workspace](../image/ccaas-icc-features.png "ICC call features")

The following table outlines the key call control features available when integrated with ICC within CSM Configurable Workspace.

<table id="table_gq5_m4j_1gc"><thead><tr><th>

Callout

</th><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Interaction record

</td><td>

View an interaction record within the global call component in the supported workspaces, such as CSM.

 An interaction record is automatically created for each call. Opening the interaction record expands any voice interaction to show additional call details, including call transcript, wrap-up options, and customer context. The agent can view and update this record during the call and in the wrap-up interaction.

**Note:** You can use an identity property and extension point to hide the conversation panel when real-time transcription is turned on or off. See: [Show or hide the conversation panel](show-hide-conversation-panel.md)

 The Interaction record page contains several other features that can be used to assist agents resolve customer issues while on call. Description of these features, such as record information, customer history, and KB search are available in the next table.

 Agents can also view interaction record details in unsupported workspaces with the call resiliency capability. See: [Call resiliency](ccaas-call-resiliency.md).

</td></tr><tr><td>

2

</td><td>

Active call component

</td><td>

Use the active call features to manage incoming, ongoing, and outgoing calls, and is available as an embedded component within the open interaction page. The active call components are available via integration with ICC.

 The agent can monitor interactions and access them using the call control panel, which provides call control buttons such as record, mute, hold, and transfer \(consult or blind\). Additionally, real-time call data is shown, such as the call's associated interaction record, hold time, and call duration. Moving away from the interaction page to another area of the workspace automatically opens the global call component.

 -   Active call: When an agent is in an active call, the associated interaction record displays. Selecting the link opens the interaction record in a new tab. During an active call, you can use buttons to hold, start, or stop recording, mute yourself or other parties, and transfer calls to a queue, other agents, or external numbers. Additionally, agents get notified when a supervisor is coaching or has joined an active call while monitoring agents directly through the CCaaS system.
-   Call transfer: Transfers calls using either consult or blind transfer methods. In a consult transfer, you can share the call context with the external contact before completing the transfer. A blind transfer immediately transfers the call to the external contact. Follow these steps to better assist a customer using the 'call transfer feature:
    -   **Initiate call transfer**

Select the transfer icon on the active call component, which places the customer call on hold.

    -   **Select Receiving agent**

Choose the agent to transfer the call to from the Agent's list.

    -   **Choose transfer method**

Consult: Talk to the agent before transferring the call. You can then either 'Merge calls' by combining your call with the new agent's call, or 'Leave &amp; Transfer calls' by disconnecting from the call and transferring the call directly.

Blind: Transfer the call directly without consultation.


</td></tr><tr><td>

3

</td><td>

Global call component

</td><td>

Enable agent movement between screens in the ServiceNow instance by displaying real-time call data in the component panel. The global call component provides an experience that enables agents to access call controls and embedded functionality within any workspace that supports the ICC enabled features. The global call components are available via OpenFrame integration. See: [Global call list](ccaas-global-call-list.md).

 This component is used to make and manage outbound and incoming calls. Agents can switch between workspaces anywhere within the application while taking ongoing calls. If an agent switches to a non-interaction tab during an ongoing call, the call continues to be active. All other active call controls can be accessed from this component.

-   Outbound call: Initiates outbound calls to contact customers, using the phone keypad to dial manually, or by selecting the call icon on the record phone field for direct calls. Avail the phone directory for ease of making outbound calls.
-   -   Callbacks: Outbound calls also support customer callback requests. When enabled and integrated within CSM, the agent can follow up on a callback request by manually completing an outbound call.

**Note:** For more information on callbacks, view [Callback interaction features](contact-center-intergration-with-icc-callback.md)

-   Phone directory: Agents can use the integrated address book to make outbound calls to queues, other agents, and external numbers. They can also enter a phone number directly in the global call list window to make calls. See: [Phone directory](ccaas-phone-directory.md).

</td></tr></tbody>
</table>## Interaction record page features within the CSM Configurable Workspace

The Interaction records page surfaces capabilities that assist agents both during and after calls. The following table describes additional features that are embedded within the record page.

<table id="table_sw5_rwf_bgc"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inbox alert card

</td><td>

When an inbound call comes through, choosing to accept or reject the call appears as an inbox notification. Manage inbound calls by accepting or rejecting them directly from the Agent Workspace. If an agent chooses to accept a call, they’re navigated to the embedded active call window within the Interaction page.

</td></tr><tr><td>

Record information

</td><td>

An agent is able to view and update the record during their call. This section displays details of the task or case linked to the interaction.

</td></tr><tr><td>

Contact information

</td><td>

This section displays customer contact details, such as phone number and email. The agent can verify, identity, and use this information for follow-ups.

</td></tr><tr><td>

Customer history

</td><td>

Agents can open an overview of the customer and their interaction history, as well as display a timeline of the all previous agent interactions. The agent can use this context to identify recurring issues or follow up on earlier cases.

</td></tr><tr><td>

Troubleshoot and KB search

</td><td>

This feature surfaces relevant knowledge articles based on the call context. The agent can browse suggested content or manually search knowledge base articles to support troubleshooting.

</td></tr><tr><td>

Wrap up

</td><td>

Now Assist automatically generates a call summary and adds it to the interaction. The agent can review the summary, select either suggested or generated wrap-up codes from Now Assist, add additional notes, and end the interaction.

 **Note:** Enable the call transcription capability to implement this feature.

</td></tr></tbody>
</table>
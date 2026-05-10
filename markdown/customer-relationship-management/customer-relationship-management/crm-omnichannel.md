---
title: Omnichannel
description: Omnichannel support enables organizations to serve customers across multiple communication channels, including voice, chat, email, SMS, consumer messaging apps, social media, and Engagement Messenger, from a single, unified workspace. Agents handle all interactions in CSM Configurable Workspace, and customers reach support through whichever channel fits them best.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 5
---

# Omnichannel

Omnichannel support enables organizations to serve customers across multiple communication channels, including voice, chat, email, SMS, consumer messaging apps, social media, and Engagement Messenger, from a single, unified workspace. Agents handle all interactions in CSM Configurable Workspace, and customers reach support through whichever channel fits them best.

## Omnichannel overview

Omnichannel integrates customer communications across platforms including email, chat, voice, and messaging applications within a centralized system, ensuring continuity as customers transition between channels. Agents access all interactions with complete context from a single workspace.

![omnichannel diagram that shows the different available channels](../image/crm-omnichannel-diagram.png "CRM omnichannel overview")

Advanced Work Assignment \(AWA\) routes work items across all channels based on agent availability, capacity, and skills. Organizations can configure routing queues independently for each channel, then apply consistent assignment logic across all of them. For example, the same routing system manages chats from the Customer Service Portal, email interactions, WhatsApp messages, and phone calls handled by Contact Center as a Service \(CCaaS\).

<table id="table_lw5_fwg_y3c"><thead><tr><th>

Channel

</th><th>

Description

</th><th>

Key capability

</th></tr></thead><tbody><tr><td>

Chat

</td><td>

Live and Virtual agent chat from portals.

</td><td>

AWA routes using pre-chat survey data.

</td></tr><tr><td>

Email

</td><td>

Inbound emails converted to interaction records via Email Interaction \(EaaI\) or directly to cases via Email to Case.

</td><td>

Agents respond or escalate to a case. Supports outbound email from contact records.

</td></tr><tr><td>

Voice

</td><td>

Customers reach agents via ServiceNow Voice for CSM, CTI, or OpenFrame integration.Additionally, Interaction Controls Component \(ICC\) embeds ServiceNow native call controls in the contact center workspaces.

</td><td>

Conversational IVR with Amazon Connect enables Virtual Agent to deflect calls before live agent routing.

</td></tr><tr><td>

Omnichannel Callback

</td><td>

Customers request a voice or video callback via Virtual Agent, Portals, or Engagement Messenger.

</td><td>

ASAP or scheduled time options. Agents manage the Callback actions component with CCaaS transfer support.

</td></tr><tr><td>

Consumer messaging

</td><td>

WhatsApp, LINE, Facebook Messenger, and Apple Messages for Business.

</td><td>

Asynchronous Messaging interactions managed in the workspace. Supports outbound conversations.

</td></tr><tr><td>

Engagement Messenger

</td><td>

Self-service interface embedded on third-party websites for knowledge browsing, case creation, and chat.

</td><td>

Supports asynchronous messaging and displays the omnichannel Callback option when agents are unavailable.

</td></tr></tbody>
</table>**Note:** CCaaS connects third-party contact center platforms such as Genesys with ServiceNow. It is an integration layer, not a standalone channel, that spans Voice \(call routing and controls\), Email Interaction \(transfer and wrap-up codes\), and omnichannel Callback \(CCaaS-routed callback management\).

## Omnichannel benefits

Omnichannel provides benefits to customers, agents, managers, and administrators.

-   **For customers:** Customers reach support through the channel that is most convenient for them, whether that is a phone call, a chat, or a WhatsApp message. Switching channels does not require customers to repeat information: the interaction record captures context that agents can reference regardless of how the conversation began.
-   **For agents:** Agents work in a single interface for all interaction types. CSM Configurable Workspace displays the right record page for each channel automatically, so agents do not have to navigate different tools for chat, email, voice, or messaging. Customer 360 surfaces account details, case history, and install base information in the same view.
-   **For managers:** All omnichannel interactions are tracked as interaction records, giving managers consistent visibility into volume, resolution, and agent activity across channels. AWA applies the same routing logic across all channels, making it possible to manage agent workloads and SLAs from a single framework.
-   **For administrators:** Communication channels are configured independently and can be activated incrementally. AWA service channels, Virtual Agent topics, and workspace record pages are shared across channels where appropriate, reducing the overhead of maintaining separate configurations for each channel.

## Products and contexts

Each product within the CRM suite uses omnichannel to connect customers with agents through the channels appropriate to its workflows.

-   **CSM**

    Customer Service Management \(CSM\) is the foundation for omnichannel contact center operations. Agents use CSM Configurable Workspace to handle interactions across chat, email, phone, messaging, Engagement Messenger, callback, and social media channels. Each interaction creates a record that links to cases, surfaces customer context, and follows the AWA routing rules configured for that channel. Channels can be activated incrementally to match an organization's current service model.

    For CCaaS environments, the Interaction Controls Component \(ICC\) embeds the CCaaS provider's call controls directly in the agent's workspace. CCaaS-routed email and callback interactions appear in the agent's inbox alongside native channel interactions, so agents in a blended contact center work from a single interface regardless of how the interaction was routed.

-   **Sales CRM**

    Sales CRM uses omnichannel to keep customer conversations connected across the quoting and fulfillment cycle. A buyer can chat live to get a quote, follow up by email when the order is placed, and check delivery status via WhatsApp or Engagement Messenger, all without repeating their details. Each interaction links to the same account, contact, and case record, giving agents full context regardless of which channel the conversation arrives on.

-   **FSM**

    Field Service Management uses the omnichannel framework to support both dispatchers managing work order queues and customers requesting onsite service. Walk-up Experience and conversational appointment booking enable customers to schedule onsite visits through self-service channels. Omnichannel Callback is available in FSM environments, allowing customers to request a callback rather than wait for an agent. Dispatchers and agents work in the shared Configurable Workspace, configured in UI Builder using the same framework as CSM.

-   **Industry solutions**

    Telecommunications, financial services, and manufacturing solutions include preconfigured omnichannel channel configurations, and workspace record pages tailored to the workflows common in those industries. Organizations deploy these preconfigured experiences as a starting point and extend channel configurations, AWA routing rules, and Virtual Agent topics in UI Builder as their requirements evolve.


## Use cases

-   **Retail banking: blended inbound and messaging support**

    A retail bank deploys chat and email as its primary inbound channels for retail customers and adds WhatsApp as a messaging channel for customers who prefer not to use the bank's portal. Inbound chat and email interactions are routed by AWA to agents based on the case type indicated in the pre-chat survey or email subject. WhatsApp conversations follow the same routing logic. Agents handle all three channel types from CSM Configurable Workspace, using the interaction record page configured for each channel. Agents needing to follow up with a customer can initiate an outbound WhatsApp message or email directly from the contact record.

-   **Telecommunications: website self-service with callback fallback**

    A telecom provider embeds Engagement Messenger on its customer support website. Customers can search knowledge articles, check order status through the service catalog, and start a chat with Virtual Agent without leaving the page. When wait times exceed a threshold, Engagement Messenger presents the omnichannel Callback option. Customers who request a callback are added to the callback queue, and agents call them back from CSM Configurable Workspace when an agent becomes available. Scheduled callbacks let customers pick a specific time, reducing abandonment during peak periods.

-   **Manufacturing: walk-up and field service**

    A manufacturer deploys Walk-up Experience for Customer Service at its service centers to manage customer check-ins for hardware repair. Customers check in at the walk-up kiosk, and agents manage the queue from CSM Configurable Workspace. When a repair requires on-site service, agents create a work order in Field Service Management from the case record. Field technicians see the work order in the FSM workspace, and customers receive updates through the email channel.


**Related topics**  


[Enable communication channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/enable-comm-channels.md)


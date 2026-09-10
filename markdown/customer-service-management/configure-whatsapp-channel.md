---
title: Configure WhatsApp channel
description: Configure WhatsApp as a consumer messaging channel within ServiceNow Customer Service Management using the WhatsApp Cloud API. WhatsApp integrates with ServiceNow Otto - Virtual Agent, to answer customer questions, with conversations routing to agents through the CRM Workspace. Twilio integration is also supported but offers more limited functionality than the Cloud API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-whatsapp-channel.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [WhatsApp, omnichannel, configure]
breadcrumb: [Configure consumer messaging apps, Configure omnichannel, Configure, Customer Service Management]
---

# Configure WhatsApp channel

Configure WhatsApp as a consumer messaging channel within ServiceNow Customer Service Management using the WhatsApp Cloud API. WhatsApp integrates with ServiceNow Otto - Virtual Agent, to answer customer questions, with conversations routing to agents through the CRM Workspace. Twilio integration is also supported but offers more limited functionality than the Cloud API.

Here's an example of a customer service journey combining WhatsApp support with omnichannel.

Amara is a customer support director at a global e-commerce company managing support across multiple channels. Customers increasingly prefer WhatsApp for support, but the team was handling WhatsApp conversations outside of ServiceNow through a separate platform, creating data silos and inconsistent service levels.

After setting up WhatsApp channel integration through the WhatsApp Cloud API \(or Twilio\), the team can now receive WhatsApp conversations directly in the CRM Workspace. They get the same queue management, assignment routing, and interaction tracking as other channels.

After setting this up, the customer saw support friction drop for WhatsApp-first users, and three channels became one unified workspace. First-response time improved by 35%, and agents now see all customer interactions \(WhatsApp, chat, email, phone\) in a single queue.

The following diagram shows the WhatsApp configuration workflow for administrators, agents, and customers.

\[Omitted image "whatsApp-configuration-diagram-draft.png"\] Alt text: Workflow diagram with three swim lanes showing Administrator setup, Agent handling, and Customer interaction steps for WhatsApp configuration.

## Common configuration steps \(required for WhatsApp\)

Every channel \(chat, email, WhatsApp\) requires the following foundational setup.

|Configuration Step|Description|Role|
|------------------|-----------|----|
|1. [Create service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-awa-channel-case-tasks.md)|Service channel is created automatically during plugin installation for each channel \(chat, email, WhatsApp\). This is the container that routes customer interactions.|System \(automatic\)|
|2. [Create a queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md)|Create a queue under each service channel in Omnichannel &gt; Administration &gt; Queues. The queue holds interactions waiting for an available agent. Each queue has a name, description, and optional schedule for availability windows.|CSM Admin|
|3. [Configure AWA routing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-assignment-rule.md)|Create an assignment rule in Advanced Work Assignment that determines how interactions are routed to agents. Examples: Most Capacity \(assigns to agent with most free time\), Least Busy, Round Robin. Create an assignment group with agents who have the required roles \(**sn\_customerservice\_agent**, **sn\_customerservice.consumer\_agent, awa\_agent**\). Link the rules and group to the queue.|CSM Admin|
|4. [Set agent presence state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-experience.md)|Add the channel to the Available presence state, so agents are eligible to receive interactions from that channel. Without this step, the queue has no target agents.|CSM Admin|
|5. [Activate channel in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md)|Verify that the channel appears in the CRM Workspace. To confirm, assign a test interaction to an agent; the WhatsApp messaging UI appears only once an interaction is assigned. Agents must see the channel in their workspace interface to receive and manage interactions.|CSM Admin|
|6. [Configure wrap-up codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/associate-wrap-up-codes-email-interactions.md)|Navigate to Interaction &gt; Wrap Up Codes to create categorization codes for interactions. Then navigate to Interaction &gt; Wrap-up configuration to assign these codes so agents can categorize interactions for reporting.|CSM Admin|

## WhatsApp integration options

WhatsApp configuration follows two separate paths: WhatsApp Cloud API or Twilio. Both paths share configuration steps.

**WhatsApp via Cloud API**

Use this path for direct integration with WhatsApp's native Cloud API. This approach skips the Twilio go-between and relies less on outside infrastructure. Customers must maintain two separate accounts: a Meta account and a ServiceNow instance.

|Configuration Step|Description|Role|
|------------------|-----------|----|
|1. [Setup WhatsApp business account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-direct-whatsapp-setup.md)|Create and verify your WhatsApp Business Account and phone number with WhatsApp directly.Yuo must complete this before configuring ServiceNow.|External \(WhatsApp\)|
|2. Register with Meta|Register your organization with Meta \(WhatsApp's parent company\) to access the WhatsApp Cloud API. Meta provides API credentials and endpoint access needed for ServiceNow integration. Copy and save these credentials in a secure location; they might not be accessible again after setup.|External / CSM Admin|
|3. [Configure omnichannel \(shared steps\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-whatsapp-channel.md)|Complete the common configuration steps in the Common configuration steps table: create queue, configure AWA routing with assignment rule and group, set channel to Available presence state, and activate channel in workspace.|CSM Admin|
|4. [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-virtual-agent-csm.md) \(optional\)|For conversational integration with WhatsApp via Cloud API, enable Virtual Agent for Customer Service so predefined topics are available over WhatsApp.|CSM Admin|

**WhatsApp via Twilio**

Use this path if your organization already works with Twilio or prefers their integration model. Twilio sits between WhatsApp and ServiceNow, handling message delivery, failover, and policy compliance. This approach doesn't support the full control features \(for example, list pickers, typing indicators, or geo-location specific features\) available through the Cloud API. Customers must maintain three separate accounts: Twilio, Meta, and ServiceNow.

|Configuration Step|Description|Role|
|------------------|-----------|----|
|1. Establish Twilio account|Set up a Twilio account and connect it to your WhatsApp Business Account. Twilio provides the messaging infrastructure between WhatsApp and ServiceNow.|External \(Twilio\)|
|2. [Setup WhatsApp business account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-whatsapp-setup.md)|Create and verify your WhatsApp Business Account and phone number with WhatsApp directly. This is a prerequisite for Twilio integration and must be completed before configuring ServiceNow.|External \(WhatsApp\)|
|3. Create message templates|Submit message templates for approval with WhatsApp. Any outbound message that isn't a direct reply within the 24-hour customer service window requires a pre-approved template.|External / CSM Admin|
|4. [Configure omnichannel \(shared steps\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-whatsapp-channel.md)|Complete the common configuration steps in the Common configuration steps table: create queue, configure AWA routing with assignment rule and group, set channel to Available presence state, and activate channel in workspace.|CSM Admin|
|5. [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-virtual-agent-csm.md) \(optional\)|For conversational integration with WhatsApp via Twilio, enable Virtual Agent for Customer Service so predefined topics are available over WhatsApp.|CSM Admin|

## ServiceNow Otto in Virtual Agent

Extend the WhatsApp channel with ServiceNow Otto in Virtual Agent so common customer questions resolve automatically before an interaction reaches an agent. Customers may also be able to access AI agents directly through WhatsApp self-service, without needing to reach a live agent first. The Otto branding shows that ServiceNow is bringing its AI capabilities into one interface, instead of keeping them as separate products.

Before you configure this capability, activate the ServiceNow Otto for CSM and Now Assist in Virtual Agent plugins. For more information, see [Configure ServiceNow Otto for Customer Service Management \(CSM\) in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/configure-now-assist-for-customer-service-management-csm-in-virtual-agent.md).


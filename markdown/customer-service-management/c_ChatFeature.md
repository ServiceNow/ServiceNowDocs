---
title: Configure chat channel
description: Configure chat as a real-time messaging channel within ServiceNow Customer Service Management. Customers can start live conversations from your web portal. Conversations route to available agents and are managed through the CRM Workspace alongside email, messaging, and phone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/c\_ChatFeature.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [chat, omnichannel, configure]
breadcrumb: [Configure omnichannel, Configure, Customer Service Management]
---

# Configure chat channel

Configure chat as a real-time messaging channel within ServiceNow Customer Service Management. Customers can start live conversations from your web portal. Conversations route to available agents and are managed through the CRM Workspace alongside email, messaging, and phone.

Here's an example of a customer service journey combining chat support with omnichannel.

Rajesh is a customer service manager at a financial services company struggling with chat request delays and poor routing. The team uses multiple tools to manage different channels, and chat requests often get missed or assigned to agents without the right skills. After setting up ServiceNow omnichannel with the chat channel, the team can now handle chat conversations directly in the CRM Workspace alongside email and phone interactions.

With chat configured, the team benefits from skill-based routing, unified queue management, and Virtual Agent escalation.

Customers get quicker resolutions through real-time conversations without delays. Agents see chat requests only in their assigned queues, and Rajesh has centralized control over chat schedules, escalation paths, and Virtual Agent topics.

After the team set this up, first-response time improved, and Rajesh got the visibility needed to manage chat as a first-class channel alongside email, messaging, and phone.

The following diagram shows the Chat configuration workflow for administrators, agents, and customers.

\[Omitted image "chat-configuration-diagram-draft.png"\] Alt text: Workflow diagram showing chat configuration steps for administrators, agents, and customers including queue setup, routing, feature activation, and conversation handling.

## Common configuration steps \(required for chat\)

Every omnichannel channel \(chat, email, WhatsApp\) requires the following foundational setup.

|Configuration Step|Description|Who does this|
|------------------|-----------|-------------|
|1. [Create service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-awa-channel-case-tasks.md)|Service channel is created automatically during plugin installation for each channel \(chat, email, WhatsApp\). This is the container that routes customer interactions.|System \(automatic\)|
|2. [Create a queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md)|Create a queue under each service channel in Omnichannel &gt; Administration &gt; Queues. The queue holds interactions waiting for an available agent. Each queue has a name, description, and optional schedule for availability windows.|CSM Admin|
|3. [Configure AWA routing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-assignment-rule.md)|Create an assignment rule in Advanced Work Assignment that determines how interactions are routed to agents. Examples: Most Capacity \(assigns to agent with most free time\), Least Busy, Round Robin. Create an assignment group with agents who have the required roles \(**sn\_customerservice\_agent**, **sn\_customerservice.consumer\_agent, awa\_agent**\). Link the rules and group to the queue.|CSM Admin|
|4. [Set agent presence state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-experience.md)|Add the channel to the Available presence state, so agents are eligible to receive interactions from that channel. Without this step, the queue has no target agents.|CSM Admin|
|5. [Activate channel in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md)|Verify the channel appears in the CRM Workspace. Agents must see the channel in their workspace interface to receive and manage interactions.|CSM Admin|
|6. [Configure wrap-up codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/associate-wrap-up-codes-email-interactions.md)|Navigate to Interaction &gt; Wrap Up Codes to create categorization codes for interactions. Then navigate to Interaction &gt; Wrap-up configuration to assign these codes so agents can categorize interactions for reporting.|CSM Admin|

## Chat-specific configuration steps

**Note:** ServiceNow is migrating from NLU-based Virtual Agent to NAVA \(Now Assist Virtual Agent\) for chat interactions. This topic reflects the current NLU-based configuration steps; NAVA configuration details will be added once available, starting with the Canada release. NAVA is part of ServiceNow's broader Now Assist and Otto AI experience.

|Configuration Step|Description|Who does this|
|------------------|-----------|-------------|
|1. [Set queue parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md)|Configure the opening question, initial agent response, not-available message, and maximum queue time before rerouting.|CSM Admin|
|2. [Set up Pre-Chat Surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-pre-chat-overview.md) \(optional\)|Two preconfigured surveys exist: CSP Pre-Chat Survey \(logged-in customers\) and CSP Anonymous Pre-Chat Survey \(anonymous users\). These aren't active by default and require the com.glide.service-portal.consumer-portal and com.glide.cs plugins.|CSM Admin|
|3. [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-virtual-agent-csm.md)|Install the Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\) to access predefined chatbot topics: Check Case Status, Get Service Request Status, and Receive Bill/Invoice. Activate Virtual Agent to resolve common questions automatically before they reach an agent.|CSM Admin|
|4. [Enable video or screen-share escalation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-chat-zoom-connector.md) \(optional\)|Install the Chat Zoom Connector application. Integrate your Zoom account, set up the Notify Zoom connector to link Zoom meetings to Notify, install the Chat Zoom Connector integration, and activate.|CSM Admin|


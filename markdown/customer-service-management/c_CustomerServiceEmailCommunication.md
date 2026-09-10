---
title: Configure Email channel
description: Configure Email Interaction so incoming customer emails create traceable interactions, route to the right agent group, and stay linked to open cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/c\_CustomerServiceEmailCommunication.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [email, omnichannel, configure]
breadcrumb: [Configure omnichannel, Configure, Customer Service Management]
---

# Configure Email channel

Configure Email Interaction so incoming customer emails create traceable interactions, route to the right agent group, and stay linked to open cases.

Here's an example of a customer service journey consolidating Email support with omnichannel.

Sophia is a support operations manager at a healthcare software company. Her team was overwhelmed with email volume, managing interactions across email clients, case systems, and chat systems. Case records often had missing or incomplete email history, replies to closed cases created duplicate work, and handling time was hard to predict.

After setting up Email Interaction for CSM, the system creates an interaction \(not a case\) for new emails. Watermarks thread customer replies to the open interaction. If an agent closes the interaction, replies route to the original linked case instead of creating a new case or interaction.

Sophia's team reduced case volume and eliminated lost emails through reply linking. AI-powered summaries and contextual matching reduced average email handling time.

The following diagram shows the Email configuration workflow for administrators, agents, and customers.

\[Omitted image "email-configuration-diagram-draft.png"\] Alt text: Workflow diagram showing email configuration steps for administrators, agents, and customers including plugin installation, flow activation, email handling, and AI tools.

## Common configuration steps \(required for email\)

Every channel \(chat, email, WhatsApp\) requires the following foundational setup.

|Configuration Step|Description|Who does this|
|------------------|-----------|-------------|
|1. [Create service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-awa-channel-case-tasks.md)|Service channel is created automatically during plugin installation for each channel \(chat, email, WhatsApp\). This is the container that routes customer interactions.|System \(automatic\)|
|2. [Create a queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md)|Create a queue under each service channel in Omnichannel &gt; Administration &gt; Queues. The queue holds interactions waiting for an available agent. Each queue has a name, description, and optional schedule for availability windows.|CSM Admin|
|3. [Configure AWA routing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-assignment-rule.md)|Create an assignment rule in Advanced Work Assignment that determines how interactions are routed to agents. Examples: Most Capacity \(assigns to agent with most free time\), Least Busy, Round Robin. Create an assignment group with agents who have the required roles \(**sn\_customerservice\_agent**, **sn\_customerservice.consumer\_agent, awa\_agent**\). Link the rules and group to the queue.|CSM Admin|
|4. [Set agent presence state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-experience.md)|Add the channel to the Available presence state, so agents are eligible to receive interactions from that channel. Without this step, the queue has no target agents.|CSM Admin|
|5. [Activate channel in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md)|Verify the channel appears in the CRM Workspace. Agents must see the channel in their workspace interface to receive and manage interactions.|CSM Admin|
|6. [Configure wrap-up codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/associate-wrap-up-codes-email-interactions.md)|Navigate to Interaction &gt; Wrap Up Codes to create categorization codes for interactions. Then navigate to Interaction &gt; Wrap-up configuration to assign these codes so agents can categorize interactions for reporting.|CSM Admin|

## Email-specific configuration steps

|Configuration Step|Description|Who does this|
|------------------|-----------|-------------|
|1. [Install Plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-email-interaction-customer-service-management.md)|Install the Email Interaction for CSM plugin \(sn\_eaai\_csm\) from System Definition &gt; Plugins. This plugin includes optional demo data and preconfigured Email service channel. For new CSM customers, related flows are enabled automatically. Existing CSM customers must manually activate the Create Interaction from Email, Update Interaction from Email, and Update Case via Reply for EaaI flows in Workflow Studio.|CSM Admin|
|2. [Activate Email flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-flow-email-interaction.md)|Manually activate three flows in Workflow Studio. Create Interaction from Email creates a new interaction for each inbound email. Update Interaction from Email updates the interaction when a customer replies. Update Case via Reply for EaaI creates a new linked interaction instead of reopening a closed one. When activating each flow, set the filter to "To contains \[your support email address\]". This ensures the flow only triggers for the actual support inbox.|CSM Admin|
|3. [Set system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/system-properties-for-configuring-email-as-an-interaction.md)|Navigate to System Properties &gt; All Properties and configure: **sn\_eaai\_csm.email\_addresses** \(comma-separated support addresses\), **sn\_eaai\_csm.period\_of\_customer\_inactivity\_to\_close\_interaction** \(days before auto-close, default 5\), **sn\_eaai\_csm.email.reroute.enabled** \(reroute if assigned agent unavailable, default false\), **sn\_eaai\_csm.notify\_agent\_on\_email\_linked\_to\_case** \(notify when reply links to open case, default true\).|CSM Admin|
|4. [Enable AI assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-email-summarization-csm.md) \(optional\)|Check your entitlements to determine whether you have access to Now Assist for CSM. Two Now Assist skills apply and are inactive by default: Email Interaction Summarization \(auto-generates email summaries\) and Contextual Email Matching \(auto-matches incoming emails to open cases\). Found under Now Assist Admin &gt; Now Assist Skills &gt; Customer &gt; CSM. These skills are part of ServiceNow's broader Now Assist and Otto AI experience. For more information, see [Activate contextual email matching for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-contextual-email-matching-csm.md).|CSM Admin|
|5. [Configure wrap-up codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/associate-wrap-up-codes-email-interactions.md)|Navigate to Interaction &gt; Wrap Up Codes, select New, fill in required fields, select Active, then submit. Then navigate to Interaction &gt; Wrap-up configuration to assign wrap-up codes to email interactions for categorization and reporting. For more information, see [Use AI to generate wrap up code and notes summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ai-generated-wrap-up-codes-and-notes-summary.md).|CSM Admin|


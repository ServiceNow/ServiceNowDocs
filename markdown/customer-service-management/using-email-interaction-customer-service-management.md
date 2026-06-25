---
title: Using Email Interaction for Customer Service Management
description: Email Interaction for CSM application enables agents to create interactions from customer emails, helping them resolve simple customer queries through these interactions. They can create a case from an interaction when further investigation is needed for resolving the customer query. This process provides clarity of the effort needed for customer query intake and actual investigation needed for query resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/using-email-interaction-customer-service-management.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 8
keywords: [Email Interaction for CSM, email replies closed interactions, AI summarization email interactions]
breadcrumb: [Customer communication, Use, Customer Service Management]
---

# Using Email Interaction for Customer Service Management

Email Interaction for CSM application enables agents to create interactions from customer emails, helping them resolve simple customer queries through these interactions. They can create a case from an interaction when further investigation is needed for resolving the customer query. This process provides clarity of the effort needed for customer query intake and actual investigation needed for query resolution.

\[Omitted image "email-interaction-for-CSM-workflow-overview.png"\] Alt text: Workflow overview

The Email Interaction for CSM application offers several key benefits:

-   Streamlines operations by helping to prevent the creation of duplicate or unnecessary cases.
-   Provides a consistent experience for agents across channels by modeling emails as an interaction, alongside voice, chat, and messaging channels.
-   Clarity of effort needed for customer problem intake, represented by interactions.
-   Clarity of effort needed for investigation and resolution, represented by cases.
-   Enables agents to initiate outbound email interactions directly from contact or consumer records.

## Email interaction routing

Email interactions can be routed through Advanced Work Assignment \(AWA\) or through an external Contact Center as a Service \(CCaaS\) solution. The system detects the routing source for each interaction, which determines the available agent actions such as wrap-up and transfer capabilities. For AWA-routed interactions, wrap-up codes are saved in the wrap-up segment table. For CCaaS-routed interactions, wrap-up codes are synced to both instance and the CCaaS system, and agents can transfer the interaction to another queue or agent.

## Inbound email interactions

When a customer sends an email, the system creates an inbound interaction instead of a case and routes it to an available agent through Advanced Work Assignment \(AWA\) or a CCaaS provider. The agent reviews the interaction, responds through the activity stream, and resolves the query directly within the interaction. If the query requires further investigation, the agent creates a case from the interaction while preserving all communication history and context.

Inbound email interactions support the following features:

-   Email-to-interaction conversion with automatic agent routing through AWA or CCaaS.
-   Activity stream for viewing email threads and agent responses.
-   Case creation from an interaction only when deeper investigation is needed.
-   Interaction closure with wrap-up codes for reporting and conformance.

## Email replies on closed interactions

When a customer replies to an email thread linked to a closed interaction, the system automatically links the reply to the correct open case or interaction instead of creating a new interaction. This preserves conversation continuity and confirms the assigned agent receives the reply in context. If no open cases or interactions are linked to the closed interaction, the system creates a new interaction for the email reply.

Email replies on closed interactions support the following:

-   Automatic routing of customer replies to the correct open case or interaction without agent action.
-   AI-based context matching when multiple open cases exist, using keyword matching. Check your entitlements to determine whether you have access to this feature.
-   Fallback linking to the most recently opened case when no confident match is found.
-   Agent notification through the bell icon when a reply is linked to an open case.
-   Support for standard cases and extended case types.

For more information on how the system evaluates and routes replies, see [Email reply linking for closed interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/email-reply-routing-closed-interactions.md).

## Outbound email interactions

Agents can initiate outbound email interactions directly from contact or consumer records in the CSM Configurable Workspace. When an agent composes and sends an email from a contact or consumer record, the system automatically creates a Work-In-Progress \(WIP\) outbound interaction and assigns it to the agent.

Outbound email interactions support the following features:

-   Automatic WIP interaction creation when an agent opens the email composition window from a contact or consumer record.
-   Draft email preservation with linking to the outbound interaction.
-   Consolidation of drafts from multiple agents into a single WIP interaction \(configurable\).
-   Configurable automated reminder emails for customers who haven’t responded.
-   Automatic closure of inactive outbound interactions in the On Hold state after a configurable period, with the default set to 30 days.
-   Automatic association of customer response emails to the same outbound interaction, with agent notification on the **Ongoing** tab.

## Multiple agents composing email for the same customer

By default, when multiple agents initiate outbound emails for the same customer, the system consolidates all drafts into a single WIP interaction. The outbound interaction is assigned to the agent who initiates the email. If the agent composes the email but doesn’t send it immediately, and another agent composes an email to the same contact or consumer during this period, the second email is linked to the same outbound interaction and ownership is reassigned to the second agent. When the email is sent, the interaction is assigned to the agent who sends it.

This behavior is configurable using the \(**sn\_eaai\_core.create\_outbound\_interaction\_per\_agent.target\_tables**\) system property. When a table is listed in this property, a new outbound interaction is created for each outbound email initiated by different agents for the same customer. For example, if Agent A and Agent B both compose emails to the same contact, each agent gets a separate outbound interaction instead of sharing one. When a table isn’t listed, all agent drafts are consolidated into a single WIP interaction.

For more information, see [System properties for configuring Email Interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/system-properties-for-configuring-email-as-an-interaction.md).

## Wrap-up codes for email interactions

When closing an email interaction, agents select an internal wrap-up code to categorize the outcome. Wrap-up codes support both AWA-routed and CCaaS-routed email interactions, improving reporting reliability and conformance tracking.

The following default wrap-up codes are available:

-   Issue resolved: Agent resolved the customer query within the interaction.
-   Task created: Automatically assigned when a case is created from the interaction.
-   Closed due to customer inactivity: Automatically assigned when the system closes an inactive interaction.

## AI summarization of email interactions

Agents can generate AI summaries of email interaction threads to get the key context without reading every message. AI summarization of email interactions supports on-demand summary generation when an agent selects **Summarize** on the interaction page.

**Note:** Check your entitlements to determine whether you have access to AI summarization.

For more information, see [AI summarization of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-ai-summarization-email-interactions.md).

## Automatic wrap-up code assignment

In the following scenarios, the system assigns a wrap-up code automatically without agent selection:

|Scenario|Wrap-up code|Action|
|--------|------------|------|
|Agent creates a case from the interaction|Task created|Interaction is automatically closed. If the interaction is routed through CCaaS, the code is synced to CCaaS.|
|System closes inactive interaction \(no customer response\)|Closed due to customer inactivity|A scheduled job checks for On Hold interactions with no customer response and closes them.|
|Agent doesn’t submit a code within the timeout|Issue resolved \(default\)|The default code is applied automatically after the configured timeout period. The default timeout is 2 minutes.|

## Transfer email interactions \(CCaaS-routed\)

For CCaaS-routed email interactions, agents can transfer the interaction to another queue or agent using the Transfer Email action. Only CCaaS-authorized queues and agents appear in the transfer options. When a transfer is initiated, the interaction record is updated in both CCaaS and the instance, and the current agent’s ownership and capacity is released.

**Related topics**  


[Omnichannel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/omnichannel.md)

[System properties for configuring Email Interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/system-properties-for-configuring-email-as-an-interaction.md)

[Wrap up email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/wrap-up-email-interactions-eaai.md)

[Transfer email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/transfer-email-interactions-eaai.md)

[Create outbound email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-outbound-email-interactions-eaai.md)

[Configure wrap-up codes for email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-wrap-up-codes-email-interactions-eaai.md)

[Associate wrap-up codes with email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/associate-wrap-up-codes-email-interactions.md)

[Routing and assigning an email interaction to agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/routing-assigning-email-interaction-agents.md)

[Email reply linking for closed interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/email-reply-routing-closed-interactions.md)

[Email reply linking scenarios for closed interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-email-reply-linking-scenarios.md)

[AI summarization of email interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/eaai-ai-summarization-email-interactions.md)


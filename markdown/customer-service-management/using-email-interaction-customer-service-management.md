---
title: Using Email Interaction for Customer Service Management
description: Email Interaction for CSM application enables agents to create interactions from customer emails, helping them resolve simple customer queries through these interactions. They can create a case from an interaction when further investigation is needed for resolving the customer query. This process provides clarity of the effort needed for customer query intake and actual investigation needed for query resolution.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Email Interaction for CSM]
breadcrumb: [Customer communication, Use, Customer Service Management]
---

# Using Email Interaction for Customer Service Management

Email Interaction for CSM application enables agents to create interactions from customer emails, helping them resolve simple customer queries through these interactions. They can create a case from an interaction when further investigation is needed for resolving the customer query. This process provides clarity of the effort needed for customer query intake and actual investigation needed for query resolution.

![Workflow overview](../image/email-interaction-for-CSM-workflow-overview.png "Email Interaction for CSM- workflow overview")

The Email Interaction for CSM application offers several key benefits:

-   Streamlines operations by helping to prevent the creation of duplicate or unnecessary cases.
-   Consistent experience for agents across channels by modeling emails also as an interaction, such as voice, chat, and messaging channels.
-   Clarity of effort needed for customer problem intake, represented by interactions.
-   Clarity of effort needed for investigation and resolution, represented by cases.
-   Enables agents to initiate outbound email interactions directly from contact or consumer records, expanding email from a reactive to a proactive channel.

## Email interaction routing

Email interactions can be routed through Advanced Work Assignment \(AWA\) or through an external Contact Center as a Service \(CCaaS\) solution. The system auto-detects the routing source for each interaction, which determines the available agent actions such as wrap-up and transfer capabilities. For AWA-routed interactions, wrap-up codes are saved in the wrap-up segment table. For CCaaS-routed interactions, wrap-up codes are synced to both instance and the CCaaS system, and agents can transfer the interaction to another queue or agent.

## Inbound email interactions

When a customer sends an email, the system creates an inbound interaction instead of a case and routes it to an available agent through Advanced Work Assignment \(AWA\) or a CCaaS provider. The agent reviews the interaction, responds through the activity stream, and resolves the query directly within the interaction. If the query requires further investigation, the agent creates a case from the interaction while preserving all communication history and context.

Inbound email interactions support the following features:

-   Email-to-interaction conversion with automatic agent routing through AWA or CCaaS.
-   Activity stream for viewing email threads and agent responses.
-   Case creation from an interaction only when deeper investigation is needed.
-   Interaction closure with wrap-up codes for reporting and compliance.

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

This behavior is configurable using the **sn\_eaai\_core.create\_outbound\_interaction\_per\_agent.target\_tables** system property. When a table is listed in this property, new outbound interaction is created for each outbound email initiated by different agents for the same customer. For example, if Agent A and Agent B both compose emails to the same contact, each agent gets a separate outbound interaction instead of sharing one. When a table isn’t listed, all agent drafts are consolidated into a single WIP interaction.

For more information, see [System properties for configuring Email Interaction](../reference/system-properties-for-configuring-email-as-an-interaction.md).

## Wrap-up codes for email interactions

When closing an email interaction, agents select an internal wrap-up code to categorize the outcome. Wrap-up codes support both AWA-routed and CCaaS-routed email interactions, improving reporting reliability and compliance tracking.

The following default wrap-up codes are available:

-   Issue resolved: Agent resolved the customer query within the interaction.
-   Task Created: Automatically assigned when a case is created from the interaction.
-   Closed due to customer inactivity: Automatically assigned when the system closes an inactive interaction.

## Automatic wrap-up code assignment

In the following scenarios, the system assigns a wrap-up code automatically without agent selection:

|Scenario|Wrap-up code|Action|
|--------|------------|------|
|Agent creates a case from the interaction|Task Created|Interaction is automatically closed. If the interaction is routed via CCaaS, the code is synced to CCaaS.|
|System closes inactive interaction \(no customer response\)|Closed due to customer inactivity|A scheduled job checks for On Hold interactions with no customer response and closes them.|
|Agent doesn’t submit a code within the timeout|Issue resolved \(default\)|The default code is applied automatically after the configured timeout period. Default time is set to 2 minutes.|

## Transfer email interactions \(CCaaS-routed\)

For CCaaS-routed email interactions, agents can transfer the interaction to another queue or agent using the Transfer Email action. Only CCaaS-authorized queues and agents appear in the transfer options. When a transfer is initiated, the interaction record is updated in both CCaaS and the instance, and the current agent’s ownership and capacity is released.

**Related topics**  


[Omnichannel](omnichannels-communicating-customers.md#)

[System properties for configuring Email Interaction](../reference/system-properties-for-configuring-email-as-an-interaction.md)

[Wrap up email interactions](../task/wrap-up-email-interactions-eaai.md)

[Transfer email interactions](../task/transfer-email-interactions-eaai.md)

[Create outbound email interactions](../task/create-outbound-email-interactions-eaai.md)

[Configure wrap-up codes for email interactions](../task/configure-wrap-up-codes-email-interactions-eaai.md)

[Associate wrap-up codes with email interactions](../task/associate-wrap-up-codes-email-interactions.md)

[Routing and assigning an email interaction to agents](routing-assigning-email-interaction-agents.md#)


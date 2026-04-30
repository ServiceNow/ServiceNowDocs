---
title: Routing and assigning an email interaction to agents
description: Route and assign email interactions to the appropriate agents based on predefined rules and criteria.Manually assign an interaction that is in the New state to yourself or another agent.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Email Interaction for CSM, Email Interaction for CSM]
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Routing and assigning an email interaction to agents

Route and assign email interactions to the appropriate agents based on predefined rules and criteria.

When agents accept email interactions routed by Advanced Work Assignment \(AWA\), the interaction state changes from New to Work in progress and it’s assigned to the agent.

For more information on the configuration required to route and assign email interactions, see [Configure Advanced Work Assignment for routing email interactions](../task/configure-advanced-work-assignment-route-email-interactions.md).

Alternatively, agents can assign the email interactions manually. For more information on how to assign email interactions, see [Assign an interaction manually](routing-assigning-email-interaction-agents.md#).

Agents can send emails to the customer requesting for more information. Agents can keep the interactions On Hold while waiting for the customer response. While an email interaction is on hold, customers receive periodic reminders prompting them to respond quickly.

Once a customer replies to the on-hold email interaction, the interaction’s status is automatically updated to Work in progress. At this point, if the agent to whom the interaction is assigned isn’t available, the email interaction can be optionally rerouted to the next available agent. This behavior occurs when the system property **sn\_eaai\_csm.email.reroute.enabled** is set to true. By default, it is set to false. The automated rerouting process confirms that customer inquiries are addressed promptly. Enterprises can unify routing of omnichannel interactions within CCaaS to reduce admin effort. For more information about unified routing of email interactions, see [Unified routing of email interactions via CCaaS](unified-email-routing-via-ccaas.md).

.

**Related topics**  


[System properties for configuring Email Interaction](../reference/system-properties-for-configuring-email-as-an-interaction.md)

[Unified routing of email interactions via CCaaS](unified-email-routing-via-ccaas.md)

## Assign an interaction manually

Manually assign an interaction that is in the New state to yourself or another agent.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, or sn\_customerservice.consumer\_agent

### About this task

The **Assign to me** button is only visible if the interaction is in the New state and the **Assigned to** field is empty.

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(![List icon](../image/List_icon.jpg)\).

3.  From the Interactions section, select **My Interactions**.

4.  Open an interaction.

5.  Assign the interaction in one of the following ways.

    |Option|Description|
    |------|-----------|
    |**Assign the interaction to yourself**|Select **Assign to me**. The Assigned to field gets populated with the agent's name and the state changes to Work in Progress.|
    |**Assign the interaction to another agent**|Select an agent in the **Assigned to** field and select **Save**.|



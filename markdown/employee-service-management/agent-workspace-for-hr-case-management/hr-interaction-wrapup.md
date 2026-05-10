---
title: HR interaction wrap up
description: Interaction wrap up provides HR agents with a brief wrap-up period at the end of customer conversations. HR agents can use this time to complete their work before moving on to assist other customers.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Contact Center as a Service \(CCaaS\), Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# HR interaction wrap up

Interaction wrap up provides HR agents with a brief wrap-up period at the end of customer conversations. HR agents can use this time to complete their work before moving on to assist other customers.

Interaction wrap up feature is available for interaction type: **Phone**. When enabled, an interaction record moves from the Work In Progress to the Wrap Up state at the end of a customer conversation. This brief, configurable period enables agents to complete tasks such as posting work notes and updating record information before moving on to other work items. While in the Wrap Up state, an agent’s capacity is not reduced until the state of the interaction moves to Closed Complete.

**Note:** You can view the wrap up record within the Wrap up sub-list inside the Interaction list.

![Interaction wrap up](../image/nav-ws.png)

## Configuring interaction wrap up

Users with the system administrator role can create an interaction wrap up configuration for the desired communication channel. Creating a configuration automatically enables the feature and the Wrap Up state for interactions that match the configuration settings.

The interaction wrap up configuration includes the following information:

-   The selected communication channel.
-   Additional conditions that apply to the interaction records included in the configuration.
-   Whether wrap up is automatically ended by the system and, if automatically ended the duration of the wrap up period.
-   Whether a countdown timer that displays the wrap up duration is shown to agents in CSM Configurable Workspace.

For more information, see [Create an interaction wrap-up configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-management/create-interaction-wrap-up-config.md).

## Starting and ending a wrap up

The wrap up period begins when either the agent or the customer ends a conversation. Ending the wrap up period can be performed manually by the agent or automatically by the system.

For more information, see [Interaction wrap up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-management/interaction-wrap-up-state.md).


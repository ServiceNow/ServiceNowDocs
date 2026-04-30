---
title: Interaction wrap up
description: Interaction wrap up provides agents with a brief wrap-up period at the end of customer conversations. Agents can use this time to complete their work before moving on to assist other customers.
locale: en-US
release: yokohama
product: Interaction Management
classification: interaction-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction wrap up

Interaction wrap up provides agents with a brief wrap-up period at the end of customer conversations. Agents can use this time to complete their work before moving on to assist other customers.

Interaction wrap up is a feature available for all types of interactions. When enabled, an interaction record moves from the Work In Progress to the Wrap Up state at the end of a customer conversation. This brief, configurable period enables agents to complete tasks such as posting work notes and updating record information before moving on to other work items.

While in the Wrap Up state, an agent’s capacity is not reduced until the state of the interaction moves to Closed Complete.

**Note:** The interaction wrap up feature works with multiple types of communication channels. This feature supports a chat and messaging interactions base system.

## Configuring interaction wrap up

Users with the system administrator role [create an interaction wrap up configuration](../task/create-interaction-wrap-up-config.md) for the desired communication channel. Creating a configuration automatically enables the feature and the Wrap Up state for interactions that match the configuration settings.

The interaction wrap up configuration includes the following information:

-   The selected communication channel.
-   Additional conditions that apply to the interaction records included in the configuration.
-   Whether wrap up is automatically ended by the system and, if automatically ended the duration of the wrap up period.
-   Whether a countdown timer that displays the wrap up duration is shown to agents in CSM Configurable Workspace.

The interaction wrap up configuration adds the Wrap Up state to the **State** field on the Interaction record. For more information about the wrap up state, see [Interaction states](../reference/interaction-states.md#section_o4v_j4r_vdb).

## Starting wrap up

The wrap up period begins when either the agent or the customer ends a conversation. The system then does the following:

-   Moves the state of the interaction from Work in Progress to Wrap Up.
-   Starts a countdown timer for the wrap up duration period.

## Manually ending wrap up

Ending the wrap up period can be performed manually by the agent or automatically by the system.

Agents can end the wrap up by clicking **End Wrap Up** on the Interaction record, which moves the interaction from Wrap Up to Closed Complete.

Agents can also end the wrap up period by closing the interaction record tab.

-   If the interaction is in the Wrap Up state, closing the tab ends the wrap up period and moves the interaction to Closed Complete. The system displays a message to the user about ending the wrap up period.
-   If the interaction is in the Work in Progress state, closing the tab skips the wrap up period and moves the interaction to Closed Complete.

## Automatically ending wrap up

If an agent has not already ended wrap up, the system can automatically end the wrap up period after a set period of time. Automatic wrap up must be enabled in the interaction wrap up configuration.

-   The system starts the wrap up duration timer when the wrap up period starts.
-   When the wrap up duration timer reaches zero, the system ends wrap up and changes the state from Wrap Up to Closed Complete.
-   The system sets the **System wrap up** field on the Interaction record to True.

**Note:** Agents can manually end the wrap up period even if automatic wrap up is enabled.

-   **[Interaction form](../reference/interaction-form.md)**  
The Interaction form displays information about a customer interaction.
-   **[Interaction wrap up timer](interaction-wrap-up-timer.md)**  
The interaction wrap up timer displays a countdown of the wrap up duration period in CSM Configurable Workspace.
-   **[Interaction wrap up scheduled job](interaction-wrap-up-scheduled-job.md)**  
The interaction wrap up feature includes a scheduled job to close any interactions in the Wrap Up state that were not closed either manually by an agent or automatically by the system.
-   **[Create an interaction wrap-up configuration](../task/create-interaction-wrap-up-config.md)**  
Create a configuration for each type of interaction that uses the interaction wrap up feature.
-   **[Create interaction wrap-up codes](../task/config-interaction-wrapup-codes.md)**  
Wrap-up codes enable agents to quickly wrap up and close interactions. Agents can select wrap-up codes from the interaction wrap-up modeless dialog.
-   **[Enable interaction wrap-up codes](../task/enable-interaction-wrapup-codes.md)**  
Enable interaction wrap-up codes and select the wrap-up codes that are available to agents in the interaction wrap-up modeless dialog.

**Parent Topic:**[Configuring Interaction Management](configuring-interaction-management.md)


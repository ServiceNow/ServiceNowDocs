---
title: Interaction states
description: Configure the behavior of an interaction by determining the routine behavior for each state that the interaction goes through during the life cycle.
locale: en-US
release: xanadu
product: Interaction Management
classification: interaction-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Interaction states

Configure the behavior of an interaction by determining the routine behavior for each state that the interaction goes through during the life cycle.

## Interaction framework

Configure each of the following interaction components to determine the behavior and life cycle.

-   Lists: Configure the interaction list view. You can also extend the interaction table. For more information about configuring lists, see [List configuration](https://www.servicenow.com/docs/access?context=c_ListConfiguration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Forms: Configure the form view to tailor interactions for each application. For more information about configuring forms, see [Form configuration](https://www.servicenow.com/docs/access?context=basic-form-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Interaction states

States determine the behavior for interactions. For each state of the interaction life cycle, you determine which routine actions to perform. For example, the **On Created** state would have a script that creates an interaction and then adds the end user as the 'opened for'. The script then sends a message to the end user to let them know that the interaction has been opened.

<table id="table_by1_k4r_vdb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

An interaction is inserted into the interaction table.

</td></tr><tr><td>

On Hold

</td><td>

The interaction is waiting for assignment.

</td></tr><tr><td>

Work In Progress

</td><td>

An agent accepts an unassigned interaction.

</td></tr><tr><td>

Wrap Up

</td><td>

This state indicates that the agent has completed a conversation with a customer and is wrapping up the interaction.

 This state is available if an interaction wrap up configuration has been created for the specific type of interaction and that configuration is active.

 For more information, see [Interaction wrap up](../concept/interaction-wrap-up-state.md).

</td></tr><tr><td>

Closed Complete

</td><td>

The interaction timed out or the agent or consumer intentionally closed the interaction.

</td></tr><tr><td>

Closed Abandoned

</td><td>

The interaction is closed because the consumer disconnects or is unresponsive.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Interaction Management](../concept/configuring-interaction-management.md)


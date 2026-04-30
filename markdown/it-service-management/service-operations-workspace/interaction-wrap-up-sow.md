---
title: Interaction wrap up with modeless dialog in Service Operations Workspace
description: Interaction wrap up provides agents with dedicated time after each call or chat to finalize interaction details. Agents can use this time to wrap up their work before starting a new conversation.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-12-03"
reading_time_minutes: 2
breadcrumb: [Interaction Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Interaction wrap up with modeless dialog in Service Operations Workspace

Interaction wrap up provides agents with dedicated time after each call or chat to finalize interaction details. Agents can use this time to wrap up their work before starting a new conversation.

When interaction wrap up is enabled, an interaction record moves from the Work In Progress state to the Wrap Up state at the end of a customer conversation. This configurable period of time enables agents to complete tasks such as posting work notes and updating record information before moving on to assist other customers.

While in the Wrap Up state, an agent’s capacity is not reduced until the state of the interaction moves to Closed Complete.

## Wrap-up modeless dialog

When wrap-up codes are enabled in the Interaction Wrap Up Configuration record, the modeless dialog is shown during the wrap-up period.

**Note:** To use the wrap-up modeless dialog, the interaction record must be assigned to the current user, and the user must have the interaction\_admin role.

<table id="table_hyj_xqn_nhc"><tbody><tr><td>

Wrap up timer

</td><td>

Time left before the modeless dialog closes.

 If the timer expires before submitting, wrap-up data is saved with the default code and no notes.

 The background color changes as the seconds count down, depending on the duration of time remaining \(100% to 50% is green, 50% to 25% is yellow, 25% to 0% is red\).

</td></tr><tr><td>

Wrap up code

</td><td>

Select a wrap-up code relating to how the interaction was resolved.

</td></tr><tr><td>

Notes

</td><td>

Enter additional information about the interaction.

</td></tr></tbody>
</table>When the wrap up submission is complete, the data is saved in a segment record and the state of the interaction changes to Closed Complete.

## Wrap-up segment record

Interaction wrap-up data is stored in segment records in the Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\] table. Segments can include multiple wrap-ups per interaction. For example, when one agent transfers an interaction to another agent, each agent can complete a wrap-up for the same interaction record.

## Interaction wrap up configuration

System administrators can access Interaction wrap up configuration to:

-   Create wrap-up codes \(in the Interaction Wrap Up Codes table\)
-   Configure wrap-up timer and wrap-up codes \(in the Interaction Wrap Up Configuration record\)
    -   Configure the display and duration of the wrap-up timer
    -   Enable wrap-up codes, set a default, and select the codes available to agents in the modeless dialog

For more information, see the following topics:

-   [Create an interaction wrap-up configuration](https://www.servicenow.com/docs/access?context=create-interaction-wrap-up-config&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Create interaction wrap up codes](https://www.servicenow.com/docs/access?context=config-interaction-wrapup-codes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Enable interaction wrap up codes](https://www.servicenow.com/docs/access?context=enable-interaction-wrapup-codes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

**Parent Topic:**[Interaction Management in Service Operations Workspace](interaction-sow.md)

**Related topics**  


[Create an interaction in Service Operations Workspace](../task/create-interaction-sow.md)

[Work on an interaction in Service Operations Workspace](../task/work-on-interaction-sow.md)

[Collaborate using Microsoft Teams from an interaction record in Service Operations Workspace](../task/collaborate-interaction-ms-teams-sow.md)

[Associate an interaction with a task record](../task/associate-interaction-record-sow.md)


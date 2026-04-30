---
title: Interaction records in Workspace
description: Using an interaction record, agents can create or reference customer information from a customer contact. Agents can then decide if the conversation is an incident, case, or request.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Getting work from chats, Finding issues to work on in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Interaction records in Workspace

Using an interaction record, agents can create or reference customer information from a customer contact. Agents can then decide if the conversation is an incident, case, or request.

An interaction represents a request for assistance made through a chat, phone call, or walk-up. Interactions can be routed to queues for assignment or assigned to agents directly. Support agents can create cases, requests, or incidents from the interaction. Interactions can also be used to capture one-and-done type requests where an agent might not want to create associated tasks.

![Interaction form in Agent Workspace](../image/InitialIMSrecord.png)

<table id="table_m3g_pjy_jdb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details, Related Tasks, User's Interactions forms

</td><td>

**Details** tab that shows detailed information from the interaction record. **Related Tasks** show tasks related to the interaction in the form pane, for example, a new incident. **User's Interactions** tab shows all interactions related to specific users.

</td></tr><tr><td>

Number

</td><td>

Number is associated to each customer interaction.

</td></tr><tr><td>

Type

</td><td>

Logs the type of channel communication, such as chat, phone, walk-up, or messaging.**Note:** **Phone** is an available type of channel communication when the OpenFrame plugin \(com.sn\_openframe\) is activated.

</td></tr><tr><td>

State

</td><td>

State of the interaction record: -   New
-   Work in Progress
-   Closed Complete
-   Closed Abandoned
-   On Hold

</td></tr><tr><td>

State reason

</td><td>

Reason for the current state of the interaction record: -   Waiting on customer
-   Waiting internal
-   null

This field appears only for messaging type interactions.

</td></tr><tr><td>

Opened for

</td><td>

Customer who initiates or receives the communication.

</td></tr><tr><td>

Duration

</td><td>

Tracks the amount of time an agent spends working on an interaction.

</td></tr><tr><td>

Assigned to

</td><td>

Agent the interaction record is assigned to.

</td></tr><tr><td>

Wait time

</td><td>

Time it takes to initially respond to the customer.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the interaction. **Note:** The short description field is empty by default, but it cannot be empty when the record is closed, saved, or associated to a related task. Populate the short description and then close, save, or associate the record, or you cannot archive the record.

</td></tr></tbody>
</table>While you are on an interaction, tasks that are viewed or created under the interaction are automatically logged on the Interaction Related tasks.

## Associating user profiles on messaging interactions

When a requester sends a message, the system checks whether the identifier matches an existing channel user profile. Channel user profiles are used to track the identities of conversation participants using an identifier associated with the source of the message. For SMS messages, the identifier is the phone number from which the message was sent.

<table id="table_dxp_vwy_gmb"><tbody><tr><td>

If there is a matching channel user profile

</td><td>

-   A new interaction is started.
-   Or the message is associated with an ongoing interaction for the matching channel user profile.

</td></tr><tr><td>

If there is no matching channel user profile

</td><td>

-   A new channel user profile is created.
-   A new interaction referencing the new channel user profile is created.
-   If the identifier matches a user, it populates the User document field of the channel user profile and the Opened for field of the interaction with a reference to that user.

</td></tr></tbody>
</table>
---
title: Virtual Agent interaction records
description: Each time a Virtual Agent conversation occurs, an interaction record captures the entire conversation in the Interactions \[interaction\] table. The record includes all topic elements used in the conversation, as well as live agent transfers.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
keywords: [Virtual Agent, interaction, records, interactions, table]
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent interaction records

Each time a Virtual Agent conversation occurs, an interaction record captures the entire conversation in the Interactions \[interaction\] table. The record includes all topic elements used in the conversation, as well as live agent transfers.

## Interactions \[interaction\] table

Each conversation in an instance generates an interaction record in the Interactions \[interactions\] table, which logs the conversation between a requester and Virtual Agent. The interaction records include conversations that occur across the supported chat channels: chat widget, native mobile app, and messaging integrations.

**Note:** The Interactions table is part of the Interaction Management plugin \(com.glide.interaction\). Virtual Agent, Agent Chat, and Connect Support use this plugin.

These interaction records provide administrators, Virtual Agent administrators, support agents, and support managers with a convenient way to review what happened during a conversation. The records also provide a quick way to see the type of conversations that occur: Virtual Agent, live agent transfers to Agent Chat, and live agent transfers to Connect Support.

![Key fields in the Interactions table, such as the Virtual Agent and Agent Chat fields that indicate the type of conversation.](../images/VA-interactions-table.png "Interactions [interaction] table")

**Note:** Conversation transcripts are available only for Virtual Agent records that have Virtual Agent conversations and live agent transfers to Agent Chat.

-   When a conversation transcript for live chat exceeds 4000 characters, the transcript is handled as an attachment to the interaction record.
-   File attachments that the user uploads are recorded in the Attachments \[sys\_attachment\] table, which corresponds to the interaction record. Attachments are automatically displayed in the activity stream.
-   For Virtual Agent conversations that have live agent transfers to Connect Support, only the Virtual Agent conversation is included in the interaction transcript. Live agent conversations in Connect Support are recorded in the activity stream.

## Key fields in the Interactions table

To view the Interactions table, navigate to **All**, and then enter `interaction.list` in the navigation filter. You can configure the fields displayed in the table using the [list collector](https://www.servicenow.com/docs/access?context=t_UseSlushbuckets&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) \(slushbucket\).

<table id="table_xs3_3hy_yjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent average response time

</td><td>

Average time based on how long the agent takes to respond to each message sent by a requester. For example:

 ```
00:00 Requester: I have a question.
00:01 Agent: What is it?
00:04 Requester: How do I reset my password?
00:05 Requester: I forgot it and can't access my account.
00:07 Agent: Here is the answer.
```

 Pair \#1 00:01-00:00 = 00:01

 Pair \#2 00:07-00:04 = 00:03

 \(00:01 + 00:03\) / 2 = 00:02 average

</td></tr><tr><td>

Agent chat

</td><td>

Flag that indicates the conversation was transferred to a live agent in Agent Chat: true or false.

</td></tr><tr><td>

Application

</td><td>

Scope of the application. Scope determines the accessible files and data available to other applications.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the fulfiller: Live agent name or Virtual Agent

</td></tr><tr><td>

Domain

</td><td>

The domain the conversation took place in. For more information, see [Domain separation and Virtual Agent](domain-separation-virtual-agent.md).

</td></tr><tr><td>

Number

</td><td>

Number of the interaction record.

</td></tr><tr><td>

Opened

</td><td>

Date and time that the conversation started.

</td></tr><tr><td>

Opened for

</td><td>

Name of the requester. Anonymous users are identified as Guests.

</td></tr><tr><td>

Sentiment

</td><td>

Shows the sentiment level of the interaction, if sentiment analysis is enabled on the instance. This value can be shown to agents in the Agent Chat interface. Business rules can be created based on this value at handoff \(Virtual Agent to live agent, live agent to live agent, or live agent to queue\). Valid values are as follows:-   Positive
-   Neutral
-   Negative
-   null \(no value assessed\)

This value is also entered in the [Interaction Insights table](../../conversational-interfaces/reference/ci-interaction-insights-table.md).

</td></tr><tr><td>

State

</td><td>

Conversation states: -   In Progress: Conversation between requester and virtual agent is in progress.
-   Closed Complete: Virtual agent ends the conversation.
-   Closed Abandoned: Requester ends the conversation before completing the conversation with the virtual agent.

 **Note:** There are different State Reasons for the Closed Complete and Closed Abandoned states, depending on whether you're using Virtual Agent only, Virtual Agent with Live Agent, or Live Agent only. For details on the State Reasons, see [Reasons for Closed Complete and Closed Abandoned states](va-interactions.md#section_vxj_vcq_b4b).

</td></tr><tr><td>

State Reason

</td><td>

Detailed explanations \(reasons\) for the conversation states Closed Complete and Closed Abandoned. To learn more, see [Reasons for Closed Complete and Closed Abandoned states](va-interactions.md#section_vxj_vcq_b4b).

</td></tr><tr><td>

Transcript

</td><td>

Log of the conversation between the requester and agents \(virtual or live\).

</td></tr><tr><td>

Type

</td><td>

Type of interaction record. Virtual Agent conversations are record type Chat.

</td></tr><tr><td>

Updated

</td><td>

Date and time that the conversation record was last updated.

</td></tr><tr><td>

Virtual agent

</td><td>

Flag that indicates whether the conversation is for Virtual Agent: true or false. A Virtual Agent conversation is flagged when a requester selects a conversation topic or when the topic discovery process starts the appropriate conversation.

</td></tr></tbody>
</table>## Reasons for Closed Complete and Closed Abandoned states

Virtual Agent closes completed and abandoned conversations for various reasons, depending on whether the conversation is for Virtual Agent \(VA\) only, Virtual Agent with Live Agent \(VA-LA\), or Live Agent \(LA\).

![Interactions table that shows the State Reason column for Closed Abandoned and Closed Complete states.](../images/va-interactions-reasons.png "Interactions table with State Reason column")

The **State Reason** field provides details on the different ways in which a conversation ends. The following table describes the reasons and also the related message displayed for dashboard analytics. For details about how Virtual Agent and Agent Chat handle idle conversations and the corresponding default timeout periods, see [Closing Virtual Agent and Agent Chat conversations](va-open-conversations.md).

<table id="table_wxj_vcq_b4b"><thead><tr><th>

State

</th><th>

State Reason

</th><th>

Virtual Agent

</th><th>

Virtual Agent &amp; Live Agent or Live Agent only

</th></tr></thead><tbody><tr><td>

Closed Abandoned

</td><td>

Left Before Engagement

</td><td>

Not applicable.

</td><td>

Requester chose to be routed to a live agent, but closed the conversation \(selecting **+ End**\) before an agent was assigned.

 Dashboard message:

 `User closed LA - before Agent engagement`

</td></tr><tr><td>

Closed Abandoned

</td><td>

No Activity

</td><td>

Requester opened a conversation, but didn't engage with the bot \(for example, closed the browser\) and didn't initiate topic discovery. The system closed the Virtual Agent idle conversation after the default timeout.

-   Virtual Agent idle chat timeout: Two hours \(default\)
-   Dashboard message: `System closed VA - user never engaged`

</td><td>

Requester chose to be routed to a live agent \(not through pre-chat setup\) but didn't engage with the agent. If the conversation timed out and the **Time Out Abandoned VA Conversations**scheduled job ran, the interaction state is Closed Abandoned with No Activity.

 Dashboard message: `System closed LA - before Agent engagement`

</td></tr><tr><td>

Closed Complete

</td><td>

User Ended

</td><td>

After engaging with the bot \(requester entered at least one utterance during a conversation or completed a conversation\), requester closed the conversation session by selecting **End**.

 Dashboard message: `User closed VA - Clicked End/X`

</td><td>

Requester started to chat with live agent but closed the chat client by selecting **End**.

 Dashboard message: `User closed LA - Clicked End/X`

</td></tr><tr><td>

Closed Complete

</td><td>

Auto Closed

</td><td>

Requester interacts with VA topic and completes the conversation. No live agent interaction.

 Dashboard message:`System closed VA - Auto Closed`

</td><td>

Not applicable.

</td></tr><tr><td>

Closed Complete

</td><td>

No User Response

</td><td>

Requester engaged with the bot \(entered at least one utterance\), but left without actively closing the conversation. The system closes the idle conversation after two hours \(default\).

 -   Virtual Agent idle chat closed: Two hours
-   Dashboard message: `System closed VA - User no response`

</td><td>

Requester engaged with live agent but stopped and left the agent hanging \(idle live chat\). The system closes the idle live chat after six minutes \(default\).

 -   Idle live chat closed: Six minutes
-   Dashboard message: `System closed LA - User no response`

</td></tr><tr><td>

Closed Complete

</td><td>

Topic Complete

</td><td>

Requester engaged with the bot in a topic but didn't respond to the Anything Else setup topic, or chose Yes to continue but didn't respond. The **Time Out Abandoned VA Conversations** job closes the interaction after the default timeout.

-   Virtual Agent idle chat closed: Two hours
-   Dashboard message: `System closed VA - Topic complete`

</td><td>

Not applicable.

</td></tr><tr><td>

Closed Complete

</td><td>

Left for search

</td><td>

Requester engaged with the bot \(entered at least one utterance\), but selected Search in the middle of the conversation and didn't return to the conversation. The system closes the conversation because of inactivity.Dashboard message:`System closed VA- Left with AI search`

</td><td>

Not applicable.

</td></tr><tr><td>

Closed Complete

</td><td>

Agent Ended

</td><td>

Not applicable.

</td><td>

After requester started a chat with a live agent, the agent actively closed the conversation by selecting **End Chat**.Dashboard message:`Agent closed LA - Clicked End/x`

</td></tr><tr><td>

Faulted

</td><td>

Error

</td><td>

A runtime exception occurred while processing a message.

</td><td>

Requester’s conversation was closed due to a runtime error.

</td></tr></tbody>
</table>## Detailed view of a Virtual Agent interaction record

From the Interactions table, you can open a specific record to see additional details about the Virtual Agent interaction: a transcript of the conversation, related tasks, and interaction logs.

**Note:** If a field is not visible, you can add it to the form view. For more information, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **Conversation transcript**

    The transcript shows the dialog exchange between the agent \(virtual or live\) and requester, as well as the time stamp for each dialog turn.

    ![A Virtual Agent chat transcript in a Virtual Agent interaction record.](../images/VA-interaction-record.png)

-   **Related Tasks**

    Any cases, incidents, or requests created or updated during the conversation are automatically attached to the interaction record as a Related Task. To ensure that these tasks are included with the interaction record, design your conversation topics using certain Virtual Agent Designer utilities and the system method vaSystem.attachRecordToConversation. For details, see [Topic design considerations](va-interactions.md#section_nd1_fs1_zjb) below.

    ![The Related Tasks tab on the Interactions record shows the incident record that was created during the interaction.](../images/VA-interaction-relatedtask.png)

-   **Interaction Logs**

    The **Interaction Logs** tab lists all the topics that run in a conversation, including the setup topics and the topics executed by topic discovery or by user selection. Each topic element is assigned a number that indicates the sequential order in which the topics run.

    ![The Interaction Logs tab on the Interactions record shows the topics that were run during the user interaction.](../images/VA-interaction-log-table.png)


## Security considerations

Information in conversation transcripts is viewable to all users. If you need to control access to records containing sensitive information, you can use scoped access control lists \(ACLs\) and lock scripted access to those records by using the Restricted Caller Access \(RCA\) feature. For details, see [Set application scope, application resource, and event access](https://www.servicenow.com/docs/access?context=scope-resource-access&version=zurich&pubname=zurich-application-development&ft:locale=en-US) and [Manage Restricted Caller Access](https://www.servicenow.com/docs/access?context=t_ConfigureSIM&version=zurich&pubname=zurich-security-management&section=restricted-caller-access&ft:locale=en-US).

## Topic design considerations

If your Virtual Agent conversations create or update incidents, cases, or requests, consider designing your topics with the following [Virtual Agent Designer utilities](../reference/va-utilities.md) and system method:

-   [Action utility](../reference/va-action.md) to create or update incidents or cases
-   [Lookup utility](../reference/va-lookup.md) to view information
-   System method vaSystem.attachRecordToConversation\(String tableName, String sysId\) to attach the task to the interaction record

Use these utilities and system method so that incidents, cases, or requests created during a Virtual Agent conversation are included in the **Related Tasks** list of the interaction record.

**Note:** Records created or updated using the [Script Action utility](../reference/va-script-action.md) are not captured as related tasks in the interaction record.

**Parent Topic:**[Virtual Agent technical reference](va-advanced-technical-reference.md)

**Related topics**  


[Virtual Agent roles](../reference/VA-roles.md#)

[Domain separation and Virtual Agent](domain-separation-virtual-agent.md)

[Virtual Agent scripts](virtual-agent-scripts.md)

[Input data types in Virtual Agent topics](../reference/va-data-types.md)

[NLU system entities](../reference/nlu-system-entities.md)

[Virtual Agent URL parameters](../reference/va-sysparm.md)

[Latency feedback in Virtual Agent](../reference/latency-feedback.md)


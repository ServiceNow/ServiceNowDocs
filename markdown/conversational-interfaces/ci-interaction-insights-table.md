---
title: Interaction Insights table
description: User sentiment analysis prepares agents for the tone of incoming conversations. Business rules can be created based on this value and agents can take appropriate actions on the chat, whether it comes from Virtual Agent, another live agent, or from a queue.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Conversational Interfaces reference, Conversational Interfaces Console, Conversational Interfaces]
---

# Interaction Insights table

User sentiment analysis prepares agents for the tone of incoming conversations. Business rules can be created based on this value and agents can take appropriate actions on the chat, whether it comes from Virtual Agent, another live agent, or from a queue.

Both synchronous and asynchronous channels support sentiment analysis. Use [Task Intelligence](https://www.servicenow.com/docs/access?context=task-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to set up sentiment analysis.

When configured, sentiment analysis is performed at the end of a Virtual Agent or live agent conversation. The user sentiment is stored in the Interaction Insights \[sys\_cs\_interaction\_insight\] table.

<table id="table_j1n_mvf_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Interaction

</td><td>

The sys ID for the conversation in the Interactions \[interaction\] table.

</td></tr><tr><td>

Sentiment

</td><td>

Shows the sentiment level of the interaction, if sentiment analysis is enabled on the instance. This value can be shown to agents in the Agent Chat interface. Business rules can be created based on this value at handoff \(Virtual Agent to live agent, live agent to live agent, or live agent to queue\). Valid values are as follows:-   Positive
-   Neutral
-   Negative
-   null \(no value assessed\)

</td></tr><tr><td>

Sentiment Normalized

</td><td>

Sentiment score between -0.5 \(negative sentiment\) and 0.5 \(positive sentiment\).You can modify these values by adjusting the **com.glide.cs.neutral\_sentiment\_max\_value** and **com.glide.cs.neutral\_sentiment\_min\_value** system parameters.

</td></tr><tr><td>

Type

</td><td>

Type of analysis performed. For example, **Sentiment**.

</td></tr><tr><td>

User

</td><td>

Name of the agent or Virtual Agent.

</td></tr><tr><td>

User Type

</td><td>

Type of user. For example, **Agent**.

</td></tr></tbody>
</table>**Parent Topic:**[Conversational Interfaces reference](../concept/ci-reference-parent.md)


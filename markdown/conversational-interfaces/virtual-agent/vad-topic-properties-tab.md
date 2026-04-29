---
title: Topic Properties tab
description: Use the Topic Properties tab to identify a topic and how it's used. You can control who uses the topic and what channels it can run in.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Topic Properties tab

Use the **Topic Properties** tab to identify a topic and how it's used. You can control who uses the topic and what channels it can run in.

The properties that you can specify depend on the method of topic discovery.

Two methods are available in Assistant Designer: large language model \(LLM\) or Natural Language Understanding \(NLU\)/Keyword.

For example, if you enable NLU/Keyword in Virtual Agent settings, the topic **Properties** tab includes fields for identifying the NLU model and intent for the topic.

For more information, see [Creating a Virtual Agent topic](../task/create-virtual-agent-topic.md).

## Topic Properties tab with LLM topic discovery

![image.topic-properties-llm-2]

## Topic Properties tab with NLU topic discovery

![image.topic-properties-nlu-2]

<table id="table_ulb_cfg_5cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application scope

</td><td>

Select the application scope where the topic becomes available.**Note:** The application scope cannot be changed once the topic is created.

</td></tr><tr><td>

Model type

</td><td>

Type of model for this topic, either LLM or NLU/keyword. The model type is locked when you create the topic.

</td></tr><tr><td>

Type

</td><td>

Type of topic, including basic topic, topic block, setup topic, and small talk topic.

</td></tr><tr><td>

Internal name

</td><td>

Internal name for the topic, not seen by customers.

</td></tr><tr><td>

Display name

</td><td>

Topic name displayed for customers.

</td></tr><tr><td class="sub-head" colspan="2">

LLM topics\[LLM model type only\]

</td></tr><tr><td>

Topic description used for discovery

</td><td>

Description used by the LLM to accurately match the user's question or request to the right topic. Thorough descriptions improve topic discovery. For more information, see [LLM topic discovery in Virtual Agent](../concept/va-llm.md).

</td></tr><tr><td>

Topic will be available in these assistant\(s\)

</td><td>

LLM assistant or assistants selected to make topics available to them.

</td></tr><tr><td class="sub-head" colspan="2">

NLU topics\[NLU/keyword model type only\]

</td></tr><tr><td>

Topic description

</td><td>

Description used to denote what this topic is used for.

</td></tr><tr><td>

NLU model

</td><td>

NLU model mapped to the topic.

</td></tr><tr><td>

Associated intent

</td><td>

NLU intent connected to the model and topic.

</td></tr><tr><td>

Enable DialogActs

</td><td>

Toggle to allow Virtual Agent to react dynamically to user statements.

</td></tr><tr><td>

Confirm modified values with users

</td><td>

Toggle to allow Virtual Agent to send confirmation messages to users when a value change is detected.

</td></tr></tbody>
</table>**Parent Topic:**[Assistant Designer interface reference](../concept/vad-reference.md)


---
title: \(Legacy\) Topic Properties tab for NLU
description: Use the Topic Properties tab to identify a topic and how it's used. You can control who uses the topic and what channels it can run in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/vad-topic-properties-tab-nlu.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Topic Properties tab for NLU

Use the **Topic Properties** tab to identify a topic and how it's used. You can control who uses the topic and what channels it can run in.

If you enable NLU/Keyword in Virtual Agent settings, the topic **Properties** tab includes fields for identifying the NLU model and intent for the topic.

For more information, see [\(Legacy\) Create a topic form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-topic-creation-form-nlu.md) and [\(Legacy\) Creating a Virtual Agent NLU topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-virtual-agent-topic-nlu.md).

## Topic Properties tab with NLU topic discovery

\[Omitted image "topic-properties-nlu.png"\] Alt text: The Natural Language Understanding section appears on the topic Properties tab for NLU topics.

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

Type of model for this topic, either LLM or NLU/keyword. The model type is locked when you create the topic.**Note:** This field is visible only if you installed Now Assist in Virtual Agent.

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
</table>**Parent Topic:**[\(Legacy\) Virtual Agent Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-reference-nlu.md)


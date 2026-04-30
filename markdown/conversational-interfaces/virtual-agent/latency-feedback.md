---
title: Latency feedback in Virtual Agent
description: The com.glide.cs.message.processing.enabled system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and Now Assist panel.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Latency feedback in Virtual Agent

The **com.glide.cs.message.processing.enabled** system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and Now Assist panel.

## Latency feedback messages

The **com.glide.cs.message.processing.enabled** property is off by default, but can be turned on in the System Properties \[sys\_properties\] table. After turning on this system property, users receive a temporary response to indicate that the LLM call is running and that their request is being processed. One of the following messages appears to users:

-   `Looking into your request...`
-   `Reviewing key details...`
-   `Gathering the needed info...`

The latency feedback messages can’t be customized and disappears after the LLM generates a response.



**Parent Topic:**[Virtual Agent technical reference](../concept/va-advanced-technical-reference.md)

**Related topics**  


[Virtual Agent roles](VA-roles.md#)

[Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md)

[Virtual Agent interaction records](../concept/va-interactions.md)

[Virtual Agent scripts](../concept/virtual-agent-scripts.md)

[Input data types in Virtual Agent topics](va-data-types.md)

[NLU system entities](nlu-system-entities.md)

[Virtual Agent URL parameters](va-sysparm.md)


---
title: Latency feedback in Virtual Agent
description: The com.glide.cs.message.processing.enabled system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/latency-feedback.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Latency feedback in Virtual Agent

The **com.glide.cs.message.processing.enabled** system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and Now Assist panel.

## Latency feedback messages

The **com.glide.cs.message.processing.enabled** property is off by default, but can be turned on in the System Properties \[sys\_properties\] table. After turning on this system property, users receive a temporary response to indicate that the LLM call is running and that their request is being processed. Message examples include:

-   `Thinking...`
-   `Looking into your request...`
-   `Reviewing key details...`
-   `Gathering the needed info...`

The latency feedback messages can’t be customized and disappears after the LLM generates a response.



\[Omitted image "va-latency-feedback-message.png"\] Alt text: "Thinking" is a temporary latency feedback message.

**Parent Topic:**[Virtual Agent technical reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-advanced-technical-reference.md)

**Related topics**  


[Domain separation and Virtual Agent]()

[Virtual Agent interaction records]()

[Virtual Agent scripts]()

[Input data types in Virtual Agent topics]()

[NLU system entities]()

[Virtual Agent URL parameters]()


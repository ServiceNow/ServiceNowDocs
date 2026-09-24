---
title: Virtual Agent technical reference
description: Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-advanced-technical-reference.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Virtual Agent, technical, reference]
breadcrumb: [Reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent technical reference

Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.

Virtual Agent utilizes a queuing system to process incoming messages coming from asynchronous channels. Dedicated worker threads pull from this queue and process the messages in their own transactions. This enables Virtual Agent to scale to meet traffic volume. Virtual Agent transactions run as non-interactive \(the scriptable method **gs.isInteractive\(\)** will return false\).

Various roles and tables are available when you activate Virtual Agent. For more information, see [\(Legacy\) Plugins installed with Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/installed-wth-virtual-agent.md). Virtual Agent also has a data retention policy to manage table size. For more information, see [Data management in Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-data-mgmt.md)

The following technical reference topics are available.

-   **[Virtual Agent interaction records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-interactions.md)**  
Each time a Virtual Agent conversation occurs, an interaction record captures the entire conversation in the Interactions \[interaction\] table. The record includes all topic elements used in the conversation, as well as live agent transfers.
-   **[Data management in Conversational Interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-data-mgmt.md)**  
Use data management tools, such as table cleaners, to maintain Conversational Interfaces tables.
-   **[Virtual Agent scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-scripts.md)**  
Use ServiceNow® Virtual Agent script methods and variables to write chat scripts, such as response, trigger, and flow scripts. Variables can also provide context for your live support topics and conversations.
-   **[Input data types in Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-data-types.md)**  
You can define inputs of commonly used Glide Virtual Agent \(com.glide.cs.chatbot\) data types in Assistant Designer without writing a script. Define the input data type on the Start node of a custom control or topic block.
-   **[Virtual Agent URL parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-sysparm.md)**  
Virtual Agent provides various system parameters that admins can add to an instance URL to control how page content is rendered.
-   **[Latency feedback in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/latency-feedback.md)**  
The **com.glide.cs.message.processing.enabled** system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and ServiceNow Otto panel.

**Parent Topic:**[Virtual Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-parent-reference.md)


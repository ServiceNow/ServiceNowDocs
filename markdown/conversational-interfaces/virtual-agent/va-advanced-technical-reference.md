---
title: Virtual Agent technical reference
description: Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-04-01"
reading_time_minutes: 2
keywords: [Virtual Agent, technical, reference]
breadcrumb: [Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent technical reference

Use these topics to learn more about scripting methods, NLU system entities, and the Virtual Agent Interactions table.

Virtual Agent utilizes a queuing system to process incoming messages coming from asynchronous channels. Dedicated worker threads pull from this queue and process the messages in their own transactions. This enables Virtual Agent to scale to meet traffic volume. Virtual Agent transactions run as non-interactive \(the scriptable method **gs.isInteractive\(\)** will return false\).

Various roles and tables are available when you activate Virtual Agent. For more information, see [Installed with Virtual Agent](../reference/installed-wth-virtual-agent.md). Virtual Agent also has a data retention policy to manage table size. For more information, see [Data management in Conversational Interfaces](va-data-mgmt.md)

The following technical reference topics are available.

-   **[Domain separation and Virtual Agent](domain-separation-virtual-agent.md)**  
Domain separation is supported in the Virtual Agent application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Virtual Agent interaction records](va-interactions.md)**  
Each time a Virtual Agent conversation occurs, an interaction record captures the entire conversation in the Interactions \[interaction\] table. The record includes all topic elements used in the conversation, as well as live agent transfers.
-   **[Virtual Agent scripts](virtual-agent-scripts.md)**  
Use ServiceNow® Virtual Agent script methods and variables to write chat scripts, such as response, trigger, and flow scripts. Variables can also provide context for your live support topics and conversations.
-   **[Input data types in Virtual Agent topics](../reference/va-data-types.md)**  
You can define inputs of commonly used Glide Virtual Agent \(com.glide.cs.chatbot\) data types in Virtual Agent Designer without writing a script. Define the input data type on the Start node of a custom control or topic block.
-   **[NLU system entities](../reference/nlu-system-entities.md)**  
Use globally defined NLU entities to identify system information that Virtual Agent can extract from the conversation. You can define entities as "nodeless" input variables for a topic. These variables can be slot-filled from NLU service provider predictions or provided outside of the scope of the topic.
-   **[Virtual Agent URL parameters](../reference/va-sysparm.md)**  
Virtual Agent provides various system parameters that admins can add to an instance URL to control how page content is rendered.
-   **[Latency feedback in Virtual Agent](../reference/latency-feedback.md)**  
The **com.glide.cs.message.processing.enabled** system property notifies requesters whenever the generative AI large language model \(LLM\) is processing their request in the Virtual Agent chat widget and Now Assist panel.

**Parent Topic:**[Virtual Agent reference](../reference/va-parent-reference.md)


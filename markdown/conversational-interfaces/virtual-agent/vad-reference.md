---
title: Virtual Agent Designer interface reference
description: The Virtual Agent Designer interface lets you create, modify, test, publish, and localize topics, topic blocks, and custom controls.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Designer interface reference

The Virtual Agent Designer interface lets you create, modify, test, publish, and localize topics, topic blocks, and custom controls.

Virtual Agent Designer provides the following views. Some tabs may not be available, depending on how you configured your instance or the type of topic you are working with.

-   **[Assistant Designer Asset library](../reference/vad-topics-page.md)**  
The Assistant Designer Asset library lists all LLM assets and NLU/Keyword topics available in your instance. You can also create more topics, subflows, actions, custom skills, AI agents, and agentic workflows.
-   **[Virtual Agent Designer legacy Topics page](../reference/vad-prev-topics-page.md)**  
The Virtual Agent Designer legacy home page lists cards for available topics in your instance.
-   **[Virtual Agent Designer All pre-built topics page](../reference/vad-additional-topics-list.md)**  
When you install pre-built conversations, such as ITSM Virtual Agent, some topics may not appear on the home page unless you install their dependent plugins. This page shows the additional topics that are available.
-   **[Create a topic form](../reference/vad-topic-creation-form.md)**  
The Create a topic form is used to set the properties for a new conversational topic for Virtual Agent.
-   **[Topic Properties tab](../reference/vad-topic-properties-tab.md)**  
Use the **Topic Properties** tab to identify a topic and how it's used. You can control who uses the topic and what channels it can run in.
-   **[Topic Flow tab](../reference/vad-topic-flow-tab.md)**  
Use the topic **Flow** tab to build the conversation flow. Use the controls for user inputs, bot responses, and utilities to define the flow.
-   **[Topic NLU Intent tab](../reference/vad-topic-nlu-intent-tab.md)**  
You can edit and refine ServiceNow NLU models from within Virtual Agent Designer. When a conversation topic is bound to an associated NLU model and intent, use the **NLU Intent** tab to review and edit utterances and associated entities.
-   **[Topic Languages tab](../reference/vad-topic-languages-tab.md)**  
Use the **Languages** tab to view the topic's translation status for languages that have been activated in Virtual Agent. If NLU is enabled on your instance, you can also view model mappings for each language.
-   **[Virtual Agent Designer controls](virtual-agent-controls.md)**  
A Virtual Agent topic consists of a collection of controls within a topic flow. Use these controls to collect, process, and present information to your users. Controls can also read, create, and update records on your instance.
-   **[Virtual Agent Designer user input controls](../reference/va-user-inputs.md)**  
Use the collection of input controls provided by Virtual Agent Designer to prompt and capture information from the user in a conversation.
-   **[Virtual Agent Designer bot responses](../reference/va-bot-responses.md)**  
Virtual Agent Designer offers various controls for displaying bot responses in a conversation. Because the bot responses occur in third-party platforms, the format for each output may vary.
-   **[Virtual Agent Designer utilities](../reference/va-utilities.md)**  
You can control interactions within a topic by using utilities in Virtual Agent Designer. These utilities perform various actions such as adding topic blocks \(reusable components\), running a script, or adding different conversation paths \(branches\) in a topic. Utilities are represented as nodes in a conversation flow but do not display anything to the user.

**Parent Topic:**[Virtual Agent reference](../reference/va-parent-reference.md)


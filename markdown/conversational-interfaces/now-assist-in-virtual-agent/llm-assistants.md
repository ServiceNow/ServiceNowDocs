---
title: LLM assistants
description: LLM assistants help with large language model \(LLM\) topic discovery. The Now Assist in Virtual Agent assistant is the default LLM assistant created during the Conversational Interfaces Assistants guided setup.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2024-11-13"
reading_time_minutes: 3
keywords: [LLM, Large Language Model, assistants, topic discovery, Conversational Interfaces, Virtual Agent Designer]
breadcrumb: [Exploring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# LLM assistants

LLM assistants help with large language model \(LLM\) topic discovery. The Now Assist in Virtual Agent assistant is the default LLM assistant created during the Conversational Interfaces Assistants guided setup.

If LLM topics aren't associated with an LLM assistant, they aren't discoverable and can't be tested from the home page via **Test assistant**. The **Test assistant** option only appears if you have an assistant selected in the home page **Select assistant** filter.

When using the **Select assistant** filter, topic blocks or custom controls that aren’t associated with an LLM assistant, but are called by a topic that's associated with an LLM assistant, appear in this filtered **Select assistant** home page view. Nested topic blocks or custom controls don’t appear in the filtered home page view unless they’re directly associated with an LLM assistant. For more information about testing LLM topics, see [Testing LLM topics](../../virtual-agent/reference/test-llm-topics.md). When a topic is associated with only one LLM assistant, the Assistant drop-down list defaults to that assistant name. If you have multiple assistants, select which assistant you want to work with using the Assistant drop-down list. For more information about creating multiple LLM assistants, see [Manage LLM virtual agents on the Assistants screen](../../virtual-agent/task/manage-llm-va.md).

**Tip:** On the Virtual Agent Designer home page, there's an **Assistant settings** option in the side panel. Use this option to navigate quickly to the Conversational Interfaces Assistants page to review or update your LLM assistants. For more information on the guided setup, see [Configuring Now Assist in Virtual Agent](../task/configure-now-assist-va.md).

If you want your LLM setup topic to be discoverable in an LLM assistant, you must flag the active setup topic as discoverable. For example, if you create an LLM setup topic by duplicating the Now Assist Live Agent setup topic and want to associate the setup topic with an LLM assistant, you must flag the duplicated topic as discoverable. Flag the topic as discoverable by going to the duplicated topic’s **Flow** tab, and then select **Active** &gt; **Included in topic discovery**. After enabling the **Included in topic discovery** toggle, the topic is then discoverable.

Alternatively, you can make a topic discoverable on the home page once you create an LLM topic and associate it with an assistant. Select the More actions on this row icon ![More actions icon.](../../virtual-agent/images/kebab-menu.png) next to your topic, and then select **Discoverable**. A checkmark appears by the text to indicate the topic is now discoverable.

![Included in topic discovery must be turned on if you want LLM setup topics to be discoverable when working with LLM assistants.](../image/llm-setup-topic-included-discovery.png "Included in topic discovery option in Virtual Agent Designer")

## Primary and secondary assistants

Primary and secondary assistants provide a framework enabling information flow between different assistants, with the flexibility to configure different experiences, such as search configuration, greeting, branding, and channels. The result is a seamless and integrated experience for the user.

Now Assist in Virtual Agent assistants can be set as a primary assistant and linked to one or more secondary assistants. A primary assistant inherits the information sources of the secondary assistants. When a user engages with a primary assistant, it understands the query and responds to the question even if the information sources required are within the secondary assistants. For Knowledge Graph, however, configurations must be done for each assistant.

A primary assistant uses search sources from secondary assistants. To set up your primary and secondary assistants, see [Configuring Now Assist in Virtual Agent](../task/configure-now-assist-va.md).

Information that is and isn't shared when linking primary and secondary assistants includes:

-   Search application: The primary assistant uses its own settings.
-   Now Assist skills: The primary assistant uses its own activation flags regardless of the secondary assistant's configuration.
-   Stop words: When there's a conflict between the primary and secondary assistant, the most recent **sys\_updated\_on** value is used.
-   Knowledge Base boosting condition: The primary profile should mirror the rules of all of its secondary assistants.

Using primary and secondary assistants is useful if different business units create and maintain their own assistants but want to have linkages between assistants to effectively share information.



![Diagram of primary and secondary assistants.](../image/NAinVA-mapping-example.png)


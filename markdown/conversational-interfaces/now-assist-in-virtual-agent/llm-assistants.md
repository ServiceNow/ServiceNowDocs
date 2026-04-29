---
title: LLM assistants
description: LLM assistants help with large language model \(LLM\) topic discovery. The Now Assist in Virtual Agent assistant is the default LLM assistant created during the Conversational Interfaces Assistants guided setup.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 4
keywords: [LLM, Large Language Model, assistants, topic discovery, Conversational Interfaces, Virtual Agent Designer]
breadcrumb: [Exploring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# LLM assistants

LLM assistants help with large language model \(LLM\) topic discovery. The Now Assist in Virtual Agent assistant is the default LLM assistant created during the Conversational Interfaces Assistants guided setup.

If LLM topics aren't associated with an LLM assistant, they aren't discoverable and can't be tested from the home page via **Test assistant**. The **Test assistant** option only appears if you have an assistant selected in the home page **Select assistant** filter.

When using the **Select assistant** filter, topic blocks or custom controls that aren’t associated with an LLM assistant, but are called by a topic that's associated with an LLM assistant, appear in this filtered **Select assistant** home page view. Nested topic blocks or custom controls don’t appear in the filtered home page view unless they’re directly associated with an LLM assistant. For more information about testing LLM topics, see [Testing LLM topics](../../virtual-agent/reference/test-llm-topics.md). When a topic is associated with only one LLM assistant, the Assistant drop-down list defaults to that assistant name. If you have multiple assistants, select which assistant you want to work with using the Assistant drop-down list. For more information about creating multiple LLM assistants, see [Manage LLM virtual agents on the Assistants screen](../../virtual-agent/task/manage-llm-va.md).

**Tip:** On the Virtual Agent Designer home page, there's an **Assistant settings** option in the side panel. Use this option to navigate quickly to the Conversational Interfaces Assistants page to review or update your LLM assistants. For more information on the guided setup, see [Configuring assistants overview](../task/configure-now-assist-va.md).

If you want your LLM setup topic to be discoverable in an LLM assistant, you must flag the active setup topic as discoverable. For example, if you create an LLM setup topic by duplicating the Now Assist Live Agent setup topic and want to associate the setup topic with an LLM assistant, you must flag the duplicated topic as discoverable. Flag the topic as discoverable on the home page once you create an LLM topic and associate it with an assistant. Select the More actions on this row icon ![](../../virtual-agent/images/kebab-menu.png) next to your topic, and then select **Discoverable**. A checkmark appears by the text to indicate the topic is now discoverable.

![Turn on the Discoverable option to make LLM setup topics available when working with LLM assistants.](../../virtual-agent/images/asset-library-discoverable.png "Discoverable option in Asset library")

## Primary and secondary assistants

Primary and secondary assistants provide a framework enabling information flow between different assistants, with the flexibility to configure different experiences, such as search configuration, greeting, branding, and channels. The result is a seamless and integrated experience for the user.

Now Assist in Virtual Agent assistants can be set as a primary assistant and linked to one or more secondary assistants. A primary assistant inherits the information sources of the secondary assistants. When a user engages with a primary assistant, it understands the query and responds to the question even if the information sources required are within the secondary assistants. For Knowledge Graph, however, configurations must be done for each assistant.

A primary assistant uses search sources from secondary assistants. To set up your primary and secondary assistants, see [Configuring assistants overview](../task/configure-now-assist-va.md).

Information that is and isn't shared when linking primary and secondary assistants includes:

-   Search application: The primary assistant uses its own settings.
-   Now Assist skills: The primary assistant uses its own activation flags regardless of the secondary assistant's configuration.
-   Stop words: When there's a conflict between the primary and secondary assistant, the most recent **sys\_updated\_on** value is used.
-   Knowledge Base boosting condition: The primary profile should mirror the rules of all of its secondary assistants.

Using primary and secondary assistants is useful if different business units create and maintain their own assistants but want to have linkages between assistants to effectively share information.

![Diagram of primary and secondary assistants.](../image/NAinVA-mapping-example.png "Primary and secondary assistants agentic workflow example")

## Applicability at an assistant level

You can also control the applicability of a gen AI skill by assistant. When the applicability is set, the skill will only be applied to a specific assistant. To set the skill applicability:

1.  Navigate to **All** and enter **sys\_gen\_ai\_skill\_applicability.list**
2.  In the Generative AI Skill Applicabilities table, find the skill for which you want to set the applicability.
3.  In the **Context Profile** column, select the assistant for which you want access to the selected skill.

    **Note:** If you see a `Security prevents writing to this field` message, set your application scope to match the skill.


In the following example, for the promoted generative AI skill - Send Email, when the context profile is set to the Now Assist Panel assistant, the skill appears when the assistant is called. But when the context profile is changed to a different assistant, the skill does not appear for the Now Assist Panel assistant.

![Setting context profile.](../image/assistant-skill-appl.png)


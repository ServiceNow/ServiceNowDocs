---
title: Long-term memory categories
description: Long-term memory \(LTM\) categories define the types of semantic information that a Now Assist AI agent can learn and retain about users over time. You can add new categories and map them to specific agents to personalize agent responses based on accumulated user context.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Set up long-term memory, Configure, Now Assist AI agents, Enable AI experiences]
---

# Long-term memory categories

Long-term memory \(LTM\) categories define the types of semantic information that a Now Assist AI agent can learn and retain about users over time. You can add new categories and map them to specific agents to personalize agent responses based on accumulated user context.

Semantic memory in the AI agent Memories table \(`sn_aia_memory_list`\) is organized by LTM categories. Each category represents a distinct type of user-specific information, such as software preferences, workplace context, or communication style. By mapping categories to an agent, you control what the agent learns and retains across interactions.

## How LTM categories work

When an agent executes, the platform evaluates the interaction for user-specific facts that match the agent's configured LTM categories. Matched facts are stored as semantic memory records in the AI Agent Memories \[sn\_aia\_memory\] table, scoped to the user and category. On subsequent interactions, the agent retrieves relevant semantic memories and uses them to personalize its responses without requiring the user to repeat context.

LTM categories are defined globally and can be mapped to one or more agents. An agent only learns and retrieves memories for the categories explicitly mapped to it.

## Default LTM categories

The platform includes the following default LTM categories:

-   **Software and tools**

    Captures information about applications, tools, and software configurations relevant to the user, such as operating system version or approved applications.

-   **Work context**

    Captures facts about the user's role, department, location, and workplace preferences, such as remote work setup or team structure.

-   **User preferences**

    Captures communication preferences and interaction style, such as preferred language, response format, or notification settings.


You can extend this list by creating custom categories suited to your organization's use cases.

## How categories affect memory extraction

During memory extraction, the platform runs an LLM prompt that evaluates the agent interaction against the descriptions of each mapped LTM category. If the interaction contains information that matches a category, a semantic memory record is created or updated in the AI Agent Memories table with the following fields:

-   **Category**

    The LTM category that the memory is associated with.

-   **User**

    The user whose interaction generated the memory.

-   **Memory**

    The extracted user-specific fact, stored as a JSON object.

-   **Type**

    Set to **Semantic** for category-based memories.


Semantic memories are retrieved at runtime using retrieval-augmented generation \(RAG\) and injected into the agent prompt to personalize the response for the current user.

## Considerations

-   Category descriptions directly influence LLM extraction quality. Use specific, unambiguous language to reduce false positives or missed extractions.
-   Mapping too many categories to a single agent can increase extraction processing time. Map only the categories relevant to the agent's use case.
-   To verify that semantic memories are being extracted, open the AI Agent Memories table and filter by **Type** = **Semantic** and the relevant agent or user.


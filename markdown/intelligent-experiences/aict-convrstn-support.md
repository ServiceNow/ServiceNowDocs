---
title: Conversational interface in AI Control Tower
description: The conversational experience of the ServiceNow AI Platform is integrated into AI Control Tower via ServiceNow Otto. The conversational interface is a single natural-language entry point that spans all AI Control Tower capabilities: answering questions about your AI portfolio, surfacing data visualizations, navigating to the right context, and executing actions—all powered by the agent orchestration of AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-convrstn-support.html
release: zurich
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [generative AI, agentic AI, AI Control Tower, Otto premium chat, Conversational support]
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# Conversational interface in AI Control Tower

The conversational experience of the ServiceNow AI Platform is integrated into AI Control Tower via ServiceNow Otto. The conversational interface is a single natural-language entry point that spans all AI Control Tower capabilities: answering questions about your AI portfolio, surfacing data visualizations, navigating to the right context, and executing actions—all powered by the agent orchestration of AI Control Tower.

## How the conversational interface works

The ServiceNow Otto chat is a chat client with agentic orchestration that delivers an AI-native experience. For information about the basic usage and features of the premium chat in the ServiceNow AI Platform, see [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/nava-integrated-chat.md).

The conversational interface understands natural language queries and intelligently routes requests to the appropriate AI Control Tower agents, which execute against live data and return structured results. The interface then presents answers, visualizations, navigation paths, and recommended actions in a conversational flow that feels natural and context-aware.

## Core concepts

The conversational interface in AI Control Tower is built on six frameworks:

-   **User Profile Framework**

    Stores and manages user attributes—role, permissions, behavioral patterns, and inferred preferences.

-   **Context Orchestration Framework**

    Instruments user context and persists it across conversation sessions and turns.

-   **Persistent Memory Framework**

    Records and references user memory across sessions.

-   **Agent Orchestration**

    Routes queries to the appropriate agents based on intent, user profile, and page context—not just on the utterance alone.

-   **Agent Framework**

    Agents have no memory or context of their own. They query live structured data to enrich responses and can query across multiple data domains and instance tables.

-   **Next Best Action Framework**

    Uses intent resolution, context, and memory to apply a confidence score to each possible interpretation of what the user should do next.


## Core capabilities

In AI Control Tower, every query uses the answer response mode. The answer mode returns precise answers to natural-language questions about any AI Control Tower entity—assets, agents, models, controls, tasks, or policies—with AI insights, analysis, recommendations, and next steps. The scope includes counts, lookups, status, rankings, comparisons, and trend summaries.


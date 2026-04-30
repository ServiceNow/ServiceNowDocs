---
title: Advantages of natural language models over keywords
description: Natural language models help Virtual Agent to process human language based on context and your company's data. In this way, what the user needs can be more accurately matched with a corresponding topic. Virtual Agent supports large language models \(LLMs\) and Natural Language Understanding \(NLU\).
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent, Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Advantages of natural language models over keywords

Natural language models help Virtual Agent to process human language based on context and your company's data. In this way, what the user needs can be more accurately matched with a corresponding topic. Virtual Agent supports large language models \(LLMs\) and Natural Language Understanding \(NLU\).

## Language is difficult

Keyword matching has its limitations. For example, sometimes an apple is a piece of fruit, and sometimes it's an electronic device. Context matters, and so does intent. Natural language models are designed to deal with the following problems:

-   There are multiple ways to describe the same thing.

    Examples: `Office password reset` or `Reset my password for Office`

-   Expressions can be ambiguous.

    Example: `Server reporting mail missing after migration`. What is missing, the server or the mail?

-   Contextual information is essential.

    Example: `activate London instance in staging`

-   Words can acquire new meanings over time.

    For example, a `cell` can pertain to biology or a cell phone.

-   Slang, acronyms, and industry idioms can be difficult to interpret.

    Example: `set up SSO on the dev instance`

-   Error messages are often hard to understand.

Virtual Agent provides two kinds of natural language topic discovery. You can use both in your instance, but only one at a time in any given chat.

-   **[LLM topic discovery in Virtual Agent](va-llm.md)**

    Use LLMs to discover topics and access generative AI capabilities without building complex models, intents, or entities.

-   **[Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](va-NLU.md)**

    Use ServiceNow NLU or a supported provider to discover topics.



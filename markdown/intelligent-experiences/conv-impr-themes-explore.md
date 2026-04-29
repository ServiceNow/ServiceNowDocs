---
title: Exploring Conversation Improvement Themes
description: The Conversation Improvement Themes application helps to transform conversation evaluations into long-term performance insights.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [explore]
breadcrumb: [Conversation Improvement Themes, Enable AI experiences]
---

# Exploring Conversation Improvement Themes

The Conversation Improvement Themes application helps to transform conversation evaluations into long-term performance insights.

## Conversation Improvement Themes overview

The Conversation Improvement Themes analyzes conversation quality data over time. The approach focuses on identifying recurring patterns linked to low conversation quality \(and high\) and categorizing user requests into actionable themes using metadata-driven classification powered by large language models \(LLMs\).

**Note:** Conversation Improvement Themes can use OpenAI, Gemini, or Claude. It’s observed in certain instances that Gemini and Claude could consume a higher number of assists, compared to the OpenAI model, which is observed to have optimal use of assists.

## How themes are created

To create themes, metadata like name, short description, and so on, from different content types like knowledge base articles, catalog items, virtual agent topics, and AI agents are analyzed. Theme generation is performed using an LLM-based categorization process that relies only on metadata rather than full article content, which helps limit token usage, reducing processing overhead. For each created theme, definitions are created using the tagged content from the LLM-based classification process, which helps in tagging primary requests from conversations.

Approach:

1.  Filter by User Satisfaction Score. For example, select conversations where evaluator results are associated with low user satisfaction score \(&lt;=1.5\) or High Score &gt;= 4.5.
2.  Extract and standardize Primary requests:
    1.  Parse the user’s Primary request, removing noise from different writing styles or phrasing.
    2.  Apply standardization so similar intents, for example, reset my password versus can't log in are grouped consistently.
3.  Frequency analysis:
    1.  Link each standardized request to a theme.
    2.  Count how often each theme appears when the virtual agent underperforms or performs well.
    3.  Highlight themes where the virtual agent handles requests poorly or well on the screen.


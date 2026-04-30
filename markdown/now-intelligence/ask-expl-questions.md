---
title: Questions and responses in an exploration
description: Ask the AI specific questions in AI Data Explorer, to which it responds with data visualizations, a summary, and suggested follow-up questions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Questions and responses in an exploration

Ask the AI specific questions in AI Data Explorer, to which it responds with data visualizations, a summary, and suggested follow-up questions.

To ask a question in an exploration, launch AI Data Explorer from a data visualization or list or open an existing exploration. You will see a field with the placeholder "Ask Now Assist a question about data." For more information, see [Launch AI Data Explorer](../task/launch-now-assist-explorer.md).

**Note:**

-   The question you ask has to be about data in one of the tables listed in the Query Generation Semantic Table Configuration table. These tables can include database views and Workflow Data Fabric tables. For more information, see [Add a table to the semantic data layer](../task/add-table-semantic-layer.md#).
-   AI Data Explorer cannot access data from secure scopes.
-   When you have submitted a question, you cannot submit another question or do other work in the exploration until your question is processed. You can cancel the processing of your question.

When you write a question in an exploration, the AI converts the question to a database query. The AI returns the following items:

-   ![Area 1](../image/callout-1.png) Your original question. You can edit this question to generate new output.
-   ![Area 2](../image/callout-2.png) The title of the response and a summarization of the AI findings.
-   ![Area 3](../image/callout-3.png) A list or data visualization. This response can be an existing visualization instead of a generated one. For more information, see [Launch AI Data Explorer](../task/launch-now-assist-explorer.md).
-   ![Area 4](../image/callout-4.png) Suggestions for follow-up questions.

You can select and drag these sections of the response to change their order.

![The response returned from a question to AI Data Explorer, showing the summary, data visualization, and suggested follow-up questions.](../image/nowass-expl-response.png)

## Viewing the response source

After you receive a response from the ServiceNow AI Platform, hover over the response to see the technical details of the response. The source details include the following information:

-   The source table
-   The filter conditions
-   The metric
-   Any grouping criteria

If the exploration is too narrow on the screen, you select **View source** instead of hovering.

![Source details for a response in an exploration.](../image/nowass-expl-response-source.png)

## Deleting a response

If you expand the rectangle of dots before the beginning of the response, you have a button to delete the response.

![Button to delete response.](../image/nowass-delete-response.png)

## Tips for asking questions

The goal of AI Data Explorer is to understand your prompts in your own words, delivering the analytics insights you want. However, if you do not know where to begin to formulate questions, or you are unsatisfied with the results, here are some tips:

-   **Name your table**

    If you know the name of the table that contains the data you are interested in, add it to your prompt. Partial names or similar names are fine too.

    Example: Instead of "How many P1s were opened this week,” write "How many P1 requests were opened this week," which references the request tables. Better yet, write "How many P1 catalog requests were opened this week," which references the specific Catalog Requests table.

-   **Explain what you mean**

    Query Generation tries to understand your terms, but you can add details to help guide it. If you get unexpected results, try being more specific about what you're looking for.

    Example: Instead of "Show me all stale incidents," write "Show me all incidents not updated in 5+ days."

-   **Be specific with names**

    When filtering by referenced records like users, groups, or services, try to use their full display names for best results. The AI model may learn from previous queries in the same document, but using full names ensures accuracy.

    Example: Instead of "Cases with Workplace Ops," write "Cases with Workplace Operations."

-   **Edit and refine queries**

    If the generated query isn't quite right, you can manually edit the filter conditions. The AI model will learn from your edits and apply them to future questions in the same document. For more information, see [Change the question or filter conditions](../task/manually-edit-source-conditions.md)

    Example: You ask "Show me critical incidents from the network team" but are not satisfied with the response. Instead of asking repeated variations of the same question, hoping for a better result, edit the filter to find records where Assignment Group is ‘Network Operations’ and Priority is ‘1 - Critical’. Then ask "Show me the inflow trend for these incidents over time”.

-   **Don't leave bad queries in your exploration**

    The AI model uses the previous document context to write the next query. Therefore, if you cannot refine a query to get a useful response, delete it. Otherwise bad queries can accumulate in your exploration, leading to ever-worsening responses.

-   **Import complex filters**

    For complex data that's hard to describe, import data visualizations or lists into your exploration. If the visualization or list is on a dashboard, you can apply any filters on the dashboard before importing. The AI model will use imported queries to understand related questions in the same document.

    Example: Don't ask "Show me servers about to retire by location." Such a prompt is vague and complex. Instead, import a visualization from a dashboard titled "PostgreSQL servers nearing retirement,” with the desired values for the dashboard filters Lifecycle State and Days Until Retirement pre-applied. Then ask "Show me the same servers but grouped by location”.


Once you have a productive exploration going, with a lot of context, you may find that you are able to ask more abstract questions and get useful answers. However, these tips might help you get started.

-   **[Extended analysis](hidden-insights.md)**  
Generate a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.
-   **[Add a data visualization from an exploration to a dashboard](../task/add-data-viz-from-expl-to-dboard.md)**  
Put the visualization contained in a response from AI Data Explorer on a new or existing dashboard. Do so without interrupting your workflow in your exploration.
-   **[Refresh a response with new data](../task/refresh-response.md)**  
Look at the age of the response to a question in an AI Data Explorer exploration. Then regenerate the response with fresh data.
-   **[Change the question or filter conditions](../task/manually-edit-source-conditions.md)**  
Regenerate the response to a question after you change the question or the filter conditions.
-   **[Duplicate, delete, copy to another exploration, or move an answer in an exploration](../task/nowass-expl-dup-del-question-resp.md)**  
Duplicate, delete or reorder an individual question and response from inside an exploration. You can also copy a response to another exploration.

**Parent Topic:**[Using AI Data Explorer](use-now-assist-explorer.md)


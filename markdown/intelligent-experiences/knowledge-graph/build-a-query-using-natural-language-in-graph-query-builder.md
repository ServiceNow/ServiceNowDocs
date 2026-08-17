---
title: Build a query using natural language in Graph Query Builder
description: You can also ask a question in natural language, the Graph Query Builder populates the query in the builder and runs it to get results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/knowledge-graph/build-a-query-using-natural-language-in-graph-query-builder.html
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Graph Query Builder, Knowledge Graph, Enable AI experiences]
---

# Build a query using natural language in Graph Query Builder

You can also ask a question in natural language, the Graph Query Builder populates the query in the builder and runs it to get results.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge graph** &gt; **Graph Query Builder**.

2.  Select a graph from the graph drop-down in the **Input query for graph** section.

    If you select Enterprise Graph or Enterprise Graph \(small\), you will see an additional tag selection field to scope the available entities to specific tables.

    **Note:** Tags aren't available for user created graphs.

    \[Omitted image "nlq\_query\_builder.png"\]

3.  Select one or more tags from the drop-down, if you want to run a query using Enterprise Graph or Enterprise Graph \(small\).

4.  Enter a natural language question in the **Ask in natural language** section.

    Example: `Show me all the incidents assigned to users in customer support department`.

    \[Omitted image "nlq\_query\_builder\_example.png"\]

5.  Select an LLM to use from the following options:

    -   NowLLM
    -   Claude
    -   NowLLM-LTS
    -   Gemini
    -   GPT
6.  Select **Run and build**.

    Graph Query Builder generates a query from your input, populates it in the query builder, runs it, and displays the results in the Query results section.

7.  Review the generated query and edit it directly in the query builder.

8.  Select **Run** to re-run the query after editing and save it, if you want to reuse it later.



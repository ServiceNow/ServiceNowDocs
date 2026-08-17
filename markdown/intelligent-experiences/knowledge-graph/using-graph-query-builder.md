---
title: Graph Query Builder
description: Graph Query Builder provides a visual interface for building and running Knowledge Graph queries without writing code. You can also use natural language to generate queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/knowledge-graph/using-graph-query-builder.html
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [graph query builder, query builder, knowledge graph query builder]
breadcrumb: [Knowledge Graph, Enable AI experiences]
---

# Graph Query Builder

Graph Query Builder provides a visual interface for building and running Knowledge Graph queries without writing code. You can also use natural language to generate queries.

You have two options on the Graph Query Builder page. You can either to ask query in Natural language or build your own query using the Query Builder.

\[Omitted image "graph\_builder\_module.png"\] Alt text: Graph Query Builder

If you prefer to build a query, you can select a graph between Enterprise Graph, Enterprise Graph Small, or a user-created graph. Choose a starting entity and add relationships to the connected entities by applying **AND** or **OR** filters on the properties. You can define which output fields appear in the results and whether to return individual records or aggregated results.

As you build, a live graph in the right panel shows the query taking shape. You can confirm it matches your intent before running it.

You can also skip this manual query construction and ask a natural language question instead. Graph Query Builder converts your natural language input into a query using the LLM of your choice and lets you review, edit, and rerun it.

Example natural language query: `Show me all incidents assigned to the Finance team.`

You can save the successful queries as private or for everyone who has access. This prevents rebuilding common or complex queries.

## Graph Query Builder benefits

Discover what you can actually query: Explore the entities, relationships, and properties available in a graph, instead of guessing at the underlying data model.

Build complex queries without writing syntax: The UI guides you through multi-hop traversal, relationship selection, and filters, step by step.

See your query before you run it: A live graph view builds alongside you as you add entities and relationships, so you can confirm the query matches your intent before executing it.

Get results in the shape you need: Choose a list of records or an aggregated result, such as a count, so the output matches what you want to answer.

Reuse and share your work: Save a successful query for yourself, or share it with everyone who has access, so complex or recurring queries does not need to be rebuilt from scratch.

Review and refine your query: Ask a natural language question and Query Builder shows you the exact query it generates, revealing how the question would be interpreted by ServiceNow® Otto for Virtual Agent or an AI agent. It is useful to refine phrasing and building trust in AI-assisted results.


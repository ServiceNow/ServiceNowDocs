---
title: Using Enterprise graph schema
description: Use Enterprise Graph for accurate natural language query responses, across the entire database.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Knowledge Graph, Enable AI experiences]
---

# Using Enterprise graph schema

Use Enterprise Graph for accurate natural language query responses, across the entire database.

Enterprise graph is a pre-configured Knowledge Graph schema that maps all instance tables and their connections, enabling natural language queries for data across all tables.

To see some examples of the Natural Language query responses, refer [Natural language queries use cases and examples](../concept/natural-language-queries-example-usecases.md).

Enterprise graph schema simplifies Knowledge Graph setup by providing a preconfigured schema, eliminating the need for custom schema creation in Knowledge Graph designer.

Admins can choose Enterprise graph as the Knowledge Graph schema when using AI agents, Now Assist Virtual Agent, or Now Assist panel admin and add tags to enhance accuracy.

By mapping all tables, the Enterprise graph schema expands query capabilities to cover the entire database, whereas a custom or out-of-the-box \(OOTB\) schema limits queries to only the tables included in its specific schema.

## Benefits of Enterprise Graph on Prebuilt integration

Now Assist Virtual Agent- With Enterprise Graph integration, Now Assist Virtual Agent can respond to a wide range of questions about their enterprise data from requester, helping to deflect queries.

Now Assist panel- With Enterprise Graph enabled, Now Assist panel allows fulfillers to obtain insights from the structured data in instance by asking natural language questions, which boosts their productivity.

AI agents- With Enterprise Graph enabled, AI agents can access relevant information from structured data in ServiceNow instance directly from the Knowledge Graph, giving them essential context for tasks.

## Modes of Enterprise Graph

Enterprise Graph has two modes:

-   Enterprise Graph- regular mode
-   Enterprise Graph \(Small\)

Regular mode is used for use cases with large number of tables \(more than 50 tables\), to:

-   Searches across all tables, but gives more priority to tables which are included in the tag added at time of configuring Enterprise Graph in the consuming app \(AI agent or VA\).
-   Useful for scenarios where answer is expected from large number of tables.

Enterprise Graph \(Small\) is a version of Enterprise Graph that limits the search to only the tables tagged with specific labels. This means it can only answer queries related to those tables. It's useful for:

-   Searches only within tables which are included in the tag added at time of configuring Enterprise Graph \(Small\) in consuming app \(AI agent or VA\). Tagging is mandatory in this mode. ​
-   Useful for latency-sensitive use cases with limit of 50 tables​

## Tags in Knowledge Graph

Tags are lists of key tables that are important for answering natural language questions in a specific use case. They are required to be used with Enterprise Graph and Enterprise Graph \(Small\).


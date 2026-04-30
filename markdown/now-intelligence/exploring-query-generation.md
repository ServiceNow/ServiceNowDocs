---
title: Exploring Query Generation
description: Query Generation is an AI-powered service that translates user questions into an executable query and returns the results. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. The results include a textual summary, a data visualization, and suggestions for follow-up.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-21"
reading_time_minutes: 2
breadcrumb: [Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Exploring Query Generation

Query Generation is an AI-powered service that translates user questions into an executable query and returns the results. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. The results include a textual summary, a data visualization, and suggestions for follow-up.

## Query Generation overview

Query Generation relies on a semantic data layer to generate queries. The semantic data layer is a flat representation of tables and table columns that the Query Generator uses to find the actual facts tables and columns related to a user utterance. Specifically, facts tables are represented by Entity records and their columns by Dimension records.

Not all facts tables are included in Query Generation, as this would overload an instance. To see which facts tables are included, open the Semantic Tables Configurations list \[sn\_query\_gen\_table\_config\_list\], and note which tables are present and have Enable Semantic Generation = true. You can add more tables to the list, but be careful of possible performance impacts. For more information, see [Add a table to the semantic data layer](../task/add-table-semantic-layer.md#).

## How Query Generation works

![The Query Generation process for producing an executable query.](../image/querygen-overview-diagram.png)

Before Query Generation can call the LLM, it has to filter the instance schema down to only the relevant entities and dimensions needed to answer the user's question. This filtration serves two critical purposes:

-   It provides the LLM with precise grounds for truth about available tables and columns, preventing hallucination of non-existent data structures.
-   It maintains a focused context window, which improves LLM performance and accuracy compared to processing the entire schema.

Query Generation uses a semantic filter to narrow the entities \(facts tables\) to the 2 closest matches to the user's question. Then from those entities, it narrows the dimensions \(columns\) to the 30 most similar to the user's question. Query Generation passes these results to the LLM, which generates a semantic query. A constitutor takes this semantic query and translates it into an executable query.

## Query Generation users

|User|Description|
|----|-----------|
|ServiceNow AI Platform administrators responsible for Now Assist in Platform Analytics \[admin\]|Administrators can add or remove tables from the semantic data layer. Only users with the admin role can read or change Query Generation records.|
|Users of Now Assist in Platform Analytics applications|Users of the Now Assist in Platform Analytics applications call Query Generation through those applications, although Query Generation is not visible to them. They should have the required Query Generation user roles through the roles granted to them to use the intermediary application.|

## What to explore next

To learn more about configuring and using Query Generation, see:

-   [Configuring Query Generation](configuring-query-generation.md)
-   [Query Generation reference](query-generation-reference.md)


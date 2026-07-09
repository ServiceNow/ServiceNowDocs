---
title: Exploring Query Generation
description: Query Generation is an AI-powered service that translates user questions into an executable query and returns the results. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. The results include a textual summary, a data visualization, and suggestions for follow-up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/exploring-query-generation.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Exploring Query Generation

Query Generation is an AI-powered service that translates user questions into an executable query and returns the results. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. The results include a textual summary, a data visualization, and suggestions for follow-up.

## Query Generation overview

Query Generation supports the following data sources:

-   Tables
-   Performance Analytics [automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md) \(excluding Data Snapshots\)

Table data is queried through a [semantic data layer](). The semantic data layer is a flat representation of tables and table columns that Query Generation uses to find the actual [facts tables]() and columns related to a user [utterance](). Specifically, facts tables are represented by [Entity]() records and their columns by [Dimension]() records.

Not all facts tables are included in Query Generation, as this would overload an instance. To see which facts tables are included, open the Semantic Tables Configurations list \[sn\_query\_gen\_table\_config\_list\], and note which tables are present and have Enable Semantic Generation = true. You can add more tables to the list, but be careful of possible performance impacts. For more information, see [Add a table to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/add-table-semantic-layer.md).

Indicator data is searched through the Indicator \[pa\_indicators\] table. Indicators are not represented in the semantic data layer.

## How Query Generation works

\[Omitted image "querygen-overview-diagram.png"\] Alt text: The Query Generation process for producing an executable query.

The filter first checks the query contents for information about whether to use table data or an indicator score in the response. The check follows these steps:

1.  Does the application calling Query Generation support only table data, only indicator data, or both?
2.  If it supports both data sources, is a data source specified in the query?
    1.  Are there keywords in the query, such as "table" or "indicator," that clearly show what data source is desired?
    2.  Is the query made in the context of a data source type? For example, is an AI Data Explorer query launched from a data visualization of table or indicator data? Is it launched from a follow-up question, and if so, what is the data source of the parent query?
3.  If the data source is not specified, the fallback defined in **sn\_query\_gen.default\_source\_type** is used. The default value is `table`.

    **Note:** If indicator data is selected, but the query would require more than two levels of breakdown in the response, Query Generation falls back to table data.


## Filtering table data

Before Query Generation can call the [LLM](), it has to filter the instance schema down to only the relevant entities and dimensions needed to answer the user's question. This filtration serves two critical purposes:

-   It provides the LLM with precise grounds for truth about available tables and columns, preventing hallucination of non-existent data structures.
-   It maintains a focused context window, which improves LLM performance and accuracy compared to processing the entire schema.

Query Generation uses a semantic filter to narrow the entities \(facts tables\) to the 2 closest matches to the user's question. Then from those entities, it narrows the dimensions \(columns\) to the 30 most similar to the user's question. Query Generation passes these results to the LLM, which generates a semantic query. A constitutor takes this semantic query and translates it into an [executable query]().

## Query Generation users

|User|Description|
|----|-----------|
|ServiceNow AI Platform administrators responsible for Now Assist in Platform Analytics \[admin, sn\_query\_gen.admin\]|Administrators can add or remove tables from the semantic data layer. Only users with the admin role can read or change Query Generation records.|
|Users of Now Assist in Platform Analytics applications \[sn\_query\_gen.user\]|Users of the Now Assist in Platform Analytics applications call Query Generation through those applications, although Query Generation is not visible to them. They should have the required sn\_query\_gen.user role through the roles granted to them to use the intermediary application.|

## What to explore next

To learn more about configuring and using Query Generation, see:

-   [Configuring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-query-generation.md)
-   [Query Generation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/query-generation-reference.md)


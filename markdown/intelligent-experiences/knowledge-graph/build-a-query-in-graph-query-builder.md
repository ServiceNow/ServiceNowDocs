---
title: Build a query in Graph Query Builder
description: Use Graph Query Builder to build a query by selecting the entities and their relationship, apply filters, choose the output columns and run the query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/knowledge-graph/build-a-query-in-graph-query-builder.html
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 2
breadcrumb: [Graph Query Builder, Knowledge Graph, Enable AI experiences]
---

# Build a query in Graph Query Builder

Use Graph Query Builder to build a query by selecting the entities and their relationship, apply filters, choose the output columns and run the query.

## Before you begin

Role required: kg\_admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge graph** &gt; **Graph Query Builder**.

2.  Select a graph from the graph drop-down in the **Input query for graph** section.

    \[Omitted image "query\_builder\_tagselection.png"\]

    If you select Enterprise Graph or Enterprise Graph \(small\), you will see an additional tag selection field to scope the available entities to specific tables.

    **Note:** Tags aren't available for user created graphs.

    \[Omitted image "query\_builder\_visual.png"\] Alt text: Graph Query Builder example

3.  Select one or more tags from the drop-down, if you want to run a query using Enterprise Graph or Enterprise Graph \(small\).

4.  Select a start node from the **Build with Query Builder** section.

5.  Select the \[Omitted image "filter-outline-24.svg"\] Alt text: filter icon option to add filters and \[Omitted image "relationship\_icon.png"\] option to add relationships and hop onto another node.

    The selected node is the root of your query. As you add conditions and relationships, you can see a live graph view of the query alongside the builder, in the right panel.

6.  Combine multiple filters with AND or OR and add second-level conditions and relationships to the existing conditions, if required.

    -   You can add a relationship to traverse to a related entity. Add connection on the node to see the outgoing, incoming, and self-referencing relationships related to that entity, including any related CMDB tables.
    -   Select a relationship to add the connected entity to your query.
    -   You can add more entities, relationships, and filters to build a multi-hop query.
7.  Select an output type from the **Output configurations** sections.

    The options are:

    -   List of records: For a list, select the output entity and the specific columns you want returned. You can rename any column with an alias.
    -   Aggregation: Select **Add numbers** and an option from the drop-down. You can then select a node and field and also rename any column with an alias, to show it in the results.
8.  Select the **Group numbers by** check box and select a field from the drop-down.

    The options are

    -   Sort list by: select a field to sort the list of records in ascending or descending order.
    -   Limit number of records: To limit records in the results.
    -   Show distinct records only: To show only distinct results.
9.  Select **Group numbers by ** option for aggregation and an option to sort the output.

    The options are:

    -   Sort the output by a column
    -   Limit the number of records returned
    -   Restrict results to distinct records
10. Select **Run Query**.

    \[Omitted image "query\_builder\_result.png"\]\[Omitted image "query\_builder\_json\_output.png"\]

    Graph Query Builder runs the query and displays the results in table view and as JSON.



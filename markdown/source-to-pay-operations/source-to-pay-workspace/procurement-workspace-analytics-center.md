---
title: Source-to-Pay Workspace Analytics Center
description: With Source-to-Pay Workspace Analytics Center, you can ask a question about your data, and see how things are performing now and trends over time.
locale: en-US
release: xanadu
product: Source-to-Pay Workspace
classification: source-to-pay-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Source-to-Pay Workspace reference, Source-to-Pay Workspace, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay Workspace Analytics Center

With Source-to-Pay Workspace Analytics Center, you can ask a question about your data, and see how things are performing now and trends over time.

This Analytics Center is modeled using Natural Language Query \(NLQ\) which is helpful in converting natural language into database queries, thus fetching relevant data from the respective database tables. In this case, NLQ is developed with the help of configurable synonyms and semantic shortcuts. In synonyms, for example, to fetch data from the Supplier column in the Purchase Line table, a synonym "vendor" is added. Similarly, multiple synonyms can be configured to further improve search results. In semantics, conditions can be configured for the synonym such that search results can be further optimized. For example, to render appropriate search results for closed contracts, a condition "active=false" is configured against the synonym "closed" for the Contract Task table.

![Source-to-Pay Workspace Analytics Center](../image/workspace-analytics-center.png "Source-to-Pay Workspace Analytics Center")

Based on these synonyms and semantic conditions, some of the predefined supported questions are listed here.

-   Purchase requisition
    -   Order type
        -   Show me purchase requisitions of type standard
        -   Show me purchase requisitions of type blanket
        -   Show me standard purchase requisitions
        -   Show me blanket purchase requisitions
    -   Requisition type
        -   Show me net new purchase requisitions
        -   Show me revised purchase requisitions
    -   Active
        -   Show me all open purchase requisitions
        -   Show me all closed purchase requisitions
-   Sourcing request: Active
    -   Show me all open sourcing requests
    -   Show me all closed sourcing requests
-   Negotiation: Active
    -   Show me all open negotiations
    -   Show me all closed negotiations
-   Purchase line: Product type
    -   Show me all purchase lines of type good
    -   Show me all purchase lines of type goods
    -   Show me all purchase lines of type service
-   Purchasing tasks and all extensions of purchasing tasks: Active
    -   Show me all open &lt;task type&gt;
    -   Show me all closed &lt;task type&gt;
-   Purchase order: Order type
    -   Show me purchase orders of type standard
    -   Show me purchase orders of type blanket
-   Purchase order line: Product type
    -   Show me all purchase order lines of type good
    -   Show me all purchase order lines of type goods
    -   Show me all purchase order lines of type service
-   Milestones
    -   Completion date
        -   Show me upcoming milestones
        -   Show me today's milestones
        -   Show me past milestones
        -   Show me historical milestones
    -   Active
        -   Show me all open milestones
        -   Show me all closed milestones
-   Receipt tasks: Active
    -   Show me all open receipt tasks
    -   Show me all closed receipt tasks
-   Procurement cases: Active
    -   Show me all open procurement cases
    -   Show me all closed procurement cases

**Note:** For any questions that you may want to ask about your data, ensure that you specify the table name as it appears in the database, along with other keywords as required, such as the state or type, for example. Search results are sometimes displayed graphically, based on the search criteria used.

If you do not get the desired search results, select **How can I improve my results?** to view tips and suggestions on improving your search.

**Parent Topic:**[Source-to-Pay Workspace reference](../../accounts-payable-operations/reference/source-to-pay-ws-reference.md)


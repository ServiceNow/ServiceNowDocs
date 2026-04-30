---
title: Search Log fields and description
description: The knowledge search log stores the history of all knowledge searches performed by the users.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View knowledge logs, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Search Log fields and description

The knowledge search log stores the history of all knowledge searches performed by the users.

The Search log stores information from all the available sources where users can access knowledge articles. It displays data from the Knowledge Searches \[ts\_query\_kb\] table.

**Note:** The Knowledge Search log captures data only from Zing searches. It does not work with AI searches.

As an administrator and knowledge manager, you can access the search log by navigating to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Search Log**.

The following table describes some of the fields in the Search log.

<table id="table_dg1_vc3_ybb"><thead><tr><th>

Search log field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search term

</td><td>

Search term used to perform the search.

</td></tr><tr><td>

Results

</td><td>

Number of matching knowledge articles returned by the search.

</td></tr><tr><td>

User

</td><td>

User ID of the user who performed the search.

</td></tr><tr><td>

Sort Order

</td><td>

Sort order \(relevance, views, newest, or alphabetical\) while performing the search.

</td></tr><tr><td>

Final Search Term

</td><td>

When this value is true, the value in **Search term** is the final successful search term used in the search session.

</td></tr><tr><td>

Highest Click Rank

</td><td>

The rank of the first search result the user clicked on to get the relevant search results. A lower search count indicates that the search operation is efficient.

</td></tr><tr><td>

Session Id

</td><td>

Unique identifier for the user session.

</td></tr></tbody>
</table>For information about finding the source used for searching a knowledge article, see [View the source of a knowledge article search](../task/find-knowledge-search-source.md).

**Parent Topic:**[View knowledge logs](../task/view-knowledge-logs.md)


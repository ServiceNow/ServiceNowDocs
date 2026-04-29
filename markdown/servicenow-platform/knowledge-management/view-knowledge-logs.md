---
title: View knowledge logs
description: Knowledge logs display information about which users have viewed knowledge articles, what they looked for, and where.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View knowledge logs

Knowledge logs display information about which users have viewed knowledge articles, what they looked for, and where.

## Before you begin

Role required: knowledge\_admin, knowledge\_manager

## About this task

Knowledge logs capture information from all the available sources where users can access knowledge articles, such as Customer Service Portal, Knowledge Management Service Portal, Now Mobile, Agent Workspace, and Knowledge Management v3.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Search Log** or **View Log**.

2.  View the Search or View logs.

<table id="table_dg1_vc3_ybb"><thead><tr><th>

Log

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search Log

</td><td>

View records of the search source, search terms, the highest click rank, and the number of search results of knowledge searches from all the available sources where users can access knowledge articles. The Search log displays data from the Knowledge Searches \[ts\_query\_kb\] table. For more information about the search source, see [View the source of a knowledge article search](find-knowledge-search-source.md).

</td></tr><tr><td>

View Log

</td><td>

View records showing who has viewed which knowledge articles, who has attached a knowledge article to a task and when, and identify final search terms when the type-ahead search suggestions feature is enabled. The View log displays data from the Knowledge Use \[kb\_use\] table.**Note:**

-   An administrator can activate the kb\_use table cleanup job to delete any older records from the Knowledge Use \[kb\_use\] table and improve the table performance. For more information, see [Modify the data retention policy for View logs](auto-flush-kb-use.md).
-   The View log record doesn't display information for a knowledge article accessed and viewed from the global search results.


</td></tr></tbody>
</table>
-   **[Search Log fields and description](../reference/km-search-logs.md)**  
The knowledge search log stores the history of all knowledge searches performed by the users.
-   **[View Log fields and description](../reference/km-view-logs.md)**  
The knowledge View log stores the history of knowledge articles views and their usage.
-   **[View the source of a knowledge article search](find-knowledge-search-source.md)**  
Analyze knowledge searches by finding the source used for searching a knowledge article.
-   **[Modify the data retention policy for View logs](auto-flush-kb-use.md)**  
Remove unwanted and older data from the Knowledge Use \[kb\_use\] table through the data retention policy.

**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)


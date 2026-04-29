---
title: Feedback information on contextual search
description: When a user clicks any of the action buttons such as This helped, Order, or Attached, the feedback information is stored in specific tables. The information helps you to understand the effectiveness of the searches. You can also create custom reports by querying these tables.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Feedback information on contextual search

When a user clicks any of the action buttons such as **This helped**, **Order**, or **Attached**, the feedback information is stored in specific tables. The information helps you to understand the effectiveness of the searches. You can also create custom reports by querying these tables.

<table id="table_ulb_rbw_wq"><thead><tr><th>

Table \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Relevant Document Detail \[cxs\_rel\_doc\_detail\]

</td><td>

The list of individual recorded actions. For example, Preview, This helped, Attach, or Order.The key fields in the Relevant Document Detail table are as follows:

-   **Original search terms**: The original search terms. This field is used only when the fulfiller has overridden the original search terms using the related search box.
-   **Relevance type**: The recorded action.
-   **Relevant document**: The reference to the search session group in the Relevant Document table.
-   **Created by**: The user who performed the action.
-   **Position**: The position of the recorded action in the result list.
-   **Search Resource**: The reference to the search resource for that particular result. Used only for a Predictive Intelligence Similarity result.

</td></tr><tr><td>

Relevant Document \[cxs\_relevant\_doc\]

</td><td>

Groups the Relevant Document Detail individual recorded actions by search session.**Note:** A new search session group is created every time you create or open a record or reload the page.

 The key fields in the Relevant Document table are as follows:

-   **Search session**: The search session group.
-   **Displayed on**: The table or record producer where the results were displayed.
-   **Relevant to**: The reference to the table record when **Displayed on** is **Table**.
-   **User/Created by**: The user who performed the action.

</td></tr></tbody>
</table>-   **[Run a report on contextual search usage](../task/t_RunAFeedbackReport.md)**  
Run a report on usage such as how many times a knowledge article is attached to a record to know the effectiveness of the contextual search results.

**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)


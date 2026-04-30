---
title: Diagnose user access to an article
description: Identify which users have access to an article and what enables that access.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User criteria diagnostics for Knowledge Management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Diagnose user access to an article

Identify which users have access to an article and what enables that access.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin, or admin

## Procedure

1.  Access the **User Criteria Diagnostics** landing page using one of these options:

<table id="table_mg3_lkl_1db"><thead><tr><th>

To access

</th><th>

Navigate to

</th></tr></thead><tbody><tr><td>

Using the application navigator

</td><td>

**Knowledge** &gt; **Administration** &gt; **User Criteria Diagnostics**.

</td></tr><tr><td>

From an article

</td><td>

1.  **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.
2.  Select the knowledge base that has the article to diagnose for user access.
3.  In the **Knowledge** related list, select the article.
4.  In the **Related Links** section, click **Run User Criteria Diagnostics**.
 The **User Criteria Diagnostics** landing page appears with the **Select article** field pre-populated.

</td></tr></tbody>
</table>2.  To diagnose user access:

    1.  In the **Select user** field, select a user.

    2.  From the **Select record type** choice list, select **Article**.

    3.  In the **Select article** field, select an article.

        Every time you select a different user, record type, or knowledge base, the page refreshes and displays data for the selected user.

    4.  Click **Diagnose**.

        The page displays these details:

        -   Whether or not the user has access to the knowledge article based on their domain. Only system administrators can view domain information and change the domain to give access to a user.
        -   Which user criteria provides read or read and contribute access for this user to the article and what type of [user criteria definition](t_SelectUCArticle.md) enables this access.
        -   Whether a role of the user has \(knowledge\_manager, knowledge\_admin, or owner of the knowledge base\) enables this access.
        -   For a user with no access to this article, which user criteria may be modified to grant the access.
        **Note:** Members of an ownership group are automatically given **Can Contribute** access to knowledge articles that their ownership group is associated with.


## Example

The following image shows an example of a diagnosis where the user Adela Cervantsz has read access to the KB article, KB0000001 v5.0, in the IT knowledge base because Adela belongs to one of the **Can Read** user criteria defined in the knowledge base.

![User criteria diagnosis for an article.](../image/user-crit-diag-article.png)


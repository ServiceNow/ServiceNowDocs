---
title: Move a knowledge article
description: You can move articles between knowledge bases.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Move a knowledge article

You can move articles between knowledge bases.

## Before you begin

Role required: User must have contributor access to the knowledge base.

**Note:**

-   When versioning is enabled, and you move an article from one knowledge base to another, the latest version of an article is moved to the new knowledge base. However, the previous versions of the article remain in the old knowledge base. It is recommended to retire the article from the old knowledge base. For more information, see [Retire a knowledge article](../concept/c_RetiredKnowledgeArticles.md).
-   Although you can move an article from one knowledge base to another consider creating an article in new knowledge base.

## Procedure

1.  Edit a knowledge article.

2.  Change the **Knowledge Base** field value.

    After moving an article, the Apply Default Values dialog box prompts you to populate certain fields in the article with default values from the new knowledge base. If the new knowledge base has no default values, the dialog box does not appear.

3.  Click **OK** to overwrite fields with the default values, or **Cancel** to leave all fields unchanged.

    A knowledge manager can define default values for articles in knowledge bases you manage using the **Set default knowledge field values** field on the Knowledge Base form.

4.  Click **Update**.


**Parent Topic:**[Creating and maintaining articles](../concept/creating-and-maintaining-articles.md)


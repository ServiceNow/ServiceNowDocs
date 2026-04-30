---
title: Add a knowledge article to featured content
description: Add a knowledge article to appear in the Featured content section of the knowledge homepage and at the top of knowledge search results page.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration tasks for knowledge managers, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a knowledge article to featured content

Add a knowledge article to appear in the Featured content section of the knowledge homepage and at the top of knowledge search results page.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin, or admin

## About this task

Adding an article to featured content requires associating an article to specific keywords. You can search a keyword in the knowledge service portal or search results page to display articles in the Featured content section or at the top of the knowledge search results list.

**Note:** The articles added to the Featured content section do not appear in the global search results and Virtual Agent conversations.

-   To display articles in the Featured content section, add a default keyword in the **glide.knowman.default\_keyword** property **Value** field and add the same keyword to all articles you want to display in that section.
-   To display articles at the top of the knowledge search results list, add a list of keywords to each article you want to display at the top of the list \(it is not applicable for AI search\).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Bases**.

2.  Select a knowledge base.

3.  On the Knowledge form, click the Featured content related list.

4.  Select **New**.

5.  On the Knowledge keyword form, in the Knowledge field, search for and select the article.

6.  In the Keywords field, click the unlock keywords icon \(![Lock icon.](../../../common/image/icon-lock.png)\).

7.  Select the lookup icon \(![look-up icon](../../../administer/notification/image/search-icon.png)\) to open the **Knowledge keywords** list.

8.  Select the keyword to add for this article.

    **Note:** If you're creating a new keyword, it must be a single word and cannot contain spaces.

9.  Select the unlock keywords icon \(![Lock icon.](../../../common/image/icon-lock.png)\) to add the keywords to the article.

10. Select **Submit**.


## Result

The featured content on the knowledge service portal displays the article.

**Parent Topic:**[Configuration tasks for knowledge managers](../concept/c_KnowledgeManager.md)

**Related topics**  


[Define a knowledge article category](t_DefineAKnowledgeCategory.md)

[Assign a knowledge base manager](t_AssignAKnowledgeBaseManager.md)


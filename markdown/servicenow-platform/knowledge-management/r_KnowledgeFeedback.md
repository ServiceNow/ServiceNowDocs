---
title: Provide feedback on knowledge articles
description: You can view and contribute to feedback on knowledge articles.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Provide feedback on knowledge articles

You can view and contribute to feedback on knowledge articles.

## Feedback options

You can submit feedback for knowledge articles in these ways:

-   Flag an article as incorrect or inappropriate.
-   Provide a rating value for the article.
-   Mark an article as helpful or not helpful.
-   View comments, add a new comment, or reply to existing comments.

Users can view comments directly on the article. Knowledge managers can view the other types of feedback by navigating to **Knowledge** &gt; **Feedback**.

**Note:** To know more about Knowledge article view properties and rating options that appear with articles, see [Knowledge article view properties](r_KnowledgeProperties.md#).

Administrators and knowledge managers can disable some feedback options using fields on the Knowledge Base form. Administrators can configure feedback options using properties.

## Flagging articles

You can flag an article for incorrect or inappropriate content. Click **Flag Article** in the article header to open a new window, allowing you to enter suggested changes.

-   Flagged comments do not appear on the Article View page. Users with the admin, knowledge\_admin, and knowledge\_manager roles can access flagged articles by navigating to **All** &gt; **Knowledge** &gt; **Articles** &gt; **All Flagged**. Users with the knowledge role can access their flagged articles by navigating to **All** &gt; **Knowledge** &gt; **Feedback Management** &gt; **My Flagged**.
-   If disabled, the author of the article and users with the admin, knowledge\_admin, and knowledge\_manager roles can see all flagged comments. Other users can see only their own flagged comments.

**Note:**

-   You cannot disable flagging for an article until you have disabled the flagging for all feedback comments for that article.
-   If Disable Suggesting is checked at the Knowledge Base level, the **Flag Article** button does not appear for any knowledge article

Flagged comments are stored in the Knowledge Feedback \(kb\_feedback\) table but not the Live Feed Messages \(live\_message\) table.

## Rating articles

The five stars below the article title allow you to indicate the article's effectiveness on a scale of 1 to 5.

**Note:** If the **Disable rating** is checked at the Knowledge Base level, the Rating Article button does not appear for any knowledge article.

## Marking articles

The question Helpful? at the bottom of the article allows you to indicate the usefulness of the article with a simple **Yes** or **No** answer. The **Yes** and **No** options are always available on the knowledge article view page even when you had selected an option earlier.

**Note:** If the **Disable Mark as helpful** is checked at the Knowledge Base level, the Marking Article button does not appear for any knowledge article.

## Comments

Knowledge comments at the bottom of the article use Live Feed to enable a conversation around a knowledge article. For example, you can post replies to comments, add attachments, or Like comments. The **glide.knowman.use\_live\_feed** property controls the display of knowledge article comments. If enabled, the system uses Live Feed to manage and display feedback on knowledge articles.

**Note:** Unauthenticated users and users with only the snc\_external role can’t add or view attachments for comments.

**Parent Topic:**[Creating and maintaining articles](../concept/creating-and-maintaining-articles.md)

**Related topics**  


[Automating feedback management to improve content](../concept/actionable-knowledge-feedback.md)

[Request a knowledge base](../task/t_RequestAKnowledgeBase.md)

[Create a knowledge article from an incident in ITSM Agent Workspace](../task/create-knowledge-article.md)


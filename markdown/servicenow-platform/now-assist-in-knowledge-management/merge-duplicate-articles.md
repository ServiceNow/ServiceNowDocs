---
title: Merge duplicate articles
description: Merge multiple duplicate knowledge articles into a single, consolidated article using Now Assist in Knowledge Management. This task helps knowledge managers reduce redundancy, preserve source article traceability, and verify readers access the most accurate and recent information.
locale: en-US
release: australia
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Merge duplicate articles

Merge multiple duplicate knowledge articles into a single, consolidated article using Now Assist in Knowledge Management. This task helps knowledge managers reduce redundancy, preserve source article traceability, and verify readers access the most accurate and recent information.

## Before you begin

Role required: admin

Ensure to configure and activate Identify duplicate articles and Merge duplicate articles skills. For more, see [Merge duplicate articles](merge-duplicate-articles.md) and [Configure and activate the Now Assist Identify duplicate articles skill](Now-Assist-configuring-identify-duplicate-article-skill.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center**.

2.  In the **Potential duplicates** card, select **View all** to view the list of potential duplicate articles.

3.  From the list of articles, select the articles that you want to merge.

4.  Select the knowledge base where you want to create this article.

5.  Select the article template that you want to use for creating the article.

6.  Select **Next**.

    **Note:**

    1.  After a merged article is created and saved, you can navigate to **Source Articles** to view all articles that were selected to create the new merged article. When the merged article is published, source articles in **Draft** or **In‑Review** state are expired, with the **Valid To** date set to the published date of the merged article.
    2.  When the merged article is published, source articles in **Published** state are handled based on the `glide.knowman.enable_article_replacement_on_retire` property. If the property is **false** the article is retired. If the property is **true** the article is retired and replaced. After the merged article is published, a notification is sent to all source article owners.
    3.  When the merged article is created from the Duplicate Article screen, source duplicate article records are marked as **Merged to new** and can’t be merged again.
    4.  Use the following table to learn about the fields and the validation rules required for merging an article.
    |Field|Validation rules|
    |-----|----------------|
    |Article count|Minimum 2, Maximum up to 5 articles.|
    |Topic|All articles must belong to the same topic.|
    |State|Draft, In Review, or Published only.|
    |Language|Use English only.|
    |Scope|Articles must be from the same scope.|
    |Knowledge Blocks|Knowledge blocks can’t be merged.|


## Result

A new article is created from the merged set of articles.

**Parent Topic:**[Using Now Assist in Knowledge Management](../concept/using-now-assist-in-km.md)


---
title: Identify and review duplicate Knowledge articles
description: Review duplicate Knowledge articles using the Now Assist Identify and review duplicate articles feature.
locale: en-US
release: yokohama
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-04-24"
reading_time_minutes: 1
breadcrumb: [Use Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Identify and review duplicate Knowledge articles

Review duplicate Knowledge articles using the Now Assist Identify and review duplicate articles feature.

## Before you begin

Role required: knowledge\_admin and knowledge\_manager

The Now Assist Knowledge skill required to enable the identify duplicate articles feature is activated by the admin. To configure the skill, see [Configure and activate the Now Assist Identify duplicate articles skill](Now-Assist-configuring-identify-duplicate-article-skill.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **Duplicate Articles**.

2.  Expand each list of duplicate topics to view the duplicate Knowledge articles.

    ![Duplicate articles list view.](../image/duplicate-article-list-view.png)

3.  Review the article categories and select the duplicate articles listed under it.

4.  From the **Actions on selected rows** menu select the **Unmark as Duplicate** action to be applied on the selected articles.

    ![Select the duplicate articles and also the action from the Action on selected rows drop-down list.](../image/review-duplicate-articles-and-unmark.png)

    **Important:**

    Articles unmarked as duplicates may reappear in the list during the next schedule of the job run due to regrouping of records. Grouping of records happens during every job run. Records created after a job run are considered for the next schedule.

    This feature can be applied to new articles, published articles, new drafts or articles that are in review.

    This feature may not work as expected for non-English articles.


**Parent Topic:**[Using Now Assist in Knowledge Management](../concept/using-now-assist-in-km.md)


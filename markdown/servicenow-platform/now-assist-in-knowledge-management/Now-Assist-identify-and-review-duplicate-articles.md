---
title: Identify and review duplicate Knowledge articles
description: Review duplicate Knowledge articles using the identify and review duplicate articles feature in ServiceNow Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-identify-and-review-duplicate-articles.html
release: australia
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use ServiceNow Otto in Knowledge Management, ServiceNow Otto in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Identify and review duplicate Knowledge articles

Review duplicate Knowledge articles using the identify and review duplicate articles feature in ServiceNow Otto.

## Before you begin

Role required: knowledge\_admin and knowledge\_manager

The ServiceNow Otto knowledge skill required to enable the identify duplicate articles feature is activated by the admin. To configure the skill, see [Configure and activate the identify duplicate articles skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-configuring-identify-duplicate-article-skill.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **Duplicate Articles**.

2.  Expand each list of duplicate topics to view the duplicate Knowledge articles.

    \[Omitted image "duplicate-article-list-view.png"\] Alt text: Duplicate articles list view.

3.  Review the article categories and select the duplicate articles listed under it.

4.  From the **Actions on selected rows** menu select the **Unmark as Duplicate** action to be applied on the selected articles.

    \[Omitted image "review-duplicate-articles-and-unmark.png"\] Alt text: Select the duplicate articles and also the action from the Action on selected rows drop-down list.

    **Note:**

    Articles unmarked as duplicates may reappear in the list during the next job run due to regrouping of records. Grouping happens during every job run. Records created after a job run are considered for the next schedule.

    This feature applies to new articles, published articles, new drafts, and articles in review.

    This feature may not work as expected for non-English articles.


**Parent Topic:**[Using ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-in-knowledge-management/using-now-assist-in-km.md)


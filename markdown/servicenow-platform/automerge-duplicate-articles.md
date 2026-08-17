---
title: Merge and publish potential duplicate articles
description: Review AI-identified groups of similar articles, merge duplicates, and publish the result. Knowledge Center generates a recommendation and confidence score for each topic to help you decide how to act.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/automerge-duplicate-articles.html
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [auto-merge, potential duplicates, Knowledge Center, duplicate articles, merge and publish]
breadcrumb: [Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Merge and publish potential duplicate articles

Review AI-identified groups of similar articles, merge duplicates, and publish the result. Knowledge Center generates a recommendation and confidence score for each topic to help you decide how to act.

## Before you begin

Role required: knowledge manager or knowledge admin.

The **Identify duplicate articles** and **Merge articles** skills must be enabled.

The `sn_km_gen_ai.auto_merge.enable` system property must be enabled. If it is not enabled, the existing potential duplicate experience opens instead of this dashboard.

The **Enable auto merge publish** flag determines what action is available for a topic on a per-knowledge-base basis. If this flag is enabled on the topic's knowledge base, the topic appears under **Ready to publish** and supports the bulk **Merge &amp; publish** action. If this flag is not enabled, the same recommendation and confidence score appear under **Ready to merge**. Only **Review draft** is available; merge and publish the article manually.

## About this task

Topics are groups of similar articles identified by AI. For each topic, an LLM generates a recommendation, a confidence score, and a rationale. The recommendation is to either **create an article** from the topic or **update an existing one**, and the score shows how certain the model is. A topic qualifies for an automated recommendation only when all its articles are in the same knowledge base and have no knowledge blocks or other media. Topics that don't qualify go under **Needs review** and may show a confidence score of zero.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center**.

2.  On the Knowledge Center homepage, select **View all** in the **Potential duplicates** insight card to open the Potential duplicates dashboard.

    The **Overview** tab opens by default.

3.  In the **Overview** tab, select the desired knowledge base from the **Knowledge Base** filter.

    The dashboard shows only the topics found in the selected knowledge base. Select **All** to view topics across every knowledge base you have permission to view.

4.  Review the summary cards: **Topics found**, **Topics ready to publish**, **Topics ready to merge**, and **Topics need review**.

5.  Under **Topics**, select a filter: **All**, **Ready to publish**, **Ready to merge**, or **Needs review**.

    Use the **Confidence** filter to narrow the list by confidence score or article count.

6.  Select a topic to expand it and review the recommendation.

    The expanded card shows the articles in the topic, the recommendation status, the confidence score, and the merge rationale.

7.  Select an action for the topic based on its status and your review.

    -   To review the recommended content before publishing, select **Review draft**. The draft version of the merged or updated article opens for review, editing, and publishing.
    -   For topics under **Ready to publish**, select their check boxes, then select **Merge &amp; publish** to merge the articles in each selected topic and publish the result in a single action.
    -   To ignore a topic that is not a true duplicate, select **Dismiss**, then confirm by selecting **Ignore** in the confirmation dialog.

## Result

Merging a topic publishes the article. Based on the recommendation, it either creates a new article or updates an existing one. The article follows the approval workflow configured for the knowledge base. If instant publishing is enabled, the article publishes immediately. If approval is required, the article goes through the approval rules before publishing.

## What to do next

Dismissing a topic deselects its articles as duplicates and removes the topic from the list. The topic can reappear if the same articles are identified as potential duplicates in a future scan.

Topics containing media content or knowledge blocks, or whose articles belong to different knowledge bases, are available for manual review only. Select **Open Topic** to open the list view, where you can act on these articles manually.

The **Articles** tab shows the existing list view, where you can review and act on individual articles.

Completed runs appear on the **History** tab. You can revert a run within a configurable period, five days by default. Reverting restores the previous version of each updated article. If the run created a new article, the new article is deleted. You revert the entire batch; you can't revert a single article within a batch, and a batch is not eligible for revert after the configured period has passed. Article modified manually after automatically merging will not be eligible for the merge and would be shown in the history tab.

**Related topics**  


[Identify and resolve duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/identify-duplicate-articles.md)

[Enable system properties for Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/enable-system-properties-for-KC.md)

[View article optimization analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-article-optimization.md)


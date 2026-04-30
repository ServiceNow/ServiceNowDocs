---
title: Recall an article that is being reviewed in Agent Workspace
description: Recall an article that is being reviewed to stop the approval process.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Recall an article that is being reviewed in Agent Workspace

Recall an article that is being reviewed to stop the approval process.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article you want to recall.

Ensure that the article versioning feature is enabled. For more information, see [Article versioning](../concept/article-versioning.md).

Role required: agent\_workspace\_user

## About this task

The author of a knowledge article, knowledge administrators, and system administrators can recall the article. If an ownership group is assigned to a knowledge article, the ownership group manager and ownership group members can also recall the knowledge article.

If a version of a knowledge article is in the **Review** workflow state, you can recall only the corresponding version to make additional changes. Recalling the article results in a minor version increment.

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **All Articles**.

3.  Click the link to the article in **Review** workflow state that you want to recall.

4.  On the Knowledge form, click **Recall**.


## Result

The article opens in edit mode and the workflow state of the article is changed to **Draft**. The version number of the article increments by 0.01.

**Related topics**  


[Edit a knowledge article in Agent Workspace](edit-article-workspace.md)

[Knowledge workflows](../reference/r_KnowledgeWorkflows.md)


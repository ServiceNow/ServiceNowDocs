---
title: Approve a knowledge article in Agent Workspace
description: Approve a knowledge article that is awaiting your review in Agent Workspace.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approve a knowledge article in Agent Workspace

Approve a knowledge article that is awaiting your review in Agent Workspace.

## Before you begin

Role required: agent\_workspace\_user

## About this task

If the article versioning feature is enabled, only users who are assigned as approvers can modify a knowledge article that is in the **Review** state. If you are not an approver but need to modify the article, consider recalling the article. For more information, see [Recall an article that is being reviewed in Agent Workspace](recall-article-review-agent.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **My Articles - Unpublished**.

3.  Click an article link in **Review** workflow state.

4.  Click **Edit**.

5.  In the Approvals related list, in the **State** column, click **Requested**.

    The Approval form opens in another tab within Agent Workspace.

6.  From the State list, select **Approved**.

7.  Click **Save**.

    The approved knowledge article is published immediately or on the scheduled publish date, if the article is scheduled for publishing. If the article versioning feature is enabled, the version number of the knowledge article increments to the next whole number \(for example, from 2.02 to 3.0\). On the Knowledge form of the article, the workflow state changes to **Published**. The new published version of the article is added to the Article Versions related list on the Knowledge form. The version is also available in the All Articles list in Agent Workspace, go to **Knowledge** &gt; **All Articles**.


**Related topics**  


[View a knowledge article in Agent Workspace](view-article-agent.md)


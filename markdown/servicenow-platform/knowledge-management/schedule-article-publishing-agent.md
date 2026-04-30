---
title: Schedule a knowledge article for publishing in Agent Workspace
description: Set a specific time and day for a knowledge article to be published in Agent Workspace automatically.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Schedule a knowledge article for publishing in Agent Workspace

Set a specific time and day for a knowledge article to be published in Agent Workspace automatically.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article you want to schedule for publishing.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated. For more information, see [Activate the Knowledge Management Advanced plugin](activate-knowledge-advanced-plugin.md).
-   The article versioning feature is enabled. For more information, see [Article versioning](../concept/article-versioning.md).

**Note:** You can also schedule a knowledge article for publishing from the Knowledge Management application in the ServiceNow AI Platform interface. For more information, see [Schedule a knowledge article for publishing](schedule-article-publishing.md).

Role required: agent\_workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **My Articles - Unpublished Articles**.

3.  Click an article link.

4.  In the **Scheduled publish date** field, click the show calendar icon \(![Show calendar icon](../image/show-calendar.png)\).

5.  Select any future date in the calendar.

6.  In the **Select Time** field, enter a time in the format hh:mm:ss.

7.  Click **OK**.

8.  Click **Publish** to enable the publishing workflow.

    **Tip:** If you want to cancel an article's scheduled publication and move the article back to the Draft state, click **Recall**.


## Result

The knowledge article is published on the scheduled publish date depending on the following workflow settings of its knowledge base:

-   If the knowledge base workflow is set to **Knowledge - Instant Publish**, the knowledge article is automatically published on the scheduled publish date. The **Workflow** field on the Knowledge form of the article is updated to **Scheduled for publish**.
-   If the knowledge base workflow is set to **Knowledge - Approval Publish**, the knowledge article is published on approval completion. The **Workflow** field on the Knowledge form of the article is updated to **Review**.

    The approval completion affects the scheduled publishing as follows:

    -   If the approvals are completed before the scheduled publish date, the **Workflow** field on the Knowledge form of the article is updated to **Scheduled for publish** and the article is published on the scheduled publish date.
    -   If the approvals are completed after the scheduled publish date, the article is published immediately on the approval completion.

**Related topics**  


[Edit a knowledge article in Agent Workspace](edit-article-workspace-1.md)

[Knowledge workflows](../reference/r_KnowledgeWorkflows.md)


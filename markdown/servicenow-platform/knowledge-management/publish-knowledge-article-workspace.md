---
title: Publish a knowledge article in Agent Workspace
description: Publish a knowledge article to make it available to users.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Publish a knowledge article in Agent Workspace

Publish a knowledge article to make it available to users.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article you want to publish.

Role required: agent\_workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge** &gt; **My Articles - Unpublished**.

3.  Click a knowledge article link.

4.  On the Knowledge form, click **Publish**.


## Result

A knowledge article is published depending on the workflow setting of its knowledge base:

-   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
-   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.

    **Note:** With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. An administrator can override this behavior by disabling the **glide.knowman.ownership\_group.enable\_self\_approval** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md).


For more information, see [Schedule a knowledge article for publishing in Agent Workspace](schedule-article-publishing-agent.md).

When published, your knowledge article appears in the My Articles - Published and All Articles lists. If the article versioning feature is enabled, the version of the article is incremented based on the [version number pattern](../concept/knowledge-article-version-numbers.md).

**Related topics**  


[Create a knowledge article in Agent Workspace](create-article-workspace.md)

[Edit a knowledge article in Agent Workspace](edit-article-workspace.md)

[Knowledge workflows](../reference/r_KnowledgeWorkflows.md)


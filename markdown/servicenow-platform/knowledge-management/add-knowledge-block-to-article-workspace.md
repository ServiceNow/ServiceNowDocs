---
title: Add a knowledge block to a knowledge article in Agent Workspace
description: Add a knowledge block to a knowledge article in Agent Workspace.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge blocks authoring in Agent Workspace, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a knowledge block to a knowledge article in Agent Workspace

Add a knowledge block to a knowledge article in Agent Workspace.

## Before you begin

-   Both the knowledge article and the knowledge block must be in the same knowledge base.
-   You must have contribute access to the knowledge base.
-   Ensure that the knowledge blocks feature is enabled for the knowledge base that the article is in. For more information, see [Enable knowledge blocks for each knowledge base](enable-knowledge-blocks-for-knowledge-base.md).

Role required: agent\_workspace\_user and knowledge

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge Articles** &gt; **All**.

3.  Click an existing article link.

    For more information, see [Edit a knowledge article in Agent Workspace](edit-article-workspace.md).

    **Note:**

    -   Knowledge blocks are supported only with HTML knowledge articles. Make sure that the **Article type** field is set to **HTML**.
    -   If a knowledge article uses an article template, you can add knowledge blocks to any fields associated with the article template.
4.  In the contextual side panel, click the add blocks icon \(![Add Blocks icon](../image/add-block.png)\).

5.  Search for the article to which you want to add the knowledge block.

    To use condition builder with advanced search, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

6.  Click **Insert** to add the knowledge block to the article.

    If there are no knowledge blocks, click **Create New Block** and follow the procedure to create another block. For more information, see [Create a knowledge block in Agent Workspace](create-knowledge-block-workspace.md).

7.  Click **Update** to save your changes.

    **Note:** You can preview the article with the blocks. For more information, see [Preview a knowledge article with knowledge blocks in Agent Workspace](preview_blocks_agent.md).

8.  Click **Publish** to publish the article.

    The knowledge article is published depending on the workflow setting of its knowledge base. For more information, see [Publish a knowledge article in Agent Workspace](publish-knowledge-article-workspace.md).



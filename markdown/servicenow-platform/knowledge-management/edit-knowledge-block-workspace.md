---
title: Edit a knowledge block in Agent Workspace
description: Edit knowledge blocks within a knowledge base in Agent Workspace to update the reused content across articles within the knowledge base.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Knowledge blocks authoring in Agent Workspace, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a knowledge block in Agent Workspace

Edit knowledge blocks within a knowledge base in Agent Workspace to update the reused content across articles within the knowledge base.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge block you want to edit. By default, the knowledge block doesn't show attached files and it only shows as a link.

Role required: agent\_workspace\_user and knowledge

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to **Lists** &gt; **Knowledge Blocks** &gt; **All**.

3.  Click a knowledge block link.

4.  Modify the fields on the Knowledge Block form.

    -   For an unpublished knowledge block, the Knowledge Block form opens when you select the article.
    -   For a published knowledge block, click **Edit** to access the Knowledge Block form.

        **Note:** If the article versioning feature is enabled, you can edit only the latest version of a knowledge block. Click **Checkout** after you click **Edit**.

5.  Click **Save**.

    The knowledge block is saved and appears in the Unpublished list under Knowledge Blocks. If the article versioning feature is enabled, the version of the knowledge block is incremented by 0.01.

6.  Publish the knowledge block by clicking **Publish**.

    The knowledge block is published depending on the workflow setting of its knowledge base.

    -   **Knowledge - Instant Publish**: The knowledge block is immediately published.
    -   **Knowledge - Approval Publish**: The knowledge block is published on approval completion.
    When published, your knowledge block appears in the Published and All lists under Knowledge Blocks in Agent Workspace. If the article versioning feature is enabled, the version number of the knowledge block is updated to the next whole number \(for example, from 2.02 to 3.0\).



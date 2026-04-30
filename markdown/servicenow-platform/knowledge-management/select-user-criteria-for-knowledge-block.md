---
title: Select user criteria for a knowledge block
description: Control which users can read or not read knowledge block content within an article in a knowledge base by setting user criteria at the knowledge base and knowledge block level. As a knowledge contributor, you can apply user criteria at the knowledge block level.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a knowledge block, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Select user criteria for a knowledge block

Control which users can read or not read knowledge block content within an article in a knowledge base by setting user criteria at the knowledge base and knowledge block level. As a knowledge contributor, you can apply user criteria at the knowledge block level.

## Before you begin

[Activate knowledge blocks](activate-knowledge-blocks.md)

Role required: knowledge\_admin or admin

## Procedure

1.  Navigate to **Knowledge** &gt; **Knowledge Blocks** &gt; **All**.

2.  Open a knowledge block.

3.  Apply the desired user criteria for the **Can Read** and **Cannot Read** fields.

    |Name|Description|
    |----|-----------|
    |Can Read|User criteria to apply for read access at the knowledge block level.|
    |Cannot Read|User criteria to apply for cannot read access at the knowledge block level.|

    **Note:**

    -   You can use existing or create new user criteria records. To create a new record, see [Create a user criteria record in Knowledge Management](create-user-criteria-record-in-knowledge-management.md).
    -   If a user meets any **Can Contribute** criteria at the knowledge base level, they can read all knowledge block content, regardless of the **Can read** and **Cannot read** criteria set at the knowledge block level.
    -   If a user meets any **Cannot read** criteria at the knowledge block level, they cannot read the block content, regardless of the **Can read** criteria set at the knowledge block level.
    -   If a user has access to knowledge article and doesn't have access to one or more blocks within article then user can still read the content but without specify block content.
    ![Who can read or not read knowledge block content based on user criteria set at the knowledge base and knowledge block level.](../image/knowledge-block-user-criteria-flow.png)

4.  Right-click the form header and click **Save**.


## What to do next

-   To finish and publish the block, see [Create a knowledge block](create-modify-knowledge-block.md).
-   To add the block to an article, as well as preview the article by impersonating different users, see [Add knowledge blocks to a knowledge article](add-knowledge-block-to-knowledge-article.md).

**Parent Topic:**[Create a knowledge block](create-modify-knowledge-block.md)


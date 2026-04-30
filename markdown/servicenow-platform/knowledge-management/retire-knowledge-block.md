---
title: Retire a knowledge block
description: You can retire a published knowledge block so that it's no longer available for users to view or search.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a knowledge block, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Retire a knowledge block

You can retire a published knowledge block so that it's no longer available for users to view or search.

## Before you begin

Role required: user must have contributor access to the knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Blocks** &gt; **Published**.

2.  Open the applicable record.

3.  Select **Retire** to retire the knowledge block.

    **Note:**

    -   Starting from the Yokohama release, you can retire the knowledge block attached to an article by setting the \(**glide.knowman.allow\_retire\_block**\) system property to true.
    -   Any additional steps required to retire the knowledge block, such as approvals, depend on the workflow for the knowledge base. See [Knowledge workflows](../reference/r_KnowledgeWorkflows.md) for more information.
    -   A knowledge block can only be deleted if it's not being used in any knowledge article, including any retired article or previous version of an article.

## Result

The retired knowledge block is no longer visible in the article.

**Parent Topic:**[Create a knowledge block](create-modify-knowledge-block.md)


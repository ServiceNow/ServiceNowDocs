---
title: Knowledge blocks in Knowledge Center
description: Knowledge blocks are reusable pieces of content secured by customizable user criteria that you can add to knowledge articles in a knowledge base. The user criteria determine which user roles can or can’t read the block content in an article, enabling only relevant content to be visible to that user.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge blocks in Knowledge Center

Knowledge blocks are reusable pieces of content secured by customizable user criteria that you can add to knowledge articles in a knowledge base. The user criteria determine which user roles can or can’t read the block content in an article, enabling only relevant content to be visible to that user.

## How to use knowledge blocks

To use knowledge blocks, a knowledge administrator or manager must enable the knowledge blocks feature for each knowledge base.

[Enable knowledge blocks in the Knowledge Center](../task/kc-enable-knowledge-blocks.md)

Knowledge contributors can create knowledge blocks and insert them into articles in a knowledge base. Knowledge blocks aren’t supported for wiki formats. By default, the knowledge block doesn't show files attached to it. However, you can see that images and text are visible on knowledge bases created from block files.

-   [Create a knowledge block in the Knowledge Center](../task/kc-create-a-knowledge-block.md)
-   [Add a knowledge block to a knowledge article](../task/kc-add-knowledge-blocks-to-a-knowledge-article.md)
-   [Edit a knowledge block in a knowledge article](../task/kc-edit-knowledge-block-in-a-knowledge-article.md)

Knowledge block content visibility in an article is controlled by criteria set at both the knowledge base and knowledge block levels. See [Select user criteria for a knowledge block](../../knowledge-management/task/select-user-criteria-for-knowledge-block.md) for more information.

Knowledge blocks don't show up in a search until they’re published. Unpublished ones are hidden until they’re ready.

## Holiday calendar with location-specific knowledge block content

Your company has offices in different locations, and each location has different holidays. There are a few ways that you can set up a holiday calendar in your knowledge base so employees can easily find the holidays that apply to them.

One way is that you could create a knowledge article for each location, with an article for Location A, Location B, and so on.

-   Pros: simplified consumption. Employees have a single article to search for and read.
-   Cons: more work for HR. HR has multiple articles to manage and update for each location where the company has employees.

Another way is that you could create a single knowledge article that includes sections for each location.

-   Pros: simplified authoring. HR has a single article to manage and update.
-   Cons: more work for employees. Employee must scroll through and disregard extraneous content to find the section in the article that pertains to them.

With knowledge blocks, you can create a single knowledge article with location-specific block content secured by user criteria. This approach helps to reduce the workload for both HR and employees. As an HR agent, you have a single article to manage and update. Employees have a single article to search for and read, with the user criteria confirming that they only view content that is relevant to them.

## Activation information

To use knowledge blocks in your application, you must [activate knowledge blocks](../../knowledge-management/task/activate-knowledge-blocks.md). For information on what components are installed with the feature, see [Components installed with knowledge blocks](../../knowledge-management/reference/components-installed-with-knowledge-blocks.md).

**Note:** Activating knowledge blocks automatically activates Knowledge Management Advanced, which enables advanced features such as article versioning. Knowledge blocks can be used with or without the article versioning feature. To disable the feature, see [Disable the article versioning feature](../../knowledge-management/task/article-versioning-disable-property.md).


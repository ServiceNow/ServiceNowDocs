---
title: Add knowledge blocks to a knowledge article
description: You can insert one or more knowledge blocks into a knowledge article within a knowledge base. Each knowledge block is secured by user criteria, which controls who can read or not read the content in an article.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add knowledge blocks to a knowledge article

You can insert one or more knowledge blocks into a knowledge article within a knowledge base. Each knowledge block is secured by user criteria, which controls who can read or not read the content in an article.

## Before you begin

[Activate the Knowledge Management Advanced plugin](activate-knowledge-advanced-plugin.md)

Role required: user must have contributor access to the knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Knowledge Articles**.

2.  Click **New** or open a record.

    On clicking **New**, you are provided options to select an article template. The article templates appear when you activate them in the **Knowledge** &gt; **Article templates**.

3.  Select an article template.

    **Note:** You can add or remove knowledge blocks in more than one HTML field of any article template including custom templates.

4.  Fill in the fields on the form, as appropriate.

    For more details on creating a knowledge article, see [Create a knowledge article from an incident in ITSM Agent Workspace](create-knowledge-article.md).

    **Note:** Knowledge blocks are only supported with HTML knowledge articles. Make sure that the **Article type** field is set to **HTML**.

5.  In the article body, click where a block needs to be inserted and then click **Add Blocks**.

    If the **Add Blocks** button is not visible, make sure that the knowledge blocks feature is enabled for the knowledge base that the article is in. See [Enable knowledge blocks for each knowledge base](enable-knowledge-blocks-for-knowledge-base.md) for more information.

    **Note:** Blocks can be added to only the text field.

    In the **Add Blocks** side panel, you can search for, do an advanced search, view, and insert knowledge blocks into the article. To use condition builder with advanced search, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US). You can also create blocks directly from the side panel.

    -   You can configure the number of search results displayed in the **Add Blocks** side panel using the **glide.knowman.add\_blocks.search\_results** property. By default, the minimum number of search results displayed is 6 and the maximum number of search results displayed is 25. See [Knowledge properties](../reference/r_KnowledgeProperties.md#) for more information.
    -   If there are knowledge blocks you cannot find, make sure that the blocks are published, in the same language, and in the same knowledge base as an article.![Insert knowledge blocks into article, as well as search for and create blocks.](../image/knowledge-blocks-insert-blocks-into-article.png)
6.  Rearrange knowledge block in the article body.

<table id="choicetable_fph_h4t_rhb"><thead><tr><th align="left" id="d418230e217">

Option

</th><th align="left" id="d418230e220">

Steps

</th></tr></thead><tbody><tr><td id="d418230e226">

**If you are using a mouse**

</td><td>

1.  Click the block to select it.
2.  Drag and drop the block within the article.


</td></tr><tr><td id="d418230e244">

**If you are using a keyboard**

</td><td>

1.  Place your cursor to the left of the block.
2.  Press the right arrow key to select the block.
3.  Use Ctrl+x and Ctrl+v to cut and paste the block within the article.


</td></tr></tbody>
</table>    The following GIF shows an example of a user moving a knowledge block within an article using a keyboard.

    ![Using the keyboard to rearrange knowledge blocks within an article.](../image/knowledge-blocks-with-keyboard.gif)

7.  Click **Save** or **Update** to create or update the article.

    **Note:** You can preview the article with the blocks by user or, if published, date. See [Preview a knowledge article with knowledge blocks](preview-knowledge-article-with-knowledge-blocks.md) for more information.

8.  Click **Publish** to publish the article.

    **Note:** Any additional steps required to publish the knowledge article, such as approvals, depend on the publishing workflow for the knowledge base. See [Knowledge workflows](../reference/r_KnowledgeWorkflows.md#) for more information.


**Parent Topic:**[Using knowledge blocks](../concept/using-knowlege-blocks.md)


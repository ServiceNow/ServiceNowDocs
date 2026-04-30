---
title: Create a knowledge block in Agent Workspace
description: Create a knowledge block for a knowledge base in Agent Workspace to reuse a piece of content in knowledge articles in that knowledge base.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Knowledge blocks authoring in Agent Workspace, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge block in Agent Workspace

Create a knowledge block for a knowledge base in Agent Workspace to reuse a piece of content in knowledge articles in that knowledge base.

## Before you begin

-   Enable the knowledge blocks feature for the knowledge base where you plan to create blocks. For more information, see [Enable knowledge blocks for each knowledge base](enable-knowledge-blocks-for-knowledge-base.md).
-   You must have contribute access to the knowledge base within which you want to create the knowledge block.

Role required: agent\_workspace\_user and knowledge

## About this task

You can also create blocks when accessing an article panel. For more information, see [Add a knowledge block to a knowledge article in Agent Workspace](add-knowledge-block-to-article-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Check whether a knowledge block on this subject is already available.

    1.  Navigate to **Lists** &gt; **Knowledge Blocks** &gt; **All**.

    2.  Set a filter to search for possible matching knowledge blocks.

        -   Click a column header. Based on the data type included in the column, in the Filter section, select the filter options or enter the filter conditions you want to apply. For example, for the Workflow column, you can select the following states:
            -   Draft
            -   Review
            -   Scheduled for publish
            -   Published
            -   Pending retirement
            -   Retired
            -   Outdated
        -   Click the show filter panel icon \(![Show filter panel icon](../image/show-filter-panel.png)\), and click **Advanced view**. In the Advanced view dialog box, specify conditions in the **All of these conditions must be met** field and click **Update**.
3.  Click **New** in a Knowledge Blocks list.

4.  On the Knowledge Block form, fill in the fields.

<table id="table_s1s_s1y_ykb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for identifying the knowledge block. This field is automatically populated.

</td></tr><tr><td>

Knowledge base

</td><td>

Name of the knowledge base to which you are adding the knowledge block.

</td></tr><tr><td>

Category

</td><td>

Name of the knowledge category or subcategory associated with the knowledge base.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge block. This field appears when the ownership groups feature is enabled \(see [Ownership groups](../concept/enable-ownership-group.md)\).**Note:** Knowledge blocks can be used without the ownership groups feature.

</td></tr><tr><td>

Can Read

</td><td>

User criteria to apply for read access at the knowledge block level.**Note:** User criteria set at the knowledge base and knowledge block level control which users can read block content within an article. \(For more information, see [Select user criteria for a knowledge block](select-user-criteria-for-knowledge-block.md).\)

</td></tr><tr><td>

Cannot Read

</td><td>

User criteria to apply for cannot read access at the knowledge block level.**Note:** User criteria set at the knowledge base and knowledge block level controls which users can read block content within an article. \(For more information, see [Select user criteria for a knowledge block](select-user-criteria-for-knowledge-block.md).\)

</td></tr><tr><td>

Valid to

</td><td>

Date that the knowledge block expires. Once the valid to date has passed:-   The Knowledge article view page no longer displays expired knowledge block content in the associated knowledge article.
-   Knowledge article searches no longer return knowledge articles if the keywords are contained only in the expired blocks.


</td></tr><tr><td>

Short description

</td><td>

Description of the knowledge block.

</td></tr><tr><td>

Article body

</td><td>

Content of the knowledge block.

</td></tr><tr><td>

Version

</td><td>

Version number of the knowledge block. This field is automatically set to a version number when the article versioning feature is enabled.**Note:** Knowledge blocks can be used without the article versioning feature. To learn more about article versioning, including how to disable the feature, see [Article versioning](../concept/article-versioning.md).

</td></tr><tr><td>

Article type

</td><td>

Markup language used for formatting the block. This field is automatically set to HTML because**Note:** knowledge blocks are supported only with HTML knowledge articles.

</td></tr><tr><td>

Workflow

</td><td>

Publication state of the block. This field is automatically set to the publication state of the block, such as Draft, Published, or Retired.

</td></tr></tbody>
</table>    **Note:** You can ignore the **Source Task** field, which is not used.

5.  Click **Save**.

    The knowledge block is saved and appears in the Unpublished list of Knowledge Blocks in Agent Workspace and additional functionality becomes available on the form.

6.  Publish the block by clicking **Publish**.

    A knowledge block is published depending on the workflow setting of its knowledge base.

    -   **Knowledge - Instant Publish**: The knowledge block is immediately published.
    -   **Knowledge - Approval Publish**: The knowledge block is published on approval completion.
    When published, your knowledge block appears in the Published and All lists under Knowledge Blocks in Agent Workspace. If the article versioning feature is enabled, the version number of the knowledge block is incremented.


**Related topics**  


[Edit a knowledge block in Agent Workspace](edit-knowledge-block-workspace.md)


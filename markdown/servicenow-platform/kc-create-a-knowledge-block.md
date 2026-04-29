---
title: Create a knowledge block in the Knowledge Center
description: Create a knowledge block to define a reusable piece of content that can be inserted into knowledge articles in a knowledge base. The knowledge block is secured by user criteria, which controls what users, groups, and roles, can read the content in an article, allowing display of content that is relevant only to them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using knowledge blocks in the Knowledge Center, Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge block in the Knowledge Center

Create a knowledge block to define a reusable piece of content that can be inserted into knowledge articles in a knowledge base. The knowledge block is secured by user criteria, which controls what users, groups, and roles, can read the content in an article, allowing display of content that is relevant only to them.

## Before you begin

-   -   You must have 'contribute' access to the knowledge base.
-   Confirm that the knowledge blocks feature is enabled for the knowledge base that the article is in. For more information, see [Enable knowledge blocks in the Knowledge Center](kc-enable-knowledge-blocks.md)

Role required: knowledge

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Center**

2.  Check whether a knowledge block on this subject is already available.

    1.  Navigate to **Lists** &gt; **Knowledge Blocks** &gt; **All**.

    2.  Set a filter to search for possible matching knowledge blocks.

        -   Select a column header. Based on the data type included in the column, in the Filter section, select the filter options or enter the filter conditions you want to apply. For example, for the workflow column, you can select the following states:
            -   Draft
            -   Review
            -   Scheduled for publish
            -   Published
            -   Pending retirement
            -   Retired
            -   Outdated
        -   Select the show filter panel icon, and select **Advanced view**. In the Advanced view dialog box, specify conditions in the **All of these conditions must be met** field and select **Update**.
3.  Select **New** to create a knowledge block.

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

Name of the knowledge base to which you’re adding the knowledge block.

</td></tr><tr><td>

Category

</td><td>

Name of the knowledge category or subcategory associated with the knowledge base.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge block. This field appears when the ownership groups feature is enabled \(see [Ownership groups](../../knowledge-management/concept/enable-ownership-group.md)\).**Note:** Knowledge blocks can be used without the ownership groups feature.

</td></tr><tr><td>

Can Read

</td><td>

User criteria to apply for read access at the knowledge block level.**Note:** User criteria set at the knowledge base and knowledge block level control which users can read block content within an article. \(For more information, see [Select user criteria for a knowledge block](../../knowledge-management/task/select-user-criteria-for-knowledge-block.md).\)

</td></tr><tr><td>

Can’t Read

</td><td>

User criteria to apply for can’t read access at the knowledge block level.**Note:** User criteria set at the knowledge base and knowledge block level control which you can read block content within an article. \(For more information, see [Select user criteria for a knowledge block](../../knowledge-management/task/select-user-criteria-for-knowledge-block.md).\)

</td></tr><tr><td>

Valid to

</td><td>

Date that the knowledge block expires. Once the valid to date has passed:-   The Knowledge article view page no longer displays expired knowledge block content in the associated knowledge article.
-   If the keywords are contained only in the expired blocks, Knowledge article searches no longer return knowledge articles


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

Version number of the knowledge block. This field is automatically set to a version number when the article versioning feature is enabled.**Note:** Knowledge blocks can be used without the article versioning feature. To learn more about article versioning, including how to disable the feature, see [Article versioning](../../knowledge-management/concept/article-versioning.md).

</td></tr><tr><td>

Article type

</td><td>

Markup language used for formatting the block. This field is automatically set to HTML because**Note:** knowledge blocks are supported only with HTML knowledge articles.

</td></tr><tr><td>

Workflow

</td><td>

Publication state of the block. This field is automatically set to the publication state of the block, such as Draft, Published, or Retired.

</td></tr></tbody>
</table>    **Note:** You can ignore the **Source Task** field, which isn’t used.

5.  Select **Save**.

    The knowledge block is saved and appears in the Unpublished list of Knowledge Blocks.

6.  Publish the block by selecting **Publish**.

    A knowledge block is published depending on the workflow setting of its knowledge base.

    -   **Knowledge - Instant Publish**: The knowledge block is immediately published.
    -   **Knowledge - Approval Publish**: The knowledge block is published on approval completion.
    When published, your knowledge block appears in the **Published** and **All** lists under **Knowledge Blocks**. If the article versioning feature is enabled, the version number of the knowledge block is incremented.



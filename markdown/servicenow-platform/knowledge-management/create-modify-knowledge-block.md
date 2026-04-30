---
title: Create a knowledge block
description: Create or modify a knowledge block to define a reusable piece of content that can be inserted into knowledge articles in a knowledge base. The knowledge block is secured by user criteria, which controls what users, groups, roles, companies, locations, or departments can read or not read the content in an article or search, enabling users to more easily view content that is relevant to them.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge block

Create or modify a knowledge block to define a reusable piece of content that can be inserted into knowledge articles in a knowledge base. The knowledge block is secured by user criteria, which controls what users, groups, roles, companies, locations, or departments can read or not read the content in an article or search, enabling users to more easily view content that is relevant to them.

## Before you begin

[Activate knowledge blocks](activate-knowledge-blocks.md)

Role required: user must have contributor access to the knowledge base.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Knowledge Blocks** &gt; **Create New**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_njc_xd3_scb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

This field is automatically set to a knowledge block number.

</td></tr><tr><td>

Knowledge base

</td><td>

Name of the knowledge base.The knowledge blocks feature must be enabled for each knowledge base that you plan to create blocks. See [Enable knowledge blocks for each knowledge base](enable-knowledge-blocks-for-knowledge-base.md).

</td></tr><tr><td>

Category

</td><td>

Name of the knowledge category or subcategory.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge block. This field appears when the ownership groups feature is enabled.Knowledge blocks can be used with or without the ownership groups feature. To learn more about ownership groups, including how to enable the feature, see [Ownership groups](../concept/enable-ownership-group.md).

</td></tr><tr><td>

Can read

</td><td>

User criteria to apply for read access at the knowledge block level.User criteria set at the knowledge base and knowledge block level controls which users can read or not read block content within an article. To learn more about selecting user criteria for a knowledge block, see [Select user criteria for a knowledge block](select-user-criteria-for-knowledge-block.md).

</td></tr><tr><td>

Cannot read

</td><td>

User criteria to apply for cannot read access at the knowledge block level.User criteria set at the knowledge base and knowledge block level controls which users can read or not read block content within an article. To learn more about selecting user criteria for a knowledge block, see [Select user criteria for a knowledge block](select-user-criteria-for-knowledge-block.md).

</td></tr><tr><td>

Valid to

</td><td>

Date that the knowledge block expires. After the valid to date:-   Knowledge article viewer will no longer display expired knowledge block content in the associated knowledge article.
-   Search will no longer return knowledge articles if the keywords are contained in the expired blocks.


</td></tr><tr><td>

Short Description

</td><td>

Description of the knowledge block.

</td></tr><tr><td>

Text

</td><td>

Text of the knowledge block.

</td></tr><tr><td>

Version

</td><td>

This field is automatically set to a version number when the article versioning feature is enabled.Knowledge blocks can be used with or without the article versioning feature. To learn more about article versioning, including how to disable the feature, see [Article versioning](../concept/article-versioning.md).

</td></tr><tr><td>

Article type

</td><td>

This field is automatically set to HTML.**Note:** Knowledge blocks are only supported with HTML knowledge articles.

</td></tr><tr><td>

Workflow

</td><td>

This field is automatically set to the publication state of the block, such as Draft, Published, or Retired.

</td></tr><tr><td>

Source task

</td><td>

Not applicable.

</td></tr></tbody>
</table>4.  Click **Save** or **Update** to create or update the block.

5.  Click **Publish** to publish the block.

    **Note:** Any additional steps required to publish the knowledge block, such as approvals, depend on the publishing workflow for the knowledge base. See [Knowledge workflows](../reference/r_KnowledgeWorkflows.md) for more information.


## What to do next

After the knowledge block is published, you can add the block to an article within the knowledge base.

-   **[Select user criteria for a knowledge block](select-user-criteria-for-knowledge-block.md)**  
Control which users can read or not read knowledge block content within an article in a knowledge base by setting user criteria at the knowledge base and knowledge block level. As a knowledge contributor, you can apply user criteria at the knowledge block level.
-   **[Retire a knowledge block](retire-knowledge-block.md)**  
You can retire a published knowledge block so that it's no longer available for users to view or search.

**Parent Topic:**[Using knowledge blocks](../concept/using-knowlege-blocks.md)


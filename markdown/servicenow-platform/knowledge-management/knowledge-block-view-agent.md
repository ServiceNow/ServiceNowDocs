---
title: Knowledge block details displayed in Agent Workspace
description: View the details of a knowledge block in Agent Workspace.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Knowledge blocks authoring in Agent Workspace, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge block details displayed in Agent Workspace

View the details of a knowledge block in Agent Workspace.

The knowledge block view page in Agent Workspace provides several details about a displayed block.

![Knowledge block view page in Agent Workspace](../image/block-view-page-workspace.png "Sample knowledge block view page in Agent Workspace")

<table id="table_tjh_2r4_jjb"><thead><tr><th>

Details

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge base

</td><td>

Knowledge base that stores the knowledge article and the article category. In the figure, Knowledge is the knowledge base and Policies is the knowledge block category.

</td></tr><tr><td>

Read time

</td><td>

Average time to read the knowledge block, which can help you decide whether you have time to read the block. The read time is calculated based on an average reading speed of 200 words per minute. For blocks in languages such as Chinese, Japanese, and Korean, the read time is calculated based on an average speed of 500 characters per minute.

 If images are present in an article, the read time is calculated using the following rules:

 -   For the first image add 12 seconds, for the second image add 11 seconds, and so on.
-   If there are more than 10 images, after the tenth image add 3 seconds for each image.

</td></tr><tr><td>

Last updated time

</td><td>

Last time the knowledge block was updated in number of days for the current week, number of weeks, or number of years.

</td></tr><tr><td>

Knowledge block content

</td><td>

Text and images in the knowledge block.

</td></tr><tr><td>

Authored by

</td><td>

Author of the knowledge block. This field appears only in the first version of a knowledge block.

</td></tr><tr><td>

Revised by

</td><td>

User who revised the knowledge block. This field appears if a knowledge block was later edited.

</td></tr><tr><td>

Knowledge block number

</td><td>

Unique number automatically assigned to the knowledge block. In the figure, KBB0000101 is the block number.

</td></tr><tr><td>

Version

</td><td>

Selected version of the knowledge block. This field appears when the article versioning feature is enabled. In the figure, 2.0 is the selected version of the knowledge block.

</td></tr></tbody>
</table>**Related topics**  


[View a knowledge block in Agent Workspace](../task/view-block-agent.md)

[Create a knowledge block in Agent Workspace](../task/create-knowledge-block-workspace.md)

[Edit a knowledge block in Agent Workspace](../task/edit-knowledge-block-workspace.md)

[Publish a knowledge block in Agent Workspace](../task/publish-block-agent.md)


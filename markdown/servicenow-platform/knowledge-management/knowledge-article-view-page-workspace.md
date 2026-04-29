---
title: Viewing knowledge article details in Agent Workspace
description: View the details of a knowledge article in Agent Workspace.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Viewing knowledge article details in Agent Workspace

View the details of a knowledge article in Agent Workspace.

The knowledge article view page in Agent Workspace provides several details about a displayed article.

![Knowledge article view page in Agent Workspace](../image/article-view-page-workspace.png "Sample knowledge article view page in Agent Workspace")

<table id="table_tjh_2r4_jjb"><thead><tr><th>

Details

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge base

</td><td>

Knowledge base that stores the knowledge article and the article category. In the figure, IT is the knowledge base and Announcements is the knowledge article category.

</td></tr><tr><td>

Read time

</td><td>

Average time to read the knowledge article, which can help you can decide whether you have time to read the article. The read time is calculated based on an average reading speed of 200 words per minute. For articles in languages such as Chinese, Japanese, and Korean, the read time is calculated based on an average speed of 500 characters per minute. If images are present in an article, the read time is calculated using the following rules:

 -   For the first image add 12 seconds, for the second image add 11 seconds, and so on.
-   If there are more than 10 images, after the tenth image add 3 seconds for each image.

</td></tr><tr><td>

Last updated time

</td><td>

Last time the knowledge article was updated in number of days for the current week, number of weeks, or number of years.

</td></tr><tr><td>

Number of views

</td><td>

Number of times the knowledge article was viewed in the past number of days set by your system administrator in the **glide.knowman.view\_age.days** property. For more information on this property, see [Knowledge portal properties](../reference/r_KnowledgeProperties.md#).

</td></tr><tr><td>

Average rating

</td><td>

Result of the weighted average rating of the knowledge article based on numeric 1 through 5 ratings. The average rating is carried on the next version of the article.

</td></tr><tr><td>

Knowledge article content

</td><td>

Text and images of the knowledge article.

</td></tr><tr><td>

Authored by

</td><td>

Author of the knowledge article. This field appears only in the first version of a knowledge article.

</td></tr><tr><td>

Revised by

</td><td>

User who revised the article. This field appears if a knowledge article was later edited.

</td></tr><tr><td>

Article number

</td><td>

Unique number automatically assigned to the knowledge article. In the figure, KB0010090 is the article number.

</td></tr><tr><td>

Version

</td><td>

Selected version of the knowledge article. This field appears when the article versioning feature is enabled. In the figure, 1.01 is the selected version of the article.

</td></tr><tr><td>

Language

</td><td>

Language of the selected article. This field appears if the translations of the knowledge article in other languages are available.

</td></tr><tr><td>

Attachments

</td><td>

List of article attachments. This field appears if the knowledge administrator has enabled it to be displayed on the knowledge article view page.

</td></tr></tbody>
</table>**Related topics**  


[View a knowledge article in Agent Workspace](../task/view-article-agent.md)

[Create a knowledge article in Agent Workspace](../task/create-article-workspace.md)

[Edit a knowledge article in Agent Workspace](../task/edit-article-workspace.md)

[Publish a knowledge article in Agent Workspace](../task/publish-knowledge-article-workspace.md)


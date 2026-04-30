---
title: Edit a knowledge article from a feedback task in Agent Workspace
description: When working on a knowledge article task, you can edit the knowledge article from within the task. A feedback task is created for a knowledge article when the article is flagged, marked as not helpful, or rated low, or a knowledge gap feedback task is created on a topic.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a knowledge article from a feedback task in Agent Workspace

When working on a knowledge article task, you can edit the knowledge article from within the task. A feedback task is created for a knowledge article when the article is flagged, marked as not helpful, or rated low, or a knowledge gap feedback task is created on a topic.

## Before you begin

Role required: You must have contribute access to the knowledge base that stores the knowledge article.

**Note:** If the article versioning feature is enabled, only the knowledge administrator, knowledge managers, and author can edit the checked-out version of an article. If the feature is disabled, any users with contribute access to an article can edit the draft version of the article. An administrator can disable the article versioning feature by setting the **glide.knowman.versioning.enabled** property \(from the **System Property** \[sys\_properties\] table\) to **false**.

Role required: agent\_workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Go to your tasks list.

    -   For feedback tasks created through knowledge gaps or if a knowledge article was marked as not helpful or rated low, go to **Knowledge** &gt; **My Tasks - Feedback**.
    -   For tasks created when an article was flagged, go to **Knowledge** &gt; **My Tasks - Flagged**.
3.  In the **Number** column, click the link to a feedback task assigned to you or your ownership group.

4.  Click **Edit Article**.

5.  If the article versioning feature is enabled, click **Checkout** for a published knowledge article.

    You can only edit the latest version of a knowledge article.

6.  Access the relevant related lists to modify the information.

<table id="table_gtg_45m_jjb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Knowledge article content and its metadata.**Note:** If the article versioning feature is enabled, the default value of the **Valid to** date in the updated article version is automatically set based on the following criteria:

-   If the **Article Validity** field in the knowledge base associated with the article is empty, the **Valid to** date value from the earlier version of the article is retained.
-   If the **Article Validity** field in the knowledge base associated with the article isn’t empty, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field \(Article updated date + article validity\).
If you move a knowledge article to another knowledge base, the default value of the **Valid to** date in the updated article is automatically set based on the following criteria:

-   If the **Article Validity** field in the selected knowledge base is empty, the earlier **Valid to** date value is retained for the knowledge article.
-   If the **Article Validity** field in the selected knowledge base isn't empty, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field \(Article updated date + article validity\).
If the dictionary value of the **Valid to** field is modified, this dictionary value overrides the default value of the **Valid to** field calculated according to the **Article Validity** field. For more information, see [Validity of a knowledge article](../concept/article-validity.md).

</td></tr><tr><td>

Feedback

</td><td>

Feedback received on the published versions of the article. To view more details about the feedback, in the **Comments** column, select a link for the desired version of an article.

</td></tr><tr><td>

Feedback Tasks

</td><td>

Details about the feedback task created for a knowledge article version.

</td></tr><tr><td>

Approvals

</td><td>

Approval history of the knowledge article.

</td></tr><tr><td>

Article Versions

</td><td>

Version history of the knowledge article.

</td></tr><tr><td>

Translated Versions

</td><td>

Translated versions of the knowledge article. This related list appears only when the translation management feature is enabled. To translate a knowledge article, select **New**. The **New** button on this related list appears when the **glide.knowman.translation.enable\_translation\_task** property is inactive.

</td></tr><tr><td>

Translation Tasks

</td><td>

Tasks submitted for translating the article. This related list appears when the Translation Management feature and the **glide.knowman.translation.enable\_translation\_task** property to enable creation of translation tasks are enabled. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

</td></tr><tr><td>

Related Articles

</td><td>

Related articles mapped to the knowledge article. For more information, see [Map a related article in Agent Workspace](map-related-articles-agent.md).

</td></tr><tr><td>

Related Catalog Items

</td><td>

Related catalog items mapped to the knowledge article. For more information, see [Map a related item in Agent Workspace](map-related-items-agent.md).

</td></tr><tr><td>

Affected Products

</td><td>

Products mapped to the knowledge article. For more information, see [Add an affected product to a knowledge article in Agent Workspace](add-affected-products-agent.md).

</td></tr></tbody>
</table>7.  Research for content related to knowledge article you're authoring using Agent assist.

    1.  In the contextual side panel, select the agent assist icon \(![Agent Assist icon.](../image/agent-assist.png)\).

        The search results in Agent assist display default content based on the text-based search.

    2.  Click the select a search resource icon \(![Select a search resource icon](../image/filter-settings.png)\), and then select a search resource.

        For example, to view knowledge articles, select **Knowledge Articles**.

    3.  In the search results, you can click a resource item, such as a knowledge article, to view its content in Agent assist.

        **Tip:** For better readability, you can resize the contextual side panel for Agent assist. For a full view of the selected resource item content, select **Full View**. The resource item content opens in another tab within the Agent Workspace.

8.  Check whether your content matches the content in an existing article.

    1.  Enter your search text in the text box available in Agent assist or retain the default text, which is the short description of the knowledge article.

    2.  Select the lookup icon \(![Lookup icon.](../image/lookup-icon.png)\).

    3.  Select a search resource by clicking the Select a search resource icon \(![Select a search resource icon.](../image/filter-settings.png)\).

        -   To find knowledge articles that have high text similarity with the entered search text, choose **Similar Articles \(ML\)**.

            **Note:** This option is available only when the Predictive Intelligence feature is enabled and your administrator has trained the similarity solution for Knowledge Management. For more information, see [Train the similarity solution for Knowledge Management to find related articles](train-similarity-solution-km.md).

        -   To find knowledge articles that match the entered search text, choose **Knowledge Articles**.
9.  Click **Save**.

    The article is saved and appears in the My Articles - Unpublished list. If the article versioning feature is enabled, the version of the knowledge article is incremented by 0.01. For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).

10. Publish the article by clicking **Publish**.

    The knowledge article is published depending on the workflow setting of its knowledge base:

    -   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
    -   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.

        **Note:** With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. An administrator can override this behavior by disabling the **glide.knowman.ownership\_group.enable\_self\_approval** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md).

    For more information, see [Schedule a knowledge article for publishing in Agent Workspace](schedule-article-publishing-agent.md).

    When published, the knowledge article appears in the My Articles - Published and All Articles lists. If the article versioning feature is enabled, the version number of the knowledge article increments to the next whole number \(for example, from 2.02 to 3.0\). For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).


**Related topics**  


[Work on a feedback task in Agent Workspace](respond-feedback-workspace.md)

[Create a knowledge article from a feedback task in Agent Workspace](create-article-feedback-agent.md)

[View a knowledge article in Agent Workspace](view-article-agent.md)

[Provide feedback for a knowledge article in Agent Workspace](respond-evaluate-articles-agent.md)

[Using Agent Assist in Agent Workspace](https://www.servicenow.com/docs/access?context=agent-assist&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)


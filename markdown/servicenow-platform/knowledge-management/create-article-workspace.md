---
title: Create a knowledge article in Agent Workspace
description: Create a knowledge article in Agent Workspace to share information across your organization.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge article in Agent Workspace

Create a knowledge article in Agent Workspace to share information across your organization.

## Before you begin

You must have contribute access to the knowledge base within which you want to create the knowledge article.

Role required: agent\_workspace\_user

## About this task

You can also create a knowledge article when adding a knowledge block. For more information, see [Add a knowledge block to a knowledge article in Agent Workspace](add-knowledge-block-to-article-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Check whether a knowledge article on this subject is already available by going to **Lists** &gt; **Knowledge** &gt; **All Articles** and setting a filter to search for possible matching articles.

3.  Click **New**.

4.  Create the knowledge article by either selecting an article template or using the default template.

<table id="choicetable_ajx_szw_hkb"><tbody><tr><td id="d529118e117">

**Selected article template**

</td><td>

Select an article template to create a knowledge article using defined fields and values.In the Create Article dialog box:

1.  From the Knowledge Base list, select a knowledge base.
2.  From the Article Template list, select the desired article template.

**Note:** The Article Template list is populated based on the article templates configured for the selected knowledge base.

3.  Select **Create Article**.
 The Create Article dialog box is available if the article versioning and the Knowledge Article Templates features are enabled. For more information, see [Article versioning](../concept/article-versioning.md) and [Knowledge article templates](../concept/knowledge-article-templates.md).

</td></tr><tr><td id="d529118e162">

**Default Standard template**

</td><td>

Create a knowledge article using the default Standard template.

</td></tr></tbody>
</table>5.  On the form, fill in the fields.

    **Note:** If you’re using an article template, the available fields will vary.

<table id="table_fdt_qgf_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge base

</td><td>

Knowledge base in which the knowledge article is stored. You can associate a knowledge article with one knowledge base only. If you’re using an article template, you can modify this value only if the template is available in the other knowledge base.

</td></tr><tr><td>

Category

</td><td>

Category for the knowledge article. This value helps users find the article within a selected category. You can select only categories available within the selected knowledge base. Articles without a category appear in the \(empty\) category.

</td></tr><tr><td>

Ownership Group

</td><td>

Ownership group for the knowledge article. An ownership group consists of a group of members and a manager who are responsible for approvals and feedback tasks. Ownership groups can publish, edit, and retire knowledge articles that they’re associated with.**Note:** This field is available only if the **glide.knowman.ownership\_group.enabled** property is enabled. If no ownership group is assigned and approvals are required to publish a knowledge article, it’s automatically submitted for approval to the knowledge administrator and knowledge manager. For more information, see [Ownership groups](../concept/enable-ownership-group.md).

</td></tr><tr><td>

Version

</td><td>

Automatically generated article version number. This number is incremented when changes are made to a published article. **Note:** This field is available if the article versioning feature has been enabled.

</td></tr><tr><td>

Workflow

</td><td>

Publishing workflow state of the knowledge article, such as **Draft**, **In Review**, or **Published**. For a new article, the workflow state is set to **Draft**.

</td></tr><tr><td>

Language

</td><td>

The language in which you’re creating the knowledge article. The list is populated based on the languages enabled for the selected knowledge base. This field appears only when the I18N:Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) is activated. For more information, see [I18N - Knowledge internationalization](../concept/c_I18NKMInternational.md).

</td></tr><tr><td>

Short description

</td><td>

Title of the knowledge article. This title appears when browsing and searching for knowledge article, and at the top of the article.You can enter up to 100 characters in this field.

 **Note:** Knowledge articles similar to the short description text will appear in Agent assist.

</td></tr><tr><td>

Article body

</td><td>

Content for the knowledge article. Use the editing functions in the HTML editor to create content. For more information, see [Editing functions for knowledge articles in the HTML editor](../concept/knowledge-html-editor.md).

</td></tr><tr><td>

Source Task

</td><td>

Task this knowledge article was created from. This field is set automatically when you create the knowledge article from a task, such as an incident or a customer service case, or from a submission record.

</td></tr><tr><td>

Scheduled publish date

</td><td>

Future date when the knowledge article will be published automatically. For more information, see [Schedule a knowledge article for publishing in Agent Workspace](schedule-article-publishing-agent-1.md).

</td></tr><tr id="valid-to-desc"><td>

Valid to

</td><td>

The date this knowledge article expires. Articles don’t appear in search results after the **Valid to** date or if the **Valid to** date is empty. The default value of the **Valid to** field is derived from the **Article Validity** field configured for the knowledge base \(see [Create a knowledge base](create-a-knowledgebase.md)\). The **Valid to** date starts from the date that the article was created until the number of days specified in the **Article Validity** field. If the **Article Validity** field is empty, the default date in the **Valid to** field for the knowledge article is set to January 1, 2100.

 An article author or editor can select whether to keep or change the default **Valid to** date. For more information, see [Validity of a knowledge article](../concept/article-validity.md).

 On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are expire in the next month. The recipient can then extend the **Valid to** date to continue using the article. For more information, see [Managing email notifications in Knowledge Management](../concept/email-notifications-km.md).

 **Note:** If the system date format or user preferences is set to use `yy` year format, you might face issues when the **Valid to** date is set to the default date. Contact your administrator or modify the user preferences to use a date format with the `yyyy` year format. For more information, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Personalize the system date format](https://www.servicenow.com/docs/access?context=t_PersonalizeTheSystemDateFormat&version=australia&pubname=australia-platform-administration&ft:locale=en-US) topics.

</td></tr><tr id="confidence-desc"><td>

Confidence

</td><td>

Maturity of an article based on its completeness and reusability.

</td></tr><tr><td>

Article type

</td><td>

Type of the article, which is automatically set to HTML. This field is available in the Standard template only.**Note:** The Wiki article type isn't supported in Agent Workspace.

</td></tr><tr><td>

Display attachments

</td><td>

Option to display attachments in the knowledge article. If the article has attachments, they’re listed below the text of a knowledge article on the knowledge article view page.

</td></tr><tr><td>

Attachment link

</td><td>

Option to automatically download an attached article when a user accesses it instead of opening the article. The Attachment link option applies to articles accessed from search links only.**Note:** Although you may attach multiple files, most web browsers permit users to download only the first attachment. To ensure download of all the files, bundle them into an archive and attach the archive. Articles accessed as links within other knowledge articles will not replicate this behavior.

</td></tr><tr id="governance-desc"><td>

Governance

</td><td>

An attribute of an article that enables you to control sensitive, critical, or regulated information. Not all articles have the same requirement for compliance reviews. Some articles are based on the collective experience of the people who use the articles \(experience-based\). Other articles have policy or legal information that require tight control \(compliance-based\).

</td></tr><tr><td>

Issue

</td><td>

Brief description about an issue.**Note:** This field is available in the KCS Article template only.

</td></tr><tr><td>

Environment

</td><td>

Details of the environment in place when the issue occurred.**Note:** This field is available in the KCS Article template only.

</td></tr><tr><td>

Cause

</td><td>

The cause of the issue.**Note:** This field is available in the KCS Article template only.

</td></tr><tr><td>

Resolution

</td><td>

Method used to resolve the issue.**Note:** This field is available in the KCS Article template only.

</td></tr><tr><td>

Question

</td><td>

Text to display as a question. **Note:** This field is available in the FAQ template only.

</td></tr><tr><td>

Answer

</td><td>

Text to display as an answer to an included question. **Note:** This field is available in the FAQ template only.

</td></tr><tr><td>

Introduction

</td><td>

Introduction to the topic. **Note:** This field is available in the How To and What Is templates only.

</td></tr><tr><td>

Instructions

</td><td>

Instructions for a how-to topic. **Note:** This field is available in the How To template only.

</td></tr><tr><td>

Explanation

</td><td>

Explanation of a what-is topic. **Note:** This field is available in the What Is template only.

</td></tr></tbody>
</table>    **Note:** The **Confidence** and **Governance** fields appear when the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) is activated. For more information, see [Managing the KCS article state](../concept/managing-kcs-article-states.md).

6.  Research for content related to knowledge article you're authoring using Agent assist.

    1.  In the contextual side panel, select the agent assist icon \(![Agent Assist icon.](../image/agent-assist.png)\).

        The search results in Agent assist display default content based on the text-based search.

    2.  Click the select a search resource icon \(![Select a search resource icon](../image/filter-settings.png)\), and then select a search resource.

        For example, to view knowledge articles, select **Knowledge Articles**.

    3.  In the search results, you can click a resource item, such as a knowledge article, to view its content in Agent assist.

        **Tip:** For better readability, you can resize the contextual side panel for Agent assist. For a full view of the selected resource item content, select **Full View**. The resource item content opens in another tab within the Agent Workspace.

7.  Check whether your content matches the content in an existing article.

    1.  Enter your search text in the text box available in Agent assist or retain the default text, which is the short description of the knowledge article.

    2.  Select the lookup icon \(![Lookup icon.](../image/lookup-icon.png)\).

    3.  Select a search resource by clicking the Select a search resource icon \(![Select a search resource icon.](../image/filter-settings.png)\).

        -   To find knowledge articles that have high text similarity with the entered search text, choose **Similar Articles \(ML\)**.

            **Note:** This option is available only when the Predictive Intelligence feature is enabled and your administrator has trained the similarity solution for Knowledge Management. For more information, see [Train the similarity solution for Knowledge Management to find related articles](train-similarity-solution-km.md).

        -   To find knowledge articles that match the entered search text, choose **Knowledge Articles**.
8.  Attach a file with supporting information by clicking the attachments icon \(![Attachments icon.](../image/attachments.png)\) in the contextual side panel and selecting the file.

9.  Add a knowledge block.

    For more information, see [Add a knowledge block to a knowledge article in Agent Workspace](add-knowledge-block-to-article-workspace.md).

10. Click **Save**.

    The article is saved and appears in the My Articles - Unpublished list and additional functionality becomes available on the form.

11. Either add to or modify the article details or publish the article.

    -   Add to or modify the article details.

        For more information, see [Edit a knowledge article in Agent Workspace](edit-article-workspace.md).

    -   Publish the article by clicking **Publish**.

        A knowledge article is published depending on the workflow setting of its knowledge base:

        -   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
        -   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.

            **Note:** With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. An administrator can override this behavior by disabling the **glide.knowman.ownership\_group.enable\_self\_approval** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md).

        For more information, see [Schedule a knowledge article for publishing in Agent Workspace](schedule-article-publishing-agent.md).

        When published, your knowledge article appears in the My Articles - Published and All Articles lists. If the article versioning feature is enabled, the version number of the knowledge article is updated. For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).


## What to do next

After you create and publish a knowledge article, you can perform the following actions related to the article:

-   Request translations for the knowledge article. For more information, see [Request translations for missing languages in Agent Workspace](request-translations-agent.md).
-   Retire the knowledge article. Click **Retire** to enable the retirement workflow. For more information, see [Retire a knowledge article](../concept/c_RetiredKnowledgeArticles.md).
-   Translate the knowledge article directly from the knowledge article. For more information, see [Translate a knowledge article in Agent Workspace](translate-directly-workspace.md).
-   Delete the published knowledge article. Click **Delete**. If the **Delete** button isn't displayed, click the more actions icon \(![More actions icon.](../image/more.png)\), and then click **Delete**.

    **Note:** Only users with the admin role can delete a published knowledge article.


**Related topics**  


[View a knowledge article in Agent Workspace](view-article-agent.md)

[Edit a knowledge article in Agent Workspace](edit-article-workspace.md)

[Work on a feedback task in Agent Workspace](respond-feedback-workspace.md)

[Provide feedback for a knowledge article in Agent Workspace](respond-evaluate-articles-agent.md)

[Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md)

[Knowledge workflows](../reference/r_KnowledgeWorkflows.md#)

[Knowledge article templates](../concept/knowledge-article-templates.md)

[bundle-platux.agent-assist]

[Create knowledge from incident or problem](t_ApproveKnowledgeSubmission.md)


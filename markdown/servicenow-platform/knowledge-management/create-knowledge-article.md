---
title: Create a knowledge article
description: Knowledge contributors can create and edit knowledge articles within a knowledge base to share information across your organization.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge article

Knowledge contributors can create and edit knowledge articles within a knowledge base to share information across your organization.

## Before you begin

To view an article template, you must activate the article templates feature and enable the desired templates.

Role required: knowledge, knowledge\_manager, knowledge\_admin, knowledge\_coach, knowledge\_domain\_expert, knowledge\_group\_member, admin. You must have contribute access to at least one active knowledge base.

## About this task

Users with at least one role can create and edit knowledge articles. These users are known as knowledge contributors. Users without any role can read articles and submit feedback, but can’t create or edit articles.

Some knowledge bases may allow only certain users to contribute. For example, a member of the IT department can create knowledge articles in the IT knowledge base, such as desktop support information or articles describing company IT processes.

## Procedure

1.  There are three ways of creating knowledge articles.

    -   Navigate to **Self-Service** &gt; **Knowledge** and select the Create an Article icon.
    -   Navigate to **Knowledge** &gt; **Articles** &gt; **Create New**.
    -   From the Knowledge Management homepage, select the more icon \(![More icon](../image/KnowledgeServicePortalOverflowIcon.png)\) and then select **Create Article**.
2.  On the Create new article page, select a knowledge base.

    The list of article templates to select in the next step is filtered according to the article templates available for the selected knowledge base.

    **Note:**

    On the Create new article page, you can select to **Switch to older version of this page** or **Switch to updated version of this page \(recommended\)**.

3.  Select an article template.

4.  Select **Next**.

    The Knowledge form is displayed based on the article template selected.

5.  On the Knowledge form, fill in the fields.

<table id="table_fdt_qgf_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the article. This field is automatically set to a number. For more information, see [Duplicate knowledge article numbers](../reference/knowledge-article-duplicate-numbers.md).

</td></tr><tr><td>

Knowledge Base

</td><td>

The knowledge base selected for this article.**Note:** An article can only be associated with one knowledge base.

You can change the knowledge base, but only if the selected article template is available in the knowledge base.

</td></tr><tr><td>

Category

</td><td>

The category for this article. Select a **Knowledge Base** before you can select a category. Articles without a category appear on the knowledge homepage in the \(empty\) category.

</td></tr><tr><td>

Ownership Group

</td><td>

The ownership group for this knowledge article. An ownership group is a group of members and a manager who are responsible for approvals, ensuring article quality, and feedback tasks. Ownership groups can publish, edit, and retire knowledge articles that they’re associated with.**Note:** If no ownership group is assigned, the article automatically goes to the knowledge administrator and knowledge manager for approval.

</td></tr><tr><td>

Language

</td><td>

Language in which you’re creating the article. The list is populated based on the languages enabled for the selected knowledge base.

</td></tr><tr><td>

Schedule publish date

</td><td>

Date in future when the article is published automatically. If approvals are enabled, the approval process must be completed before this date.

</td></tr><tr><td>

Valid to

</td><td>

The date this knowledge article expires. Articles don’t appear in search results after the **Valid to** date or if the **Valid to** date is empty. The default value of the **Valid to** field is derived from the **Article Validity** field configured for the knowledge base \(see [Create a knowledge base](create-a-knowledgebase.md)\). The **Valid to** date starts from the date that the article was created until the number of days specified in the **Article Validity** field. If the **Article Validity** field is empty, the default date in the **Valid to** field for the knowledge article is set to January 1, 2100.

 An article author or editor can select whether to keep or change the default **Valid to** date. For more information, see [Validity of a knowledge article](../concept/article-validity.md).

 On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are expire in the next month. The recipient can then extend the **Valid to** date to continue using the article. For more information, see [Managing email notifications in Knowledge Management](../concept/email-notifications-km.md).

 **Note:** If the system date format or user preferences is set to use `yy` year format, you might face issues when the **Valid to** date is set to the default date. Contact your administrator or modify the user preferences to use a date format with the `yyyy` year format. For more information, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Personalize the system date format](https://www.servicenow.com/docs/access?context=t_PersonalizeTheSystemDateFormat&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) topics.

</td></tr><tr><td>

Confidence

</td><td>

Maturity of an article based on its completeness and reusability.

</td></tr><tr><td>

Version

</td><td>

Version of the article. This field appears only when the article versioning feature is enabled. For more information, see [Article versioning](../concept/article-versioning.md).

</td></tr><tr><td>

Parent

</td><td>

Number of the article that represents the base language article. This setting keeps translations of the same article related to each other. Consider choosing the same language consistently for the parent article. This field appears only when the I18N:Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) is activated. For more information, see [I18N - Knowledge internationalization](../concept/c_I18NKMInternational.md).**Note:** The **Parent** field contains the first version of the parent article only. This field is used by the translation management feature to maintain the relationship between the source article and its translations.

</td></tr><tr><td>

Article type

</td><td>

The type of article, either HTML or wiki.**Note:** This field is only visible in the standard template.

</td></tr><tr><td>

Workflow

</td><td>

\[Read-Only\] The publication state of the article, such as **Draft**, **In Review**, or **Published**. When inserting a new article from an existing article, the state of the new article is reset to **Draft**.

</td></tr><tr><td>

Source

</td><td>

The task this knowledge article was created in response to, if any. This field is set automatically when you create the knowledge article from a task record.

</td></tr><tr><td>

Attachment link

</td><td>

Option for downloading an attached file automatically when a user accesses the article, instead of opening the article view. Add one or more attachments to the article to use this option.**Note:** You may attach multiple files, but most web browsers permit users to download only the first one. To ensure download of all the files, bundle them into an archive, such as with WinZip, and attach the archive. The Attachment link option applies to articles accessed from search links only. Articles accessed as links within other knowledge articles won’t replicate this behavior.

</td></tr><tr><td>

Display attachments

</td><td>

Option for displaying attachments to users viewing this knowledge article. Attachments appear below the article text. Add one or more attachments to the article to use this option.

</td></tr><tr><td>

Governance

</td><td>

An attribute of an article that enables you to control sensitive, critical, or regulated information. Not all articles have the same requirement for compliance reviews. Some articles are based on the collective experience of the people who use the articles \(experience-based\). Other articles have policy or legal information that require tight control \(compliance-based\).

</td></tr><tr><td>

Short description

</td><td>

The title of the article. This title appears when browsing and searching for a knowledge article, and at the top of the article.You can enter up to 100 characters in this field.

**Note:** If contextual search is enabled, the knowledge articles similar to the entered short description text appear in the Knowledge results section.

</td></tr><tr><td>

Article body

</td><td>

Content for the article. A preview of the content appears when browsing and searching for a knowledge article.Use the editing functions in the HTML editor to create content. For more information, see [Editing functions for knowledge articles in the HTML editor](../concept/knowledge-html-editor.md).

</td></tr><tr><td>

Meta

</td><td>

Tags for optimizing search from external search engines. Separate multiple entries by commas. You may need to configure the form to add this field. For more information, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).**Note:** If AI Search is enabled for the Knowledge Management Service Portal, the tags you add to the **Meta** field aren't indexed. To fine-tune AI Search results, your administrator can configure result improvement rules. For more information, see [AI Search in Service Portal](https://www.servicenow.com/docs/access?context=ai-search&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>    **Note:** The **Confidence** and **Governance** fields appear when the Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\) is activated. For more information, see [Managing KCS article states](../concept/managing-kcs-article-states.md).

6.  To preview the article select the **View Article** link in the Related Links section located below the form.

    **Note:**

    Viewing the article through this link is only to facilitate a preview of the edited article and, does not add to the actual view count of the article on the document site.

7.  To search for similar articles, enter the text in the **Related Search** field or continue with the default text in the Knowledge results section.

    If the Knowledge results section isn’t displayed on the Knowledge form, an administrator can configure the form layout to add the **Contextual Search Results** field to the form.

    -   To find knowledge articles that have high text similarity with the entered search text, choose **Similar Articles \(ML\)**.

        **Note:** This option is available only when the Predictive Intelligence feature is enabled and your administrator has trained the similarity solution for Knowledge Management. For more information, see [Train the similarity solution for Knowledge Management to find related articles](train-similarity-solution-km.md).

    -   To find knowledge articles that match the entered search text, choose **Search Articles**.
8.  To view the entire article in a pop-up window, select the link to the article title.

9.  Select **Submit** to create the article.

10. Select **Search for Duplicates** for any redundant content in existing articles.

11. Select the link in the **For SEO suggestions on this article, click here** message, if available, to review suggestions for improving your article.

    Suggestions are provided to help you improve the search engine optimization and accessibility of your article, such as removing multiple **Heading 1** or `<H1>` tags. Suggestions are provided for the heading 1 `<h1>`, anchor `<a>`, and image `<img>` tags.

12. Either add to or modify the article details or publish the article.

    -   Add to or modify the article details.

        For more information, see [Edit a knowledge article](edit-knowledge-article.md).

    -   Publish the article by selecting **Publish**.

        A knowledge article is published depending on the workflow setting of its knowledge base:

        -   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it’s scheduled to be published at a later date.
        -   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it’s scheduled to be published at a later date.

            **Note:** With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. An administrator can override this behavior by disabling the **glide.knowman.ownership\_group.enable\_self\_approval** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md).

        For more information, see [Schedule a knowledge article for publishing](schedule-article-publishing.md).

        If an article is visible to a guest user, a message appears that reads `This article may be visible to unauthenticated users after it is published. Do you still want to proceed?`

        When published, the knowledge article appears in the Published and All lists. To view the Published list, navigate to **Knowledge** &gt; **Articles** &gt; **Published**. To view the All list, navigate to **Knowledge** &gt; **Articles** &gt; **All**.

        If the article versioning feature is enabled, the version number of the knowledge article increments to the next whole number \(for example, from 2.02 to 3.0\). For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).


## What to do next

After saving the article record, you can add tags to organize the article.

After you create and publish a knowledge article, you can perform the following actions related to the article:

-   Request translations for the knowledge article. For more information, see [Request missing translations for available languages](request-translations-missing-languages.md).
-   Retire the knowledge article. Select **Retire** to enable the retirement workflow. For more information, see [Retire a knowledge article](../concept/c_RetiredKnowledgeArticles.md).
-   Translate the knowledge article directly from the knowledge article. For more information, see [Translate a knowledge article from a translation task](translate-knowledge-article.md).
-   Delete the published knowledge article. Select **Delete**. If the **Delete** button isn't displayed, select the more actions icon \(![More actions icon](../image/more.png)\), and then select **Delete**.

    **Note:** Only users with the admin role can delete a published knowledge article.


**Parent Topic:**[Creating and maintaining articles](../concept/creating-and-maintaining-articles.md)

**Related topics**  


[Map related articles](map-related-articles.md)

[Predictive Intelligence for Knowledge Management](../concept/predictive-intelligence-for-km.md)


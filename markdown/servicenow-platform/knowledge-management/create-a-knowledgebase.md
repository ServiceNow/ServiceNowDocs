---
title: Create a knowledge base
description: Create a knowledge base to provide a self-service platform for users to store, share, and manage content. Configure knowledge bases into product or service categories and manage user access based on permissions. Customize workflows for publishing and retiring articles in the knowledge base.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a knowledge base

Create a knowledge base to provide a self-service platform for users to store, share, and manage content. Configure knowledge bases into product or service categories and manage user access based on permissions. Customize workflows for publishing and retiring articles in the knowledge base.

## Before you begin

Understand the [requirements](../reference/set-up-knowledge-admin-user.md) for setting up a knowledge base.

Role required: knowledge\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge bases**.

2.  In the Knowledge Bases list, click **New**.

3.  On the Knowledge base form, fill in the following fields as appropriate:

<table id="table_ykv_cfz_f2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Unique name for the knowledge base.

</td></tr><tr><td>

Article Validity

</td><td>

Number of default days articles will be valid for after their created date. **Note:** The **Article Validity** field is configured to set the **Valid to** date for an article. The **Valid to** date is the date this knowledge article expires. When you create an article within a knowledge base, the date value in the **Valid to** field of the article is calculated as follows: Created \(sys\_created\_on\) + Article Validity \(in days\). An article author or editor can select whether to keep or change the **Valid to** date  \(see [Create a knowledge article](create-knowledge-article.md)\). If the **Article Validity** field is blank, the date in the **Valid to** field date is set to  January 1, 2100.

</td></tr><tr><td>

Icon

</td><td>

An image that provides a visual reference to describe the knowledge base. This image is displayed next to all articles from this knowledge base in the article search results page.

</td></tr><tr><td>

Disable commenting

</td><td>

Option to disable commenting. If selected, users cannot comment on articles in the knowledge base.

</td></tr><tr><td>

Disable suggesting

</td><td>

Option to disable edit suggestions. If selected, users cannot suggest edits to articles in the knowledge base.

</td></tr><tr><td>

Disable category editing

</td><td>

Option to disable editing of knowledge categories. If selected, only knowledge managers can add or edit knowledge categories for the knowledge base.

</td></tr><tr><td>

Disable rating

</td><td>

Option to disable the rating for knowledge articles. If selected, users cannot rate the article in the knowledge base.

</td></tr><tr><td>

Disable mark as helpful

</td><td>

Option to disable the mark as helpful. If selected, user cannot mark any article as helpful in the knowledge base.

</td></tr><tr><td>

Enable blocks

</td><td>

Option to enable the knowledge blocks feature. If selected, you can create knowledge blocks to add to knowledge articles within a knowledge base.

</td></tr><tr><td>

Checklist

</td><td>

Checklist to evaluate the quality of articles in the knowledge base.

</td></tr><tr><td>

Application

</td><td>

Application scope of the knowledge base. **Note:** This field is automatically set to the application selected in the application picker. For information about a scoped knowledge base, see [Scoped knowledge bases](../concept/scoped-knowledge-base-administration.md).

</td></tr><tr><td>

Owner

</td><td>

The user responsible for the knowledge base. A knowledge base owner can assign other [roles](../reference/r_KnowledgeRoles.md#) to the knowledge base.

</td></tr><tr><td>

Managers

</td><td>

Users who perform administrative functions on the knowledge base.

</td></tr><tr><td>

Publish workflow

</td><td>

The workflow for publishing the articles in the knowledge base. -   **Knowledge - Instant Publish:** publishes articles in the knowledge base without requiring an approval.
-   **Knowledge - Approval Publish:** requests approval from the manager of the knowledge base before moving the articles to the published state.


</td></tr><tr><td>

Retire workflow

</td><td>

The workflow for retiring the articles in the knowledge base. -   **Knowledge - Instant Retire:** retires articles in the knowledge base without requiring an approval.
-   **Knowledge - Approval Retire:** requests approval from the manager of the knowledge base before moving the articles to the retired state.


</td></tr><tr><td>

Active

</td><td>

Option to indicate that the knowledge base is active. If not selected, only users with the admin role or knowledge administrators can create, search for, or view its articles.

</td></tr><tr><td>

Description

</td><td>

A short description to describe the knowledge base.

</td></tr><tr><td>

Set default knowledge field values

</td><td>

Default configuration settings for the knowledge base.

</td></tr><tr><td>

Related products

</td><td>

List of products related to the knowledge base content.

</td></tr><tr><td>

Auto-create translation tasks

</td><td>

Option to enable creating translation tasks automatically after an article is published. If this option is selected, when a knowledge article is published in this knowledge base, translation tasks are automatically created for the configured languages.This field appears only when the translation management feature and **glide.knowman.translation.enable\_translation\_task** property are enabled. For more information, see [Translation management](../concept/translation-management.md) and [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

</td></tr><tr><td>

Languages

</td><td>

Languages enabled for the knowledge articles in this knowledge base. If your system has more languages, use this option to select only those languages in which you want to translate knowledge articles in this knowledge base.

 You can add more languages later. However, you can remove languages only when no knowledge articles exist in that language.

 This field appears only when the translation management feature and **glide.knowman.translation.enable\_translation\_task** property are enabled. For more information, see [Translation management](../concept/translation-management.md) and [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  In the related list section, view or configure the following items related to the knowledge base:

<table id="table_evp_fd1_g2b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge

</td><td>

List of knowledge articles stored in this knowledge base.

</td></tr><tr><td>

Can Read

</td><td>

List of user criteria that grants read access and enables user matching the criteria to read articles in a knowledge base. **Note:** It is recommended to assign appropriate user criteria to secure read access. See, [Select user criteria for a knowledge base](t_SelectUserCriteria.md).

</td></tr><tr><td>

Can Contribute

</td><td>

List of user criteria that grants contribute access and enables user matching the criteria to create and modify articles in a knowledge base. **Note:** It is recommended to assign appropriate user criteria to secure contribute access. See, [Select user criteria for a knowledge base](t_SelectUserCriteria.md).

</td></tr><tr><td>

Article Templates

</td><td>

If you have activated the Knowledge Management Advanced \(com.snc.knowledge\_advanced\) plugin, the **Article Templates** related list is displayed. If there are article templates in the related list, articles in that knowledge base can only be created using one of the article templates listed.

 If the **Article Templates** related list is empty, articles can be created using any article template.

 Click **Edit** to map article templates to the knowledge base.

**Note:** Admins, knowledge admins, and knowledge managers can edit the article templates for the knowledge base.

</td></tr><tr><td>

Featured Content

</td><td>

List of knowledge articles that appear in the homepage **Featured Content** section based on the corresponding keyword search set for each article.

</td></tr><tr><td>

Knowledge Categories

</td><td>

List of knowledge categories associated with this knowledge base.**Note:** If the category is marked as inactive then you can't associate articles to the category. However, it does not have any effect on the existing articles of that category.

</td></tr></tbody>
</table>6.  Click **Submit**.


**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)

**Related topics**  


[Control access at the knowledge base level through user criteria](t_SelectUserCriteria.md)

[Explicit roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)

[Knowledge workflows](../reference/r_KnowledgeWorkflows.md#)

[Knowledge Management properties](../reference/r_KnowledgeProperties.md#)

[Create a custom knowledge homepage](t_CreateACustomKnowledgeHomepage.md)

[I18N - Knowledge internationalization](../concept/c_I18NKMInternational.md)


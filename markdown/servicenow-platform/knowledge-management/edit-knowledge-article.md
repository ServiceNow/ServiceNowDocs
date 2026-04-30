---
title: Edit a knowledge article
description: Edit knowledge articles within a knowledge base to update information shared across your organization.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a knowledge article

Edit knowledge articles within a knowledge base to update information shared across your organization.

## Before you begin

Role required: knowledge

## About this task

Users with at least one role can edit knowledge. These users are known as knowledge contributors. Users without any role can read articles and submit feedback, but cannot edit articles.

However, knowledge managers can configure User Criteria to restrict access to certain knowledge bases. For example, only members of the IT department can create or edit knowledge articles in the IT knowledge base, such as desktop support information or articles describing company IT processes.

**Note:**

-   If the article versioning feature is enabled, the author cannot edit the article if it is already checked out by the contributor. If the feature is disabled, any users with contribute access to an article can edit the draft version of the article. An administrator can disable the article versioning feature by setting the **glide.knowman.versioning.enabled** property \(from the **System Property** \[sys\_properties\] table\) to **false**.
-   If an ownership group is associated with a knowledge article, the author or reviser of the article can't contribute to the article after the article is published. An administrator can override this behavior by enabling the **glide.knowman.ownership\_group.override** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md).
-   If the **glide.knowman.translation.enable\_translation\_task** property is enabled, you can’t modify the knowledge base of existing articles.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles**.

2.  Select an article from the **Published** or **Unpublished** category.

3.  On the Knowledge form, click **Edit**.

    **Note:** If the knowledge article was created using Microsoft Word, you can edit the article only in Microsoft Word. In this case, select **Open in Word** to open the article in Word Online. For more information, see [Edit a knowledge article in Microsoft Word](edit-article-word.md).

    If you want to edit the article using the HTML editor, you can unlink the article from Word. For more information, see [Unlink knowledge articles from linked Microsoft Word documents](unlink-word-document.md).

4.  If the article versioning feature is enabled, click **Checkout** for a published knowledge article.

    You can only edit the latest version of a knowledge article.

5.  Click **Update**.

    When you edit a knowledge article, a default value appears in the **Valid to** field. You can select whether to keep or change the default **Valid to** date.

    **Note:** If the article versioning feature is enabled, the default value of the **Valid to** date in the updated article version is automatically set based on the following criteria:

    -   If the **Article Validity** field in the knowledge base associated with the article is blank, the **Valid to** date value from the earlier version of the article is retained.
    -   If the **Article Validity** field in the knowledge base associated with the article is not blank, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field \(Article updated date + article validity\).
    If you move a knowledge article to another knowledge base, the default value of the **Valid to** date in the updated article is automatically set based on the following criteria:

    -   If the **Article Validity** field in the selected knowledge base is blank, the earlier **Valid to** date value is retained for the knowledge article.
    -   If the **Article Validity** field in the selected knowledge base isn't blank, the **Valid to** date is automatically updated to start from the date the article was updated until the number of days specified in the **Article Validity** field \(Article updated date + article validity\).
    If the dictionary value of the **Valid to** field is modified, this dictionary value overrides the default value of the **Valid to** field calculated according to the **Article Validity** field. For more information, see [Validity of a knowledge article](../concept/article-validity.md).

    The article is saved. If the article versioning feature is enabled, the version of the knowledge article is incremented by 0.01. For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md)

6.  Select the link in the **For SEO suggestions on this article, click here** message, if available, to review suggestions for improving your article.

    Suggestions are provided to help you improve the search engine optimization and accessibility of your article, such as removing multiple **Heading 1** or `<H1>` tags. Suggestions are provided for the heading 1 `<h1>`, anchor `<a>`, and image `<img>` tags.

7.  Publish the article by clicking **Publish**.

    The knowledge article is published depending on the workflow setting of its knowledge base:

    -   **Knowledge - Instant Publish**: The knowledge article is immediately published unless it is scheduled to be published at a later date.
    -   **Knowledge - Approval Publish**: The knowledge article is published on approval completion unless it is scheduled to be published at a later date.

        **Note:**

        -   With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. An administrator can override this behavior by disabling the **glide.knowman.ownership\_group.enable\_self\_approval** property. For more information, see [Ownership groups](../concept/enable-ownership-group.md)
        -   If an article is visible to a guest user, a message appears that reads `This article may be visible to unauthenticated users after it is published. Do you still want to proceed?`
    For more information, see [Schedule a knowledge article for publishing](schedule-article-publishing.md).

    When published, the knowledge article appears in the Published and All lists. To view the Published list, navigate to **Knowledge** &gt; **Articles** &gt; **Published**. To view the All list, navigate to **Knowledge** &gt; **Articles** &gt; **All**.

    If the article versioning feature is enabled, the version number of the knowledge article increments to the next whole number \(for example, from 2.02 to 3.0\). For more information, see [Knowledge article version numbers](../concept/knowledge-article-version-numbers.md).


**Parent Topic:**[Creating and maintaining articles](../concept/creating-and-maintaining-articles.md)

**Related topics**  


[Article versioning changes](../concept/article-versioning-changes.md)


---
title: Generate a Knowledge article from the classic environment with Now Assist
description: As an author or an agent, generate new Knowledge articles using Now Assist on tasks within the classic environment.As an author, generate new Knowledge articles using Now Assist on tasks within the classic environment.
locale: en-US
release: yokohama
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate a Knowledge article from the classic environment with Now Assist

As an author or an agent, generate new Knowledge articles using Now Assist on tasks within the classic environment.

## Before you begin

Only standard and KCS templates are available when generating Knowledge articles from the classic environment using Now Assist. For details on how to enable these settings in individual workspaces, refer to the respective knowledge article generation topics.

To see the Now Assist experience on the Create Article page, the following Knowledge generation criteria should be configured:

-   Confirm that the KB generation skills are installed.
-   In Now Assist Admin confirm with your admin that the following criteria are in place:
    -   The table record and input fields must be specified.
    -   The conditions for skill availability must be specified from the list of attributes.
    -   The display of the KB generation feature In-product or Now Assist panel must be specified.

Role required: author or agent

## Generate article in classic environment for agents

## Procedure

1.  Open a task that is assigned to you.

2.  Generate an article by using the UI actions that appear in the record.

    **Note:** Based on the template selection made by your administrator while configuring Knowledge Management system properties, you can apply either the KCS or standard template to the article.

3.  In the Use Al to draft this article? modal, select **Yes, draft with Now Assist**.

    ![Enable Now Assist in the workspace for KB article generation.](../image/now-assist-kb-dialog-box.png)

4.  Select up to five additional relevant cases in the new modal, powered by generative AI, to generate the article and select **Continue with selected tasks**.

    ![Select up to five additional relevant cases in the new modal to generate the article.](../../customer-service-management/image/now-assist-kb--multiple-similar-cases.png)

    The article appears in a new tab with a unique ID number for the article.


**Parent Topic:**[Using Now Assist in Knowledge Management](../concept/using-now-assist-in-km.md)

## Generate article in classic environment for authors

As an author, generate new Knowledge articles using Now Assist on tasks within the classic environment.

### Before you begin

Role required: author

### Procedure

1.  For the author experience in a classic environment, navigate to **Lists** &gt; **Knowledge** &gt; **All articles** and select **New**.

2.  In the Create article modal, select a Knowledge Base and an article template and select **Create Article**.

3.  In the Use AI to draft this article modal, select **Yes, draft with Now Assist**.

4.  In the Search for tasks to draft this article modal, select the up to five task types and enter the keywords or task number to find similar cases.

    ![Use selected tasks to generate article.](../image/NA-KB-coreui-author.png)

5.  Select **Use selected tasks to help draft new article** to generate the article.

    The completed article is displayed in the chosen template, along with the success message: `This article was drafted by Now Assist. Be sure to review it for accuracy before saving`.

    **Note:**

    -   If no similar tasks exist, this modal won’t appear, and the article is created. The generated article, based on the chosen relevant records, is linked to both the parent task and all the relevant cases selected.
    -   You can modify the draft before saving it. The article appears in a new tab with a unique ID number for the Knowledge article and is attached to the parent record.
    -   After reviewing the Now Assist generated article, when you select **Save** or **Publish**, the Now Assist success message disappears indicating that it’s no longer a Now LLM Service- generated article.
    -   If Now LLM Service fails to generate a result, an error message appears.
    -   When creating an article using Now Assist, once the process is triggered, it can't be stopped. Now Assist continues to generate the article even if you close the modal.
6.  Review the Now Assist generated article and select **Save** or **Publish**.

    The Now Assist success message disappears indicating that it’s no longer a Now LLM Service- generated article.



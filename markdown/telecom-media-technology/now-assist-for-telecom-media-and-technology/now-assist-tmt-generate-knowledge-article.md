---
title: Generate a knowledge article for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate the knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment with Now Assist.
locale: en-US
release: yokohama
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Now Assist for Telecommunications, Media and Technology \(TMT\), Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Generate a knowledge article for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate the knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment with Now Assist.

## Before you begin

To generate a knowledge article for a case, the case must be in the resolved and closed state, and must not already have a knowledge article linked to it.

Install the Knowledge Management Advanced plugin to use the Knowledge Centered Service \(KCS\) template when you’re generating knowledge articles. For more information, see [Activate the Knowledge Management Advanced plugin](https://www.servicenow.com/docs/access?context=activate-knowledge-advanced-plugin&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Make sure that your administrator enables Now Assist experience on the Create Article page to ensure that the following knowledge base generation criteria is configured:

-   The knowledge skills are installed.
-   In the Now Assist Admin console, ensure that the following criteria are in place:
    -   Specify the table record and input fields.
    -   Specify the conditions for the skill availability from the list of attributes.
    -   Display the knowledge base generation feature In-product and specify the Now Assist panel.
-   Configure **Create Article** to apply the supported template; For example, Standard and KCS article HTML.

-   Currently, only the Create Article experience is available.

Role required: agent

## About this task

In  CSM Configurable Workspace and classic environment, you can generate the knowledge article information for a case by selecting **Create Knowledge** on the case record. This UI action displays the Use Al to draft this article modal. By using this modal, you can choose to write the article yourself or draft an article with  Now Assist and review and edit the knowledge article text.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Open a case that is assigned to you.

    The case record status should be either resolved or closed.

3.  Create the article by selecting **Create Knowledge** from the UI actions for the case record.

    **Note:**

    The **Create Knowledge** UI action is only visible when a case doesn't have an existing knowledge article that is associated with it.

4.  In the Create article modal, select a knowledge base and an Article template, if displayed.

    **Note:** If no options are displayed, the default template selected by your administrator in the Now Assist Admin console is used.

5.  Select **Create article**.

6.  In the Use Al to draft this article modal, select **Yes, draft with Now Assist**.

    ![Enable Now Assist in CSM for KB article generation.](../image/serviceproblemcase-knowledge-article.png "Modal to draft article using AI")

7.  In the new modal, search for similar cases that can be used to generate the article; otherwise, select **Cancel**.

    ![Select up to five additional relevant cases in the new modal to generate the article.](../image/additional-relevant-task-tmt.png "Additional relevant tasks")

    The completed article is displayed in the chosen template with a success message "This article was drafted by Now Assist. Be sure to review it for accuracy before saving."

    **Note:**

    -   If no similar cases exist, this modal doesn’t appear, and the article is created. The generated article, based on the chosen relevant records, is linked to both the account case and all the relevant cases selected.
    -   You can select up to five additional relevant cases in the new modal to generate the article.
    -   You can modify the draft before saving it. The article appears in a new tab with a unique ID number for the knowledge article and is attached to the parent record.
    -   If Now LLM Service fails to generate a result, an error message is displayed.
    -   When creating an article by using Now Assist, after the process is triggered, it can't be stopped. Now Assist continues to generate the article even if you close the modal.
8.  Select the **Knowledge Base** and the **Language** in the pop-up window **What language should Now Assist draft this article in**.

9.  Select **Continue**.

    The article is generated in the selected knowledge base and language, and the content is displayed in that same language.

10. Select **Insert** to paste the generated response.

11. Review the Now Assist generated article and select **Save** or **Publish**.

    The Now Assist success message disappears which means that it’s no longer a Now LLM Service generated article.


**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

**Related topics**  


[Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=now-assist-knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)


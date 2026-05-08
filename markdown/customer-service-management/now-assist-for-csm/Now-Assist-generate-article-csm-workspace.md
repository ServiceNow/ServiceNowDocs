---
title: Generate a knowledge article from the CSM Configurable Workspace and classic environment with Now Assist
description: Generate the knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment with Now Assist.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Generate a knowledge article from the CSM Configurable Workspace and classic environment with Now Assist

Generate the knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment with Now Assist.

## Before you begin

To generate a knowledge article for a case, the case must be in the **Resolved** and **Closed** state, and must not already have a knowledge article linked to it. Although the **Create Knowledge** button appears in other states, it won’t trigger the skill. In those cases, clicking the button just opens the KB article form for manual entry.

Verify that [Configure knowledge generation](../../customer-service-management/task/configure-knowledge-generation-in-now-assist_0.md) is set up.

**Important:**

-   -   For Now Assist panel, if property sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled then it will create article using standard template for cases.
-   For Core UI / Workspace, if sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled then it will not show **Create Knowledge** button on case form.

Make sure that your administrator enables Now Assist experience on the Create Article page to confirm that the following knowledge base generation criteria is configured:

-   The KB generation skill is activated.
-   In the Now Assist Admin console, verify that the following criteria are in place:
    -   Specify the table record and input fields.
    -   Specify the conditions for the skill availability from the list of attributes.
    -   Display the knowledge base generation feature In-product and specify the Now Assist panel.
-   To manage who can access knowledge bases and knowledge articles, you can set permissions to define which users or user groups can read or contribute to the content. For more info, see Managing access to knowledge bases and knowledge articles

Role required: agent

## About this task

In  CSM Configurable Workspace and classic environment, you can generate the knowledge article information for a case by selecting **Create Knowledge** on the case record. This UI Action displays the Use Al to draft this article modal. By using this modal, you can choose to write the article yourself or draft an article with  Now Assist and review and edit the knowledge article text.

**Note:**

The Create Knowledge UI action is available to the customer service agents who have assigned cases in the Resolve or Close state. You can also generate knowledge article information on demand from the Now Assist panel. For more information, see [Knowledge article generation](Now-Assist-generate-article-csm-workspace.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Open a case that is assigned to you.

    The case record status should be either resolved or closed.

3.  Create the article by selecting **Create Knowledge** from the UI actions for the case record.

    **Note:**

    The **Create Knowledge** UI Action is only visible when a case doesn't have an existing knowledge article that is associated with it.

    Alternative way to trigger the skill [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](../../customer-service-management/task/request-gen-ai-capabilities-csm-now-assist-panel.md).

4.  In the Create article modal, select a knowledge base and an Article template, if displayed.

    **Note:** If no options are displayed, the default template selected by your administrator in the Now Assist Admin console is used.

5.  Select **Create Article**.

6.  In the Use Al to draft this article modal, select **Yes, draft with Now Assist**.

    ![Enable Now Assist in CSM for KB article generation.](../../customer-service-management/image/now-assist-kb-dialog-box.png "Modal to draft article using AI")

7.  In the new modal, search for similar cases that can be used to generate the article; otherwise, select **Cancel**.

    The completed article is displayed in the chosen template with a success message "This article was drafted by Now Assist. Be sure to review it for accuracy before saving."

    **Note:**

    -   If no similar cases exist, this modal doesn’t appear, and the article is created. The generated article, based on the chosen relevant records, is linked to both the account case and all the relevant cases selected. Similar cases are populated by the AI Search profile titled \[KM\] Multi-task Article Generation.
    -   You can select up to five additional relevant cases in the new modal to generate the article.
    -   You can modify the draft before saving it. The article appears in a new tab with a unique ID number for the knowledge article and is attached to the parent record.
    -   If Now LLM Service fails to generate a result, an error message is displayed.
    -   When creating an article by using Now Assist, after the process is triggered, it can't be stopped. Now Assist continues to generate the article even if you close the modal.
8.  Select the **Knowledge Base** and the **Language** in the pop-up window **What language should Now Assist draft this article in**.

9.  Select **Continue**.

    The article is generated in the selected knowledge base and language, and the content is displayed in that same language.

10. Select some text in the KB article and then select the Now Assist icon![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).

    Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg) generates a recommended text that is based on the context of the selected content in the article up to that point. You can refine your response by selecting to elaborate or shorten the selected text.

11. Select **Insert** to paste the generated response.

12. Review the Now Assist generated article and select **Save** or **Publish**.

    The Now Assist success message disappears which means that it’s no longer a Now LLM Service generated article.

    **Note:** Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg) is also available for the published KB articles.


**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../../customer-service-management/concept/now-assist-csm-using.md)

**Related topics**  


[bundle-platcap.now-assist-knowledge-management]


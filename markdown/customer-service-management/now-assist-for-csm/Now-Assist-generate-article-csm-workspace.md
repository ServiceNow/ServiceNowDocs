---
title: Generate a knowledge article with ServiceNow Otto
description: Generate knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment using ServiceNow Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/Now-Assist-generate-article-csm-workspace.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI skills, ServiceNow Otto for CSM, Customer Service Management]
---

# Generate a knowledge article with ServiceNow Otto

Generate knowledge articles for resolved and closed cases within the CSM Configurable Workspace and classic environment using ServiceNow Otto.

## Before you begin

To generate a knowledge article for a case, the case must be in the **Resolved** or **Closed** state and must not already have a knowledge article linked to it. Although the **Create Knowledge** button appears in other states, it does not trigger the skill. In those cases, selecting the button opens the KB article form for manual entry.

Before generating articles, confirm that [Configure knowledge generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-knowledge-generation-in-now-assist_0.md) is configured.

**Warning:**

-   -   For the ServiceNow Otto panel, if property sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled, the article is created using the standard template for cases.
-   For Core UI / Workspace, if sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled, the **Create Knowledge** button does not appear on the case form.

Your administrator must enable the ServiceNow Otto experience on the Create Article page and configure the following knowledge base generation criteria:

-   Activate the KB generation skill.
-   In the ServiceNow Otto AI Admin console, confirm that the following criteria are in place:
    -   The table record and input fields are specified.
    -   The conditions for skill availability are specified from the list of attributes.
    -   The knowledge base generation feature is set to display In-product, the panel, or both.
-   To manage access to knowledge bases and articles, set permissions that define which users or groups can read or contribute. For more information, see [Managing access to knowledge bases and knowledge articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/user-access-knowledge.md).

Role required: agent

## About this task

In the CSM Configurable Workspace and classic environment, generate knowledge article information for a case by selecting **Create Knowledge** on the case record. The Use AI to draft this article modal opens. Choose to write the article yourself or draft it with ServiceNow Otto, then review and edit the text.

**Note:**

The Create Knowledge UI action is available to customer service agents with assigned cases in the Resolve or Close state. You can also generate knowledge article information on demand from the ServiceNow Otto panel. For more information, see [Knowledge article generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/Now-Assist-generate-article-csm-workspace.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Open a case assigned to you.

    The case must be in the resolved or closed state.

3.  Select **Create Knowledge** from the UI actions on the case record.

    **Note:**

    The **Create Knowledge** UI action is only visible when a case doesn't have an existing knowledge article associated with it.

    For an alternative way to trigger the skill, see [Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/request-gen-ai-capabilities-csm-now-assist-panel.md).

4.  In the Create article modal, select a knowledge base and an article template, if displayed.

    **Note:** If no options are displayed, the default template configured in the AI Admin console is used.

5.  Select **Create Article**.

6.  In the Use AI to draft this article modal, select **Yes, draft with Otto**.

7.  In the modal, search for similar cases to include in the article; otherwise, select **Cancel**.

    The completed article is displayed in the chosen template with a success message: `This article was drafted by ServiceNow Otto. Review it for accuracy before saving.`

    **Note:**

    -   If no similar cases exist, this modal doesn't appear and the article is created directly. The generated article is linked to the account case and all selected relevant cases. Similar cases are populated by the AI Search profile titled \[KM\] Multi-task Article Generation.
    -   You can select up to five additional relevant cases in the new modal to generate the article.
    -   You can modify the draft before saving. The article appears in a new tab with a unique ID and is attached to the parent record.
    -   If the LLM service fails to generate a result, an error message is displayed.
    -   After the article generation process is triggered, it can't be stopped. Generation continues even if you close the modal.
8.  Select the **Knowledge Base** and the **Language** in the **What language should ServiceNow Otto draft this article in** dialog.

9.  Select **Continue**.

    The article is generated in the selected knowledge base and displayed in the selected language.

10. Select some text in the KB article and then select the ServiceNow Otto icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text:.

    The icon generates recommended text based on the selected content. Select **Elaborate** or **Shorten** to refine the response.

11. Select **Insert** to add the generated response to the article.

12. Review the generated article and select **Save** or **Publish**.

    The ServiceNow Otto success message disappears, indicating the article is no longer AI-generated.

    **Note:** The icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: is also available for published KB articles.


**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-knowledge-management.md)


---
title: Generate a Knowledge article from the classic environment with ServiceNow Otto
description: As an author or agent, generate Knowledge articles using ServiceNow Otto on tasks within the classic environment.As an author, generate Knowledge articles using ServiceNow Otto on tasks within the classic environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-in-knowledge-management/Now-Assist-generate-article-coreui.html
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 3
breadcrumb: [Use ServiceNow Otto in Knowledge Management, ServiceNow Otto in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate a Knowledge article from the classic environment with ServiceNow Otto

As an author or agent, generate Knowledge articles using ServiceNow Otto on tasks within the classic environment.

## Before you begin

Only standard and KCS templates are available when generating Knowledge articles from the classic environment using ServiceNow Otto. For details on enabling these settings in individual workspaces, see the respective knowledge article generation topics.

To see the experience on the Create Article page, configure the following Knowledge generation criteria:

-   Confirm that the KB generation skills are installed.
-   In the ServiceNow Otto AI Admin console, confirm that the following criteria are in place:
    -   The table record and input fields are specified.
    -   The conditions for skill availability are specified from the list of attributes.
    -   The KB generation feature is set to display In-product, the panel, or both.

Role required: author or agent

## Procedure

1.  Open a task assigned to you.

2.  Generate an article by using the UI actions that appear in the record.

    **Note:** Based on the template selection made by your administrator while configuring Knowledge Management system properties, you can apply either the KCS or standard template to the article.

3.  In the Use AI to draft this article? modal, select **Yes, draft with Otto**.

    \[Omitted image "now-assist-kb-dialog-box.png"\] Alt text: Enable the KB article generation skill in the workspace.

4.  Select up to five additional relevant cases in the modal and select **Continue with selected tasks**.

    \[Omitted image "now-assist-kb--multiple-similar-cases.png"\] Alt text: Select up to five additional relevant cases to generate the article.

    The article appears in a new tab with a unique ID.


**Parent Topic:**[Using ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/using-now-assist-in-km.md)

**Related topics**  


[Generate a knowledge article from the Service Operations Workspace for ITSM and classic environment by using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)

[Generate a knowledge article with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/Now-Assist-generate-article-csm-workspace.md)

[Generate a knowledge article from HR Agent Workspace with ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/gen-kb-now-assisthr.md)

[Generate a knowledge article from the CSM/FSM Configurable Workspace and classic environment with Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/na-fsm-generate-kb-article.md)

## Generate article in classic environment for authors

As an author, generate Knowledge articles using ServiceNow Otto on tasks within the classic environment.

### Before you begin

Role required: author

### Procedure

1.  For the author experience in a classic environment, navigate to **Lists** &gt; **Knowledge** &gt; **All articles** and select **New**.

2.  In the Create article modal, select a Knowledge Base and an article template and select **Create Article**.

3.  In the Use AI to draft this article modal, select **Yes, draft with Otto**.

4.  In the Search for tasks to draft this article modal, select up to five task types and enter the keywords or task number to find similar cases.

5.  Select **Use selected tasks to help draft new article** to generate the article.

    The completed article is displayed in the chosen template, along with the success message: `This article was drafted by ServiceNow Otto. Review it for accuracy before saving.`

    **Note:**

    -   If no similar tasks exist, this modal doesn't appear and the article is created. The generated article is linked to both the parent task and all the relevant cases selected.
    -   You can modify the draft before saving. The article appears in a new tab with a unique ID and is attached to the parent record.
    -   After reviewing the generated article, select **Save** or **Publish**. The success message disappears, indicating the article is no longer AI-generated.
    -   If Now LLM Service fails to generate a result, an error message appears.
    -   After the article generation process is triggered, it can't be stopped. Generation continues even if you close the modal.
6.  Review the generated article and select **Save** or **Publish**.

    The ServiceNow Otto success message disappears, indicating the article is no longer AI-generated.



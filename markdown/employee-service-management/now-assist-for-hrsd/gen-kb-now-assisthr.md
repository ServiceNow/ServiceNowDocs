---
title: Generate a knowledge article from HR Agent Workspace with Now Assist
description: Create drafts of knowledge articles that are based on the case descriptions with Now Assist for HR Service Delivery \(HRSD\). Creating Knowledge content with generative AI enables you to write efficiently as you address user concerns.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2024-10-16"
reading_time_minutes: 5
breadcrumb: [Using Now Assist for HR Service Delivery \(HRSD\), Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a knowledge article from HR Agent Workspace with Now Assist

Create drafts of knowledge articles that are based on the case descriptions with Now Assist for HR Service Delivery \(HRSD\). Creating Knowledge content with generative AI enables you to write efficiently as you address user concerns.

## Before you begin

-   Install the following plugins:
    -   Knowledge Management advanced plugin \[com.snc.knowledge\_advanced.installer\].
    -   Now Assist in Knowledge Management \[sn\_km\_gen\_ai\]
    -   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
    -   Latest version of Agent Workspace for HR Case Management \[sn\_hr\_agent\_ws\]
    -   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
    -   Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\]
-   Activate the Knowledge Assist skill from the Now Assist Admin console.

Role required:

-   sn\_hr\_core.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on the HR Case \[sn\_hr\_core\_case\] and its extended tables.
-   sn\_hr\_le.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on HR life cycle Events Cases.
-   sn\_hr\_er.case\_reader, sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on employee relations cases.
-   sn\_hr\_core.admin role to change specific options or indexed sources.
-   You should also have the required role for the knowledge base that you selected in the Now Assist Admin configuration.

## About this task

You can use the KB generation skill in either Core UI or Agent Workspace for HR Case Management. The fields that are used as inputs for generating a knowledge article are the Short description, description, close notes, worknotes, and additional comments fields.

**Note:** The KB generation skill is supported in the Now Assist panel for the HR Case records \[sn\_hr\_core\_case\] table, but not on its extended table records.

## Procedure

1.  Navigate to **Workspaces** &gt; **HR Agent Workspace**.

2.  Go to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

3.  Open the record named **HR Case**

4.  Validate that the record is active and select **Index all tables**

5.  **Note:** sn\_hr\_core.admin role is required for indexed source changes. After you validate and index the tables in the initial steps, you can proceed with opening an HR case and drafting a knowledge article.

6.  Open an HR case that is assigned to you.

7.  Set the HR case to the **Close Complete** state.

8.  Select the More actions icon \(![More Actions icon.](../reference/images/more-icon.png)\), then select **Create Knowledge**.

9.  If displayed, select a knowledge base and an article template.

    **Note:**

    -   If the Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\] is installed, one article template might be enabled. Select a knowledge base and article template. Otherwise, the article is created with the standard template.
    -   Only the KCS article template and standard template are supported. Disable the **Use Now Assist to draft an article** toggle if you don’t want the AI to generate a KB article.
10. Select **Draft article**.

    The article appears in a tab with a unique ID number for the knowledge article.

11. View, edit, or publish the article by using the UI actions on the screen.


**Parent Topic:**[Using Now Assist for HR Service Delivery \(HRSD\)](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation by using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Summarize a Sidebar discussion by using Now Assist for HR Service Delivery \(HRSD\)](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](chat-recommendations-nahr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](email-recommendation-nahr.md)

[Summarize a case by using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-summarize-case.md)

[Detect sensitive topics by using sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-sensitivity-detection.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Generate the resolution notes for a case by using the Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-res-note.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use the Now Assist panel in Agent Workspace for HR Case Management](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=now-assist-knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)


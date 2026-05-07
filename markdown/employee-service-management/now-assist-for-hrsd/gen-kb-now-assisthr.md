---
title: Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD
description: Create drafts of knowledge articles that are based on the case descriptions with Now Assist for HR Service Delivery \(HRSD\). Generating article content with generative AI enables you to write efficiently as you address user concerns.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD

Create drafts of knowledge articles that are based on the case descriptions with Now Assist for HR Service Delivery \(HRSD\). Generating article content with generative AI enables you to write efficiently as you address user concerns.

## Before you begin

-   Install the following plugins:
    -   Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\]; This is not a mandatory plugin and it cannot be uninstalled.
    -   Now Assist in Knowledge Management \[sn\_km\_gen\_ai\]
    -   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
    -   Latest version of Agent Workspace for HR Case Management \[sn\_hr\_agent\_ws\]
    -   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
    -   Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\]
-   Activate the Knowledge Assist skill from the Now Assist Admin console.

Role required:

-   sn\_hr\_core.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on the HR Case \[sn\_hr\_core\_case\] and its extended tables.
-   sn\_hr\_le.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on HR Lifecycle Events Cases.
-   sn\_hr\_er.case\_reader, sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on employee relations cases.
-   You should also have the required role for the knowledge base that you selected in the Now Assist Admin configuration.

## About this task

You can use the KB generation skill in either Core UI or Agent Workspace for HR Case Management. The fields that are used as inputs for generating a knowledge article are the Short description, description, close notes, worknotes, and additional comments fields.

**Note:** The KB generation skill is supported in Now Assist panel for the HR Case records \[sn\_hr\_core\_case\] table, but not on its extended table records.

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of a Now Assist skill](https://www.servicenow.com/docs/access?context=make-a-copy-of-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **HR Agent Workspace**.

2.  Select the **Lists** icon \(![HR Workspace Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Open an HR case in the **Close Complete** state.

4.  Select the More Actions icon\( ![More actions icon](../reference/images/EllipsisIcon.png)\)

5.  Select **Create Knowledge**.

6.  Select a knowledge base and an article template in the modal, then select **Create Article**.

    **Note:** If the Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\] is installed and at least one article template is enabled, a modal is displayed so that you can select a knowledge base and article template. Otherwise, the article is created with the standard template.

7.  Select one of the following in the **Use AI to draft this article?** modal.

<table id="choicetable_cql_m25_vcc"><thead><tr><th align="left" id="d378129e227">

Option

</th><th align="left" id="d378129e230">

Description

</th></tr></thead><tbody><tr><td id="d378129e236">

**Yes, draft with Now Assist**

</td><td>

Use Now Assist to draft an article based on task details.You can review and edit the article before it is published.

</td></tr><tr><td id="d378129e247">

**No, write it myself**

</td><td>

Draft the article manually.

</td></tr></tbody>
</table>8.  Review the **Article body**.

9.  Select **Save**.

    The article appears in a new tab with a unique ID number for the knowledge article.

10. View, save, or publish the article by using the UI actions on the screen.


**Parent Topic:**[Use Now Assist for HR Service Delivery \(HRSD\) in Agent Workspace](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Summarize a Sidebar discussion by using Now Assist for HRSD](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HRSD](chat-recommendations-nahr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation using Now Assist for HRSD](email-recommendation-nahr.md)

[Summarize an HR case using Now Assist for HRSD](now-assist-hrsd-summarize-case.md)

[Generate resolution notes using Now Assist for HRSD](now-assist-hrsd-res-note.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use Now Assist for HR - Galileo Inside to answer HR-related questions](use-galileo-inside.md)

[Use the Now Assist panel in HR Agent Workspace](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)](analyze-sentiments-now-assist.md)

[Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=now-assist-knowledge-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)


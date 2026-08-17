---
title: Generate a knowledge article from HR Agent Workspace with Now Assist
description: Create drafts of knowledge articles that are based on the case descriptions with ServiceNow Otto for HR Service Delivery \(HRSD\). Generating article content with generative AI enables you to write efficiently as you address user concerns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-assist-for-hrsd/gen-kb-now-assisthr.html
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a knowledge article from HR Agent Workspace with Now Assist

Create drafts of knowledge articles that are based on the case descriptions with ServiceNow Otto for HR Service Delivery \(HRSD\). Generating article content with generative AI enables you to write efficiently as you address user concerns.

## Before you begin

-   Install the following plugins:
    -   Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\]; This is not a mandatory plugin and it cannot be uninstalled.
    -   Now Assist in Knowledge Management \[sn\_km\_gen\_ai\]
    -   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
    -   Latest version of Agent Workspace for HR Case Management \[sn\_hr\_agent\_ws\]
    -   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
    -   Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\]
-   Activate the KB generation skill from the AI Admin Hub console. For more information, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

Role required:

-   sn\_hr\_core.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on the HR Case \[sn\_hr\_core\_case\] and its extended tables.
-   sn\_hr\_le.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on HR Lifecycle Events Cases.
-   sn\_hr\_er.case\_reader, sn\_hr\_core.kb\_writer roles to view the **Create Knowledge** option on employee relations cases.
-   You should also have the required role for the knowledge base that you selected in the AI Admin Hub configuration.

## About this task

You can use the KB generation skill in either Core UI or Agent Workspace for HR Case Management. The fields that are used as inputs for generating a knowledge article are the Short description, description, close notes, worknotes, and additional comments fields.

**Note:** The KB generation skill is supported in Now Assist panel for the HR Case records \[sn\_hr\_core\_case\] table, but not on its extended table records.

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **HR Agent Workspace**.

2.  Select the **Lists** icon \(\[Omitted image "agent-ws-hr-list-icon.png"\] Alt text: HR Workspace Lists icon\).

3.  Open an HR case in the **Close Complete** state.

4.  Select the More Actions icon\( \[Omitted image "EllipsisIcon.png"\] Alt text: More actions icon\)

5.  Select **Create Knowledge**.

6.  Select a knowledge base and an article template in the modal, then select **Create Article**.

    **Note:** If the Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\] is installed and at least one article template is enabled, a modal is displayed so that you can select a knowledge base and article template. Otherwise, the article is created with the standard template.

7.  Select one of the following in the **Use AI to draft this article?** modal.

<table id="choicetable_cql_m25_vcc"><thead><tr><th align="left" id="d365834e240">

Option

</th><th align="left" id="d365834e243">

Description

</th></tr></thead><tbody><tr><td id="d365834e249">

**Yes, draft with Now Assist**

</td><td>

Use Now Assist to draft an article based on task details.You can review and edit the article before it is published.

</td></tr><tr><td id="d365834e260">

**No, write it myself**

</td><td>

Draft the article manually.

</td></tr></tbody>
</table>8.  Review the **Article body**.

9.  Select **Save**.

    The article appears in a new tab with a unique ID number for the knowledge article.

10. View, save, or publish the article by using the UI actions on the screen.


**Parent Topic:**[Use ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Generate a chat reply recommendation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Generate a knowledge article from multiple cases]()

[Generate an email reply recommendation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use Galileo Inside to answer HR-related questions]()

[Use the Now Assist panel in Agent Workspace for HR Case Management]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Detect sensitive topics by using sensitivity detection in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Now Assist in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-knowledge-management.md)


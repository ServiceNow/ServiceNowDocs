---
title: Generate a knowledge article from multiple cases
description: Create drafts of knowledge articles from multiple cases with the ServiceNow Otto for HR Service Delivery \(HRSD\) application. Use generative AI to gather and create the content from multiple cases so that you can reduce the amount of time that you would have spent manually to get the same information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/gen-kb-now-assisthr-multi-case.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a knowledge article from multiple cases

Create drafts of knowledge articles from multiple cases with the ServiceNow Otto for HR Service Delivery \(HRSD\) application. Use generative AI to gather and create the content from multiple cases so that you can reduce the amount of time that you would have spent manually to get the same information.

## Before you begin

-   Install the following plugins:
    -   Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\]; This is not a mandatory plugin and it cannot be uninstalled.
    -   ServiceNow Otto for Knowledge Management \[sn\_km\_gen\_ai\]
    -   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
    -   Latest version of Agent Workspace for HR Case Management \[sn\_hr\_agent\_ws\]
    -   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
    -   Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_relations\]
-   Activate the KB generation skill from the AI Admin Hub console. For more information, see [.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

Role required:

-   sn\_hr\_core.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Generate article** option on the HR Case \[sn\_hr\_core\_case\] and its extended tables.
-   sn\_hr\_le.case\_reader and sn\_hr\_core.kb\_writer roles to view the **Generate article** option on HR Lifecycle Events Cases.
-   sn\_hr\_er.case\_reader, sn\_hr\_core.kb\_writer roles to view the **Generate article** option on the employee relations cases.
-   You must have the required role for the knowledge base that you selected in the AI Admin Hub configuration.

**Note:** For Core UI users, in the **AI search indexed sources**, you must set the **Active** state to **true** for the HR Case \(source: HR Case sn\_hr\_core\_case\) table. The required roles to make this change are the **HR Admin** and **Agent** roles.

## About this task

You can use the KB generation skill in either Core UI or Agent Workspace. The fields that are used as inputs for generating knowledge articles are the Short description, description, close notes, work notes, and additional comments fields. You can also use up to five additional relevant tasks to help you create knowledge articles.

**Note:** The KB generation skill is supported in the ServiceNow Otto panel for the HR Case records \[sn\_hr\_core\_case\] table, but not on its extended table records.

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **HR Agent Workspace**.

2.  Open an HR case that is assigned to you.

3.  Set the HR case to the **Close Complete** state.

4.  Select **Create knowledge**.

    **Note:** You can now select what type of article that you want to create.

5.  If displayed, select a **Knowledge base** and an **Article template**.

    **Note:**

    -   If your admin installed the Knowledge Management Advanced plugin \[com.snc.knowledge\_advanced.installer\] and enabled at least one article template, a modal is displayed so that you can select the knowledge base and article template. Otherwise, the article is created with the standard template.
    -   Disable the Use ServiceNow Otto to draft an article toggle if you don't want the AI to generate a knowledge article.
    -   Additional tasks that are relevant to your case can be used to draft your article. You can select up to five relevant tasks to help you create your article.
6.  Select **Create Article**.

7.  Select **Draft article**.

    **Note:** You see the message "We have found additional relevant tasks-select up to 5 to help in the creation of article." You also see a list of relevant tasks that you can select from.

8.  Select up to five tasks to help you create your article.

9.  If you don't need any other tasks to help you create your article, select **Continue without more tasks**.

10. **Note:** ServiceNow Otto starts to generate a draft of a an knowledge article and you see the "Drafting article" message box. After ServiceNow Otto finishes the draft and loading the article successfully, the article gets a unique ID number.

11. View, edit, or publish the article by using the UI actions on the screen.

    ServiceNow Otto has generated your article from multiple cases.


**Parent Topic:**[Using ServiceNow Otto for HR Service Delivery \(HRSD\) in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HRSD]()

[Generate a chat reply recommendation by using ServiceNow Otto for HRSD]()

[Generate a knowledge article from HR Agent Workspace with ServiceNow Otto for HRSD]()

[Generate an email reply recommendation using ServiceNow Otto for HRSD]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Summarize an ER case using ServiceNow Otto for HRSD]()

[Summarize an ER case interview using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use ServiceNow Otto for HRSD – Galileo Inside to answer HR-related questions]()

[Use the ServiceNow Otto panel in HR Agent Workspace]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()


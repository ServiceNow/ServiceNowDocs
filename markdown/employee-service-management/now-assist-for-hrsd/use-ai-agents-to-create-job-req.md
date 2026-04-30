---
title: Use AI agents to create job requisition
description: Use an AI agent to help hiring managers to create requisitions more efficiently and accurately on the first attempt by providing the necessary guidance through the agentic workflow.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 2
keywords: [AI agents, Agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Use AI agents to create job requisition

Use an AI agent to help hiring managers to create requisitions more efficiently and accurately on the first attempt by providing the necessary guidance through the agentic workflow.

The AI agent is in read-only mode and Active status by default. The following configurations must be done to make the agent discoverable in the Virtual Agent chat window:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agents**.
2.  Select the agent and navigate to the Define Availability section.
3.  In the Select display section, turn on the **Display** option.
4.  In the **Assistants where AI agents are discoverable** field, select the assistant that is set up for Employee Center and is active.

The following should be considered when using the AI agent to create a job requisition:

-   The job requisition creation using AI agent is only supported from the Virtual Agent chat window and not from the Now Assist panel.
-   Two restricted caller access records \(RCAs\) are available in the HR Talent AI Agent Collection plugin in Requested status by default. The status of these RCAs must be updated to Allowed to grant read access to the AI agent, enabling it to fetch data from the Employee Profile &amp; Education and Training tables.
-   A base template is available by default for creating a job description. To create an organization-specific job description template, a template must be created in the Templates table. The sys\_id value in **sn\_talent\_aia.job\_description\_template** must be replaced with the sys\_id of the new template.
-   The sn\_talent\_aia.catalog\_question\_displayValue property specifies the sys\_id of the payload record in the sn\_talent\_aia\_payload table. The payload record contains the catalog questions in a readable format. If the catalog questions must be customized, the default value of this property must be updated to the sys\_id of the new payload record containing the customized questions.

|AI Agent|Role|
|--------|----|
|Job requisition creation AI agent|Gathers essential information from the hiring manager to understand the role and create a requisition, leveraging past requisitions or matching candidate profiles to pre-fill fields. It also asks the hiring manager if they want to consider hiring someone with similar skills to an existing candidate. If so, it fetches and pre-fills relevant details while requesting any missing information. Additionally, it supports job description creation by offering the hiring manager options to reuse an existing description, use a preconfigured template, or draft a new job description.|


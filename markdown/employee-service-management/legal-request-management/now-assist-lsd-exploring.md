---
title: ServiceNow Otto for Legal Service Delivery \(LSD\)
description: ServiceNow Otto for Legal Service Delivery \(LSD\) provides AI-powered summarization for legal requests and matters, and generates actionable answers from knowledge article search results in Employee Center, Legal Counsel Center, and global search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-request-management/now-assist-lsd-exploring.html
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, ServiceNow Otto, generative AI]
breadcrumb: [Explore, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# ServiceNow Otto for Legal Service Delivery \(LSD\)

ServiceNow Otto for Legal Service Delivery \(LSD\) provides AI-powered summarization for legal requests and matters, and generates actionable answers from knowledge article search results in Employee Center, Legal Counsel Center, and global search.

## ServiceNow Otto for Legal Service Delivery \(LSD\) overview

The following AI capabilities are available in ServiceNow Otto for Legal Service Delivery \(LSD\):

-   Summarization capability for the request fulfillers to get a concise summary of a request or matter. This AI summary helps request fulfillers understand the context of the request for faster resolution. The summarization capability is available in Legal Counsel Center and the ServiceNow Otto panel.
-   Q&amp;A Genius Results capability for request fulfillers and legal users to generate concise, actionable answers from knowledge article results in Legal Counsel Center, Employee Center, and global search.
-   Conversational intake experience allows legal users to initiate Conflict of Interest \(COI\) requests through ServiceNow Otto in Virtual Agent, guiding them with context driven follow‑up questions to capture required details.

## Legal Request and Legal Matter summarization

The ServiceNow Otto for Legal Service Delivery \(LSD\) application generates an AI‑powered summary of a legal request or matter. This summary captures key details and the actions taken throughout the lifecycle of the request or matter. Request fulfillers can review the summary to quickly understand context, refresh it as needed, and post it to work notes for reference and collaboration.

The summary is displayed above the activity stream and includes the information from the fields and variablesconfigured as inputs.\[Omitted image "lsd-sum-matter-landing.png"\] Alt text: Legal matter summarization

For more information on the fields and variables that are considered for summarization, see [Skill inputs for ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/now-assist-lsd-skill-inputs.md) and [Configure variables for AI summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/configure-variables-for-now-assist-summarization.md).

For information on activating the Legal Request summarization skill or the Legal Matter summarization skill, see [Configure ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/now-assist-lsd-configuring.md). For information on how to use the skills on Legal Counsel Center, see [Summarize a legal request or matter by using ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/now-assist-lsd-summarize-case.md).

## Q&amp;A Genius Results

Q&amp;A Genius Results uses AI to generate search results from knowledge article results in Employee Center, Legal Counsel Center, and global search.

The answer card shows a topic snippet and an answer snippet that was extracted from a knowledge article, with direct access to the full article for additional context. For more information, see [Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/genius-results-ais.md).

It is enabled when both AI Search and ServiceNow Otto for Legal Service Delivery \(LSD\) are activated.

\[Omitted image "lsd-na-genius-result.png"\] Alt text: Q&amp;A Genius search results in Legal Counsel Center.

## Conversational intake

Conversational Intake guides legal users through submitting Conflict of Interest \(COI\) requests using a chat‑based experience from the ServiceNow Otto in Virtual Agent interface of Employee Center

Instead of completing static forms, legal users can describe the COI details in natural language. Details provided in conversational language are automatically populated into the intake form, reducing the effort required to fill in form fields. The system asks relevant follow‑up questions based on the request type, and validates responses to ensure that all required details are captured accurately.

After submission, the system evaluates the COI request to determine risk. Low‑risk requests are auto‑approved, while medium‑ and high‑risk requests are routed for approval.

For more information on COI application and the risk assessment, see [Legal Conflict of Interest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-conflict-of-interest/legal-conflict-of-interest-landing-page.md) and [Exploring Legal Conflict of Interest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-conflict-of-interest/conflict-of-interest-overview.md).

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

## ServiceNow Otto for Legal Service Delivery \(LSD\) users

<table id="table_ns3_1vj_qcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator\[sn\_lg\_gen\_ai.admin\]

</td><td>

Provides administrative access to ServiceNow Otto for Legal Service Delivery \(LSD\).Installs ServiceNow Otto for Legal Service Delivery \(LSD\) plugin, and activates the required skills.

</td></tr><tr><td>

Request Fulfiller\[sn\_lg\_gen\_ai.request\_fulfiller\]

</td><td>

Provides access for users to use skills for legal requests provided via ServiceNow Otto for Legal Service Delivery \(LSD\).

</td></tr><tr><td>

Matter Fulfiller\[sn\_lg\_gen\_ai.matter\_fulfiller\]

</td><td>

Provides access for users to use skills for legal matters provided via ServiceNow Otto for Legal Service Delivery \(LSD\).

</td></tr></tbody>
</table>## Application information

Activate the ServiceNow Otto for LSD store app \(sn\_lg\_gen\_ai\) to use the summarization skills.

This store app has the following dependencies which will be installed automatically:

-   Legal Request Management \(sn\_lg\_ops\)
-   ServiceNow Otto for Platform \(sn\_genai\_platform\) - Version 7.x and above
-   AI Admin Hub \(sn\_nowassist\_admin\)

You need to install the following applications manually:

-   Legal Counsel Center \(sn\_lg\_cf\_workspace\) - Version 1.5.1 and later
-   Legal Matter Management \(sn\_lg\_matter\) – Required for Legal Matter summarization

For more information, see [Configure ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/now-assist-lsd-configuring.md).

## Supported user interfaces

The ServiceNow Otto for LSD application includes the skills that are listed in the following table.

<table id="table_odd_d2y_wyb"><thead><tr><th>

Skill

</th><th>

Interface

</th></tr></thead><tbody><tr><td>

-   Legal Request summarization
-   Legal Matter summarization

</td><td>

-   Core UI
-   Legal Counsel Center

</td></tr><tr><td>

Q&amp;A Genius Results

</td><td>

-   Employee Center
-   Global search

</td></tr><tr><td>

Conversational intake

</td><td>

ServiceNow Otto in Virtual Agent

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Legal Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/legal-request-management-overview.md)


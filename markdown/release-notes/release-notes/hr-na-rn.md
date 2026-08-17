---
title: ServiceNow Otto for HR Service Delivery \(HRSD\) release notes
description: The ServiceNow ServiceNow Otto for HR Service Delivery \(HRSD\) application enables agents to summarize case information, generate resolution notes, and summarize the chat information for an interaction. Your agents can understand the chat and case context and propose quicker resolutions to your customers. ServiceNow Otto for HR Service Delivery \(HRSD\) was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# ServiceNow Otto for HR Service Delivery \(HRSD\) release notes

The ServiceNow® ServiceNow Otto for HR Service Delivery \(HRSD\) application enables agents to summarize case information, generate resolution notes, and summarize the chat information for an interaction. Your agents can understand the chat and case context and propose quicker resolutions to your customers. ServiceNow Otto for HR Service Delivery \(HRSD\) was enhanced and updated in the Yokohama release.

## ServiceNow Otto for HR Service Delivery \(HRSD\) highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Create a copy of the KB generation skill to create custom templates.
-   View the list of sources that are used to generate an email reply recommendation.
-   Select citations to view the source articles and industry research from Galileo AI Assistant for HR.
-   Leverage an AI agent to generate a step-wise fulfillment plan for an HR case from both Core UI and Agent Workspace for HR Case Management.
-   Make career conversations easy to create and track using the growth conversations agentic workflow.

Yokohama Patch 3

-   Automate the resolution of routine employee inquiries by using the Resolve noncritical HR cases agentic workflow.
-   Receive research-backed responses to HR management queries that are sourced from both internal knowledge bases and The Josh Bersin content library.
-   Use the new Growth &amp; Performance AI agents to streamline your employee growth discussions in Career Conversations.

Yokohama Patch 1: Improve agent productivity by managing long-running cases with the Triage cases AI agent.

Yokohama Early Availability

-   Use the new Virtual Agent topics to place employee requests in the Human Capital Management \(HCM\) system.
-   Use Knowledge Graph to create personalized knowledge models in the form of Knowledge Graph schemas.
-   Create Journey Accelerator plans by using ServiceNow Otto for HRSD in Journey designer.

See  for more information.

**Important:** ServiceNow Otto for HRSD is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

Yokohama Patch 6

-   **Resolve HR cases agentic workflow**

    Generate a step-wise fulfillment plan for an HR case by selecting the **Generate Plan** button on the HR Case. HR agents can add prompts to further refine the AI generated fulfillment plan before the plan is published to the work notes of the case.


-   **Growth Conversations agentic workflow**

    Use the new growth conversations workflow to streamline your employee growth discussions in Career Conversations.


-   **New third-party AI model provider options available for all Now Assist applications**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   ****

    Create a copy of the KB generation skill to create custom templates that are based on your organization's requirements. When a skill copy is activated, the main skill is automatically deactivated.


-   ****

    View the list of KB articles, related records, and current records that are used to generate email reply recommendations.

-   ****

    Simplify employee onboarding with AI agents that gather inputs, structure tasks, enable manager review, and deliver personalized onboarding plans.


Yokohama Patch 3

-   ****

    Use the Resolve noncritical HR cases agentic workflow for faster mean time to repair \(MTTR\) cases, automate the resolution of routine employee inquiries, and reduce the costs for HR operations organizers.

    |Agentic workflow|Description|
    |----------------|-----------|
    |Resolve noncritical HR cases|AI agents detect criticality and retrieve relevant knowledge-based responses to automate the resolution of employee queries.|

-   **Access knowledge from internal and external content sources**

    Find reliable answers to HR management queries from multiple data sources, including the research and articles from The Josh Bersin Company, with attribution to each source.

-   **Override sensitivity detection false positives**

    Proceed with the interaction when the virtual agent incorrectly identifies a phrase as containing sensitive information.

-   **Create a growth conversation with the help of an agent in Now Assist**

    As a manager, use the growth conversations preparation AI agent to schedule and prepare for employee growth discussions. The agent provides a clear summary of employee activity and career journey, with data-driven talking points to make conversations more focused and impactful.

    **Note:** This feature is available when you have both ServiceNow Otto for HR Service Delivery \(HRSD\), which will install Now Assist for Talent and HR Talent AI Agent Collection


Yokohama Patch 1

-   ****

    Use the Resolve policy use case for faster mean time to repair \(MTTR\) cases that require validation that is based on the policies that are built for tuition reimbursement.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Resolve policy for tuition reimbursement|AI agents resolve tuition reimbursement requests by connecting to various parties \(for example, the manager for approval\) and resolving the case, while keeping the human agent in the loop.|


Yokohama Early Availability

-   ****

    Use the  Virtual Agent topics to place employee requests in the HCM system. Examples of requests are when an employee requests time off or updates their personal details.

-   ****

    Create and manage personalized knowledge models as Knowledge Graph schemas that are represented as nodes, edges, and their properties. Virtual Agent uses the assigned Knowledge Graph schema to resolve employee requests and queries.

-   ****

    Create Journey Accelerator plans by entering prompts to Virtual Agent without having to manually create lists and forms.


## Changed in this release

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **Flow name**

    The Resolve noncritical HR cases flow has been renamed to Resolve HR cases flow.


## Activation information

Install ServiceNow Otto for HRSD by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   ****

    Use the AI Admin Hub console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   ****

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   ****

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   ****

    The Agent Workspace for HR Case Management application enables you to interact with employees, respond to inquiries, and resolve issues quickly.

-   ****

    The Journey designer application enables managers and employees to create and track journeys. Journeys include transition plans, such as promotions, offboarding, onboarding, and role changes for employees.


**Parent Topic:**[HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/hr-service-delivery-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)


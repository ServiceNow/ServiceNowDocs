---
title: Now Assist for IT Service Management \(ITSM\) release notes
description: The ServiceNow Now Assist for IT Service Management \(ITSM\) application brings generative AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
keywords: [Now Assist, generative AI]
---

# Now Assist for IT Service Management \(ITSM\) release notes

The ServiceNow® Now Assist for IT Service Management \(ITSM\) application brings generative AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Xanadu release.

## Now Assist for IT Service Management \(ITSM\) highlights for the Xanadu release

**Xanadu Patch 9**

-   Identify the category, subcategory, and configuration item for a given incident automatically using a team of AI agents in the Triage and categorize ITSM incidents agentic workflow.
-   Get recommendations to resolve incidents by using a team of AI agents for catalog, knowledge, and past incidents in the Investigate and resolve ITSM incidents agentic workflow.
-   Manage Microsoft 365 group members using AI agents in the Manage Microsoft 365 group members agentic workflow.
-   Generate the **Risk and impact analysis** and the **Justification** fields using the AI agents in the Generate change request plans agentic workflow.

[Xanadu Patch 7](../quality/xanadu-patch-7.md): Scale your workflows, enhance productivity, and complete work autonomously using IT Service Management AI agent collection.

[Xanadu Patch 3](../quality/xanadu-patch-3.md)

-   Provide change managers with an explanation of the risk rating in a change request by using the Now Assist icon .![Now assist icon](../../common/image/icon-ai-sparkle.png)
-   Enable agents to ask questions that are related to an incident in the Now Assist panel.
-   Enable agents to generate resolution notes for an incident on demand by using the Now Assist context menu.
-   Provide requesters with proactive actionable notifications as part of ITSM Virtual Agent pre-built large language model \(LLM\) topic conversations.

[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   Enable agents to make a more informed decision quickly and efficiently when they’re approving a change by using change request summarization.
-   Enable agents to reply to common questions asked in chats by using the Now Assist icon ![Now assist icon.](../../common/image/icon-ai-sparkle.png) in chat reply recommendations.
-   Enable agents to get a better understanding of the chat and incident context by using the Sidebar discussion summarization when they’re proposing resolutions to the requesters.

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for ITSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

**Xanadu Patch 9**

-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Triage and categorize ITSM incidents|Identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.|
    |Investigate and resolve ITSM incidents|Get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.|
    |Manage Microsoft 365 group members|Add or remove groups and email distribution lists from the Microsoft 365 group.|

-   **[IT Service Management AI agent collection Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the following additional AI agents to handle change requests.

    |AI agent|Description|
    |--------|-----------|
    |Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
    |Change justification proposal AI agent|Proposes justification for a change request.|

-   **[Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-mim-email-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Draft a communication for a major incident using an email template. You can fill in the template field values with an AI-generated response.

-   **[Generate comments and work notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable your agents to generate comments and work notes quickly and add them to incidents using the Now Assist panel.

-   **[Incident sentiment and sentiment trend](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Make informed decisions on incidents by considering the requester's sentiments and the reasoning behind them.

-   **[Suggested steps generation in Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Automatically generate suggested steps to resolve an incident by analyzing the solutions from clusters of similar resolved incidents.

-   **[Summarizing attachments in the Incident summarization skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Summarize, analyze, and extract data from attachments that are of type PNG or JPEG using Document Intelligence in the Incident summarization skill.

-   **[Using self service to deflect incidents in a ServiceNow portal by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Refine the explanation to a change risk by shortening or lengthening a response by using Now Assist for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from Now Assist for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

<table id="table_gjc_gkw_g2c"><thead><tr><th>

AI agent use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate post incident reviews

</td><td>

Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.**Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Generate change request plans

</td><td>

Enhance IT productivity and help decrease the time to schedule change and manage change risk using AI agents. These AI agents can look up similar changes, generate implementation, back out, and test plans to manage change effectively.

</td></tr><tr><td>

Categorize incidents

</td><td>

Autonomously recommend incident categorization using AI agents. The AI agent assigns a category, subcategory, and a configuration item \(CI\) to incidents based on the incident description. The assigned CI is also based on callers associated with that item.

</td></tr><tr><td>

Notify users with Twilio

</td><td>

Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.**Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Risk rating explanation for a change request](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your change managers with a better understanding of the risk rating of a change request, including the potential impacts and risks, by generating the risk explanation by using the Now Assist icon. The risk rating explanation can be generated on the change request form and in the Now Assist panel.

-   **[Ask questions about an incident by using the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable your agents to quickly obtain common incident information conversationally within the incident record by asking questions in the Now Assist panel. Topics include the caller's assets, caller's recent incidents, on-call experts, and similar resolved incidents.

-   **[Enhanced incident resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=resolve-incident-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your agents with enhanced resolution notes information in the incident summary, including the root cause and steps taken to resolve the issue, by using the Now Assist context menu.

-   **[Proactive actionable ITSM Virtual Agent notifications](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your agents with proactive actionable notifications as part of ITSM Virtual Agent pre-built Large Language Model \(LLM\) topic conversations that are designed to help your users complete common IT-related tasks.

-   **[Change request summarization enhancements](https://www.servicenow.com/docs/access?context=summarize-change-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your change managers with an improved change request summary including additional details, such as the affected configuration items \(CIs\) and impacted services.

-   **[Incident summarization enhancements](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your agents with an improved incident summary by including additional details, such as the service level agreements \(SLAs\), affected CIs and impacted services, and child incidents.


-   **[Summarize a change request](https://www.servicenow.com/docs/access?context=summarize-change-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your change managers with a better understanding of the content, intent, and impact of a change request by viewing the change summarization on the change request form and in the Now Assist panel.

-   **[Generating a knowledge article from similar incidents](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable your agents to generate a comprehensive knowledge article by leveraging information from a similar set of incidents.

-   **[Generating chat reply recommendations](https://www.servicenow.com/docs/access?context=now-assist-itsm-chat-recommendation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Provide your agents with quick answers to common questions that are asked in chats by using the Now Assist icon ![Now assist icon.](../../common/image/icon-ai-sparkle.png) in chat reply recommendations.

-   **[Summarizing a Sidebar discussion](https://www.servicenow.com/docs/access?context=now-assist-itsm-sidebar-discussion&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enable your agents to summarize Sidebar chats and post summaries into the work notes of incidents, changes, requests, problems, and knowledge base tasks \(any record type where Sidebar discussions are enabled\) by using Sidebar discussion summarization.


## UI changes

-   **[Terminology change](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   The term use case is replaced with the term agentic workflow. For example, the Notify users with Twilio use case is now referred to as the Notify users with Twilio agentic workflow.
    -   The naming of the AI agents has changed. For example, Twilio SMS texter has been renamed to Twilio SMS texter AI agent.
-   **[New look and feel for the display of incident and change request summarizations](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Get the summary of an incident or a change request by using the new and more intuitive summarization user interface. The new interface is available in Service Operations Workspace and in the Core UI.


## Changed in this release

**Xanadu Patch 9**

-   **[System property to display knowledge article templates](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Display Knowledge article templates that you can use to create articles by using a system property. In earlier releases, the templates were displayed by default.

-   **[IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.

    The following AI agents have been added to the workflow:

    -   Link major incident AI agent
    -   Link incident to problem AI agent
    The Incident categorize AI agent has been renamed to Categorize incident AI agent.

-   **[Xanadu Patch 3](../quality/xanadu-patch-3.md) [Resolution notes generation skill enhancements \(for upgrade customers\)](https://www.servicenow.com/docs/access?context=configure-now-assist-for-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Enhance your existing incident resolution notes generation skill to show the root cause and resolution steps taken. Enable this enhancement by using the toggle switch on the Configure response screen in the Now Assist Admin console.

    **Note:** This option is available only when the incident resolution notes generation skill has been activated prior to upgrading.


## Activation information

Install Now Assist for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

-   **Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


## Additional requirements

The Now Assist for ITSM application requires an IT Service Management Pro Plus or Enterprise Plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)


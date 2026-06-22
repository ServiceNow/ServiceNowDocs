---
title: Combined Now Assist for IT Service Management \(ITSM\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Now Assist for IT Service Management \(ITSM\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-nowassistforitservicemanagementitsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 36
breadcrumb: [Products combined by family]
---

# Combined Now Assist for IT Service Management \(ITSM\) release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Now Assist for IT Service Management \(ITSM\) from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist for IT Service Management \(ITSM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist for IT Service Management \(ITSM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

</td></tr><tr><td>

Zurich

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

 The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US).

 Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.

</td></tr><tr><td>

Australia

</td><td>

To use the Knowledge Article Advanced Editor page in the generate a knowledge article skill, you must activate the knowledge content recommendation skill. Follow these steps to activate the skill.

1.  Go to **Admin** &gt; **Now Assist admin**.
2.  Select **Now Assist Skills**.
3.  Select **Platform**.
4.  Select **Knowledge**.
5.  Make sure the knowledge content recommendation skill is active.

 The incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] incident assist skill, with enhancements. When you upgrade to [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US), if you have the \[DEPRECATED\] incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US).

 Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Now Assist for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=yokohama&ft:locale=en-US)**

Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&family=yokohama&ft:locale=en-US)**

The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&family=yokohama&ft:locale=en-US)**

You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&family=yokohama&ft:locale=en-US)**

You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&family=yokohama&ft:locale=en-US)**

For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=yokohama&ft:locale=en-US)**

For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&family=yokohama&ft:locale=en-US)**

For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=yokohama&ft:locale=en-US)**

When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&family=yokohama&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&family=yokohama&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&family=yokohama&ft:locale=en-US)**

Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&family=yokohama&ft:locale=en-US)**

Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&family=yokohama&ft:locale=en-US)**

Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&family=yokohama&ft:locale=en-US)**

Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&family=yokohama&ft:locale=en-US)**

Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[Diagnose and resolve issues on DEX monitored devices](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&family=yokohama&ft:locale=en-US)**

Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&family=yokohama&ft:locale=en-US)**

Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=yokohama&ft:locale=en-US)**

Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=yokohama&ft:locale=en-US)**

Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&family=yokohama&ft:locale=en-US)**

When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&family=yokohama&ft:locale=en-US)**

When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&family=yokohama&ft:locale=en-US)**

To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Editing prompts using the Now Assist skill kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&family=yokohama&ft:locale=en-US)**

As an admin, you can clone the following skills, then access the skill in the Now Assist skill kit, and update the prompts:

    -   Resolution notes generation skill
    -   Knowledge article generation skill
    -   Incident summarization skill
-   **[Prompt inputs for Major incident email content recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&family=yokohama&ft:locale=en-US)**

Use related tables and fields as prompt inputs to generate a Major incident email content recommendation.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&family=yokohama&ft:locale=en-US)**

Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Triage and categorize ITSM incidents|Identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.|
    |Investigate and resolve ITSM incidents|Get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.|
    |Manage Microsoft 365 group members|Add or remove groups and email distribution lists from the Microsoft 365 group.|

-   **[Generate change request plans](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&family=yokohama&ft:locale=en-US)**

Use the following additional AI agents to handle change requests.

    |AI agent|Description|
    |--------|-----------|
    |Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
    |Change justification proposal AI agent|Proposes justification for a change request.|

-   **[Generate a Major Incident email recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-mim-email-recommendation&family=yokohama&ft:locale=en-US)**

Draft a communication for a major incident using an email template. You can fill in the template field values with an AI-generated response.

-   **[Generate comments and work notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&family=yokohama&ft:locale=en-US)**

Enable your agents to generate comments and work notes quickly and add them to incidents using the Now Assist panel.

-   **[Incident sentiment and sentiment trend](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&family=yokohama&ft:locale=en-US)**

Make informed decisions on incidents by considering the requester's sentiments and the reasoning behind them.

-   **[Generate suggested steps](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&family=yokohama&ft:locale=en-US)**

Automatically generate suggested steps to resolve an incident by analyzing the solutions from clusters of similar resolved incidents.

-   **[Summarizing attachments in the Incident summarization skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&family=yokohama&ft:locale=en-US)**

Summarize, analyze, and extract data from attachments that are of type PNG or JPEG using Document Intelligence in the Incident summarization skill.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&family=yokohama&ft:locale=en-US)**

Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

<table><thead><tr><th>

AI agent use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate post incident reviews

</td><td>

Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.**Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&family=yokohama&ft:locale=en-US).

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

Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.**Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Using self service to deflect incidents in a ServiceNow portal by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&family=yokohama&ft:locale=en-US)**

Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=yokohama&ft:locale=en-US)**

Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&family=yokohama&ft:locale=en-US)**

Refine the explanation to a change risk by shortening or lengthening a response by using Now Assist for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&family=yokohama&ft:locale=en-US)**

Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&family=yokohama&ft:locale=en-US)**

Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from Now Assist for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&family=yokohama&ft:locale=en-US)**

Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Insights and Opportunities for Incident dashboard](https://www.servicenow.com/docs/access?context=insights-opportunities-incident-dashboard&family=zurich&ft:locale=en-US)**

Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns, along with insights into SLA performance, sentiment, channel adoption, and geographic distribution using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.


-   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=zurich&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Password reset voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=zurich&ft:locale=en-US)**

Use the Password reset with voice AI agent to reset your password by receiving instructions from a knowledge article via email, a reset link via SMS, or having the reset URL read out by voice.


-   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=zurich&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Incident assist](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&family=zurich&ft:locale=en-US)**

Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US)**

The features in the \[DEPRECATED\] Incident assist skill is available in the Incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Configure summaries for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&family=zurich&ft:locale=en-US)**

As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&family=zurich&ft:locale=en-US)**

View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.


-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=zurich&ft:locale=en-US)**

Use the demo Submit account unlock catalog with the voice AI agent to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=zurich&ft:locale=en-US)**

Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&family=zurich&ft:locale=en-US)**

Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&family=zurich&ft:locale=en-US)**

Automatically generate a response in record activity streams using the activity response generation skills for requests and requested items.

-   **[Knowledge Article Advanced Editor page](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&family=zurich&ft:locale=en-US)**

Use the new Knowledge Article Advanced Editor page to create or edit Knowledge articles using open prompts.

-   **[Diagnose and resolve issues on DEX monitored devices](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&family=zurich&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&family=zurich&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&family=zurich&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=zurich&ft:locale=en-US)**

Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&family=zurich&ft:locale=en-US)**

The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&family=zurich&ft:locale=en-US)**

You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&family=zurich&ft:locale=en-US)**

You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Creating a knowledge article in any incident state](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&family=zurich&ft:locale=en-US)**

Create knowledge articles from any incident state by configuring a system property for the required states.

-   **[Edit a knowledge article when one article is attached to an incident](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&family=zurich&ft:locale=en-US)**

You can edit a knowledge article if your administrator has enabled the system property to display the **Edit knowledge** button and if you have only one article attached to the incident.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&family=zurich&ft:locale=en-US)**

For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=zurich&ft:locale=en-US)**

For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&family=zurich&ft:locale=en-US)**

For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=zurich&ft:locale=en-US)**

When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&family=zurich&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&family=zurich&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Selecting the desired knowledge base and template for creating knowledge articles using the new interface](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&family=zurich&ft:locale=en-US)**

With this new interface, you can select the desired knowledge base and the template to create the article in Service Operations Workspace or Core UI.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&family=zurich&ft:locale=en-US)**

Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&family=zurich&ft:locale=en-US)**

Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&family=zurich&ft:locale=en-US)**

Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&family=zurich&ft:locale=en-US)**

Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&family=zurich&ft:locale=en-US)**

Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[Diagnose and resolve issues on DEX monitored devices](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&family=zurich&ft:locale=en-US)**

Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&family=zurich&ft:locale=en-US)**

Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=zurich&ft:locale=en-US)**

Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Wrap-up and resolve incident agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-wrap-up-resolve-incident-aw&family=zurich&ft:locale=en-US)**

Generate resolution notes including root cause and resolution steps to resolve an incident, create or attach Knowledge Base \(KB\) articles, update duplicate incident information to the incident record. Attach Known Error \(KE\) articles when the resolution code is a known error. The agentic workflow has the following AI Agents:

    -   Incident resolution details AI agent
    -   Incident knowledge article AI agent
    -   Incident known error article AI agent
-   **[Assess conflicts for a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-conflicts-workflow&family=zurich&ft:locale=en-US)**

Autonomously identify conflict types and summarize the impacted schedules, CIs and services related to the change request using the Change conflict assessor AI agent.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=zurich&ft:locale=en-US)**

Assess the quality of a change request and generate suggestions to improve the quality as needed using the Change quality assessor AI agent.

-   **[Explain SLA](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-explain-sla-workflow&family=zurich&ft:locale=en-US)**

View the detailed breakdown of the assignment and ownership relevant to the SLA for an incident, problem, case, or change request using the Explain SLA AI agent.

-   **[Schedule a change agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-schedule-change-agentic-workflow&family=zurich&ft:locale=en-US)**

Find and schedule the optimum slots for change requests using the Schedule Change Request AI agent.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=zurich&ft:locale=en-US)**

Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&family=zurich&ft:locale=en-US)**

When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&family=zurich&ft:locale=en-US)**

When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&family=zurich&ft:locale=en-US)**

To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.


</td></tr><tr><td>

Australia

</td><td>

-   **[Insights and Opportunities for Incident dashboard](https://www.servicenow.com/docs/access?context=insights-opportunities-incident-dashboard&family=australia&ft:locale=en-US)**

Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns, along with insights into SLA performance, sentiment, channel adoption, and geographic distribution using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.


-   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=australia&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Password reset voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

Use the Password reset with voice AI agent to reset your password by receiving instructions from a knowledge article via email, a reset link via SMS, or having the reset URL read out by voice.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=australia&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Incident assist](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&family=australia&ft:locale=en-US)**

Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US)**

The features in the \[DEPRECATED\] incident assist skill are available in the incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

Use the Submit account unlock catalog with the voice AI agent, which is a primer, to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[Knowledge Article Advanced Editor page](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&family=australia&ft:locale=en-US)**

Use the new Knowledge Article Advanced Editor page to create or edit Knowledge articles using open prompts.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&family=australia&ft:locale=en-US)**

Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Getting summary of an incident in the Details tab](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&family=australia&ft:locale=en-US)**

Resolve incidents faster by getting the incident summary in the **Details** tab of the incident.

-   **[Configure summaries and responses for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&family=australia&ft:locale=en-US)**

As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
    -   Request activity response generation
    -   Requested item activity response generation
    -   Catalog task activity response generation
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-skill&family=australia&ft:locale=en-US)**

View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&family=australia&ft:locale=en-US)**

Generate a response in record activity streams of requests, requested items, and catalog tasks.

-   **[Diagnose and resolve issues on DEX monitored devices](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&family=australia&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the Digital End-User Experience \(DEX\) issue diagnosis and resolution agentic workflow, which integrates Zoom- specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&family=australia&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&family=australia&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Now Assist for IT Service Management \(ITSM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=yokohama&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&family=yokohama&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization
-   **Yokohama Patch 6 [Removing the prompt headers from the Customize prompt screen](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&family=yokohama&ft:locale=en-US)**

The prompt headers have been removed from the Customize prompt screen in the Incident summarization and Change summarization skill to support third-party Large Language Models \(LLMs\).

-   **Yokohama Early Availability[System property to display knowledge article templates](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&family=yokohama&ft:locale=en-US)**

Display Knowledge article templates that you can use to create articles by using a system property. In earlier releases, the templates were displayed by default.

-   **Yokohama Patch 3 [Triage and categorize ITSM incidents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&family=yokohama&ft:locale=en-US)**

The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.

The following AI agents have been added to the workflow:

    -   Link major incident AI agent
    -   Link incident to problem AI agent
The Incident categorize AI agent has been renamed to Categorize incident AI agent.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US)**

The Incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=zurich&ft:locale=en-US)**

The voice AI demo agents have been renamed as primers.

-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=zurich&ft:locale=en-US)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&family=zurich&ft:locale=en-US)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&family=zurich&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&family=zurich&ft:locale=en-US)**

The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To Incident|\(DEMO\) Add Comment To Incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close Incident|\(DEMO\) Close Incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark Incident Unresolved|\(DEMO\) Mark Incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve Incident|\(DEMO\) Resolve Incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**



-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&family=zurich&ft:locale=en-US)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.


-   ****
-   ****
-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&family=zurich&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization

</td></tr><tr><td>

Australia

</td><td>

-   ****
-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US)**

The incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

The voice AI demo agents have been renamed as primers.

-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&family=australia&ft:locale=en-US)**

For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=australia&ft:locale=en-US)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&family=australia&ft:locale=en-US)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&family=australia&ft:locale=en-US)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.

-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&family=australia&ft:locale=en-US)**

The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To incident|\(DEMO\) Add Comment To incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close incident|\(DEMO\) Close incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark incident Unresolved|\(DEMO\) Mark incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve incident|\(DEMO\) Resolve incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Now Assist for IT Service Management \(ITSM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Now Assist for IT Service Management \(ITSM\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Zurich

</td><td>

-   Starting with the [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US) release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&family=zurich&ft:locale=en-US). To transition to LEAP, you must install the LEAP \(sn\_itom\_leap\) plugin. For information on the Suggested steps skill, see [Generate suggested steps](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&family=zurich&ft:locale=en-US) and [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).
-   Starting with the [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US) release, the [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US) is deprecated, moved to the **Archived** folder and is no longer available for use.
-   The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Now Assist for ITSM by requesting it from the ServiceNow Store. 

 -   **Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&family=yokohama&ft:locale=en-US).

-   **Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

Install Now Assist for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Now Assist for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Now Assist for ITSM application requires an IT Service Management Pro Plus or Enterprise Plus license.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist for IT Service Management \(ITSM\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit.
-   Use the Now Assist context menu \(NACM\) to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

 Yokohama Patch 3

-   Identify the category, subcategory, and configuration item for a given incident automatically using a team of AI agents in the Triage and categorize ITSM incidents agentic workflow.
-   Get recommendations to resolve incidents by using a team of AI agents for catalog, knowledge, and past incidents in the Investigate and resolve ITSM incidents agentic workflow.
-   Manage Microsoft 365 group members using AI agents in the Manage Microsoft 365 group members agentic workflow.
-   Generate the **Risk and impact analysis** and the **Justification** fields using the AI agents in the Generate change request plans agentic workflow.

 Yokohama Patch 1: Scale your workflows, enhance productivity, and complete work autonomously using the IT Service Management AI agent collection.

 Yokohama Early Availability

-   Manage change risk explanations effectively by copying an existing change risk explanation skill and configuring it for your business needs.
-   Deflect IT issues in the ServiceNow portal with AI-powered solutions.
-   Automatically generate an email as a recommendation to help agents save time and learn efficient ways to respond to requesters.
-   View a summary of incidents and change requests in an intuitive summarization interface.
-   Track the status of common IT-related tasks by using the Now Assist application.

 See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

-   Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.
-   Use the Password reset with voice AI agent to reset your password.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Answer incident-related questions with context-aware agents using the Incident assist agentic workflow.
-   Generate summaries for Request Management records.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate automatic responses for requests and requested items.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit \(NASK\).
-   Use the Now Assist context menu to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

[Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use the Assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, identify affected CIs, and view the list of impacted services.
-   Use the Schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
-   Use the Explain SLA agentic workflow to understand the breakdown of task assignment and ownership for the SLA relevant to a specific incident, problem, case, or change request. Gain insight into the potential causes of a breach or delays.
-   Use the Assess quality of a Change Request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
-   Use the Wrap-up and resolve incident agentic workflow to resolve incidents, create, or attach Knowledge Base \(KB\) articles, update duplicate incident information, and attach Known Error \(KE\) articles to the incident record.

 See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.

[Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.
-   Use the Password reset with voice AI agent to reset your password.

[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Answer incident-related questions with context-aware agents using the incident assist agentic workflow.
-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate summaries and responses for Request Management records.
-   Use the Knowledge Article Advanced Editor page to create and edit articles.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

 See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


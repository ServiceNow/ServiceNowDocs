---
title: Now Assist for IT Service Management \(ITSM\) release notes
description: The ServiceNow Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 15
keywords: [Now Assist, generative AI]
---

# Now Assist for IT Service Management \(ITSM\) release notes

The ServiceNow® Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Yokohama release.

## Now Assist for IT Service Management \(ITSM\) highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

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

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for IT Service Management \(ITSM\) to Yokohama

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

## New in the Yokohama release

-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Editing prompts using the Now Assist skill kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    As an admin, you can clone the following skills, then access the skill in the Now Assist skill kit, and update the prompts:

    -   Resolution notes generation skill
    -   Knowledge article generation skill
    -   Incident summarization skill
-   **[Prompt inputs for Major incident email content recommendation](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use related tables and fields as prompt inputs to generate a Major incident email content recommendation.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Triage and categorize ITSM incidents|Identify the category, subcategory, and configuration item for an incident automatically, and link associated major incidents or known problems.|
    |Investigate and resolve ITSM incidents|Get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.|
    |Manage Microsoft 365 group members|Add or remove groups and email distribution lists from the Microsoft 365 group.|

-   **[IT Service Management AI agent collection Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use the following additional AI agents to handle change requests.

    |AI agent|Description|
    |--------|-----------|
    |Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
    |Change justification proposal AI agent|Proposes justification for a change request.|

-   **[Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-mim-email-recommendation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Draft a communication for a major incident using an email template. You can fill in the template field values with an AI-generated response.

-   **[Generate comments and work notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Enable your agents to generate comments and work notes quickly and add them to incidents using the Now Assist panel.

-   **[Incident sentiment and sentiment trend](https://www.servicenow.com/docs/access?context=now-assist-itsm-skills&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Make informed decisions on incidents by considering the requester's sentiments and the reasoning behind them.

-   **[Suggested steps generation in Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Automatically generate suggested steps to resolve an incident by analyzing the solutions from clusters of similar resolved incidents.

-   **[Summarizing attachments in the Incident summarization skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Summarize, analyze, and extract data from attachments that are of type PNG or JPEG using Document Intelligence in the Incident summarization skill.


-   **[Using IT Service Management AI agent collection](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use the IT Service Management AI agent collection to boost productivity, and autonomously resolve business tasks.

<table id="table_gjc_gkw_g2c"><thead><tr><th>

AI agent use case

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Generate post incident reviews

</td><td>

Enhance IT productivity during major incidents by minimizing the time required to generate post-incident reviews using AI agents. This process helps improve communication and avoid outages​.**Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

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

Send text messages via SMS to recipients manually using AI agents to help improve the time required for subject matter expert response.**Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>
-   **[Using self service to deflect incidents in a ServiceNow portal by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Refine the explanation to a change risk by shortening or lengthening a response by using Now Assist for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from Now Assist for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


## UI changes

-   **[Yokohama Patch 11](../quality/yokohama-patch-11.md)[Changing the password reset topic to an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The Virtual Agent **Password reset** topic has been changed to a Virtual Agent AI agent. The agent guides the users with instructions to reset passwords using KB articles in their self-service portal.

-   **Yokohama Patch 3[Terminology change](https://www.servicenow.com/docs/access?context=now-assist-itsm-ai-agents-use-cases&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**
    -   The term use case is replaced with the term agentic workflow. For example, the Notify users with Twilio use case is now referred to as the Notify users with Twilio agentic workflow.
    -   The naming of the AI agents has changed. For example, Twilio SMS texter has been renamed to Twilio SMS texter AI agent.
-   **__Yokohama Early Availability__ [New look and feel for the display of incident and change request summarizations](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Get the summary of an incident or a change request by using the new and more intuitive summarization user interface. The new interface is available in Service Operations Workspace and in the Core UI.


## Changed in this release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization
-   **Yokohama Patch 6 [Removing the prompt headers from the Customize prompt screen](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The prompt headers have been removed from the Customize prompt screen in the Incident summarization and Change summarization skill to support third-party Large Language Models \(LLMs\).

-   **Yokohama Early Availability[System property to display knowledge article templates](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Display Knowledge article templates that you can use to create articles by using a system property. In earlier releases, the templates were displayed by default.

-   **Yokohama Patch 3 [IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.

    The following AI agents have been added to the workflow:

    -   Link major incident AI agent
    -   Link incident to problem AI agent
    The Incident categorize AI agent has been renamed to Categorize incident AI agent.


## Deprecations

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

## Activation information

Install Now Assist for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

-   **Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).


## Additional requirements

The Now Assist for ITSM application requires an IT Service Management Pro Plus or Enterprise Plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)


---
title: ServiceNow Otto for IT Service Management \(ITSM\) release notes
description: The ServiceNow ServiceNow Otto for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. ServiceNow Otto for IT Service Management \(ITSM\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 22
---

# ServiceNow Otto for IT Service Management \(ITSM\) release notes

The ServiceNow® ServiceNow Otto for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. ServiceNow Otto for IT Service Management \(ITSM\) was enhanced and updated in the Zurich release.

## ServiceNow Otto for IT Service Management \(ITSM\) highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   Automatically classify user queries as an incident that needs resolution or as an item to be requested through the catalog.
-   Retrieve on-call roster information for specific shifts, groups, or time periods using the Who is On Call agentic workflow.

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

-   Resolve issues directly within the Create incident form using in-form deflection in ServiceNow Otto for ITSM.

-   Generate answers and reasoning for change risk assessment questions by using ServiceNow Otto for ITSM. Review, adjust, or accept the suggested answers, or complete the assessment manually.

-   Analyze topic-specific performance and identify improvement areas using enhanced Topics analytics in the ITSM Virtual Agent dashboard.


[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.

[Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)

-   Track which knowledge articles and catalog items support successful virtual agent deflections instead of transferring to human agents using the ITSM Virtual Agent Analytics dashboard.
-   Use the Password reset with voice AI agent to reset your password.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Answer incident-related questions with context-aware agents using the Incident assist agentic workflow.
-   Generate summaries for Request Management records.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate automatic responses for requests and requested items.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit \(NASK\).
-   Use the Now Assist context menu to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use the Assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, identify affected CIs, and view the list of impacted services.
-   Use the Schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
-   Use the Explain SLA agentic workflow to understand the breakdown of task assignment and ownership for the SLA relevant to a specific incident, problem, case, or change request. Gain insight into the potential causes of a breach or delays.
-   Use the Assess quality of a Change Request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
-   Use the Wrap-up and resolve incident agentic workflow to resolve incidents, create, or attach Knowledge Base \(KB\) articles, update duplicate incident information, and attach Known Error \(KE\) articles to the incident record.

See [ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm.md) for more information.

**Important:** ServiceNow Otto for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow Otto for IT Service Management \(ITSM\) to Zurich

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist.md).

Starting with the [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.

## New in the Zurich release

-   **[Automatically classifying user queries as an incident or a request item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-deflection-overview.md)**

    Receive a personalized catalog item recommendation, rather than generic troubleshooting steps, when your description asks for something new, such as a replacement laptop or new headphones. ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as an incident or a request and tailors the response to match.

-   **[Who is on call agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-on-call-usecase.md)**

    Use the Who is On Call agentic workflow to retrieve on-call roster information for specific shifts, groups, or time periods. The agent provides accurate information to conversationally understand who is on-call.


-   **[In-form deflection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-deflection-overview.md)**

    In-form deflection enables end users to find resolutions without creating an incident. When a user describes an issue in the **Short description** field, ServiceNow Otto for IT Service Management \(ITSM\) searches the knowledge base and returns relevant solutions tailored to that specific user's context.

-   **[Generate change risk assessment answers by using ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/generate-change-risk-assessment-answers-now-assist.md)**

    Generate answers and reasoning for each supported question in a change risk assessment, directly from a change request in Core UI or Service Operations Workspace \(SOW\). This Now Assist skill is turned on by default. When you select Generate Answers, Now Assist reviews the change request, related records, and knowledge articles, and then suggests an answer and a reasoning for each supported question. The Reasoning field explains why Now Assist selected each answer, so you can review and adjust the answers before you submit, or complete the assessment manually. The skill supports Likert-scale questions only. In SOW, this skill is available in version 9.2 or later.

-   **[ITSM Virtual Agent topics analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-conversational-dashboard-topics.md)**

    Analyze topic-specific performance and user interaction patterns using the enhanced Topics analytics in the ITSM Virtual Agent dashboard. View detailed per-topic drill-downs showing key performance indicators. Track topic trends and failure rates with sortable columns, and identify areas for improvement.


-   **[Insights and Opportunities for Incident dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/insights-opportunities-incident-dashboard.md)**

    Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns, along with insights into SLA performance, sentiment, channel adoption, and geographic distribution using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.


-   **[ITSM Virtual Agent resources analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-conversational-dashboard-resources.md)**

    Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Password reset voice AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

    Use the Password reset with voice AI agent to reset your password by receiving instructions from a knowledge article via email, a reset link via SMS, or having the reset URL read out by voice.


-   **[ITSM Virtual Agent resources analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-conversational-dashboard-resources.md)**

    Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Incident assist agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist-workflow.md)**

    Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist.md)**

    The features in the \[DEPRECATED\] Incident assist skill is available in the Incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Configure summaries for Request Management records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-request-summarization-skill.md)**

    As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
-   **[Summarize Request Management records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/summarize-request-related-activity-response-generation.md)**

    View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.


-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

    Use the demo Submit account unlock catalog with the voice AI agent to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

    Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[ITSM Conversational analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/using-itsm-conversational-analytics-dashboard.md)**

    Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Generate a response to request activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/summarize-request-related-activity-response-generation.md)**

    Automatically generate a response in record activity streams using the activity response generation skills for requests and requested items.

-   **[Knowledge Article Advanced Editor page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)**

    Use the new Knowledge Article Advanced Editor page to create or edit Knowledge articles using open prompts.

-   **[DEX issue diagnosis and resolution agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-dex-diagnosis-resolution-workflow.md)**

    Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/investigate-and-resolve-zoom-call-issues.md)**

    Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/investigate-and-resolve-boot-time-issues.md)**

    Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

    Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-va-ai-agents.md)**

    The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-record-summ-skill.md)**

    You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-record-summ-skill.md)**

    You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Creating a knowledge article in any incident state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-skill.md)**

    Create knowledge articles from any incident state by configuring a system property for the required states.

-   **[Edit a knowledge article when one article is attached to an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)**

    You can edit a knowledge article if your administrator has enabled the system property to display the **Edit knowledge** button and if you have only one article attached to the incident.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-incident-resolver-workflow.md)**

    For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-catincidents-usecase.md)**

    For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-change-planner-usecase.md)**

    For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-change-risk-skill.md)**

    When a change risk is calculated, ServiceNow Otto for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-gen-resolution-notes-skill.md)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-activity-response-skill.md)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Selecting the desired knowledge base and template for creating knowledge articles using the new interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/Now-Assist-generate-article-SOW-itsm.md)**

    With this new interface, you can select the desired knowledge base and the template to create the article in Service Operations Workspace or Core UI.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/supporting-information-now-assist-itsm.md)**

    Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request.md)**

    Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-create-outages-for-a-change-request.md)**

    Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-create-change-request-workflow.md)**

    Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-create-standard-change-template-proposal.md)**

    Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[DEX issue diagnosis and resolution agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-dex-diagnosis-resolution-workflow.md)**

    Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/dpr-generate-release-notes.md)**

    Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-catincidents-usecase.md)**

    Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Wrap-up and resolve incident agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-wrap-up-resolve-incident-aw.md)**

    Generate resolution notes including root cause and resolution steps to resolve an incident, create or attach Knowledge Base \(KB\) articles, update duplicate incident information to the incident record. Attach Known Error \(KE\) articles when the resolution code is a known error. The agentic workflow has the following AI Agents:

    -   Incident resolution details AI agent
    -   Incident knowledge article AI agent
    -   Incident known error article AI agent
-   **[IT Service Management AI agent collection assess conflicts for a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-assess-conflicts-workflow.md)**

    Autonomously identify conflict types and summarize the impacted schedules, CIs and services related to the change request using the Change conflict assessor AI agent.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-assess-quality-change-request-workflow.md)**

    Assess the quality of a change request and generate suggestions to improve the quality as needed using the Change quality assessor AI agent.

-   **[IT Service Management AI agent collection explain SLA agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-explain-sla-workflow.md)**

    View the detailed breakdown of the assignment and ownership relevant to the SLA for an incident, problem, case, or change request using the Explain SLA AI agent.

-   **[IT Service Management AI agent collection schedule a change agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-schedule-change-agentic-workflow.md)**

    Find and schedule the optimum slots for change requests using the Schedule Change Request AI agent.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-catincidents-usecase.md)**

    Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-twilio-text-usecase.md)**

    When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-O365-groupmembers-workflow.md)**

    When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/request-gen-ai-capabilities-itsm-now-assist-panel.md)**

    To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)[Changing the password reset topic to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-va-ai-agents.md)**

    The Virtual Agent **Password reset** topic has been changed to a Virtual Agent AI agent. The agent guides the users with instructions to reset passwords using KB articles in their self-service portal.


## Changed in this release

-   **Now Assist &gt; ServiceNow Otto announcement**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Customize the change risk assessment answer generator skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-change-risk-assessment-skill.md)**

    Control the data that the change risk assessment answer generator skill uses to suggest answers. Create, modify, or deactivate **AI Risk Data Sources** to change which related records and knowledge articles the skill receives. Six data sources are available out of the box, including related affected CIs, impacted services, impacted business applications, service offerings, active change tasks, and outages. To change which change request fields the skill reads, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-assess-quality-change-request-workflow.md)**
    -   Use the assess quality of a change request agentic workflow to rate a change request and get field improvement suggestions. The change quality assessor AI agent rates the request against an active change policy document, suggesting values only for fields the policy defines. If no policy applies, the agent rates the request against similar closed change requests.
    -   The agent scores the short description, description, implementation plan, backout plan, test plan, risk and impact analysis, and justification. Results are recorded in the **AI Change Quality Scores** table.
    -   Track change quality trends in Platform Analytics on the `ai_change_quality_score` table. A line chart shows the average score by month.
    -   To change how the agent evaluates a field, or to assess a custom field, override the `POLICY_EXTRACTION_KEYS` entries in the `ChangeQualityUtil` script rather than the protected `ChangeQualityUtilSNC` script. This ensures your changes remain after you upgrade. Use the `u_custom_field` entry to assess a custom field, and use the `overall_chg_policy` entry to set policies for the whole change request.

-   **[Renaming the Incident assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist.md)**

    The Incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md)**

    The voice AI demo agents have been renamed as primers.

-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cust-now-assist-itsm-change-risk-skill.md)**

    Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Role masking for change risk explanation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/supporting-information-now-assist-itsm.md)**

    Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


-   **[Skills activated by default in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/using-now-assist-for-itsm.md)**

    For new ServiceNow Otto for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Virtual agent topics available as demo data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-va-prebuilt-topics.md)**

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

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request.md)**

    Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/using-now-assist-for-itsm.md)**

    For new ServiceNow Otto for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization

## Deprecations

-   Starting with the [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md) release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/aiops-leap.md). To transition to LEAP, you must install the LEAP \(sn\_itom\_leap\) plugin. For information on the Suggested steps skill, see [Suggested steps generation in ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/resolution-steps-generation-now-assist-itsm.md) and [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).
-   Starting with the [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md) release, the [Incident assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-incident-assist.md) is deprecated, moved to the **Archived** folder and is no longer available for use.
-   The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

## Activation information

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-service-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


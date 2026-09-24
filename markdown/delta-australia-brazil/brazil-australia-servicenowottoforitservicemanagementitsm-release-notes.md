---
title: Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-servicenowottoforitservicemanagementitsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for IT Service Management \(ITSM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for IT Service Management \(ITSM\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

To use the Knowledge Article Advanced Editor page in the generate a knowledge article skill, you must activate the knowledge content recommendation skill. Follow these steps to activate the skill.

    1.  Go to **Admin** &gt; **Now Assist admin**.
    2.  Select **Now Assist Skills**.
    3.  Select **Platform**.
    4.  Select **Knowledge**.
    5.  Make sure the knowledge content recommendation skill is active.
The incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] incident assist skill, with enhancements. When you upgrade to [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US), if you have the \[DEPRECATED\] incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US).

Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Otto for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Create change request AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-create-change-ai-agent-auto&family=australia&ft:locale=en-US)**

This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.

-   **[Change CI suggestion AI agent \(latest\)](https://www.servicenow.com/docs/access?context=itsm-change-ci-suggestion-ai-agent-auto&family=australia&ft:locale=en-US)**

This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change requestwithout requiring multiple user interactions.

-   **[Change request plans AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-request-plans-ai-agent-auto&family=australia&ft:locale=en-US)**

This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.

-   **[Change template suggestion AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-template-suggestion-ai-agent-auto&family=australia&ft:locale=en-US)**

This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.


 -   **[Automatically classifying user queries as an incident or a request item](https://www.servicenow.com/docs/access?context=now-assist-itsm-deflection-overview&family=australia&ft:locale=en-US)**

Receive a personalized catalog item recommendation, rather than generic troubleshooting steps, when your description asks for something new, such as a replacement laptop or new headphones. ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as an incident or a request and tailors the response to match.

-   **[Who is on call agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-on-call-usecase&family=australia&ft:locale=en-US)**

Use the Who is On Call agentic workflow to retrieve on-call roster information for specific shifts, groups, or time periods. The agent provides accurate information to conversationally understand who is on-call.


 -   **[In-form deflection](https://www.servicenow.com/docs/access?context=now-assist-itsm-deflection-overview&family=australia&ft:locale=en-US)**

In-form deflection enables end users to find resolutions without creating an incident. When a user describes an issue in the **Short description** field, ServiceNow Otto for IT Service Management \(ITSM\) searches the knowledge base and returns relevant solutions tailored to that specific user's context.

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=australia&ft:locale=en-US)**

Generate answers and reasoning for each supported question in a change risk assessment, directly from a change request in Core UI or Service Operations Workspace \(SOW\). This Now Assist skill is turned on by default. When you select Generate Answers, Now Assist reviews the change request, related records, and knowledge articles, and then suggests an answer and a reasoning for each supported question. The Reasoning field explains why Now Assist selected each answer, so you can review and adjust the answers before you submit, or complete the assessment manually. The skill supports Likert-scale questions only. In SOW, this skill is available in version 9.2 or later.

-   **[Topics](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-topics&family=australia&ft:locale=en-US)**

Analyze topic-specific performance and user interaction patterns using the enhanced Topics analytics in the ITSM Virtual Agent dashboard. View detailed per-topic drill-downs showing key performance indicators. Track topic trends and failure rates with sortable columns, and identify areas for improvement.


 -   **[Insights and Opportunities for Incident dashboard](https://www.servicenow.com/docs/access?context=insights-opportunities-incident-dashboard&family=australia&ft:locale=en-US)**

Automatically cluster incidents into trend categories and get AI-generated summaries of incident patterns, along with insights into SLA performance, sentiment, channel adoption, and geographic distribution using the Insights and Opportunities for Incident dashboard in Service Operations Workspace.


 -   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=australia&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Password reset voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

Use the Password reset with voice AI agent to reset your password by receiving instructions from a knowledge article via email, a reset link via SMS, or having the reset URL read out by voice.


 -   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&family=australia&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&family=australia&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

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


</td></tr><tr><td>

Brazil

</td><td>

-   **[Create change request AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-create-change-ai-agent-auto&family=brazil&ft:locale=en-US)**

This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.

-   **[Change CI suggestion AI agent \(latest\)](https://www.servicenow.com/docs/access?context=itsm-change-ci-suggestion-ai-agent-auto&family=brazil&ft:locale=en-US)**

This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change request without requiring multiple user interactions.

-   **[Change request plans AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-request-plans-ai-agent-auto&family=brazil&ft:locale=en-US)**

This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.

-   **[Change template suggestion AI agent \(autonomous\)](https://www.servicenow.com/docs/access?context=itsm-change-template-suggestion-ai-agent-auto&family=brazil&ft:locale=en-US)**

This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Otto for IT Service Management \(ITSM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=australia&ft:locale=en-US)**

The skill now also reads all dynamic schema store type fields on the change request form. These fields are retrieved automatically, so they don't require an **AI Risk Data Sources** record or an entry in the change request fields property. The skill uses the retrieved values when it suggests answers.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=australia&ft:locale=en-US)**

The new autonomous mode is introduced, where the AI agent automatically records the quality rating and the explanation as a work note on the change request. The agent also creates a record in the AI Change Quality Scores table. This record stores the change request, the explanation, the per-field score, the rating, and the numerical score. The agent does not update any fields on change request.


 -   **Now Assist &gt; ServiceNow Otto announcement**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Customize the change risk assessment answer generator skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-assessment-skill&family=australia&ft:locale=en-US)**

Control the data that the change risk assessment answer generator skill uses to suggest answers. Create, modify, or deactivate **AI Risk Data Sources** to change which related records and knowledge articles the skill receives. Six data sources are available out of the box, including related affected CIs, impacted services, impacted business applications, service offerings, active change tasks, and outages. To change which change request fields the skill reads, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=australia&ft:locale=en-US)**
    -   Use the assess quality of a change request agentic workflow to rate a change request and get field improvement suggestions. The change quality assessor AI agent rates the request against an active change policy document, suggesting values only for fields the policy defines. If no policy applies, the agent rates the request against similar closed change requests.
    -   The agent scores the short description, description, implementation plan, backout plan, test plan, risk and impact analysis, and justification. Results are recorded in the **AI Change Quality Scores** table.
    -   Track change quality trends in Platform Analytics on the `ai_change_quality_score` table. A line chart shows the average score by month.
    -   To change how the agent evaluates a field, or to assess a custom field, override the `POLICY_EXTRACTION_KEYS` entries in the `ChangeQualityUtil` script rather than the protected `ChangeQualityUtilSNC` script. This ensures your changes remain after you upgrade. Use the `u_custom_field` entry to assess a custom field, and use the `overall_chg_policy` entry to set policies for the whole change request.

 -   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=australia&ft:locale=en-US)**

Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&family=australia&ft:locale=en-US)**

Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&family=australia&ft:locale=en-US)**

Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


 -   **[Some generative AI skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=australia&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US)**

The incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

The voice AI demo agents have been renamed as primers.

-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&family=australia&ft:locale=en-US)**

For new ServiceNow Otto for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
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


</td></tr><tr><td>

Brazil

</td><td>

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=brazil&ft:locale=en-US)**

The skill now also reads all dynamic schema store type fields on the change request form. These fields are retrieved automatically, so they don't require an **AI Risk Data Sources** record or an entry in the change request fields property. The skill uses the retrieved values when it suggests answers.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=brazil&ft:locale=en-US)**

The new autonomous mode is introduced, where the AI agent automatically records the quality rating and the explanation as a work note on the change request. The agent also creates a record in the AI Change Quality Scores table. This record stores the change request, the explanation, the per-field score, the rating, and the numerical score. The agent does not update any fields on the change request.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow Otto for IT Service Management \(ITSM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow Otto for IT Service Management \(ITSM\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


 -   Starting with the [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US) release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&family=australia&ft:locale=en-US). To transition to LEAP, you must install the LEAP \(sn\_itom\_leap\) plugin. For information on the Suggested steps skill, see [Generate suggested steps](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&family=australia&ft:locale=en-US) and [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).

 -   Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US) release, the [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US) is deprecated, moved to the **Archived** folder and is no longer available for use.

</td></tr><tr><td>

Brazil

</td><td>

-   ****
    -   **[ITSM Virtual Agent NLU topics](https://www.servicenow.com/docs/access?context=using-itsm-va&family=brazil&ft:locale=en-US)**

Starting with the Brazil release, ITSM Virtual Agent pre-built topics is being prepared for future deprecation.

    -   **[ITSM Virtual Agent Lite](https://www.servicenow.com/docs/access?context=itsm-virtual-agent-lite&family=brazil&ft:locale=en-US)**

ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\) is being prepared for future deprecation.

    -   **[Large language models](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=brazil&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** ServiceNow Otto for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


**Important:** ServiceNow Otto for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for IT Service Management \(ITSM\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   Automatically classify user queries as an incident that needs resolution or as an item to be requested through a catalog.
-   Retrieve on-call roster information for specific shifts, groups, or time periods using the Who is On Call agentic workflow.

[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Resolve issues directly within the Create incident form using in-form deflection in ServiceNow Otto for ITSM.

-   Generate answers and reasoning for change risk assessment questions by using ServiceNow Otto for ITSM. Review, adjust, or accept the suggested answers, or complete the assessment manually.

-   Analyze topic-specific performance and identify improvement areas using enhanced Topics analytics in the ITSM Virtual Agent dashboard.


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

 See [ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Accelerate incident resolution by using agentic AI workflows that autonomously triage, categorize, investigate, and resolve ITSM incidents, reducing manual effort for service desk agents.
-   Boost agent productivity with generative AI skills that summarize incidents, chat interactions, and change requests, and automatically generate resolution notes and knowledge articles.
-   Extend AI-driven automation across Change Management, Incident Management, and Digital End-User Experience with purpose-built AI agents and agentic workflows.

 See [ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)


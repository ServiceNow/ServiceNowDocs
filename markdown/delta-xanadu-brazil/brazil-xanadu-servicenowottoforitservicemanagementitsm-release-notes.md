---
title: Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-servicenowottoforitservicemanagementitsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 19
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for IT Service Management \(ITSM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for IT Service Management \(ITSM\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Upgrade information**

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).


</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US).

Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US), the Incident assist skill has been deprecated, moved to the **Archive** section, and is no longer available for use.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Using self service to deflect incidents in a ServiceNow portal by using ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=deflect-incidents-now-assist-itsm&family=yokohama&ft:locale=en-US)**

Designed to reduce the number of incidents to be resolved by deflecting issues with self-service.

-   **[Customizing a Now Assist for IT Service Management \(ITSM\) change risk skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&family=yokohama&ft:locale=en-US)**

Efficiently explain the risk of a change request by adding custom input fields to the following input tables:

    -   Change request
    -   Past similar change request
    -   Incident caused by change
-   **[Refining a change risk explanation response](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&family=yokohama&ft:locale=en-US)**

Refine the explanation to a change risk by shortening or lengthening a response by using ServiceNow Otto for IT Service Management \(ITSM\).

-   **[Risk Assessment as input to calculate a change risk](https://www.servicenow.com/docs/access?context=change-risk-exp-now-assist&family=yokohama&ft:locale=en-US)**

Use risk assessment values as an input to explain the risk of a change request.

-   **[Generating an email response by using ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm-email-recommendation&family=yokohama&ft:locale=en-US)**

Get recommendations for email responses that agents can review and send to users. Agents can also get email template and content edit recommendations from ServiceNow Otto for IT Service Management \(ITSM\).

-   **[Monitoring task status using pre-built LLM topics with Now Assist in ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-customize-itsm-llm-topic&family=yokohama&ft:locale=en-US)**

Copy and customize a ITSM Virtual Agent core ITSM topic template to track the status of a task by using Now Assist in ITSM Virtual Agent.


</td></tr><tr><td>

Zurich

</td><td>

-   **[In-form deflection](https://www.servicenow.com/docs/access?context=now-assist-itsm-deflection-overview&family=zurich&ft:locale=en-US)**

In-form deflection enables end users to find resolutions without creating an incident. When a user describes an issue in the **Short description** field, ServiceNow Otto for IT Service Management \(ITSM\) searches the knowledge base and returns relevant solutions tailored to that specific user's context.

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=zurich&ft:locale=en-US)**

Generate answers and reasoning for each supported question in a change risk assessment, directly from a change request in Core UI or Service Operations Workspace \(SOW\). This Now Assist skill is turned on by default. When you select Generate Answers, Now Assist reviews the change request, related records, and knowledge articles, and then suggests an answer and a reasoning for each supported question. The Reasoning field explains why Now Assist selected each answer, so you can review and adjust the answers before you submit, or complete the assessment manually. The skill supports Likert-scale questions only. In SOW, this skill is available in version 9.2 or later.

-   **[Topics](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-topics&family=zurich&ft:locale=en-US)**

Analyze topic-specific performance and user interaction patterns using the enhanced Topics analytics in the ITSM Virtual Agent dashboard. View detailed per-topic drill-downs showing key performance indicators. Track topic trends and failure rates with sortable columns, and identify areas for improvement.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Yokohama Patch 6 [Removing the prompt headers from the Customize prompt screen](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&family=yokohama&ft:locale=en-US)**

The prompt headers have been removed from the Customize prompt screen in the Incident summarization and Change summarization skill to support third-party Large Language Models \(LLMs\).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Customize the change risk assessment answer generator skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-assessment-skill&family=zurich&ft:locale=en-US)**

Control the data that the change risk assessment answer generator skill uses to suggest answers. Create, modify, or deactivate **AI Risk Data Sources** to change which related records and knowledge articles the skill receives. Six data sources are available out of the box, including related affected CIs, impacted services, impacted business applications, service offerings, active change tasks, and outages. To change which change request fields the skill reads, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=zurich&ft:locale=en-US)**
    -   Use the assess quality of a change request agentic workflow to rate a change request and get field improvement suggestions. The change quality assessor AI agent rates the request against an active change policy document, suggesting values only for fields the policy defines. If no policy applies, the agent rates the request against similar closed change requests.
    -   The agent scores the short description, description, implementation plan, backout plan, test plan, risk and impact analysis, and justification. Results are recorded in the **AI Change Quality Scores** table.
    -   Track change quality trends in Platform Analytics on the `ai_change_quality_score` table. A line chart shows the average score by month.
    -   To change how the agent evaluates a field, or to assess a custom field, override the `POLICY_EXTRACTION_KEYS` entries in the `ChangeQualityUtil` script rather than the protected `ChangeQualityUtilSNC` script. This ensures your changes remain after you upgrade. Use the `u_custom_field` entry to assess a custom field, and use the `overall_chg_policy` entry to set policies for the whole change request.

</td></tr><tr><td>

Australia

</td><td>

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=australia&ft:locale=en-US)**

The skill now also reads all dynamic schema store type fields on the change request form. These fields are retrieved automatically, so they don't require an **AI Risk Data Sources** record or an entry in the change request fields property. The skill uses the retrieved values when it suggests answers.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=australia&ft:locale=en-US)**

The new autonomous mode is introduced, where the AI agent automatically records the quality rating and the explanation as a work note on the change request. The agent also creates a record in the AI Change Quality Scores table. This record stores the change request, the explanation, the per-field score, the rating, and the numerical score. The agent does not update any fields on change request.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Zurich

</td><td>

-   Starting with the [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US) release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&family=zurich&ft:locale=en-US). To transition to LEAP, you must install the LEAP \(sn\_itom\_leap\) plugin. For information on the Suggested steps skill, see [Generate suggested steps](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&family=zurich&ft:locale=en-US) and [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).

</td></tr><tr><td>

Australia

</td><td>

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install ServiceNow Otto for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

    -   **Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Major Incident Management](https://www.servicenow.com/docs/access?context=activate-major-incident-management-plugin&family=yokohama&ft:locale=en-US).

    -   **Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://www.servicenow.com/docs/access?context=twilio-spoke&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Additional requirements**

The ServiceNow Otto for ITSM application requires an IT Service Management Pro Plus or Enterprise Plus license.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

 See [ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   Automatically classify user queries as an incident that needs resolution or as an item to be requested through the catalog.
-   Retrieve on-call roster information for specific shifts, groups, or time periods using the Who is On Call agentic workflow.

 [Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US)

-   Resolve issues directly within the Create incident form using in-form deflection in ServiceNow Otto for ITSM.

-   Generate answers and reasoning for change risk assessment questions by using ServiceNow Otto for ITSM. Review, adjust, or accept the suggested answers, or complete the assessment manually.

-   Analyze topic-specific performance and identify improvement areas using enhanced Topics analytics in the ITSM Virtual Agent dashboard.


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

 See [ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)


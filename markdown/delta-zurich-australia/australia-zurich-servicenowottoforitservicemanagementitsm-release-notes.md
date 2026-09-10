---
title: Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowottoforitservicemanagementitsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for IT Service Management \(ITSM\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow Otto for IT Service Management \(ITSM\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for IT Service Management \(ITSM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for IT Service Management \(ITSM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

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

-   **[Resources](https://www.servicenow.com/docs/access?context=now-assist-itsm-conversational-dashboard-resources&family=australia&ft:locale=en-US)**

Identify which knowledge article or catalog item resources support successful deflections and which ones are unable in preventing the transfer to a live agent using the **Resources** tab in the ITSM Virtual Agent dashboard to gain visibility into the ITSM Virtual Agent usage and effectiveness.

-   **[Password reset voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&family=australia&ft:locale=en-US)**

Use the Password reset with voice AI agent to reset your password by receiving instructions from a knowledge article via email, a reset link via SMS, or having the reset URL read out by voice.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for IT Service Management \(ITSM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Generate change risk assessment answers](https://www.servicenow.com/docs/access?context=generate-change-risk-assessment-answers-now-assist&family=zurich&ft:locale=en-US)**

The skill now also reads all dynamic schema store type fields on the change request form. These fields are retrieved automatically, so they don't require an **AI Risk Data Sources** record or an entry in the change request fields property. The skill uses the retrieved values when it suggests answers.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=zurich&ft:locale=en-US)**

The new autonomous mode is introduced, where the AI agent automatically records the quality rating and the explanation as a work note on the change request. The agent also creates a record in the AI Change Quality Scores table. This record stores the change request, the explanation, the per-field score, the rating, and the numerical score. The agent does not update any fields on the change request.


</td></tr><tr><td>

Australia

</td><td>

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Customize the change risk assessment answer generator skill](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-assessment-skill&family=australia&ft:locale=en-US)**

Control the data that the change risk assessment answer generator skill uses to suggest answers. Create, modify, or deactivate **AI Risk Data Sources** to change which related records and knowledge articles the skill receives. Six data sources are available out of the box, including related affected CIs, impacted services, impacted business applications, service offerings, active change tasks, and outages. To change which change request fields the skill reads, update the `sn_itsm_gen_ai.com.snc.asmt_answer_generator.change_request_fields` system property.

-   **[Assess quality of a change request](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&family=australia&ft:locale=en-US)**
    -   Use the assess quality of a change request agentic workflow to rate a change request and get field improvement suggestions. The change quality assessor AI agent rates the request against an active change policy document, suggesting values only for fields the policy defines. If no policy applies, the agent rates the request against similar closed change requests.
    -   The agent scores the short description, description, implementation plan, backout plan, test plan, risk and impact analysis, and justification. Results are recorded in the **AI Change Quality Scores** table.
    -   Track change quality trends in Platform Analytics on the `ai_change_quality_score` table. A line chart shows the average score by month.
    -   To change how the agent evaluates a field, or to assess a custom field, override the `POLICY_EXTRACTION_KEYS` entries in the `ChangeQualityUtil` script rather than the protected `ChangeQualityUtilSNC` script. This ensures your changes remain after you upgrade. Use the `u_custom_field` entry to assess a custom field, and use the `overall_chg_policy` entry to set policies for the whole change request.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for IT Service Management \(ITSM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow Otto for IT Service Management \(ITSM\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Starting with the [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US) release, the Suggested steps skill is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. This feature is being replaced with [Learning Enhanced Automation Platform \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&family=zurich&ft:locale=en-US). To transition to LEAP, you must install the LEAP \(sn\_itom\_leap\) plugin. For information on the Suggested steps skill, see [Generate suggested steps](https://www.servicenow.com/docs/access?context=resolution-steps-generation-now-assist-itsm&family=zurich&ft:locale=en-US) and [How to get started with LEAP](https://www.servicenow.com/community/itom-articles/leap-learning-enhanced-automation-platform-how-to-get-started/ta-p/3555322).

</td></tr><tr><td>

Australia

</td><td>

-   Starting with the [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US) release, the [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US) is deprecated, moved to the **Archived** folder and is no longer available for use.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for IT Service Management \(ITSM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Otto for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for IT Service Management \(ITSM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


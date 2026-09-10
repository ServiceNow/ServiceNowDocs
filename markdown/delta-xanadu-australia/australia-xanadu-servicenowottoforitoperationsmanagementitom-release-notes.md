---
title: Combined ServiceNow Otto for IT Operations Management \(ITOM\) release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto for IT Operations Management \(ITOM\) from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowottoforitoperationsmanagementitom-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for IT Operations Management \(ITOM\) release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto for IT Operations Management \(ITOM\) from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for IT Operations Management \(ITOM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for IT Operations Management \(ITOM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for IT Operations Management \(ITOM\).

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

-   **[Analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&family=yokohama&ft:locale=en-US)**

Analyze the impact of alerts and identify the possible causes with the Analyze alert impact agentic workflow. The workflow interacts with observability tools, such as Kentik and New Relic, to surface alert details and provide insights.

-   **[Now Assist for IT Operations Management \(ITOM\) Triage and analyze alert agentic workflow](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&family=yokohama&ft:locale=en-US)**

Automatically assign, acknowledge, and summarize the alerts, determine their significance through history analysis, and analyze the related incidents. Initiate multiple parallel processes to triage and analyze the different alerts.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&family=zurich&ft:locale=en-US)**

Automate alert triage, impact analysis, and root cause investigation with an AI-driven workflow that replaces manual operator steps with autonomous decision-making. The workflow processes incoming alerts end-to-end and surfaces consolidated insights through Express List, giving operators immediate visibility into what happened, what's affected, and why.

-   **[Configure the Datadog and Gemini Cloud Assistant observability skills](https://www.servicenow.com/docs/access?context=itom-ai-agent-configuration&family=zurich&ft:locale=en-US)**

Set up the new Datadog and Gemini Cloud Assistant observability skills to get insights from those tools in the manage alerts autonomously agentic workflow. With Datadog and Google Gemini, the workflow now supports five observability tools, including Dynatrace, Kentik, and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[AIOps LEAP skill setup](https://www.servicenow.com/docs/access?context=change-leap-large-languauge-model-llm&family=zurich&ft:locale=en-US)**

Status information for records grouping job run is available when skills are modified with support KB content.

-   **[AIOps LEAP settings page](https://www.servicenow.com/docs/access?context=setup-aiops-leap-properties&family=zurich&ft:locale=en-US)**

The new interface for the AIOps LEAP properties includes default configuration to achieve opportunity savings and reporting.

-   **[Action Insights panel](https://www.servicenow.com/docs/access?context=automation-opportunity-sub-groups&family=zurich&ft:locale=en-US)**

The Action Insights panel on the automation opportunity details page provides suggestion to create sub-groups when there are large volumes of records. This helps optimize opportunities and knowledge gaps for architects.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for IT Operations Management \(ITOM\) features.

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

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&family=yokohama&ft:locale=en-US)**

Four AIOps AI agents have been removed from the analyze alert impact agentic workflow as they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&family=zurich&ft:locale=en-US)**

Four AIOps AI agents have been removed from the analyze alert impact agentic workflow because they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[AIOps LEAP rebranding](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&family=zurich&ft:locale=en-US)**

AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation.

-   **[Service Operations Workspace \(SOW\) Integration](https://www.servicenow.com/docs/access?context=view-and-use-aiops-leap-playbooks-in-sow&family=zurich&ft:locale=en-US)**

Playbooks appear in SOW module.

-   **[Data Range Display](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&family=zurich&ft:locale=en-US)**

The AIOps LEAP landing page shows analyzed data date range for automation teams to be aware of time-ranges of analysis.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for IT Operations Management \(ITOM\) features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow Otto for IT Operations Management \(ITOM\) features or functionality were deprecated.

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

-   Starting with version 2.0.1 of AI Agents for Observability, the sn\_obs\_aia.admin role, previously required to configure AI agents in the Analyze alert impact agentic workflow, has been removed. Users must now have the credential\_admin and connection\_admin roles instead.
-   Starting with version 2.0.1 of AI Agents for Observability, the prompt `How severe is this alert?` no longer appears in the Analyze alert impact agentic workflow.

</td></tr><tr><td>

Zurich

</td><td>

In [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US), the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent and set up the Dynatrace MCP server agent. For configuration details, see [Configure the Dynatrace MCP server agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace-mcp&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for IT Operations Management \(ITOM\).

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

-   **Activation information**

Install AIOps Experience \[sn\_sow\_aiops\] and ServiceNow Otto for ITOM from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for IT Operations Management \(ITOM\) we have noted them here.

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

-   **Additional requirements**

The ServiceNow Otto for ITOM application requires an ITOM Pro Plus or Enterprise Plus license.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for IT Operations Management \(ITOM\) we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for IT Operations Management \(ITOM\), such as specific requirements or compliance levels.

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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for IT Operations Management \(ITOM\) we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for IT Operations Management \(ITOM\) we have noted them here.

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

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for ITOM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Use the Microsoft Azure and Google Cloud AI agents for deeper analysis in the analyze alert impact agentic workflow.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

 Use the ITOM MCP Server with an MCP client application to investigate alerts, review configuration item \(CI\) reliability, assess incident impact, and create service level objectives \(SLOs\).

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   AIOps LEAP added support for new third-party model Claude Sonnet 4.6.
-   Auto-generate service level objectives \(SLOs\) to help teams track service reliability in SRM.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Use the Dynatrace Model Context Protocol \(MCP\) server agent for deeper analysis in the analyze alert impact and manage alerts autonomously agentic workflows.
-   Analyze a Service Observability dashboard to find performance insights.
-   Understand service health by analyzing all available Service Observability dashboards for a service.
-   Expand support for 3P AI Model in AIOps LEAP to include additional model options across Small \(OpenAI GPT-4o mini, Claude Haiku 4.5, Gemini 2.0 Flash\) and Large \(OpenAI GPT-4o, Claude Sonnet 4.5, Gemini 2.0 Pro\) tracks.

[Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Now Assist skills used in the analyze potential impact agentic workflow are turned on by default.
-   Use the new manage alerts autonomously workflow to efficiently manage alerts and minimize resolution times, including an AI agent for triage, impact analysis, and root cause investigation.
-   -   **[\[Placeholder link text to key aiops-leap\]](https://www.servicenow.com/docs/access?context=aiops-leap&family=zurich&ft:locale=en-US)**

Create Knowledge Base articles with embedded command snippets

Guided chat workflow to create and manage Playbook and KBs

Break large groups into targeted sub-groups using generative AI

Generate comprehensive resolution steps from multiple web sources

Regenerate resolutions when new data sources are enabled


[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   View an error analysis by Now Assist in Agent Client Collector.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

[Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Get deeper impact analysis in the analyze alert impact agentic workflow with five new AI agents.
-   Enhance security for Now Assist AI agents with access control lists \(ACLs\).
-   Find all TLS certificates expiring within a determined time and renew them in a single prompt.
-   Use the triage and analyze alert agentic workflow to perform initial triage and analysis in the context of an incident.
-   Review Alert analysis, and relevant information for new mixed alert groups in the Now Assist panel to help investigate alerts more effectively.

 See [ServiceNow Otto for ITOM](https://www.servicenow.com/docs/access?context=now-assist-itom&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)


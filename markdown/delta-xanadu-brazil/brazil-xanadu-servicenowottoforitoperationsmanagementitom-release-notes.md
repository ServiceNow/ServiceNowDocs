---
title: Combined ServiceNow Otto for IT Operations Management \(ITOM\) release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for IT Operations Management \(ITOM\) from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-servicenowottoforitoperationsmanagementitom-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for IT Operations Management \(ITOM\) release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ServiceNow Otto for IT Operations Management \(ITOM\) from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for IT Operations Management \(ITOM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for IT Operations Management \(ITOM\) to Brazil

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
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Otto for IT Operations Management \(ITOM\).

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

-   **[Configure the Dynatrace analysis AI agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace&family=yokohama&ft:locale=en-US)**

Set up the Dynatrace analysis AI agent in the Analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the Analyze alert impact agentic workflow with four new AIOps agents](https://www.servicenow.com/docs/access?context=now-assist-itom-use-aia&family=yokohama&ft:locale=en-US)**

Get a fuller view of alert impact with four new AIOps agents in the Analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Enhance your decision-making process with the Analyze Potential Impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-analyze-potential-impact-workflow&family=yokohama&ft:locale=en-US)**

Assess the potential impact of a change using the Analyze Potential Impact agentic workflow. This workflow provides an analysis of the relevant servers and suggested services that might be impacted by your change request, ensuring you have all the insights needed to make informed decision before a change.

-   **[Add access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[Utilize the Triage and analyze alerts agentic workflow in the context of an incident](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&family=yokohama&ft:locale=en-US)**

Initiate the Triage and analyze alerts agentic workflow from the Now Assist panel in the context of the incident form to perform all the functions of the workflow. This workflow automatically assigns, acknowledges, and summarizes origin alerts, determines their significance through historical analysis, and analyzes related incidents.


</td></tr><tr><td>

Zurich

</td><td>

-   **[View an error analysis by ServiceNow Otto in ACC](https://www.servicenow.com/docs/access?context=agent-errors-now-assist&family=zurich&ft:locale=en-US)**

Starting in version 6.0.0, use Now Assist AI agents to gather information about errors occurring on Agent Client Collector agents. For example, you can verify the underlying cause behind a specific error or error code.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Otto for IT Operations Management \(ITOM\) features.

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

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow Otto for IT Operations Management \(ITOM\) features or functionality were removed.

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

Between your current release family and Brazil, some ServiceNow Otto for IT Operations Management \(ITOM\) features or functionality were deprecated.

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

In [Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US), the Google Gemini Cloud Assist agent is being prepared for future deprecation. To continue receiving Google Cloud insights, use the analyze alert impact agentic workflow which includes the Gemini Cloud Assist A2A Investigation Agent. For configuration instructions, see [\[Placeholder link text to key configure-integration-agents-for-now-assist\]](https://www.servicenow.com/docs/access?context=configure-integration-agents-for-now-assist&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)


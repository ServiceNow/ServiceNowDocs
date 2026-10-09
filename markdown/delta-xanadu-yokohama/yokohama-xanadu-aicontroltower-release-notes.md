---
title: Combined AI Control Tower release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for AI Control Tower from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-aicontroltower-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined AI Control Tower release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for AI Control Tower from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Control Tower release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Control Tower to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

General availability release, no upgrade.


</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for AI Control Tower.

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

-   **[Health tab in AI Control Tower](https://www.servicenow.com/docs/access?context=aict-health-tab&family=yokohama&ft:locale=en-US)**

Monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your AI assets.

-   **[Evaluation tab](https://www.servicenow.com/docs/access?context=ai-evaluation&family=yokohama&ft:locale=en-US)**

Measure and improve the quality of interactions with virtual agents using the Evaluation tab.


 -   **[Explore AI model providers](https://www.servicenow.com/docs/access?context=ai-model-providers&family=yokohama&ft:locale=en-US)**

Enable choice for third party model providers powering ServiceNow® skills and agents.


 -   **[AI Governance](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&family=yokohama&ft:locale=en-US)**
    -   A single pane view of the AI inventory, its state, and its risk and compliance posture.
    -   Lifecycle to manage AI asset onboarding and deployment.
    -   Helps user oversee and manage AI Asset inventory's risk profile with regard to enterprise policies and global regulations, as defined by the user, with a focus on privacy, data governance, and ethical AI.
    -   AI Case management to oversee AI asset-related inquiries and cases, enabling faster response and improved tracking.
    -   Multi-instance management to synchronize AI asset inventory from sub-prod to prod instances to initiate governance early in the build process.
    -   Control settings to block only ''other'' skills in Now Assist AI deployment pending approvals.

 -   **[AI Governance](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&family=yokohama&ft:locale=en-US)**
    -   AI Steward role- Facilitate and coordinate governance activities between innovation, legal, security, risk and compliance teams.
    -   AI Asset inventory- Unified data model on the ServiceNow AI Platform to catalog AI Model, datasets, prompts, and other related artifacts including Now Assist and AI leveraging Generative AI Controller.
    -   AI skills Approvals- Review and approval flows for Now Assist skills and other related assets like AI Models and AI datasets deployed through Now Assist or generative AI Controller.
    -   AI Control Tower Workspace- Intuitive workspace to surface governance tasks, reports, inventory, and insights.

</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing AI Control Tower features.

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


 -   **[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)**

Enhancements to landing page dashboards for AI steward.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some AI Control Tower features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some AI Control Tower features or functionality were deprecated.

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

AI Gateway application is deprecated from the Yokohama release and are no longer supported.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Control Tower.

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

The AI Control Tower application is installed as part of the generative AI Controller.


**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Control Tower we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Control Tower we have noted them here.

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

-   **Browser requirements**

The AI Control Tower application supports all the browsers.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Control Tower, such as specific requirements or compliance levels.

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

-   **Accessibility information**

The AI Control Tower application supports all the platform accessibility features.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Control Tower we have noted them here.

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

-   **Localization information**
    -   **[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)**

The AI Control Tower application isn’t localized


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Control Tower we have noted them here.

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
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&family=yokohama&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&family=yokohama&ft:locale=en-US)- Azure Foundry and Copilot
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&family=yokohama&ft:locale=en-US)
    -   [GCP Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&family=yokohama&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&family=yokohama&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&family=yokohama&ft:locale=en-US)

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Monitor the performance of guardrails enabled through AI Guardian using the Health tab.
-   Measure and improve the quality of interactions with virtual agents using the Evaluation tab.

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   AI Control Tower helps customers manage and oversee performance, risk profile &amp; workforce transformation while also helping to seamlessly embed AI into enterprise strategy.

 -   -   Create an AI steward role.
-   Use the AI Asset inventory to catalog AI-related artifacts.
-   Use the AI skills Approvals to review and approval flows.
-   Create a AI Control Tower Workspace.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)


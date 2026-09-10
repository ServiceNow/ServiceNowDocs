---
title: Combined ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowottoforsecurityincidentresponsesirsir-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) to Australia

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

-   **Upgrade information**

**Note:** The following Now Assist skills, agents, and agentic workflows for ServiceNow Otto for Security Incident Response \(SIR\) are activated by default:

Skills

    -   Security incident summarization
    -   Resolution notes generation
    -   Post incident analysis
    -   Security incident recommended actions
    -   Correlation insights generation
    -   Security incident quality assessment
    -   Natural language condition evaluator
    -   Generate content for shift handover
    -   Quality assessment report NACM
    -   Security incident resolution plan
    -   Security operations metrics analysis
Agentic workflows

    -   Wrap up security incident
    -   Resolve security incident
    -   Generate SIR shift handover report
    -   Analyze security operations metrics
Agents

    -   EDR AI agent
    -   Exchange online integration handling AI agent
    -   Observable analysis AI agent
    -   Security incident activities handling AI agent
    -   Security incident resolution AI agent
    -   Security incident retrieval AI agent
    -   Security incident shift handover AI agent
    -   Security incident wrap up generator AI agent
    -   Security metrics analysis AI agent
For more information, see [AI assets on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)

**Note:** Upgrading the Now Assist plugins activates any designated skills that were previously untouched by the customer.

    -   If you installed the plugins for a skill but never configured it, meaning you never activated it nor adjusted associated roles, any skill on by default is activated on a per skill basis when upgrade.
    -   If you previously toggled a skill from active and then back to inactive, or updated any roles for that skill, that skill remains inactive when upgrading.
    -   You maintain full control over deactivating individual skills at any time after activation.
When you update the ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) application, the dependency applications are automatically updated.

For more information about required applications for ServiceNow Otto for Security Incident Response \(SIR\), see [Supporting information](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&family=zurich&ft:locale=en-US).

The AI Search application must be enabled so that the recommended actions skill works for security incidents with ServiceNow Otto for Security Incident Response \(SIR\). To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search isn’t enabled.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\).

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

-   **[Generate SIR Shift Handover Report](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&family=yokohama&ft:locale=en-US)**

The AI Agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Resolve a security incident](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&family=zurich&ft:locale=en-US)**

Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) features.

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

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The following Now Assist skills for ServiceNow Otto for Security Incident Response \(SIR\) and ServiceNow Otto for Unified Security Exposure Management are activated by default.

    -   Security incident summarization \(SIR\)
    -   Resolution notes generation \(SIR\)
    -   Post incident analysis \(SIR\)
    -   Security incident recommended actions \(SIR\)
    -   Correlation insights generation \(SIR\)
    -   Security incident quality assessment \(SIR\)
The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Resolve a security incident](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&family=zurich&ft:locale=en-US)**

Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\).

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

Install ServiceNow Otto for Security Incident Response \(SIR\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) we have noted them here.

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

Review details on accessibility information for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\), such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) we have noted them here.

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

If there are specific highlight considerations for ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) we have noted them here.

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

[Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.
-   Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills are now turned on by default.
-   Use generative AI to create a quality assessment report of a security incident.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Help analysts to add security incidents details to the Shift Handover report by chatting with AI agents in the Now Assist panel.

 Zurich Early Availability

-   Help your analysts to gain insight into security incident record metrics with an agentic workflow. Chat with AI agents in natural language from the Now Assist panel.
-   Help your analysts to resolve security incidents by chatting with AI agents in the Now Assist panel where the AI agent can assist in providing a resolution plan.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)


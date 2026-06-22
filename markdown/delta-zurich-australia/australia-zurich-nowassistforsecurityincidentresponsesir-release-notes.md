---
title: Combined Now Assist for Security Incident Response \(SIR\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Now Assist for Security Incident Response \(SIR\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-nowassistforsecurityincidentresponsesir-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Now Assist for Security Incident Response \(SIR\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Now Assist for Security Incident Response \(SIR\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist for Security Incident Response \(SIR\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist for Security Incident Response \(SIR\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

**Note:** The following Now Assist skills, agents, and agentic workflows for Now Assist for Security Incident Response are activated by default:

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

 When you update the Now Assist for Security Incident Response \(SIR\) application, the dependency applications are automatically updated.

 For more information about required applications for Now Assist for Security Incident Response, see [Supporting information](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&family=zurich&ft:locale=en-US).

 The AI Search application must be enabled so that the recommended actions skill works for security incidents with Now Assist for Security Incident Response. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search isn’t enabled.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Now Assist for Security Incident Response \(SIR\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Resolve a security incident](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&family=zurich&ft:locale=en-US)**

Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Explore Security incident quality assessment](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&family=zurich&ft:locale=en-US)**

Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.


-   **[Generate SIR Shift Handover Report](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&family=zurich&ft:locale=en-US)**

The AI agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.


-   **[Use agentic workflows](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&family=zurich&ft:locale=en-US)**

The analyze security operations metrics agentic workflow helps security managers to analyze their teams' performance.

    -   Generate metrics for Security Incident Response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) for a date range of your choosing.
    -   Request suggestions for how to improve MTTR, MTTA, and volume based on your metrics.
-   **[Enhancements to correlation insights in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=generating-insights-for-now-assist-for-security&family=zurich&ft:locale=en-US)**

You can generate and view results for correlation insights in the Security Incident Response Workspace.

    -   Correlation insights aren’t limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
    -   You can generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
    -   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
    -   Results are displayed in a modeless dialog that you can size and move.
-   **[Using the security incident resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&family=zurich&ft:locale=en-US)**

Use the security incident resolution agentic workflow to close your security incidents. Analysts can chat with AI agents in natural language to resolve the security incidents. The AI agent analyzes the incident details, existing runbooks, Knowledge articles, and past similar security incidents as inputs, and provides a resolution plan. The AI agent also assists the analysts to resolve the security incident.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Now Assist for Security Incident Response \(SIR\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, some Now Assist for Security Incident Response \(SIR\) features or functionality were removed.

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

Between your current release family and Australia, some Now Assist for Security Incident Response \(SIR\) features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Now Assist for Security Incident Response \(SIR\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Now Assist for Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist for Security Incident Response \(SIR\) we have noted them here.

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

If any specific browser requirements were introduced or changed for Now Assist for Security Incident Response \(SIR\) we have noted them here.

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

Review details on accessibility information for Now Assist for Security Incident Response \(SIR\), such as specific requirements or compliance levels.

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

If there are specific localization considerations for Now Assist for Security Incident Response \(SIR\) we have noted them here.

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

If there are specific highlight considerations for Now Assist for Security Incident Response \(SIR\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


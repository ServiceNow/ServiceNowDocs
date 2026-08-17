---
title: Combined ServiceNow Otto for Unified Security Exposure Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto for Unified Security Exposure Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowottoforunifiedsecurityexposuremanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Unified Security Exposure Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto for Unified Security Exposure Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Unified Security Exposure Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Unified Security Exposure Management to Australia

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

For more information about required applications for ServiceNow Otto for Unified Security Exposure Management, see [Supporting information](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=yokohama&ft:locale=en-US).

 **Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

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

Between your current release family and Australia, new features were introduced for ServiceNow Otto for Unified Security Exposure Management.

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

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=yokohama&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use Now Assist for Vulnerability Response in Security Posture Control](https://www.servicenow.com/docs/access?context=using-now-assist-api-connector&family=yokohama&ft:locale=en-US)**

You have the option to use Now Assist to help you automatically complete some of the steps in the Connector builder in the Security Posture Control workspace. Use the Connector builder to create your own service graph connectors for Security Posture Control.

-   **[Generate insights to prioritize risks](https://www.servicenow.com/docs/access?context=sem-insights-skill&family=yokohama&ft:locale=en-US)**

Use generative AI to provide contextual summaries, actionable recommendations, and quick links in the Security Exposure Management Workspace, helping you prioritize critical risks and accelerate remediation.

-   **[Generate recommendation for approval impact analysis](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&family=yokohama&ft:locale=en-US)**

Use generative AI to provide on-demand recommendations to approve or reject a request directly from the Exception Change Approval record, enabling approvers to make fast, consistent decisions while reducing manual analysis effort.


-   **[Granular roles](https://www.servicenow.com/docs/access?context=now-assist-vr-acticvate-agentic-workflow&family=yokohama&ft:locale=en-US)**

The sn\_vul\_ai.write\_rem\_insights and sn\_vul\_ai.read\_rem\_insights granular roles have been added and are inherited by the sn\_vul.vulnerability\_admin and sn\_vul.vulnerability\_analyst roles automatically. These roles provide you with more control over read and write access for the records on the Remediation Compliance Insights \[sn\_vul\_ai\_remediation\_insights\] caching table. The VR.System role also inherits these granular roles so background job execution for the workflow can occur.


-   **[Identify duplicate vulnerable items](https://www.servicenow.com/docs/access?context=dedupe-host-vi-now-assist-vulnerability-response&family=yokohama&ft:locale=en-US)**

Use generative AI to identify duplicates for your active host vulnerable items that are imported by your vulnerability scanners. Use generative AI reasoning with Now Assist to help your analysts differentiate between primary vulnerability items \(VITs\) and those VITs that are duplicates. Close duplicate VITs and move their associated detections automatically to the primary VIT records.

-   **[Suggest vulnerability solutions](https://www.servicenow.com/docs/access?context=solutions-now-assist-vulnerability-response&family=yokohama&ft:locale=en-US)**

Use generative AI to analyze available remediation options pulled from integrated third-party products like Red Hat, Tenable for Vulnerability Response, or internal solution management systems. Evaluate each option against the specific configuration item context, for example, the OS version or software version, and get recommendations for the most viable fix for implementation.

-   ****

-   **[Use agentic workflows](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-vr&family=yokohama&ft:locale=en-US)**

The Assess vulnerability exposure agentic workflow enables vulnerability managers to determine your exposure to vulnerabilities.

    -   Determine your exposure to the most current Cybersecurity and Infrastructure Security Agency \(CISA\) known vulnerabilities in your environment and assess their potential impact to your configuration items \(CIs\) and business services.
    -   Identify assets with Common Vulnerabilities and Exposures \(CVEs\).
    -   Determine the number of active vulnerability items \(VITs\) that correspond to CVEs. Create watch topics for VIT remediation.
The Analyze vulnerability remediation status agentic workflow enables vulnerability managers to monitor and assess remediation target compliance.

    -   Track Service Level Agreement \(SLA\) compliance - Understand how effectively your organization is meeting remediation goals for vulnerabilities based on your SLAs.
    -   Analyze missed SLAs by severity, assignment group, and configuration item \(CI\) class - Pinpoint gaps in remediation by categorizing overdue VITs based on severity, assignment groups, and CI classes to enable targeted interventions and smarter resource allocation.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for Unified Security Exposure Management features.

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



-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The following Now Assist skills for ServiceNow Otto for Unified Security Exposure Management are activated by default.

    -   Recommend preferred solution for VIT \(VR\)
    -   Vulnerable item de-duplication \(VR\)
    -   Approval Recommendation \(VR\)\(USEM\)
    -   Security Exposure Management \(SEM\) Insights \(VR\)\(USEM\)
    -   SPC Setup Connector \(Security Posture Control\)
The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for Unified Security Exposure Management features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto for Unified Security Exposure Management features or functionality were deprecated.

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

Review information on how to activate ServiceNow Otto for Unified Security Exposure Management.

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

Install ServiceNow Otto for Unified Security Exposure Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Unified Security Exposure Management we have noted them here.

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

If any specific browser requirements were introduced or changed for ServiceNow Otto for Unified Security Exposure Management we have noted them here.

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

Review details on accessibility information for ServiceNow Otto for Unified Security Exposure Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for ServiceNow Otto for Unified Security Exposure Management we have noted them here.

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

If there are specific highlight considerations for ServiceNow Otto for Unified Security Exposure Management we have noted them here.

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

-   Review changes to Now Assist usage measurement. See the "Changed in this release" section below.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use ServiceNow Otto for Unified Security Exposure Management with Security Posture Control to help you with [Creating an API connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=using-now-assist-api-connector&family=yokohama&ft:locale=en-US).

 -   [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

Help your analysts identify duplicate host vulnerable items and analyze available remediation options with generative AI skills with ServiceNow Otto for Unified Security Exposure Management.

    -   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
See [ServiceNow Otto for Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&family=yokohama&ft:locale=en-US) for more information.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)


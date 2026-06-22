---
title: Combined Code Signing release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Code Signing from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-codesigning-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Code Signing release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Code Signing from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Code Signing release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Code Signing to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Code Signing.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Code Signing Installation using Plugin](https://servicenow-staging.fluidtopics.net/access?context=enable-codesiging&family=zurich&ft:locale=en-US)**

Customer administrators can now install the Code Signing plugin directly from the ServiceNow Plugin portal without the need to contact the Customer Service and Support team to enable the Code Signing framework. This enhancement supports self-service deployment and simplifies the installation process.

-   **[Quorum Controlled Certificate Revocation](https://servicenow-staging.fluidtopics.net/access?context=certificate-revocation&family=zurich&ft:locale=en-US)**

Revoke Code Signing certificates using a quorum-based control policy. Revoke certificates to help prevent them from being used to verify signatures. A quorum-based approval flow promotes added security by requiring approvals from multiple stakeholders, to help prevent unintended or unauthorized certificate revocations.

-   **[Code Signing Health and Status Dashboard](https://servicenow-staging.fluidtopics.net/access?context=code-signing-health-and-status-dashboard&family=zurich&ft:locale=en-US)**

The new **Code Signing Health and Status** dashboard provides a centralized, user-friendly interface to monitor the overall health and configuration of your code signing environment. It highlights configuration settings, displays the status of essential components, and offers actionable guidance to help resolve issues effectively.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Code Signing features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Enhancements to the guardrails check](https://servicenow-staging.fluidtopics.net/access?context=cse-ppi-config&family=yokohama&ft:locale=en-US)**

The Code Signing Guardrails check has been improved to enhance signature verification, resulting in more secure workflows. In addition, multiple optimizations have been implemented to improve the performance benchmarks of the Guardrails scan, and log files now feature a more intuitive naming convention, which simplifies file identification within your system.


-   **[Generate update sets with a maximum size of 10,000 records](https://servicenow-staging.fluidtopics.net/access?context=cse-turn-on-cse&family=yokohama&ft:locale=en-US)**

Code Signing now enforces limits on large update sets to improve the user experience. The maximum size for an update set is 10,000 records.


-   **[Naming updates for trusted and production instances](https://servicenow-staging.fluidtopics.net/access?context=code-signing-landing&family=yokohama&ft:locale=en-US)**

The trusted non-production instance has been renamed to trusted instance, and the protected production instance has been renamed to protected instance. These naming updates have been made to better align with customer usage.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://servicenow-staging.fluidtopics.net/access?context=config-code-signing&family=zurich&ft:locale=en-US)**

You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Code Signing features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Code Signing features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Code Signing.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configuring Code Signing](https://servicenow-staging.fluidtopics.net/access?context=config-code-signing&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configure](https://servicenow-staging.fluidtopics.net/access?context=config-code-signing&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Code Signing we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Code Signing we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Code Signing, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Code Signing we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Code Signing we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.

 See [Code Signing](https://servicenow-staging.fluidtopics.net/access?context=code-signing-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Code Signing OOB Apps Signatures plugin](https://servicenow-staging.fluidtopics.net/access?context=explore-code-signing&family=zurich&ft:locale=en-US)**

Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.


 -   Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.
-   Use the Code Signing Migration workflow to identify the signatures that are created with expired or inactive certificates and re-assign them to the appropriate records automatically.
-   Revoke Code Signing certificates securely using a quorum-based approval policy to prevent unauthorized use.
-   Monitor and manage your Code Signing environment with the new Health and Status dashboard.
-   The restructured navigation panel and the renamed pages provide improved accessibility and streamlined functionality.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)


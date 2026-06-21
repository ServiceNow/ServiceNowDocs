---
title: Combined Code Signing release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Code Signing from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-codesigning-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Code Signing release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Code Signing from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Code Signing release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Code Signing to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Code Signing.

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

-   **[Code Signing Installation using Plugin](https://www.servicenow.com/docs/access?context=enable-codesiging&family=zurich&ft:locale=en-US)**

Customer administrators can now install the Code Signing plugin directly from the ServiceNow Plugin portal without the need to contact the Customer Service and Support team to enable the Code Signing framework. This enhancement supports self-service deployment and simplifies the installation process.

-   **[Quorum Controlled Certificate Revocation](https://www.servicenow.com/docs/access?context=certificate-revocation&family=zurich&ft:locale=en-US)**

Revoke Code Signing certificates using a quorum-based control policy. Revoke certificates to help prevent them from being used to verify signatures. A quorum-based approval flow promotes added security by requiring approvals from multiple stakeholders, to help prevent unintended or unauthorized certificate revocations.

-   **[Code Signing Health and Status Dashboard](https://www.servicenow.com/docs/access?context=code-signing-health-and-status-dashboard&family=zurich&ft:locale=en-US)**

The new **Code Signing Health and Status** dashboard provides a centralized, user-friendly interface to monitor the overall health and configuration of your code signing environment. It highlights configuration settings, displays the status of essential components, and offers actionable guidance to help resolve issues effectively.


</td></tr><tr><td>

Australia

</td><td>

-   **[Utilities Dashboard](https://www.servicenow.com/docs/access?context=code-signing-utilities&family=australia&ft:locale=en-US)**

Use the **Utilities Dashboard** tab within the Code Signing Health and Status dashboard to monitor signature status, detect configuration issues, and maintain the overall health of your Code Signing environment.

-   **[Multiple signatures for a record across certificates](https://www.servicenow.com/docs/access?context=signature-verification-in-code-signing&family=australia&ft:locale=en-US)**

Leverage support for multiple signatures for records across different certificates, thus ensuring that valid signatures from any trusted source are recognized. Allow multiple signatures to be added to a record and have the system determine validity by evaluating all existing signatures from newest to oldest.

-   **[Code Signing OOB Apps Signatures plugin](https://www.servicenow.com/docs/access?context=explore-code-signing&family=australia&ft:locale=en-US)**

Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.

-   **[New key pair](https://www.servicenow.com/docs/access?context=code-signing-certificates&family=australia&ft:locale=en-US)**

A new cryptographic key pair is generated to strengthen the Circle of Trust and to ensure a secure signing process. You can see this key pair within the **Key Pair and Certificates** tab of the **Code Signing Health and Status** dashboard.

-   **[Wild Card Purpose for KMF Signature Configuration](https://www.servicenow.com/docs/access?context=explore-code-signing&family=australia&ft:locale=en-US)**

Use the "Wild Card Purpose" entry in the signature configurations to eliminate import warnings for script includes and business rules.

-   **[Code signing for probes](https://www.servicenow.com/docs/access?context=sign-files-nonprod&family=australia&ft:locale=en-US)**

Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Code Signing features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Enhancements to the guardrails check](https://www.servicenow.com/docs/access?context=cse-ppi-config&family=yokohama&ft:locale=en-US)**

The Code Signing Guardrails check has been improved to enhance signature verification, resulting in more secure workflows. In addition, multiple optimizations have been implemented to improve the performance benchmarks of the Guardrails scan, and log files now feature a more intuitive naming convention, which simplifies file identification within your system.


-   **[Generate update sets with a maximum size of 10,000 records](https://www.servicenow.com/docs/access?context=cse-turn-on-cse&family=yokohama&ft:locale=en-US)**

Code Signing now enforces limits on large update sets to improve the user experience. The maximum size for an update set is 10,000 records.


-   **[Naming updates for trusted and production instances](https://www.servicenow.com/docs/access?context=code-signing-landing&family=yokohama&ft:locale=en-US)**

The trusted non-production instance has been renamed to trusted instance, and the protected production instance has been renamed to protected instance. These naming updates have been made to better align with customer usage.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://www.servicenow.com/docs/access?context=config-code-signing&family=zurich&ft:locale=en-US)**

You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.


</td></tr><tr><td>

Australia

</td><td>

-   **[Guardrail process optimization and scope increase](https://www.servicenow.com/docs/access?context=signature-verification-status&family=australia&ft:locale=en-US)**

Allows you to run the guardrail scan and identify records that have missing signatures, enabling you to proactively address records that are eligible for code signing but remain unsigned. Previously, the system only checked records with existing signatures and marked them as valid or invalid, which meant records without signatures were overlooked. Now, the process starts from the signature configuration itself, every eligible record is checked to see if it has a signature. If a record is missing a signature, it's clearly identified.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Code Signing features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Code Signing features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

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

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configuring Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configure](https://www.servicenow.com/docs/access?context=config-code-signing&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\). For details, see [Configure](https://www.servicenow.com/docs/access?context=config-code-signing&family=australia&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

 See [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Code Signing OOB Apps Signatures plugin](https://www.servicenow.com/docs/access?context=explore-code-signing&family=zurich&ft:locale=en-US)**

Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.


 -   Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.
-   Use the Code Signing Migration workflow to identify the signatures that are created with expired or inactive certificates and re-assign them to the appropriate records automatically.
-   Revoke Code Signing certificates securely using a quorum-based approval policy to prevent unauthorized use.
-   Monitor and manage your Code Signing environment with the new Health and Status dashboard.
-   The restructured navigation panel and the renamed pages provide improved accessibility and streamlined functionality.

</td></tr><tr><td>

Australia

</td><td>

-   Gain complete visibility into Code Signing coverage by proactively identifying eligible records with missing signatures using the optimized guardrail scan.
-   Install build time signatures for records in all trued-up ServiceNow Store application versions, thus eliminating the self-signing process.
-   Ensure reliable script verification by supporting multiple signatures for a record across certificates. Reduce upgrade failures and improve compliance for customers using custom and ServiceNow® certificates.

 See [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


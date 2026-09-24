---
title: Combined Code Signing release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Code Signing from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-codesigning-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Code Signing release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Code Signing from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Code Signing release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Code Signing to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Code Signing.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr><tr><td>

Brazil

</td><td>

-   **[Signature generation during source control commit](https://www.servicenow.com/docs/access?context=c_cs_commit_signing&family=brazil&ft:locale=en-US)**

Generate Code Signing signatures automatically when you commit application files to source control from a trusted instance. Signatures are created for eligible records during the commit and pushed to the remote repository in the same update set as their source records, so a protected instance can validate the records it receives.

-   **[Code Signing change audit data](https://www.servicenow.com/docs/access?context=cs-vault-audit-data&family=brazil&ft:locale=en-US)**

Review the create, update, and delete operations that users perform on records protected by Code Signing. Each audit record identifies the changed record, the user who changed it, the operation type, and the date and time of the change. Audit data is recorded by default on production instances when Code Signing is active, and users with the codesigning\_auditor role can view and report on it. A scheduled job manages the size of the audit data based on a configurable retention period and maximum record count.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Code Signing features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Guardrail process optimization and scope increase](https://www.servicenow.com/docs/access?context=signature-verification-status&family=australia&ft:locale=en-US)**

Allows you to run the guardrail scan and identify records that have missing signatures, enabling you to proactively address records that are eligible for code signing but remain unsigned. Previously, the system only checked records with existing signatures and marked them as valid or invalid, which meant records without signatures were overlooked. Now, the process starts from the signature configuration itself, every eligible record is checked to see if it has a signature. If a record is missing a signature, it's clearly identified.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Code Signing features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Code Signing features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\). For details, see [Configure](https://www.servicenow.com/docs/access?context=config-code-signing&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Code Signing is a ServiceNow AI Platform feature available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\). For details, see [Configure](https://www.servicenow.com/docs/access?context=config-code-signing&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Code Signing we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   Gain complete visibility into Code Signing coverage by proactively identifying eligible records with missing signatures using the optimized guardrail scan.
-   Install build time signatures for records in all trued-up ServiceNow Store application versions, thus eliminating the self-signing process.
-   Ensure reliable script verification by supporting multiple signatures for a record across certificates. Reduce upgrade failures and improve compliance for customers using custom and ServiceNow® certificates.

 See [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Prevent unauthorized code execution by enabling cryptographic verification of all scripts on your MID Servers.
-   Detect tampering instantly by identifying modifications to signed records and automatically blocking compromised code.
-   Streamline security enforcement by automating signature verification across integrations without requiring manual intervention.
-   Support compliance needs by maintaining comprehensive audit records of all signature verification events.

 See [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)


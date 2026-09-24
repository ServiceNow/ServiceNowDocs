---
title: Combined Encryption release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Encryption from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-encryption-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Encryption release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Encryption from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption to Brazil

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

-   **Important information for upgrading to Brazil**
    -   If you're using scheduled upgrade to upgrade your Edge Encryption proxy from a pre-Brazil release to Brazil, you must meet the following requirements before you attempt the upgrade:
        -   Upgrade the Java version to Java 21 or later.
        -   Ensure you're on Zurich Patch 13 \(ZP13\) or Australia Patch 6 \(AP6\) or later. If you're on an earlier version, scheduled upgrade will not work.
    -   If you're using command-line upgrade, you must upgrade the Java version to Java 21 or later.
    -   Java 17 is required to install Edge Encryption on versions Yokohama through Australia. Prior to upgrading to Brazil, you must upgrade to Java 21. See [Installing Edge Encryption](https://www.servicenow.com/docs/access?context=c_InstallEdgeEncryptionProxy&family=brazil&ft:locale=en-US) for installation details.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Encryption.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Manage Field Encryption Enterprise with an enhanced Administration interface](https://www.servicenow.com/docs/access?context=now-platform-encryption&family=australia&ft:locale=en-US)**

Configure encryption settings, monitor key usage, and streamline administration for Field Encryption and Field Encryption Enterprise with the following features:

    -   Simplify key rotation and policy updates.
    -   Access encryption status and audit details.
    -   Navigate improved layouts for faster configuration.
-   **[Integrate External Key Management Service \(EKMS\) with Encryption Modules](https://www.servicenow.com/docs/access?context=ekms-external-key-management&family=australia&ft:locale=en-US)**

Configure and manage encryption keys externally through EKMS integration with an enhanced encryption framework, which enables you to:

    -   Hold encryption keys outside the instance for improved security.
    -   Perform key rotation and revocation with automated security tasks.
    -   Manage EKMS configurations and enforce the immutability of critical fields after they're active.
    -   Simplify rekeying following instance clone and restore operations.
    -   Monitor key state transitions, encrypted cache, and node-to-node communication.
    -   Access UI improvements for configuration visibility and error handling.
    -   Benefit from telemetry and performance-tested operations.

</td></tr><tr><td>

Brazil

</td><td>

-   **Edge Encryption proxy now supports Java 21**

Install and run the Edge Encryption proxy on systems with Java 21.0 or later. You can now use newer Java versions for enhanced security and performance benefits. Current supported versions are Java 21.0 or later in the 21.x version series, and Java 17.0.3 or later in the 17.x version series. For installation details, see [Installing Edge Encryption](https://www.servicenow.com/docs/access?context=c_InstallEdgeEncryptionProxy&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Encryption features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Field Encryption user interface changes](https://www.servicenow.com/docs/access?context=now-platform-encryption&family=australia&ft:locale=en-US)**

The new Field Encryption and Field Encryption Enterprise UI includes updates to key rotation and policies, access to encryption status and audit details, and changes to layouts.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Encryption features or functionality were removed.

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

Between your current release family and Brazil, some Encryption features or functionality were deprecated.

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

Review information on how to activate Encryption.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Platform Encryption is available with activation of the com.glide.encryption.external\_kms, which requires a separate subscription. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Platform Encryption Key Management Framework is available with activation of the com.glide.encryption.external\_kms, which requires a separate subscription. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=australia&pubname=australia-platform-security&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Encryption we have noted them here.

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

If any specific browser requirements were introduced or changed for Encryption we have noted them here.

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

Review details on accessibility information for Encryption, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Encryption we have noted them here.

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

If there are specific highlight considerations for Encryption we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   ManageField Encryption and Field Encryption Enterprise using the redesigned user interface.
-   Enhance data security with the newly added External Key Management Service \(EKMS\) integration, enabling you to store encryption keys outside the instance for enhanced security.

 See [Encryption](https://www.servicenow.com/docs/access?context=encryption-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

The ServiceNow® Encryption application protects your sensitive data and helps you meet regulatory requirements and standards. Encryption provides multiple solutions to safeguard your instance, including Key Management Framework, Field Encryption, Cloud Encryption, Edge Encryption, Database Encryption, and certificate management.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)


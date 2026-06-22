---
title: Combined Encryption release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Encryption from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-encryption-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Encryption release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Encryption from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

-   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
-   For instances created with the Zurich release or later, this API isn’t supported.
-   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

 In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Encryption.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Encrypt data using Row Conditions](https://www.servicenow.com/docs/access?context=encrypt-data-using-row-conditions&family=zurich&ft:locale=en-US)**

Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.


</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Encryption features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Field Encryption Enterprise](https://www.servicenow.com/docs/access?context=now-platform-encryption&family=zurich&ft:locale=en-US) API**

Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Encryption features or functionality were removed.

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

Between your current release family and Australia, some Encryption features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Prepare your instance for GlideEncrypter deprecation](https://www.servicenow.com/docs/access?context=check-3des&family=zurich&ft:locale=en-US)**

Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.


</td></tr><tr><td>

Australia

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

Zurich

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

 Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see the [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Platform Encryption is available with activation of the com.glide.encryption.external\_kms, which requires a separate subscription. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Encryption we have noted them here.

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

If any specific browser requirements were introduced or changed for Encryption we have noted them here.

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

Review details on accessibility information for Encryption, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Encryption we have noted them here.

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

If there are specific highlight considerations for Encryption we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.
-   Use any of the three Field Encryption APIs to encrypt attachments.

 See [Encryption](https://www.servicenow.com/docs/access?context=encryption-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   ManageField Encryption and Field Encryption Enterprise using the redesigned user interface.
-   Enhance data security with the newly added External Key Management Service \(EKMS\) integration, enabling you to store encryption keys outside the instance for enhanced security.

 See [Encryption](https://www.servicenow.com/docs/access?context=encryption-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


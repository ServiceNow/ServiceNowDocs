---
title: Combined Encryption release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Encryption from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-encryption-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 3
breadcrumb: [Products combined by family]
---

# Combined Encryption release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Encryption from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

-   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
-   For instances created with the Zurich release or later, this API isn’t supported.
-   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

 In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Encryption.

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

-   **[Encrypt data using Row Conditions](https://servicenow-staging.fluidtopics.net/access?context=encrypt-data-using-row-conditions&family=zurich&ft:locale=en-US)**

Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Encryption features.

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

-   **[Field Encryption Enterprise](https://servicenow-staging.fluidtopics.net/access?context=now-platform-encryption&family=zurich&ft:locale=en-US) API**

Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Encryption features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Encryption features or functionality were deprecated.

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

-   **[Prepare your instance for GlideEncrypter deprecation](https://servicenow-staging.fluidtopics.net/access?context=check-3des&family=zurich&ft:locale=en-US)**

Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Encryption.

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

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

 Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see the [Encryption and Key Management subscription bundle](https://servicenow-staging.fluidtopics.net/access?context=encryption-sku&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Encryption we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Encryption we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Encryption, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Encryption we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Encryption we have noted them here.

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

-   Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.
-   Use any of the three Field Encryption APIs to encrypt attachments.

 See [Encryption](https://servicenow-staging.fluidtopics.net/access?context=encryption-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


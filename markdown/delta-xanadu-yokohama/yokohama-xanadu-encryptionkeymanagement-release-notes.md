---
title: Combined Encryption Key Management release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Encryption Key Management from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-encryptionkeymanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Encryption Key Management release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Encryption Key Management from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption Key Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption Key Management to Yokohama

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

-   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
    -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Encryption Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[New plugin available for Code Signing roles and administrative features](https://www.servicenow.com/docs/access?context=cs-role-landing&family=xanadu&ft:locale=en-US)**

Activate the plugin to access the new roles and administration features. The new plugin creates signature migration jobs, new code signing roles, and a new code signing administration page.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Column Level Encryption is now Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://www.servicenow.com/docs/access?context=access-observer&family=yokohama&ft:locale=en-US)**

Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Encryption Key Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Changes to Code Signing requirements](https://www.servicenow.com/docs/access?context=code-signing-landing&family=xanadu&ft:locale=en-US)**

As a part of improving security around Root of Trust, signing of script and attachments records can only be done on your trusted non-production instance or using the standalone signing tool. The exception is notarization, which can still be performed in the protected production instance.

-   **[Enhancement requests for the Code Signing Standalone signing tool](https://www.servicenow.com/docs/access?context=sa-code-signing-tool&family=xanadu&ft:locale=en-US)**

Updates to Code Signing enable your administrators to work with keystores, signature records, and records to be signed outside of the local system.

-   **[Improved activation process for Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&family=xanadu&ft:locale=en-US)**

Activate Code signing with a new UI page that is designed to streamline the activation process.

-   **[Download All Button for Multiple Attachments is available when Edge Encryption is enabled](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionOverview&family=xanadu&ft:locale=en-US)**

By using the download all functionality, you can now download multiple documents into a zip file when you also enable Edge Encryption.

-   **[Edge Encryption jRobin dashboards have been migrated to NEXT Experience](https://www.servicenow.com/docs/access?context=code-signing-reference&family=xanadu&ft:locale=en-US)**

View troubleshooting and performance on dashboards that were migrated from the deprecated jRobin framework. These dashboards display the same information that was available in previous versions.

-   **[Column Level Encryption Enterprise is installable by administrators after purchase](https://www.servicenow.com/docs/access?context=activate-platform-encryption&family=xanadu&ft:locale=en-US)**

After purchasing Column Level Encryption Enterprise, your administrator can typically activate the product without needing technical assistance.

-   **[Support for full string UTF-8 in Column Level Encryption](https://www.servicenow.com/docs/access?context=set-encrypted-field-config&family=xanadu&ft:locale=en-US)**

CLE supports encryption and decryption of the full range of UTF-8 characters, including emoji.

-   **[Improved readability for Column Level Encryption logging](https://www.servicenow.com/docs/access?context=code-signing-reference&family=xanadu&ft:locale=en-US)**

With the improved system, node, application, and audit logging, your administrators can analyze and troubleshoot their CLE or CLEE implementation.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Encryption Key Management features or functionality were removed.

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

Between your current release family and Yokohama, some Encryption Key Management features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Encryption Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Column Level Encryption Enterprise, Cloud Encryption, and Database Encryption.

 Column Level Encryption Enterprise is the unlimited license of Column Level Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

 Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Encryption Key Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Encryption Key Management we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for Encryption Key Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Encryption Key Management we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Encryption Key Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Start using Code Signing's improved activation process. You can use the new Code Signing UI page for a faster, streamlined activation.
-   Administer Column Level Encryption with new Column Level Encryption APIs, roles, and administration features. Column Level Encryption logging has been enhanced for improved readability.
-   Download all encrypted attachments as a zip file by using the new **Download All** button.

 See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Column Level Encryption has been rebranded and redesigned to now be called Field Encryption.
-   Use Access Observer to help plan for and troubleshoot Field Encryption implementations.
-   Edge Encryption administrators can use the new process to migrate from Edge Encryption to Field Encryption.

 See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)


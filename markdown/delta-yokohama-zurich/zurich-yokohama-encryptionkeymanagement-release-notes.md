---
title: Combined Encryption Key Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Encryption Key Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-encryptionkeymanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Encryption Key Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Encryption Key Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption Key Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption Key Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
    -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr><tr><td>

Zurich

</td><td>

-   In previous releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Zurich release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Zurich instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Zurich instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Encryption Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Column Level Encryption is now Field Encryption](https://servicenow-staging.fluidtopics.net/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://servicenow-staging.fluidtopics.net/access?context=access-observer&family=yokohama&ft:locale=en-US)**

Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://servicenow-staging.fluidtopics.net/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Keep track of Field Encryption and Key Management changes](https://servicenow-staging.fluidtopics.net/access?context=c_UnderstandingTheSysAuditTable&family=zurich&ft:locale=en-US)**

By default, the changes to the records on these tables are now logged to the Sys Audits \[sys\_audit\] table:

    -   Encrypted Field Configurations \[sys\_platform\_encryption\_configuration\]
    -   Module Access Policies \[sys\_kmf\_crypto\_caller\_policy\]
    -   Cryptographic Modules \[sys\_kmf\_crypto\_module\]
For details on accessing the Sys Audits \[sys\_audit\] table, see [Review](https://servicenow-staging.fluidtopics.net/access?context=c_UnderstandingTheSysAuditTable&family=zurich&ft:locale=en-US).


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Encryption Key Management features.

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

-   **[Updates to GlideEncrypter functionality](https://servicenow-staging.fluidtopics.net/access?context=glideencrypter-deprecation&family=zurich&ft:locale=en-US)**

The GlideEncrypter API has been updated to use AES256-GCM encryption via the Key Management Framework. If needed, your instance can be changed to use legacy 3DES encryption, but this task can only be done by ServiceNow support.

-   **[Disable GlideEncrypter on your instance](https://servicenow-staging.fluidtopics.net/access?context=check-3des&family=zurich&ft:locale=en-US)**

GlideEncrypter can be enabled or turned off using the **glide.security.glideencrypter.allow** system property. This property is unavailable on new Zurich instances, but administrators with the security\_admin role can edit this property in upgraded instances. When this system property is set to **false**, users see this error when attempting to run GlideEncrypter.

    ```
Unsupported call to GlideEncrypter. Details: GlideEncrypter is deprecated and now returns null, please refer KB1320986
    ```


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Encryption Key Management features or functionality were removed.

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

Between your current release family and Zurich, some Encryption Key Management features or functionality were deprecated.

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

Review information on how to activate Encryption Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

 Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://servicenow-staging.fluidtopics.net/access?context=encryption-sku&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

 Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://servicenow-staging.fluidtopics.net/access?context=encryption-sku&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Encryption Key Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Encryption Key Management we have noted them here.

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

Review details on accessibility information for Encryption Key Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Encryption Key Management we have noted them here.

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

If there are specific highlight considerations for Encryption Key Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Column Level Encryption has been rebranded and redesigned to now be called Field Encryption.
-   Use Access Observer to help plan for and troubleshoot Field Encryption implementations.
-   Edge Encryption administrators can use the new process to migrate from Edge Encryption to Field Encryption.

 See [Key Management Framework](https://servicenow-staging.fluidtopics.net/access?context=encryption&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   See the changes to the Key Management and Field Encryption records that are now logged on the Sys Audits \[sys\_audit\] table.
-   The GlideEncrypter API has been updated and now uses AES256-GCM encryption via the Key Management Framework.
-   Enable or disable GlideEncrypter by using the **glide.security.glideencrypter.allow** system property.

 See [Key Management Framework](https://servicenow-staging.fluidtopics.net/access?context=encryption&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)


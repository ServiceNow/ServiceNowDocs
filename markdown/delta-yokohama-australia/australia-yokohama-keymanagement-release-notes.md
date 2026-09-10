---
title: Combined Key Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Key Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-keymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Key Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Key Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Key Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Key Management to Australia

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

-   **Upgrade information**
    -   In pre-Zurich releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Australia release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
        -   New Australia instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
        -   if you’re upgrading your Australia instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
        -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Column Level Encryption is now Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://www.servicenow.com/docs/access?context=access-observer&family=yokohama&ft:locale=en-US)**

Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&family=yokohama&ft:locale=en-US)**

Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Keep track of Field Encryption and Key Management changes](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&family=zurich&ft:locale=en-US)**

By default, the changes to the records on these tables are now logged to the Sys Audits \[sys\_audit\] table:

    -   Encrypted Field Configurations \[sys\_platform\_encryption\_configuration\]
    -   Module Access Policies \[sys\_kmf\_crypto\_caller\_policy\]
    -   Cryptographic Modules \[sys\_kmf\_crypto\_module\]
For details on accessing the Sys Audits \[sys\_audit\] table, see [Review](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **[Added SHA512 support for message digests](https://www.servicenow.com/docs/access?context=c_GlideDigestScopedAPI&family=australia&ft:locale=en-US)**

GlideDigest has been updated to allow creation and verification of message digests using the SHA512 cryptographic hash function.

-   **Offline key exchange to share module keys between instances**

Admins can share module keys between instances offline to facilitate instance clones between on-premise instances using KMF.

-   **[Sign and verify JSON web tokens \(JWT\) through KMFCryptoOperation](https://www.servicenow.com/docs/access?context=KMFCryptoOperationBothAPI&family=australia&ft:locale=en-US)**

The signing and verification processes for JWTs are now integrated as operation types in the existing KMFCryptoOperation class.

-   **Centralized Crypto Management console**

Use the new Crypto Management Console to streamline and track the certificate management lifecycle. The new console scans your instance for certificates and displays their details in a central location,

-   **Clone and restore support for on-premise instances**

Support for cloning and restoring on-premise instances. Support has also been added from migrating a commercial instance to on-premise instances, and vice-versa.

-   **Certificate Revocation List \(CRL\) validation support**

ServiceNow now supports Certificate Revocation List \(CRL\) validation for certificate revocation checks as an alternative to Online Certificate Status Protocol \(OCSP\), with automatic fallback when OCSP is unavailable.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Key Management features.

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

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Updates to GlideEncrypter functionality](https://www.servicenow.com/docs/access?context=glideencrypter-deprecation&family=zurich&ft:locale=en-US)**

The GlideEncrypter API has been updated to use AES256-GCM encryption via the Key Management Framework. If needed, your instance can be changed to use legacy 3DES encryption, but this task can only be done by ServiceNow support.

-   **[Disable GlideEncrypter on your instance](https://www.servicenow.com/docs/access?context=check-3des&family=zurich&ft:locale=en-US)**

GlideEncrypter can be enabled or turned off using the **glide.security.glideencrypter.allow** system property. This property is unavailable on new Zurich instances, but administrators with the security\_admin role can edit this property in upgraded instances. When this system property is set to **false**, users see this error when attempting to run GlideEncrypter.

    ```
Unsupported call to GlideEncrypter. Details: GlideEncrypter is deprecated and now returns null, please refer KB1320986
    ```


</td></tr><tr><td>

Australia

</td><td>

-   **[Updated workflow for creating cryptographic modules](https://www.servicenow.com/docs/access?context=create-cryptographic-module&family=australia&ft:locale=en-US)**

Use the streamlined workflow designed for faster, easier creation of cryptographic modules.

-   **[SecurityUtils Enhancements](https://www.servicenow.com/docs/access?context=GlideSecurityUtilsScopedAPI&family=australia&ft:locale=en-US)**

The SecurityUtils API has been enhanced to help prevent cross-site scripting attacks, including methods to sanitize and escape input.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Key Management features or functionality were removed.

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

Between your current release family and Australia, some Key Management features or functionality were deprecated.

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

Review information on how to activate Key Management.

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

-   **Activation information**

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Key Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Key Management we have noted them here.

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

Review details on accessibility information for Key Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Key Management we have noted them here.

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

If there are specific highlight considerations for Key Management we have noted them here.

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

-   GlideDigest has been updated to allow creation and verification of message digests using the SHA512 cryptographic hash function
-   Admins can share module keys between instances offline to facilitate instance clones between on-premise instances using KMF.
-   The signing and verification processes for JWTs are now integrated as operation types in the existing KMFCryptoOperation class.

 See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


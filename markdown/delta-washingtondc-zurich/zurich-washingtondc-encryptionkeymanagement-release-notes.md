---
title: Combined Encryption Key Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Encryption Key Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-encryptionkeymanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Encryption Key Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Encryption Key Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Encryption Key Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Encryption Key Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

If you upgrade your instance to Washington DC but don’t upgrade your MID Server, Secrets Management authentication fails. Avoid authentication failures by upgrading your MID Server to Washington DC. If you can’t upgrade, you must turn off authentication until MID Server is upgraded to Washington DC to avoid authentication failures.

 For details on MID Server upgrades, see [MID Server upgrades](https://servicenow-staging.fluidtopics.net/access?context=c_UpgradeAndTestMIDServer&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

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

Washington DC

</td><td>

-   **[PostgreSQL database support](https://servicenow-staging.fluidtopics.net/access?context=dare-overview&family=washingtondc&ft:locale=en-US)**

Support the PostgreSQL databases for primary, secondary, read replica, gateway \(shard\), and Logical Corruption Protection \(LCP\) databases for cloud encryption. LCP databases are a variant of the read replica database.

-   **[Trusted timestamps within the Code Signing framework](https://servicenow-staging.fluidtopics.net/access?context=code-signing-landing&family=washingtondc&ft:locale=en-US)**

View when a signature is issued by using timestamped Key Management Framework \(KMF\) Signature \[sn\_kmf\_record\_signature\] records.

-   **[Reusable key for agent-to-agent credential sharing](https://servicenow-staging.fluidtopics.net/access?context=client-access-secret-landing&family=washingtondc&ft:locale=en-US)**

Configure client-side asymmetric key pairs for API authentication. With the reusable key feature, every conceptual cryptographic module has only one active conceptual key at any point, generated on the client side and wrapped with its respective public key.

-   **[Simplified process for 3DES deprecation](https://servicenow-staging.fluidtopics.net/access?context=check-3des&family=washingtondc&ft:locale=en-US)**

Remove GlideEncrypter by using the guidance from the improved user interface for 3DES deprecation. Within the critical update app in Security Center, you can find information about the full and partial deprecation of 3DES, and view all impacted legacy password2 fields before deprecating 3DES.

-   **[Property-driven multi-layer caller inspection for Code Signing](https://servicenow-staging.fluidtopics.net/access?context=code-sign-properties&family=washingtondc&ft:locale=en-US)**

Increase the number of caller layers to be validated during the ECC queue notarization to improve security. Starting in Washington DC, the number of validated caller layers is driven by a system property.

-   **[Switch between ServiceNow Root of Trust \(ROT\) and your own ROT](https://servicenow-staging.fluidtopics.net/access?context=change-rot-overview&family=washingtondc&ft:locale=en-US)**

Switch between ServiceNow Root of Trust \(ROT\) and your own ROT.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[New plugin available for Code Signing roles and administrative features](https://servicenow-staging.fluidtopics.net/access?context=cs-role-landing&family=xanadu&ft:locale=en-US)**

Activate the plugin to access the new roles and administration features. The new plugin creates signature migration jobs, new code signing roles, and a new code signing administration page.


</td></tr><tr><td>

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

Washington DC

</td><td>

-   **[Web Service Consumer plugin tables reject access by default](https://servicenow-staging.fluidtopics.net/access?context=r_AvailableWebServices&family=washingtondc&ft:locale=en-US)**

To improve security, default access to tables in the Web Service Consumer \(com.glide.web\_service\_consumer\) plugin are set to **Reject**. The following tables are affected.

    -   sys\_rest\_message
    -   sys\_rest\_message\_fn
    -   sys\_auth\_profile\_basic
    -   sys\_auth\_profile\_oauth2
    -   sys\_soap\_message
    -   sys\_soap\_message\_function
    -   ws\_security\_x509\_profile\_outbound
    -   ws\_security\_username\_profile\_outbound
Default access to tables in the External App Authentication \(com.glide.external.app\) plugin are also set to **Reject**. The following tables are affected.

    -   token\_verification
    -   hash\_message\_verification

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Changes to Code Signing requirements](https://servicenow-staging.fluidtopics.net/access?context=code-signing-landing&family=xanadu&ft:locale=en-US)**

As a part of improving security around Root of Trust, signing of script and attachments records can only be done on your trusted non-production instance or using the standalone signing tool. The exception is notarization, which can still be performed in the protected production instance.

-   **[Enhancement requests for the Code Signing Standalone signing tool](https://servicenow-staging.fluidtopics.net/access?context=sa-code-signing-tool&family=xanadu&ft:locale=en-US)**

Updates to Code Signing enable your administrators to work with keystores, signature records, and records to be signed outside of the local system.

-   **[Improved activation process for Code Signing](https://servicenow-staging.fluidtopics.net/access?context=config-code-signing&family=xanadu&ft:locale=en-US)**

Activate Code signing with a new UI page that is designed to streamline the activation process.

-   **[Download All Button for Multiple Attachments is available when Edge Encryption is enabled](https://servicenow-staging.fluidtopics.net/access?context=c_EdgeEncryptionOverview&family=xanadu&ft:locale=en-US)**

By using the download all functionality, you can now download multiple documents into a zip file when you also enable Edge Encryption.

-   **[Edge Encryption jRobin dashboards have been migrated to NEXT Experience](https://servicenow-staging.fluidtopics.net/access?context=code-signing-reference&family=xanadu&ft:locale=en-US)**

View troubleshooting and performance on dashboards that were migrated from the deprecated jRobin framework. These dashboards display the same information that was available in previous versions.

-   **[Column Level Encryption Enterprise is installable by administrators after purchase](https://servicenow-staging.fluidtopics.net/access?context=activate-platform-encryption&family=xanadu&ft:locale=en-US)**

After purchasing Column Level Encryption Enterprise, your administrator can typically activate the product without needing technical assistance.

-   **[Support for full string UTF-8 in Column Level Encryption](https://servicenow-staging.fluidtopics.net/access?context=set-encrypted-field-config&family=xanadu&ft:locale=en-US)**

CLE supports encryption and decryption of the full range of UTF-8 characters, including emoji.

-   **[Improved readability for Column Level Encryption logging](https://servicenow-staging.fluidtopics.net/access?context=code-signing-reference&family=xanadu&ft:locale=en-US)**

With the improved system, node, application, and audit logging, your administrators can analyze and troubleshoot their CLE or CLEE implementation.


</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Zurich, some Encryption Key Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Starting with the Washington DC release, Database Encryption is being prepared for future deprecation. Cloud Encryption is the replacement solution for data at rest encryption. For details, see [Encryption and Key Management](https://servicenow-staging.fluidtopics.net/access?context=dare-overview&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

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
</table>## Activation information

Review information on how to activate Encryption Key Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Column Level Encryption Enterprise, Cloud Encryption, and Database Encryption.

 Column Level Encryption Enterprise is the unlimited license of Column Level Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://servicenow-staging.fluidtopics.net/access?context=encryption-sku&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Column Level Encryption Enterprise, Cloud Encryption, and Database Encryption.

 Column Level Encryption Enterprise is the unlimited license of Column Level Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://servicenow-staging.fluidtopics.net/access?context=encryption-sku&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If any specific browser requirements were introduced or changed for Encryption Key Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review details on accessibility information for Encryption Key Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific localization considerations for Encryption Key Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific highlight considerations for Encryption Key Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Support the PostgreSQL databases for primary, secondary, read replica, gateway \(shard\), and Logical Corruption Protection \(LCP\) databases for cloud encryption. LCP databases are a variant of the read replica database.
-   View when a signature is issued by using timestamped Key Management Framework \(KMF\) Signature \[sn\_kmf\_record\_signature\] records.
-   Remove GlideEncrypter by using the guidance from the improved user interface for 3DES deprecation. Within the critical update app in Security Center, you can find information about the full and partial deprecation of 3DES, and view all impacted legacy password2 fields before deprecating 3DES.

 See [Encryption and Key Management](https://servicenow-staging.fluidtopics.net/access?context=encryption&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Start using Code Signing's improved activation process. You can use the new Code Signing UI page for a faster, streamlined activation.
-   Administer Column Level Encryption with new Column Level Encryption APIs, roles, and administration features. Column Level Encryption logging has been enhanced for improved readability.
-   Download all encrypted attachments as a zip file by using the new **Download All** button.

 See [Key Management Framework](https://servicenow-staging.fluidtopics.net/access?context=encryption&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)


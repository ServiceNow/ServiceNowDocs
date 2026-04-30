---
title: Encryption Key Management release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Encryption Key Management release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Zurich release.

## Encryption Key Management highlights for the Zurich release

-   See the changes to the Key Management and Field Encryption records that are now logged on the Sys Audits \[sys\_audit\] table.
-   The GlideEncrypter API has been updated and now uses AES256-GCM encryption via the Key Management Framework.
-   Enable or disable GlideEncrypter by using the **glide.security.glideencrypter.allow** system property.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## Important information for upgrading to Zurich

-   In previous releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Zurich release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Zurich instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Zurich instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

## New in the Zurich release

-   **[Keep track of Field Encryption and Key Management changes](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    By default, the changes to the records on these tables are now logged to the Sys Audits \[sys\_audit\] table:

    -   Encrypted Field Configurations \[sys\_platform\_encryption\_configuration\]
    -   Module Access Policies \[sys\_kmf\_crypto\_caller\_policy\]
    -   Cryptographic Modules \[sys\_kmf\_crypto\_module\]
    For details on accessing the Sys Audits \[sys\_audit\] table, see [Viewing Sys Audit and Audit Relationship Change tables](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Updates to GlideEncrypter functionality](https://www.servicenow.com/docs/access?context=glideencrypter-deprecation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The GlideEncrypter API has been updated to use AES256-GCM encryption via the Key Management Framework. If needed, your instance can be changed to use legacy 3DES encryption, but this task can only be done by ServiceNow support.

-   **[Disable GlideEncrypter on your instance](https://www.servicenow.com/docs/access?context=check-3des&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    GlideEncrypter can be enabled or turned off using the **glide.security.glideencrypter.allow** system property. This property is unavailable on new Zurich instances, but administrators with the security\_admin role can edit this property in upgraded instances. When this system property is set to **false**, users see this error when attempting to run GlideEncrypter.

    ```
    Unsupported call to GlideEncrypter. Details: GlideEncrypter is deprecated and now returns null, please refer KB1320986
    ```


## Activation information

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Encryption and Key Management](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.

-   **[Key Management Framework](https://www.servicenow.com/docs/access?context=understanding-kmf&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.

-   **[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Code Signing creates digital signatures for the data, which are later checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of Vault.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


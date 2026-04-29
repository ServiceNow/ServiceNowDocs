---
title: Key Management release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Key Management release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Australia release.

## Encryption Key Management highlights for the Australia release

-   GlideDigest has been updated to allow creation and verification of message digests using the SHA512 cryptographic hash function
-   Admins can share module keys between instances offline to facilitate instance clones between on-premise instances using KMF.
-   The signing and verification processes for JWTs are now integrated as operation types in the existing KMFCryptoOperation class.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=australia&pubname=australia-platform-security&ft:locale=en-US) for more information.

## Important information for upgrading to Australia

-   In pre-Zurich releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Australia release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Australia instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Australia instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

## New in the Australia release

-   **[Added SHA512 support for message digests](https://www.servicenow.com/docs/access?context=c_GlideDigestScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    GlideDigest has been updated to allow creation and verification of message digests using the SHA512 cryptographic hash function.

-   **Offline key exchange to share module keys between instances**

    Admins can share module keys between instances offline to facilitate instance clones between on-premise instances using KMF.

-   **[Sign and verify JSON web tokens \(JWT\) through KMFCryptoOperation](https://www.servicenow.com/docs/access?context=KMFCryptoOperationBothAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The signing and verification processes for JWTs are now integrated as operation types in the existing KMFCryptoOperation class.

-   **Centralized Crypto Management console**

    Use the new Crypto Management Console to streamline and track the certificate management lifecycle. The new console scans your instance for certificates and displays their details in a central location,

-   **Clone and restore support for on-premise instances**

    Support for cloning and restoring on-premise instances. Support has also been added from migrating a commercial instance to on-premise instances, and vice-versa.

-   **Certificate Revocation List \(CRL\) validation support**

    ServiceNow now supports Certificate Revocation List \(CRL\) validation for certificate revocation checks as an alternative to Online Certificate Status Protocol \(OCSP\), with automatic fallback when OCSP is unavailable.


## Changed in this release

-   **[Updated workflow for creating cryptographic modules](https://www.servicenow.com/docs/access?context=create-cryptographic-module&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Use the streamlined workflow designed for faster, easier creation of cryptographic modules.

-   **[SecurityUtils Enhancements](https://www.servicenow.com/docs/access?context=GlideSecurityUtilsScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The SecurityUtils API has been enhanced to help prevent cross-site scripting attacks, including methods to sanitize and escape input.


## Activation information

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


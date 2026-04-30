---
title: Encryption Release Notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Encryption Release Notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.

## Encryption highlights for the Zurich release

-   Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.
-   Use any of the three Field Encryption APIs to encrypt attachments.

See [Encryption](https://www.servicenow.com/docs/access?context=encryption-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## Important information for upgrading Encryption to Zurich

For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

-   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
-   For instances created with the Zurich release or later, this API isn’t supported.
-   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.

## New in the Zurich release

-   **[Encrypt data using Row Conditions](https://www.servicenow.com/docs/access?context=encrypt-data-using-row-conditions&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.


## Changed in this release

-   **[Field Encryption Enterprise](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) API**

    Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


## Deprecations

-   **[Prepare your instance for GlideEncrypter deprecation](https://www.servicenow.com/docs/access?context=check-3des&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.


## Activation information

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see the [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.


-   **[Key Management Framework Reference](https://www.servicenow.com/docs/access?context=understanding-kmf&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.


-   **[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Code Signing creates digital signatures for the data, which are later checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of Vault.


-   **[Cloud Encryption with Key Management](https://www.servicenow.com/docs/access?context=dare-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Cloud Encryption offers encrypted storage for the database by using block encryption, with enhanced key management. Cloud Encryption is available with the Platform Encryption subscription bundle and the ServiceNow Vault subscription bundle.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


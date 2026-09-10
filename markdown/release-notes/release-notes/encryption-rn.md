---
title: Encryption Release Notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Encryption Release Notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.

## About Encryption

-   Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.
-   Use any of the three Field Encryption APIs to encrypt attachments.

See [Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/encryption-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

    Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see the [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/encryption-sku.md).

-   **Upgrade information**

    For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

    -   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
    -   For instances created with the Zurich release or later, this API isn’t supported.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).
    In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-security-rn-landing.md)

## Zurich

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 validated key protection. Encryption Key Management was enhanced and updated in the Zurich release.

### What's new

-   **[Encrypt data using Row Conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/encrypt-data-using-row-conditions.md)**

    Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.


### What's changed

-   **[Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/now-platform-encryption.md) API**

    Use all three Encryption APIs to encrypt on attachments, without needing to use any one specific API.


### What's deprecated or removed

-   **[Prepare your instance for GlideEncrypter deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/check-3des.md)**

    Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.



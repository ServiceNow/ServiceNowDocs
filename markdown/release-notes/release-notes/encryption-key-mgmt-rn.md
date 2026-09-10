---
title: Encryption Key Management release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Encryption Key Management release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.

## About Encryption Key Management

-   Column Level Encryption has been rebranded and redesigned to now be called Field Encryption.
-   Use Access Observer to help plan for and troubleshoot Field Encryption implementations.
-   Edge Encryption administrators can use the new process to migrate from Edge Encryption to Field Encryption.

See [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/encryption.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

    Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/encryption-sku.md).

-   **Upgrade information**
    -   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
        -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
        -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
        -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)

## Yokohama

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.

### What's new

-   **[Column Level Encryption is now Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/column-level-encryption-landing.md)**

    Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-observer.md)**

    Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/column-level-encryption-landing.md)**

    Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.



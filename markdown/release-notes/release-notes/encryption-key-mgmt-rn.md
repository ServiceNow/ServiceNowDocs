---
title: Encryption Key Management release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Encryption Key Management release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Yokohama release.

## Encryption Key Management highlights for the Yokohama release

-   Column Level Encryption has been rebranded and redesigned to now be called Field Encryption.
-   Use Access Observer to help plan for and troubleshoot Field Encryption implementations.
-   Edge Encryption administrators can use the new process to migrate from Edge Encryption to Field Encryption.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

## Important information for upgrading to Yokohama

-   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
    -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

## New in the Yokohama release

-   **[Column Level Encryption is now Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Column Level Encryption has been rebranded to Field Encryption Starter \(FES\), while Column Level Encryption Enterprise is now Field Encryption Enterprise \(FEE\).

-   **[Access observer](https://www.servicenow.com/docs/access?context=access-observer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Use access observer to understand the people and processes that access data on your instance.

-   **[Improved migration process from Edge Encryption to Field Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Use the new process for migration from Edge Encryption to Field Encryption \(formerly Column Level Encryption\). This improved workflow ensures that your data migrates from Edge Encryption to Field encryption without spending time in an unencrypted state.


## Activation information

The Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Encryption and Key Management](https://www.servicenow.com/docs/access?context=encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.

-   **[Key Management Framework](https://www.servicenow.com/docs/access?context=understanding-kmf&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.

-   **[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Code Signing creates digital signatures for the data, which are later checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of Vault.

-   **[Edge Encryption](https://www.servicenow.com/docs/access?context=edge-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Edge Encryption encrypts sensitive data on your company premises before sending it over the internet to your instance \(encrypted in flight\), where it remains encrypted at rest.

-   **[Cloud Encryption with Key Management](https://www.servicenow.com/docs/access?context=dare-overview&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Cloud Encryption offers encrypted storage for the database by using block encryption, with enhanced key management. Cloud Encryption is available with the Platform Encryption subscription bundle and the ServiceNow Vault subscription bundle.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


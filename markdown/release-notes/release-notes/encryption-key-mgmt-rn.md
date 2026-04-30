---
title: Encryption Key Management release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Encryption Key Management release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the release.

## Encryption Key Management highlights for the Xanadu release

-   Start using Code Signing's improved activation process. You can use the new Code Signing UI page for a faster, streamlined activation.
-   Administer Column Level Encryption with new Column Level Encryption APIs, roles, and administration features. Column Level Encryption logging has been enhanced for improved readability.
-   Download all encrypted attachments as a zip file by using the new **Download All** button.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[New plugin available for Code Signing roles and administrative features](https://www.servicenow.com/docs/access?context=cs-role-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Activate the plugin to access the new roles and administration features. The new plugin creates signature migration jobs, new code signing roles, and a new code signing administration page.


## Changed in this release

-   **[Changes to Code Signing requirements](https://www.servicenow.com/docs/access?context=code-signing-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    As a part of improving security around Root of Trust, signing of script and attachments records can only be done on your trusted non-production instance or using the standalone signing tool. The exception is notarization, which can still be performed in the protected production instance.

-   **[Enhancement requests for the Code Signing Standalone signing tool](https://www.servicenow.com/docs/access?context=sa-code-signing-tool&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Updates to Code Signing enable your administrators to work with keystores, signature records, and records to be signed outside of the local system.

-   **[Improved activation process for Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Activate Code signing with a new UI page that is designed to streamline the activation process.

-   **[Download All Button for Multiple Attachments is available when Edge Encryption is enabled](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionOverview&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    By using the download all functionality, you can now download multiple documents into a zip file when you also enable Edge Encryption.

-   **[Edge Encryption jRobin dashboards have been migrated to NEXT Experience](https://www.servicenow.com/docs/access?context=code-signing-reference&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    View troubleshooting and performance on dashboards that were migrated from the deprecated jRobin framework. These dashboards display the same information that was available in previous versions.

-   **[Column Level Encryption Enterprise is installable by administrators after purchase](https://www.servicenow.com/docs/access?context=activate-platform-encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    After purchasing Column Level Encryption Enterprise, your administrator can typically activate the product without needing technical assistance.

-   **[Support for full string UTF-8 in Column Level Encryption](https://www.servicenow.com/docs/access?context=set-encrypted-field-config&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    CLE supports encryption and decryption of the full range of UTF-8 characters, including emoji.

-   **[Improved readability for Column Level Encryption logging](https://www.servicenow.com/docs/access?context=code-signing-reference&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    With the improved system, node, application, and audit logging, your administrators can analyze and troubleshoot their CLE or CLEE implementation.


## Activation information

The Platform Encryption subscription bundle is a group commercial entitlement that includes Column Level Encryption Enterprise, Cloud Encryption, and Database Encryption.

Column Level Encryption Enterprise is the unlimited license of Column Level Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Encryption and Key Management](https://www.servicenow.com/docs/access?context=encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.

-   **[Key Management Framework](https://www.servicenow.com/docs/access?context=understanding-kmf&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.

-   **[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Code Signing creates digital signatures for the data, which are later checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of Vault.

-   **[Edge Encryption](https://www.servicenow.com/docs/access?context=edge-encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Edge Encryption encrypts sensitive data on your company premises before sending it over the internet to your instance \(encrypted in flight\), where it remains encrypted at rest.

-   **[Cloud Encryption with Key Management](https://www.servicenow.com/docs/access?context=dare-overview&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Cloud Encryption offers encrypted storage for the database using block encryption, with enhanced key management. Cloud Encryption is available with the Platform Encryption subscription bundle.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


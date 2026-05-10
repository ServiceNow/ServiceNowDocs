---
title: Encryption release notes
description: The ServiceNow Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Encryption release notes

The ServiceNow® Encryption Key Management application protects your data by using encryption, tightly controlled key access, National Institute of Standards and Technology \(NIST\) 800-57-based key life-cycle management, and FIPS 140-2-L3 key protection. Encryption Key Management was enhanced and updated in the Australia release.

## Encryption highlights for the Australia release

-   ManageField Encryption and Field Encryption Enterprise using the redesigned user interface.
-   Enhance data security with the newly added External Key Management Service \(EKMS\) integration, enabling you to store encryption keys outside the instance for enhanced security.

See [Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/encryption-landing.md) for more information.

## New in the Australia release

-   **[Manage Field Encryption Enterprise with an enhanced Administration interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-platform-encryption.md)**

    Configure encryption settings, monitor key usage, and streamline administration for Field Encryption and Field Encryption Enterprise with the following features:

    -   Simplify key rotation and policy updates.
    -   Access encryption status and audit details.
    -   Navigate improved layouts for faster configuration.
-   **[Integrate External Key Management Service \(EKMS\) with Encryption Modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ekms-external-key-management.md)**

    Configure and manage encryption keys externally through EKMS integration with an enhanced encryption framework, which enables you to:

    -   Hold encryption keys outside the instance for improved security.
    -   Perform key rotation and revocation with automated security tasks.
    -   Manage EKMS configurations and enforce the immutability of critical fields after they're active.
    -   Simplify rekeying following instance clone and restore operations.
    -   Monitor key state transitions, encrypted cache, and node-to-node communication.
    -   Access UI improvements for configuration visibility and error handling.
    -   Benefit from telemetry and performance-tested operations.

## UI changes

-   **[Field Encryption user interface changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-platform-encryption.md)**

    The new Field Encryption and Field Encryption Enterprise UI includes updates to key rotation and policies, access to encryption status and audit details, and changes to layouts.


## Activation information

Platform Encryption is available with activation of the com.glide.encryption.external\_kms, which requires a separate subscription. For details, see [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/encryption-sku.md).

## Plugin information

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    -   Column Level Encryption \(com.glide.encryption\): Planned for deprecation in the C release. Activate the Field Encryption Starter or Field Encryption Enterprise plugins instead.
    -   Column Level Encryption Enterprise\(com.glide.now.platform.encryption\): Planned for deprecation in July 2031. Activate the Field Encryption Starter or Field Encryption Enterprise instead.
    -   [Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EdgeEncryptionOverview.md) \(com.glide.edgeencryption\): Planned for deprecation in December 2028.Use Platform Encryption instead. For more information, see the [Edge Encryption End of Renewal \[KB2007685\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article on the Now Support Knowledge Base.
    -   [Edge Encryption Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EdgeEncryptionOverview.md) \(com.glide.edgeencryption.core\): Planned for deprecation in December 2028. Use Platform Encryption instead. For more information, see the [Edge Encryption End of Renewal \[KB2007685\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article on the Now Support Knowledge Base.

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


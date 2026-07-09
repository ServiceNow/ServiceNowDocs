---
title: Code Signing release notes
description: The Code Signing application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Code Signing release notes

The Code Signing application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Yokohama release.

## Code Signing highlights for the Yokohama release

Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.

See [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/code-signing-landing.md) for more information.

## Changed in this release

-   **[Enhancements to the guardrails check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/cse-ppi-config.md)**

    The Code Signing Guardrails check has been improved to enhance signature verification, resulting in more secure workflows. In addition, multiple optimizations have been implemented to improve the performance benchmarks of the Guardrails scan, and log files now feature a more intuitive naming convention, which simplifies file identification within your system.


-   **[Generate update sets with a maximum size of 10,000 records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/cse-turn-on-cse.md)**

    Code Signing now enforces limits on large update sets to improve the user experience. The maximum size for an update set is 10,000 records.


-   **[Naming updates for trusted and production instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/code-signing-landing.md)**

    The trusted non-production instance has been renamed to trusted instance, and the protected production instance has been renamed to protected instance. These naming updates have been made to better align with customer usage.


## Activation information

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/config-code-signing.md).

## Related ServiceNow applications and features

-   **[Encryption and Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/encryption.md)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.

-   **[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/understanding-kmf.md)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.

-   **[Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/edge-encryption.md)**

    Edge Encryption encrypts sensitive data on your company premises before sending it over the internet to your instance \(encrypted in flight\), where it remains encrypted at rest.

-   **[Cloud Encryption with Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/dare-overview.md)**

    Cloud Encryption offers encrypted storage for the database by using block encryption, with enhanced key management. Cloud Encryption is available with the Platform Encryption subscription bundle.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)


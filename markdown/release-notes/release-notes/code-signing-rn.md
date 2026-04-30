---
title: Code Signing release notes
description: The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Code Signing release notes

The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.

## Code Signing highlights for the Zurich release

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Code Signing OOB Apps Signatures plugin](https://www.servicenow.com/docs/access?context=explore-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US#cs-validation-jobs)**

    Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.


-   Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.
-   Use the Code Signing Migration workflow to identify the signatures that are created with expired or inactive certificates and re-assign them to the appropriate records automatically.
-   Revoke Code Signing certificates securely using a quorum-based approval policy to prevent unauthorized use.
-   Monitor and manage your Code Signing environment with the new Health and Status dashboard.
-   The restructured navigation panel and the renamed pages provide improved accessibility and streamlined functionality.

## New in the Zurich release

-   **Code Signing Installation using Plugin**

    Customer administrators can now install the Code Signing plugin directly from the ServiceNow Plugin portal without the need to contact the Customer Service and Support team to enable the Code Signing framework. This enhancement supports self-service deployment and simplifies the installation process.

-   **[Quorum Controlled Certificate Revocation](https://www.servicenow.com/docs/access?context=certificate-revocation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Revoke Code Signing certificates using a quorum-based control policy. Revoke certificates to help prevent them from being used to verify signatures. A quorum-based approval flow promotes added security by requiring approvals from multiple stakeholders, to help prevent unintended or unauthorized certificate revocations.

-   **[Code Signing Health and Status Dashboard](https://www.servicenow.com/docs/access?context=code-signing-health-and-status-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The new **Code Signing Health and Status** dashboard provides a centralized, user-friendly interface to monitor the overall health and configuration of your code signing environment. It highlights configuration settings, displays the status of essential components, and offers actionable guidance to help resolve issues effectively.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://www.servicenow.com/docs/access?context=config-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.


## Activation information

Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configuring Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Encryption and Key Management](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Encryption is a cryptographic procedure that converts plain text into cipher text, which helps prevent anyone but the intended recipient from reading that data.

-   **[Key Management Framework](https://www.servicenow.com/docs/access?context=understanding-kmf&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The Key Management Framework lets you fully customize and manage how cryptographic operations are performed on your instance.

-   **[Edge Encryption](https://www.servicenow.com/docs/access?context=edge-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Edge Encryption encrypts sensitive data on your company premises before sending it over the internet to your instance \(encrypted in flight\), where it remains encrypted at rest.

-   **[Cloud Encryption with Key Management](https://www.servicenow.com/docs/access?context=dare-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Cloud Encryption offers encrypted storage for the database by using block encryption, with enhanced key management. Cloud Encryption is available with the Platform Encryption subscription bundle.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)


---
title: Code Signing release notes
description: The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Code Signing release notes

The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.

## About Code Signing

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Code Signing OOB Apps Signatures plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/explore-code-signing.md#cs-validation-jobs)**

    Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.


-   Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.
-   Use the Code Signing Migration workflow to identify the signatures that are created with expired or inactive certificates and re-assign them to the appropriate records automatically.
-   Revoke Code Signing certificates securely using a quorum-based approval policy to prevent unauthorized use.
-   Monitor and manage your Code Signing environment with the new Health and Status dashboard.
-   The restructured navigation panel and the renamed pages provide improved accessibility and streamlined functionality.

## Activation and other requirements

-   **Activation information**

    Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. For details, see [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/config-code-signing.md).


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-security-rn-landing.md)

## Zurich

The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Zurich release.

### What's new

-   **Code Signing Installation using Plugin**

    Customer administrators can now install the Code Signing plugin directly from the ServiceNow Plugin portal without the need to contact the Customer Service and Support team to enable the Code Signing framework. This enhancement supports self-service deployment and simplifies the installation process.

-   **[Quorum Controlled Certificate Revocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/certificate-revocation.md)**

    Revoke Code Signing certificates using a quorum-based control policy. Revoke certificates to help prevent them from being used to verify signatures. A quorum-based approval flow promotes added security by requiring approvals from multiple stakeholders, to help prevent unintended or unauthorized certificate revocations.

-   **[Code Signing Health and Status Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/code-signing-health-and-status-dashboard.md)**

    The new **Code Signing Health and Status** dashboard provides a centralized, user-friendly interface to monitor the overall health and configuration of your code signing environment. It highlights configuration settings, displays the status of essential components, and offers actionable guidance to help resolve issues effectively.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Enhanced Code-Signing Verification for ACC Framework Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/config-code-signing.md)**

    You can now generate KMF signature files for tables that extend Agent Client Collector Configuration \(`sn_agent_configuration_file`\) and Agent Client Collector Plugin \(`sn_agent_asset`\). This enhancement allows attachments from the tables to successfully pass code-signing verification and be downloaded to the MID Server when code signing is enabled.



---
title: Code Signing release notes
description: The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Australia release.The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Code Signing release notes

The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Australia release.

## About Code Signing

-   Gain complete visibility into Code Signing coverage by proactively identifying eligible records with missing signatures using the optimized guardrail scan.
-   Install build time signatures for records in all trued-up ServiceNow Store application versions, thus eliminating the self-signing process.
-   Ensure reliable script verification by supporting multiple signatures for a record across certificates. Reduce upgrade failures and improve compliance for customers using custom and ServiceNow® certificates.

See [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/code-signing-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Code Signing is a ServiceNow AI Platform feature that is available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\). For details, see [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/config-code-signing.md).


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-security-rn-landing.md)

## Australia

The Code Signing \(CS\) application validates scripts and code that runs on your instance. Code Signing was enhanced and updated in the Australia release.

### What's new

-   **[Utilities Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/code-signing-utilities.md)**

    Use the **Utilities Dashboard** tab within the Code Signing Health and Status dashboard to monitor signature status, detect configuration issues, and maintain the overall health of your Code Signing environment.

-   **[Multiple signatures for a record across certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/signature-verification-in-code-signing.md)**

    Leverage support for multiple signatures for records across different certificates, thus ensuring that valid signatures from any trusted source are recognized. Allow multiple signatures to be added to a record and have the system determine validity by evaluating all existing signatures from newest to oldest.

-   **[Code Signing OOB Apps Signatures plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explore-code-signing.md#cs-validation-jobs)**

    Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.

-   **[New key pair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/code-signing-certificates.md)**

    A new cryptographic key pair is generated to strengthen the Circle of Trust and to ensure a secure signing process. You can see this key pair within the **Key Pair and Certificates** tab of the **Code Signing Health and Status** dashboard.

-   **[Wild Card Purpose for KMF Signature Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explore-code-signing.md#sign-update-set)**

    Use the "Wild Card Purpose" entry in the signature configurations to eliminate import warnings for script includes and business rules.

-   **[Code signing for probes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/sign-files-nonprod.md)**

    Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.


### What's changed

-   **[Guardrail process optimization and scope increase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/signature-verification-status.md)**

    Allows you to run the guardrail scan and identify records that have missing signatures, enabling you to proactively address records that are eligible for code signing but remain unsigned. Previously, the system only checked records with existing signatures and marked them as valid or invalid, which meant records without signatures were overlooked. Now, the process starts from the signature configuration itself, every eligible record is checked to see if it has a signature. If a record is missing a signature, it's clearly identified.


### Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Code Signing OOB Apps Signatures \(com.glide.code\_signing.oob\_apps\_signatures\): This plugin installs build time signatures for all relevant records in the trued-upServiceNow® Store application versions.



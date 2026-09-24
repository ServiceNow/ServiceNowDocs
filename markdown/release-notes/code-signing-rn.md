---
title: Code Signing release notes
description: The ServiceNow Code Signing application validates scripts and code that run on your instance to prevent unauthorized or tampered records from being processed. See the following sections for release notes by version.Generate Code Signing signatures automatically during a source control commit, and review a change audit trail for the records that Code Signing protects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/code-signing-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Code Signing, source control, commit, signature generation, ServiceNow Studio, audit trail, change tracking]
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Code Signing release notes

The ServiceNow® Code Signing application validates scripts and code that run on your instance to prevent unauthorized or tampered records from being processed. See the following sections for release notes by version.

## About Code Signing

-   Prevent unauthorized code execution by enabling cryptographic verification of all scripts on your MID Servers.
-   Detect tampering instantly by identifying modifications to signed records and automatically blocking compromised code.
-   Streamline security enforcement by automating signature verification across integrations without requiring manual intervention.
-   Support compliance needs by maintaining comprehensive audit records of all signature verification events.

See [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Code Signing is a ServiceNow AI Platform feature available with activation of the Code Signing \(com.glide.code\_signing\_enterprise\) plugin. Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\). For details, see [Configuring Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/config-code-signing.md).


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-security-rn-landing.md)

## Brazil Early Availability

Generate Code Signing signatures automatically during a source control commit, and review a change audit trail for the records that Code Signing protects.

### What's new

-   **[Signature generation during source control commit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_cs_commit_signing.md)**

    Generate Code Signing signatures automatically when you commit application files to source control from a trusted instance. Signatures are created for eligible records during the commit and pushed to the remote repository in the same update set as their source records, so a protected instance can validate the records it receives.

-   **[Code Signing change audit data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-vault-audit-data.md)**

    Review the create, update, and delete operations that users perform on records protected by Code Signing. Each audit record identifies the changed record, the user who changed it, the operation type, and the date and time of the change. Audit data is recorded by default on production instances when Code Signing is active, and users with the codesigning\_auditor role can view and report on it. A scheduled job manages the size of the audit data based on a configurable retention period and maximum record count.



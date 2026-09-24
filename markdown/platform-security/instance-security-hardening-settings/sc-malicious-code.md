---
title: Malicious code
description: The Malicious Code category ensures that best efforts are made to confirm that your code is free of vulnerabilities and unwanted functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-malicious-code.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Malicious code

The Malicious Code category ensures that best efforts are made to confirm that your code is free of vulnerabilities and unwanted functionality.

This includes ensuring secure and proper handling for malicious activity, no time based attacks, no outbound communications to untrusted destinations, and that no unauthorized or attacker-controlled code is included. This category includes audit or third party libraries from the application codebase.

-   **[Apply static analysis to all users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-apply-static-analysis-to-all-users.md)**  
Configure static analysis to examine scripts from both authenticated and unauthenticated users rather than limiting analysis to guest users only.
-   **[Block rooted or jailbroken mobile devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-block-rooted-or-jailbroken-mobile-devices.md)**  
Secure your instance by preventing unauthorized access from jailbroken devices.
-   **[Enable Code Signing for application configuration data and scripts \[Removed in Security Center 1.3\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-code-signing-for-application-configuration-data-and-scripts.md)**  
Manage Code Signing for application configuration data and scripts on your instance.
-   **[Enable static analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-static-analysis.md)**  
Enable static analysis to provide compile-time security checks for JavaScript code in the scripting sandbox.
-   **[Enable synchronous mode for static analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enable-synchronous-mode-for-static-analysis.md)**  
The **com.glide.script.static\_analysis.enable\_sync** property controls whether static analysis security violations block script execution synchronously or are recorded asynchronously. Setting this property to `true` enables synchronous mode, which blocks scripts with security violations.
-   **[Enforce signature verification for Flow Designer artifacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-enforce-signature-verification-for-flow-designer-artifacts.md)**  
The **com.glide.hub.code\_signing.full.validation.enabled** property controls the strictness of checks enforced when Code Signing is fully enabled.

**Parent Topic:**[Hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/security-hardening-settings.md)


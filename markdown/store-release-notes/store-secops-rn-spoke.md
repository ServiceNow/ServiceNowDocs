---
title: Security Operations Spoke release notes
description: Version history for the Security Operations Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-spoke.html
release: store
topic_type: reference
last_updated: "2025-06-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Operations Spoke release notes

Version history for the Security Operations Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.6.7 - June 2025**

    Fixed: Duplicate Knowledge Base \(KB\) numbers created after installing the SIR plugin.

-   **Version 10.6.6 - May 2025**

    Bug fixes with respect to subflow to flow.

-   **Version 10.6.5 - February 2025**

    Changed: Migrated base system workflows to Flow Designer flows.

-   **Version 10.6.3 - June 2024**

    Changed: App dependency was updated from "Security Incident Response Workspace" to "Security Support Common."

-   **Version 10.6.1 - May 2024**

    Fixed: Automated Phishing Playbook - Workflow was stuck and unable to exploit the stack trace.

-   **Version 10.6.0 - February 2024**
    -   New:
        -   Added the following playbooks:
            -   Credential Sniffing
            -   T1070 - Windows Event Logs Cleared
            -   OSQuery External Address in /etc/hosts
            -   User Deleting .bash\_history - Cloud
            -   Successful VPN Attempts from Service Accounts - Corp/Cloud
            -   Attempted Access to Deactivated Accounts
            -   T1003 - Defense Evasion - Mimikatz DCShadow
            -   T1003 - Credential Dumping - Mimikatz Dcsync
            -   Okta User Login Failures from Multiple IPs
            -   ModSec Bruteforce by IP Burst
-   **Version 10.5.8 - November 2023**
    -   New:
        -   Added the following playbooks:
            -   Office 365 - Malicious File Detected
            -   Repeat Detection
            -   Spoofed Emails \(Using the same Display name\)
            -   Endpoint Detection
            -   Possible Password Spray
            -   T1003 - Detect Credential Dumping Tools
            -   Email Spoof Detection
            -   Typo Squatted Domain
-   **Version 10.5.5 - August 2021**
    -   Fixed:
        -   Modified Malware Automation playbook to work without any hard dependency on a specific workflow.
        -   Modified Transform phishing flow to create observables before adding them to a security incident.
-   **Version 10.5.2 - November 2020**

    Changed: Changes as part of the inclusive language initiative.

-   **Version 10.5.0 - September 2020**

    Fixed: Failed login playbook improvements and text formatting changes.

-   **Version 10.3.0 - June 2020**
    -   New: New playbook to generate the final verdict from the automated triage of phishing incidents.
    -   Fixed:
        -   Bug fix for email search query creation in Transform phishing email to security incident flow.
        -   Bug fix for security incidents created by User Reported Phishing flow.
-   **Version 10.0.0 - March 2020**
    -   New:
        -   Failed Login Playbook
        -   Flow for rolling up data from a child security incident to the parent security incident.
-   **Version 9.0.0 - November 2019**

    New: Transformation flow to create security incidents from phishing emails, as a part of URP 2.0.

-   **Version 8.0.9 - June 2019**

    Refer to Security Incident Response release notes for product changes and updates in the Madrid release.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


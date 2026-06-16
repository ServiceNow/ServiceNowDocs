---
title: Check Point Integration for Security Operations release notes
description: Version history for the Check Point Integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-checkpoint.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Check Point Integration for Security Operations release notes

Version history for the Check Point Integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.4.11 - June 2026**

    Fixed: Cobalt Raven Non-Glide Query ACLs Directive.

-   **Version 10.4.10 - August 2025**
    -   Fixed:
        -   Inconsistent status updates that left block requests in "pending" without escalation to blocklist actions.
        -   Handling of subflow triggers to prevent foreground execution delays and optimized system performance.
-   **Version 10.4.3 - November 2024**

    Changed: Migrated base system workflows to Flow Designer flows.

-   **Version 10.4.0 - August 2024**

    Changed: Migrated Enrichment workflows to flow designer.

-   **Version 10.3.4 - February 2023**

    New: Updated to support Security Incident Response workspace.

-   **Version 10.3.2 - November 2020**
    -   Changed:
        -   As part of the inclusive language initiative, the Tag type and Integration Tile configuration have been updated to mention Allow List.
        -   As part of the inclusive language initiative, ATF tests have been updated to mention Allow List.
-   **Version 10.0.1 - May 2020**
    -   New:
        -   Ability to configure HTTPS Trimming in a URL Block List for HTTPS Inspection.
        -   Ability to configure URLs to inherit the domain behavior.
-   **Version 8.1.0 - September 2019**

    New:

    -   Proper implementation of wildcard support and domains for preventing the addition of individual URL blocklist entries
    -   Manually created block list entries should always create an observable entry to link to for Check Point Block Request Integration.
-   **Version 8.0.0 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Bug fixes
-   **Version 5.0.0 - March 2019**
    -   Flexibility to create multiple Block Lists that apply to multiple Check Point Gateways
    -   Detailed reporting on the types of sites being blocked \(phishing, malware, and allow listed sites\)
    -   Tagging of ServiceNow AI Platform security incidents with Block List entries by the observable type \(URL, domain, IP address\)
    -   Configuring Block List expiration periods to maintain Block List size by automatically expiring or removing older entries
    -   Searching Block List entries between different Block Lists
    -   Linking Block List entries to observable records and security incidents that include threat intelligence results and details about why an entry is blocked


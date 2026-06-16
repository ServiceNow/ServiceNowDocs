---
title: Palo Alto Networks NGFW for Security Operations release notes
description: Version history for the Palo Alto Networks NGFW for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-palo-alto.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Palo Alto Networks NGFW for Security Operations release notes

Version history for the Palo Alto Networks NGFW for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.3 - June 2026**

    Fixed: IPv6 CIDR conflict detection.

-   **Version 10.5.2 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.4.7 - May 2025**

    Fixed: Pop-up loop when creating EDL Entry with different Expiration Date than default.

-   **Version 10.4.6 - November 2024**

    Changed: Migration of Workflows to Flow Designer flows.

-   **Version 10.4.2 - February 2023**

    New: Updated to support Security Incident Response workspace.

-   **Version 10.3.1 - November 2020**

    Changed: Updated the Tag type and Integration Tile configuration to use Allow List.

-   **Version 5.0.3 - January 2019**
    -   Provides London version support
    -   Allows for disabling approvals via checkbox on the EDL list configuration
-   **Version 5.0.1 - June 2018**
    -   Flexibility to create multiple External Dynamic Lists \(EDLs\) that apply to different firewall \(FW\) deny or allow policies. This flexibility allows more detailed reporting on submitted sites, e.g., phishing, malware, allow listed sites.
    -   Tagging ServiceNow incidents that contain EDL entries by observable type \(URL, domain, IP address\).
    -   Configuring EDL expiration periods to maintain EDL list size by automatically expiring or removing older entries.
    -   Searching for and removing EDL entries, or migrating EDL entries between EDL lists.
    -   Linking EDL entries to observable records and SIR incidents that include threat intelligence results to determine why an IP, URL, or domain is being blocked.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


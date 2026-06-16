---
title: Security Incident Response Integration with CrowdStrike Next-Gen SIEM release notes
description: Version history for the Security Incident Response Integration with CrowdStrike Next-Gen SIEM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-int-crowdstrike-next-gen-siem.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response Integration with CrowdStrike Next-Gen SIEM release notes

Version history for the Security Incident Response Integration with CrowdStrike Next-Gen SIEM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.4.2 - June 2026**
    -   Fixed:
        -   Presence of Non-ASCII characters affecting WorkNotes sync.
        -   Updates on re-opened detection creating multiple security incidents.
        -   Aggregation Conditions not working as expected in CrowdStrike NG-SIEM Detection Profile.
        -   CrowdStrike NG-SIEM storing rule versions as Correlation rules instead of rules.
        -   Cobalt Raven Non-Glide Query ACLs Directive.
-   **Version 2.4.1 - May 2026**

    Fixed: SIRs are not being created from SIEM ingestion due to "Secure Notes" access issue with the Crypto module since Yokohama upgrade, if System access Module Access policy is not in place.

-   **Version 2.4.0 - March 2026**
    -   New: Handled missing CMDB CIs and User records by attaching Unmatched CI and Unmatched Affected User to the SIR when no corresponding records are found.
    -   Fixed:
        -   Localisation issues.
        -   Issues with Pagination for Correlation Rules.
        -   Better handling of ui message when no Correlation Rules are configured in CrowdStrike.
-   **Version 2.3.1 - December 2025**

    New: Upgraded dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 2.0.2 - October 2025**
    -   Fixed:
        -   Empty SIR records created during aggregation in domain-separated environments.
        -   SIRs not being created when event payloads lacked all detections from the query.
-   **Version 2.0.0 - August 2025**

    The CrowdStrike Next-Gen SIEM Ingestion integration allows you to automatically retrieve incidents from CrowdStrike, convert them into security incidents, and enable automated response actions.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


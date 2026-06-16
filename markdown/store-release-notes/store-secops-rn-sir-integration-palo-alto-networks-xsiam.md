---
title: Security Incident Response Integration with Palo Alto Networks XSIAM release notes
description: Version history for the ServiceNow Security Incident Response Integration with Palo Alto Networks XSIAM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-integration-palo-alto-networks-xsiam.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Incident Response Integration with Palo Alto Networks XSIAM release notes

Version history for the ServiceNow® Security Incident Response Integration with Palo Alto Networks XSIAM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 3.1.3 - May 2026**

    Fixed:Access issues for Security Analyst while querying tables.

-   **Version 3.1.0 - March 2026**
    -   Fixed: Aggregation on the cmdb\_ci or affected\_user field was not attaching all mapped CIs or affected users to the SIR incase multivalue mapping.
    -   Changed: Handling unmatched CI and Unmatched affected users.
-   **Version 3.0.2 - January 2026**
    -   Fixed:
        -   Bidirectional Sync for aggregated incidents.
        -   Issue with related incident closure when the parent SIR is closed.
        -   Loading time issue of alert sources and priority in profiles.
-   **Version 3.0.0 - December 2025**

    The Palo Alto Networks XSIAM SIEM ingestion integration allows you to automatically retrieve incidents from XSIAM, convert them into security incidents, and enable automated response actions.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


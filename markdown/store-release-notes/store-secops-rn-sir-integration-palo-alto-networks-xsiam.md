---
title: Security Incident Response Integration with Palo Alto Networks XSIAM release notes
description: Version history for the ServiceNow Security Incident Response Integration with Palo Alto Networks XSIAM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-integration-palo-alto-networks-xsiam.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# Security Incident Response Integration with Palo Alto Networks XSIAM release notes

Version history for the ServiceNow® Security Incident Response Integration with Palo Alto Networks XSIAM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 3.2.4 - September 2026**
    -   New: Admins can now configure bidirectional field sync between SIR and Palo Alto XSIAM. Up to 32 identified fields in PA XSIAM can be mapped and automatically synchronized with SIR on incident updates. A new UI enables admins to define field mappings, apply transformations, and manage which fields are included. A top-level option allows enabling or disabling automatic sync, and admins can fetch record details for specific incidents or cases to assist with mapping.
    -   A new interface supports SIR to XSIAM field mapping with transformation options. The mapping screen uses a four-column layout for target fields, source fields, transformation selection, and removal controls. Admins can reference either live SIR data or sample data when configuring mappings.
-   **Version 3.2.0 - August 2026**
    -   New: Security Incident war room attachments are now synced from XSIAM Cases into SIR. When a Security Incident is created from an XSIAM Case, all existing war room attachments are automatically fetched and attached. New attachments added to the XSIAM Case are also synced on subsequent polling intervals, with duplicate attachments prevented and metadata preserved.
    -   Work notes added to Security Incidents in SIR are now written directly into the corresponding XSIAM Case war room. Real-time collaboration is enabled by syncing new work notes using the Case-level War Room API, ensuring both systems remain in sync without manual intervention.
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


**Parent Topic:**[ServiceNow Store - Security Incident Response version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


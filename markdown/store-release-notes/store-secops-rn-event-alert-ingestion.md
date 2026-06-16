---
title: Event and Alert Ingestion for Security Operations release notes
description: Version history for the Event and Alert Ingestion for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-event-alert-ingestion.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Event and Alert Ingestion for Security Operations release notes

Version history for the Event and Alert Ingestion for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.2.1 - June 2026**

    Fixed: SIR record creation failures during event ingestion when the secure\_notesfield is mapped, caused by stricter crypto module access policies introduced in the Yokohama release.

-   **Version 11.2.0 - March 2026**
    -   New: Handled missing CMDB CIs and User records by attaching Unmatched CI and Unmatched Affected User to the SIR when no corresponding records are found.
    -   Fixed: Issue with Integration Run records cleanup.
-   **Version 11.0.15 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance the security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 11.0.1 - December 2020**

    Fixed: This release contains minor fixes.

-   **Version 11.0.0 - September 2020**

    Fixed: Minor bug fixes.

-   **Version 10.1.1 - May 2020**

    Changed: Support for related list mapping such as Assignment Group, Assigned to, Category and Sub-Category.

-   **Version 10.0.3 - March 2020**
    -   Create multiple event profiles in your ServiceNow AI Platform instance that permit you to ingest and select sample fired correlated events.
    -   Map Splunk fired correlated events values to associated SIR security incident fields with dynamic drag-and- drop mapping.
    -   Aggregate fired correlated events to existing security incidents when you determine the new notable events are related to existing security incidents.
    -   Validate your mapping with a preview of the alert values in a security incident. You can edit the fields if you are not satisfied with the mapping.
    -   Retrieve historical alerts with a one-time retrieval, or, schedule and ingest on-going, future alerts on configurable intervals.


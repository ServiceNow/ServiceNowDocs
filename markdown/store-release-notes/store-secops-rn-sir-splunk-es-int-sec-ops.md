---
title: Splunk ES Integration for Security Operations release notes
description: Version history for the Splunk ES Integration for Security Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-splunk-es-int-sec-ops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Splunk ES Integration for Security Operations release notes

Version history for the Splunk ES Integration for Security Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.5.1 - June 2026**
    -   Fixed:
        -   Refactored the UI macros and backend logic to correctly distinguish between sample types, removed unreachable dead code, and fixed correlation rule name lookup for multi-rule profiles.
        -   Access issues for Security Analyst while querying tables.
-   **Version 12.5.0 - April 2026**
    -   New:
        -   Handling missing CMDB CIs gracefully by attaching them as Unmatched CI.
        -   New correlation rules in Splunk ES  automatically imported periodically based on system property.
    -   Fixed:
        -   Provided fix for ingestion of Updated Notables which supports Splunk ES version 8.0.x  and later versions.
        -   Added KMF support for encrypted fields like secure notes mapping.
-   **Version 12.4.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 12.3.0 - November 2025**
    -   Fixed:
        -   New splunk upgrade failing xml parsing and blocks SIR creation.
        -   Not able to edit existing Field translations.
-   **Version 12.2.2 - October 2025**
    -   Fixed:
        -   Token restoration bug in SplunkESEventIngestionQueryAbstract.\_buildInputValue corrupts literal values that look like $$ \(e.g., $DOVERIE01$\), leaving \_\_\_\_ placeholders and producing malformed input.
        -   SplunkES LockTable should have profile admin role instead of admin role.
        -   Aggregation bug in case of domain separation.
-   **Version 12.2.1 - September 2025**

    Fixed: Splunk ES update multiple is working in iterative mode. We have added fix to clean up the stale records in internal tables.

-   **Version 12.2.0 - August 2025**
    -   New:
        -   Enabling users with "sn\_si.ingestion\_profile\_admin" role to manage ingestion profiles on Splunk ES Integration.
        -   Update Field values for notable events in splunk ES.
        -   Ability to Aggregate SIR Security Incidents using the "State" field.
        -   Work Notes and Comments Synchronization for Splunk ES.
        -   Splunk ES Bidirectional Updates or Closure.
    -   Fixed:
        -   Aggregation not working in case of OR operator when the first field is empty.
        -   User is able to create multiple field translations for an attribute . Observed this in domain seperation case.
-   **Version 12.1.10 - July 2025**
    -   Fixed:
        -   Issue: The Splunk Enterprise Security \(ES\) process responsible for sending events to the Security Incident Response \(SIR\) job was causing memory contention on nodes, resulting in unexpected node restarts.
        -   Improvement: Performance optimizations were implemented in Splunk ES, effectively resolving the memory contention issue and preventing further node restarts.
-   **Version 12.1.9 - June 2025**
    -   Fixed:
        -   Bug: The Splunk ES process for sending events to the Security Incident Response \(SIR\) job was causing memory contention on nodes, leading to node restarts.
        -   Improvement: Performance improvements were implemented for Splunk ES, which resolved the memory contention issue on nodes.
-   **Version 12.1.6 - May 2025**
    -   Fixed:
        -   The following bugs as part of this release:
            -   Supports adding multiple affected users during Splunk Enterprise event ingestion for Security Operations.
            -   sys\_scope issue on the Xanadu instance that prevented linking a created source to the profile using the sn\_si.admin role.
            -   An issue where the Splunk ES Event Profiles were not updating the existing notables and only new notables were being ingested.
            -   An issue where updated notables were not ingested if the correlation rule name contained a trailing space.
            -   When there is an issue in data for any record in the Splunk raw data table, event import was failing for remaining entries, these remaining entries are now executed as expected.
-   **Version 12.1.1 - November 2024**

    The Splunk ES Event Ingestion integration for Security Operations allows security operations center \(SOC\) analysts to generate ServiceNow AI Platform Security Incident Response \(SIR\) incidents automatically when certain configured Splunk ES Notable Events are triggered. Analysts can also manually forward selected events on-demand from the Splunk ES console. Analysts respond to the security incidents that are created with workflows in the ServiceNow AI Platform that automate incident response activities and remediation.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


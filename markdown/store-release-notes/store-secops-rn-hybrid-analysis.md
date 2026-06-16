---
title: Hybrid Analysis integration release notes
description: Version history for the Security Operations Hybrid Analysis integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-hybrid-analysis.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Hybrid Analysis integration release notes

Version history for the Security Operations Hybrid Analysis integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.6.0 - August 2024**

    Changed: Migrated workflows to flow designer.

-   **Version 10.5.2 - February 2023**

    New: Updated to support the Security Incident Response workspace.

-   **Version 10.5.0 - November 2022**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured duration/period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.3.3 - January 2022**

    Fixed: Migrated Hybrid Analysis APIs from V1 to V2.

-   **Version 10.3.1 - June 2020**

    New: Hybrid Analysis now supports the IPv6 protocol.

-   **Version 10.0.0 - March 2020**

    New: Implementation Flow to support Integration capability framework v2.0.

-   **Version 9.0.1 - December 2019**

    Fixed: Fixed Hybrid Analysis plugin for Threat Intelligence that performs lookups on URLs as domains.

-   **Version 1.0.0 - February 2018**
    -   Automatic threat intelligence lookups on file hashes, IP addresses, and URLs run upon incident creation.
    -   After the application is configured, the workflow launches automatically, and Hybrid Analysis lookup execution and completion status is recorded in work notes on the Security Incident form.
    -   Observables can be looked up manually by attaching them to the Security Incident form and launching workflows.
    -   Results display under the Threat Lookup Results tab at the bottom of the Security Incident form. Child observables and raw Hybrid Analysis lookup details display in the Show IOC link in Related Links.


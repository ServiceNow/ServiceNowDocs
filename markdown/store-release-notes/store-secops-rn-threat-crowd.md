---
title: ThreatCrowd integration release notes
description: Version history for the Security Operations Threat Crowd integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-threat-crowd.html
release: store
topic_type: reference
last_updated: "2023-02-02"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# ThreatCrowd integration release notes

Version history for the Security Operations Threat Crowd integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

**Note:**

Beginning in May 2023, the ThreatCrowd integration has been deprecated and is no longer supported.

## Version history

-   **Version 10.4.1 - February 2023**

    New: Added supporting changes for the Security Incident Response workspace.

-   **Version 10.4.0 - November 202**
    -   New:
        -   Introducing a filter that allows running automated threat lookup on an observable only once within a configured duration. Any re-runs for the same observable will be skipped until the configured duration/period has passed.
        -   Introducing a threat lookup finding calculator, which calculates the findings based on the responses received. For third-party integrations that provide the computed results, the threat lookup finding calculator maps the results to supported findings in the system.
-   **Version 10.0.0 - March 2020**
    -   Fixed:
        -   Improved error handling of non existent observables.
        -   Rate limiting the queries made to ThreatCrowd.
        -   Description and Integration Configuration updates.
-   **Version 5.0.12 - September 2019**
    -   Fixed:
        -   Improved error handling of nonexistent observables
        -   Rate limiting the queries made to ThreatCrowd
        -   Description and Integration Configuration updates
-   **Version 1.0.0 - February 2018**
    -   Supports threat intelligence lookups for URLs, IPs, hashes, and email addresses.
    -   After the application is configured, the workflow launches automatically, and Threat Crowd lookup execution and completion status is recorded in work notes on the Security Incident form.
    -   Observables can be looked up manually by adding them to the Security Incident form and launching workflows.
    -   Results display under the Threat Intelligence Results tab along with raw Threat Crowd lookup details.
    -   Supported observable types include:
        -   IP address
        -   URL
        -   Domain
        -   Email address
        -   File hashes
        -   Antivirus detections

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)


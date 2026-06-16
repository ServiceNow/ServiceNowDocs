---
title: DLP Incident Response integration with Proofpoint release notes
description: Version history for the DLP Incident Response integration with Proofpoint on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-dlp-incident-response-proofpoint.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# DLP Incident Response integration with Proofpoint release notes

Version history for the DLP Incident Response integration with Proofpoint on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - June 2026**
    -   Fixed:
        -   Fixed the issue of simultaneous incident update callbacks and response actions triggering multiple login requests, causing token expiration and invalidating the response action call.
        -   Fixes related to Cobalt Raven Non-Glide Query ACL directives, ensuring proper ACL enforcement for non-Glide query operations.
-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 1.0.15 - May 2025**

    New: Provided additional support for Proofpoint Data Loss Prevention Incidents from Non-US regions.

-   **Version 1.0.14 - April 2025**

    Fixed :

    Provided Support for OAuth 2 Proofpoint authentication.

-   **Version 1.0.13 - February 2025**
    -   New:
        -   Evidence File Preview with Download Option:
            -   Added a preview icon for evidence files in the DLP Workspace.
                -   Users can now preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.
-   **Version 1.0.11 - November 2024**

    New: The integration now supports Evidence File Storage in ServiceNow which includes the implementation of Proofpoint Evidence File external storage, by enabling better management and accessibility of evidence files.

-   **Version 1.0.8 - February 2024**
    -   New:
        -   Added correlation ID mapping for the DLP incidents in the transform map.
        -   Added support of the DLP incidents archival.
-   **Version 1.0.6 - November 2023**

    New: Previously, the endpoint incidents created by Proofpoint were only supported but now the application also supports the email type events from Proofpoint.

-   **Version 1.0.3 - August 2022**

    New: Allow Setting from DLP core whether to display matched content on form or not for integrations,

-   **Version 1.0.1 - May 2022**
    -   New:
        -   Import DLP incidents from Proofpoint to provide an incident response workflow for customers.
        -   Support incidents created by data-at-rest scan from Proofpoint at near-real-time and on-demand scan for cloud and email.
        -   Support endpoint incidents created by Proofpoint.
        -   Provides the ability to perform actions from within the DLP end-user portal for end-users.


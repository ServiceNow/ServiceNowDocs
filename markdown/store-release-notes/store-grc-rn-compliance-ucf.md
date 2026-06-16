---
title: GRC: Compliance UCF release notes
description: Version history for the GRC: Compliance UCF on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-compliance-ucf.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Compliance UCF release notes

Version history for the GRC: Compliance UCF on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026**
    -   New:
        -   This release introduces the following enhancements:
            -   Enhanced application security by enabling query range ACLs for all relevant tables.
    -   Fixed:
        -   This release resolves the following issues:
            -   UCF integration creating empty mappings in the Citation to Control Objective M2M table.
-   **Version 21.1.0 - December 2025 \(Zurich\)**

    Fixed: This update addresses and resolves previously identified security issues.

-   **Version 21.0.0 - August 2025**

    Fixed Issues: Resolved resource contention issues in UCF import process by implementing a custom queue.

-   **Version 20.1.0 - May 2025**

    Fixed: Schedule job should be run as admin user.

-   **Version 20.0.1 - February 2025**

    Changed: When authority documents/citations/control objectives are imported from common controls hub, duplicate citations are not created.

-   **Version 19.0.0 - August 2024**

    Fixed: Security improvements to ensure the authorization key is not accessed outside the scope of the application.

-   **Version 17.0.0 - August 2023**

    Removed: OAuth authentication for integrating with common controls hub APIs

-   **Version 16.0.0 - February 2023**

    Fixed: Reduction in installation size of the application.

-   **Version 14.1.0 - March 2022**

    Fixed: Ability to download more than 100 authority documents using multiple shared lists

-   **Version 13.0.0 - September 2021**

    Fixed: UCF-tracked controls API not returning latest controls mapped to Authority documents.

-   **Version 12.0.1 - June 2021**

    Fixed: A UCF import error caused the deletion of shared list and deactivated all UCF related records \(authority document, citation, control objective, control\)

-   **Version 12.0.0 - March 2021**

    Fixed: Added property to UCF Download Wait Time.

-   **Version 11.1.0 - December 2020**

    Changed: Encryption of Password \(2 Way\) fields using KMF. For details, see KB0542976.

-   **Version 11.0.0 - October 2020**

    Fixed: UCF Import fails when attachment extensions defined in property 'glide.attachment.extensions'

-   **Version 10.1.0 - June 2020**

    Fixed: Fixed report\_view ACLs for sensitive platform tables

-   **Version 10.0.0 - March 2020**

    New: This application is compatible with Orlando

-   **Version 9.0.0 - November 2019**

    This application was updated in the Jakarta family release and is still compatible with New York.



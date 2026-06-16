---
title: Accounts Payable Operations Integration with Oracle release notes
description: Version history for the Accounts Payable Operations Integration with Oracle application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fca-accounts-payable-operations-oracle.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Accounts Payable Operations Integration with Oracle release notes

Version history for the Accounts Payable Operations Integration with Oracle application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.1 - June 2026**
    -   Fixed:
        -   Integration service job tracker records are not marked as failed for the following subflows when they encounter an internal server error or similar server-side errors:
            -   Fetch invoice payment status from Oracle EBS
            -   Fetch AP invoices from Oracle EBS
-   **Version 2.1.0 - December 2025**
    -   Changed: Added granular roles to system properties in accordance with new directives
    -   Fixed: Removed hard-coded timeout values to improve configurability and system flexibility.
-   **Version 2.0.3 - August 2025**

    Minor Fixes: Updated all error messages in the script includes to use gs.getMessage for translation

-   **Version 2.0.2 - May 2025**

    Minor bug fixes patch release.

-   **Version 2.0.1 - October 2024**
    -   New:
        -   Added integration to create invoices from ServiceNow APO into Oracle
        -   Added integration to fetch invoice payment details from Oracle into APO
-   **Version 1.1.0 - August 2024**
    -   New:
        -   Fetch AP Invoices - Mapping Changes
        -   Fetch Invoice Payment Status
-   **Version 1.0.1 - July 2024**

    This application enables bi-directional integration between Accounts Payable Operations to Oracle EBS/Oracle Fusion and allows you to create, update invoices.



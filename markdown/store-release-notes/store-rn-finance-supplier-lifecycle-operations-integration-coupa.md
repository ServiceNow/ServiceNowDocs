---
title: Supplier Lifecycle Operations Integration with Coupa release notes
description: Version history for the Supplier Lifecycle Operations Integration with Coupa application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-supplier-lifecycle-operations-integration-coupa.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Supplier Lifecycle Operations Integration with Coupa release notes

Version history for the Supplier Lifecycle Operations Integration with Coupa application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - June 2026**
    -   New:
        -   Added Create Supplier Payment Information subflow in Coupa.
        -   Added Create or Update Supplier Location flow in Coupa.
    -   Fixed:
        -   Added ERP source validation check in Create, Update, or Deactivate Supplier flow to ensure non-empty values.
        -   Removed address field mappings from Create, Update, or Deactivate Supplier subflow.
-   **Version 2.1.1 - December 2025**

    New: Added sn\_so \(Supplier Operations\) as a dependent plugin for Supplier Lifecycle Operations Integration with the Coupa application.

-   **Version 2.1.0 - August 2025**
    -   New:
        -   Supplier Lifecycle Operations Integration with Coupa enables you to perform the following:
            -   Create a supplier
            -   Update supplier details
            -   Look up and pull the supplier's details
            -   Lookup supplier payment details
            -   Deactivate the supplier and related information \(For example, banking information\)
-   **Version 2.0.0 - March 2025**
    -   New:
        -   Added an integration to create suppliers from ServiceNow Supplier Lifecycle Operations \(SLO\) into Coupa
        -   Added an integration to fetch supplier details from Coupa into ServiceNow Supplier Lifecycle Operations \(SLO\)
-   **Version 1.0.0 - November 2024**

    This application enables bidirectional integration between Supplier Lifecycle Operations \(SLO\) and Coupa allowing you to create and update supplier data.



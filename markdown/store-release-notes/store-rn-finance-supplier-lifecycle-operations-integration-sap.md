---
title: Supplier Lifecycle Operations Integration with SAP release notes
description: Version history for the Finance Operations Management Supplier Lifecycle Operations Integration with SAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-supplier-lifecycle-operations-integration-sap.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Supplier Lifecycle Operations Integration with SAP release notes

Version history for the Finance Operations Management Supplier Lifecycle Operations Integration with SAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.10 - December 2025**

    Fixed: Added sn\_so \(Supplier Operations\) as a hard dependency for Supplier Lifecycle Operations Integration with SAP. This plugin now contains the Supplier Outbound table needed for SAP supplier job triggers, previously located in sn\_slm.

-   **Version 3.0.8 - November 2025**

    Fixed: Minor fixes

-   **Version 3.0.6 - August 2025**
    -   Fixed:
        -   Addressed the creation of duplicate records.
        -   Modified the flow to improve performance.
-   **Version 3.0.4 - June 2025**
    -   Fixed:
        -   The integration status was not being updated to "Inprocess" before the supplier data was sent to the ERP system.
        -   Deprecation of the negative flows, which were used for retry functionality in Create Supplier.
        -   The "Create Supplier in ERP" flow was being triggered multiple times when the "Sync to ERP" action was performed, leading to inconsistent integration status updates in the Supplier outbound table.
-   **Version 3.0.2 - March 2025**
    -   New:
        -   Create and update supplier details from ServiceNow to SAP ECC and S4 HANA
        -   Create and update supplier location from ServiceNow to SAP ECC and S4 HANA
        -   Create and update payment information from ServiceNow to SAP ECC and S4 HANA
        -   Create and update legal entity from ServiceNow to SAP ECC and S4 HANA
        -   Lookup supplier details from SAP ECC and S4 HANA to ServiceNow
-   **Version 3.0.1 - January 2025**
    -   New:
        -   Create and update supplier details from ServiceNow to SAP ECC and S4 HANA
        -   Create and update supplier location from ServiceNow to SAP ECC and S4 HANA
        -   Create and update payment information from ServiceNow to SAP ECC and S4 HANA
        -   Create and update legal entity from ServiceNow to SAP ECC and S4 HANA
        -   Fetch supplier details from SAP ECC and S4 HANA to ServiceNow
-   **Version 3.0.0 - October 2024**
    -   New: Created integrations to support SAP ECC and S4 HANA with ServiceNow.
    -   Changed:
        -   Updated the SAP RFC connector to support the new integration framework.
        -   Added tables to the integration framework to capture supplier details such as payment information, legal entity, locations, and so on.
-   **Version 1.0.0 - July 2023**

    This application provides you with the ability to send suppliers that are created or updated in Supplier Lifecycle Operations to SAP ECC and SAP S4 HANA.



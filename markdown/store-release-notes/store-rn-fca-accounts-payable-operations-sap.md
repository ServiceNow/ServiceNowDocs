---
title: Accounts Payable Operations Integration with SAP release notes
description: Version history for the Finance Operations Management Accounts Payable Operations Integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fca-accounts-payable-operations-sap.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Accounts Payable Operations Integration with SAP release notes

Version history for the Finance Operations Management Accounts Payable Operations Integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.0 - June 2026 \(Australia\)**

    Fixed: Implemented Directive DIRS0000421 – Non-Glide Cobalt Raven ACLs in Product Code, along with the corresponding true-up support enhancements.

-   **Version 2.3.4 - March 2026**
    -   New: Added functionality to cancel invoices from SAP ECC through the Accounts Payable Operations \(APO\) integration.
    -   Fixed: Applied a fix to address the security directive, ensuring compliance with security requirements.
-   **Version 2.3.0 - January 2026**
    -   New: Added functionality to Cancel Invoice in SAP OData Subflow.
    -   Fixed: Removed all unnecessary 'gs.info' log messages to improve code cleanliness.
-   **Version 2.1.0 - December 2025**
    -   New: Created the Authorize Payment subflow for payment hold removal in SAP.
    -   Changed: Added granular roles to system properties in accordance with new directives.
    -   Fixed: Removed hard-coded timeout values to improve configurability and system flexibility.
-   **Version 2.0.12 - November 2025**
    -   Minor Fixes:
        -   1. Script include changes regarding gs.getMessage - APO
        -   2. Explicit status field update on invoice line throws error in the create invoice old PSM flow
        -   3. An Integration Error task such as "Error creating invoice receipt in ERP :" is getting created after successful Invoice creation. \(This issue is happening for PO Invoice, Non-PO Invoice and Credit Memo\) \(Spoke - SAP ECC S2PO\)
        -   4. Incorrect data pill is mapped in subflow to check status code in Create Invoice in SAP ECC v2 subflow
-   **Version 2.0.9 - August 2025**
    -   Minor fixes:
        -   Create Invoice HANA RFC,IDOC and ECC IDOC- Code need to be modified as tax code field deprecated\(tax\_code\) getting used in Washington and new field\(tax\_code\_ob\_inv\) introduced in Xanadu version
        -   Explicit status field update on invoice line throws error in the create invoice old PSM flow
-   **Version 2.0.5 - June 2025**

    Minor bug fixes to address UI issues in Purchase Order form actions load.

-   **Version 2.0.4 - May 2025**

    Minor bug fixes patch release. No improvements in this version.

-   **Version 2.0.3 - January 2025**
    -   New:
        -   Invoices created in Accounts Payable Operations can be sent synchronously or asynchronously to SAP ECC and SAP S/4HANA
        -   Errors from SAP ECC and SAP S/4HANA are captured and displayed as tasks on the invoice object
        -   Invoices created in ERP can be pulled into ServiceNow
        -   Invoice payments details can be pulled from ERP into ServiceNow
        -   Integration using SAP IDOC, RFC, ODATA Connectors is supported
-   **Version 2.0.2 - November 2024**

    Fixed: Updated integration to correctly send shipping, discount and other charges into SAP.

-   **Version 2.0.0 - October 2024**
    -   New: Created integrations to support ODATA connectors
    -   Changed: Updated the RFC connector to support the new integration framework
    -   Fixed: Fixed issue to ensure that the ERP posting date is correctly populated in ServiceNow
-   **Version 1.1.1 - January 2024**

    New: Resubmit for errored records is now available in the respective plugins.

-   **Version 1.1.0 - October 2023**

    New: Ability to integrate using SAP IDOC connectors.

-   **Version 1.0.0 - July 2023**
    -   Initial release.
    -   New: Send payables invoices created in Accounts Payable Operations synchronously or asynchrnously to SAP ECC and SAP S4 HANA.


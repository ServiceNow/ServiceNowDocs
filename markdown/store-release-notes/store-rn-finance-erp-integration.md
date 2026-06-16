---
title: Finance - ERP Integration Framework release notes
description: Version history for the Finance Operations Management Finance - ERP Integration Framework on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-erp-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Finance - ERP Integration Framework release notes

Version history for the Finance Operations Management Finance - ERP Integration Framework on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 19.0.3 - June 2026 \(Australia\)**

    New: Added Access Control Lists \(ACLs\) to support the Non‑Glide Cobalt Raven Brazil directive.

-   **Version 18.0.4 - June 2026**

    New: Added Access Control Lists \(ACLs\) to support the Non‑Glide Cobalt Raven Brazil directive.

-   **Version 17.12.0 - March 2026**
    -   New: Implemented Automated Test Frameworks \(ATFs\) for Cost Center and Legal Entity.
    -   Changed: Updated inbound PRL and PO processing to create missing Buyer Group primary data automatically.
-   **Version 17.5.0 - January 2026**
    -   Changed:
        -   Updated inbound staging fields and tables to support Buyer Group data changes.
        -   Added a new field and corresponding transform mapping to improve supplier data handling.
        -   Added new staging tables for Buyer Group entities to enable processing and validation of buyer group data.
-   **Version 17.0.5 - December 2025**
    -   New:
        -   Added the missing contract entity option in the ERP Source configuration for integration service record creation
        -   Added missing 'sn\_fcms\_intg.admin' ACL for ERP Plant Address mapping table
        -   Implemented security fixes.
        -   Added metrics to track customers with the ERP Integration Framework installed
        -   Added metrics to track system usage by customers connecting through OOB spokes versus FSC spokes
        -   Added metrics to track which systems customers connect to via out-of-the-box spokes
        -   Created metrics to track systems configured using the ERP Integration Framework
        -   Analyzed and implemented Purchase Requisition inbound cost allocation functionality
        -   Implemented generic atomicity behavior for Purchase Requisition tables
        -   Created transform maps to transfer data from Purchase Requisition Inbound Header and Line tables to base tables
        -   Developed outbound flow for Purchase Requisition processing
        -   Created an integration table for Purchase Requisition Header outbound processing
        -   Implemented comprehensive Purchase Requisition inbound and outbound flows with staging tables and transform maps
        -   Created module and UI actions for retry functionality in error handling
        -   Implemented a retry mechanism for Purchase Order entities with scheduled jobs and error list screen options for single or multiple record retry
        -   Added retry logic for failed records in Purchase Order fetch operations
        -   Created a custom hook for Purchase Order inbound flows to enable extra mapping without cloning subflows
        -   Implemented data gathering action for dynamic choice fields to address customer needs for hooking additional fields without cloning workflow components
    -   Changed:
        -   Granted sub-administrative roles for sourcing tasks instead of the admin role, updating system property access controls
        -   Decoupled fulfiller roles for integration flows to improve security and role management
        -   Updated system properties with granular role changes per new security directives for ERP integration admin role
        -   Changed the hard-coded grace period in Ariba flows to a custom configuration
        -   Implemented remaining changes for Standard versus Professional classification for ERP Integration and Source-To-Pay Integration frameworks
        -   Enhanced granular admin controls.
    -   Fixed:
        -   Error occurring during cost allocation record transformation for Purchase Order Lines
        -   Incorrect test cases for 'ERPSourceConfigCRUD' functionality
        -   Incorrect file location of 'sn\_fcms\_intg\_imp\_delivery\_address.xml'
        -   "Cannot read property erp\_source from undefined" error
    -   Removed:
        -   Duplicate fetch bids functionality between ERP Integration and Spend Integration plugins
        -   Duplicate deny unless ACLs in app-fin-close-intg repository
-   **Version 16.0.0 - August 2025**
    -   Updates:
        -   Update Transform Map Logic to accept Parent Child records as a whole
            1.  Example, when a Purchase order with multiple lines is posted and say 2 of the Purchase Order lines fail \(child records\), then the entire data set which has parent child relationship should fail
            2.  This is implemented by marking error status for the record and creating an error task
            3.  Users will not be able to use the record until the error is fixed
-   **Version 15.16.7 - June 2025**

    Fixed: Receipt status field was missing in the Staging table \(sn\_fcms\_intg\_imp\_receipt\), which prevented the system from storing and transforming the receipt status data coming from Coupa.

-   **Version 14.5.9 - June 2025 \(Xanadu\)**

    Fixed: When fetching Purchase Orders \(POs\) from Coupa, there was an error if the PO Status \(u\_po\_status\) was 'contract\_hold' due to the lack of a near status match to map.

-   **Version 15.16.3 - May 2025**

    Changed: The upgraded data excludes the ERP source column from global tables but will be accessible in the mapping table.

-   **Version 15.6.0 - March 2025**

    New: A provision has been added for accepting attachments in inbound sourcing flows.

-   **Version 14.5.5 - March 2025**
    -   New
        -   Shipment staging table has been relocated from the Source-to-pay integration framework to the ERP Integration Framework
        -   Integrated outbound remittance location tables.
-   **Version 15.0.0 - February 2025**

    New: Update the ERP Integration Framework to allow users to schedule jobs for the Sourcing and Shipment entities.

-   **Version 14.5.2 - January 2025**
    -   New: Added integration tables for remittance location
    -   Changed: Migrated the shipment stage table and transform map to ERP Integration Framework
-   **Version 12.7.1 - January 2025 \(Washington DC\)**

    New: Added integration tables for remittance location.

-   **Version 14.0.0 - November 2024**

    Changed: Evaluated sandbox access for client-callable script.

-   **Version 12.6.5 - November 2024 \(Washington DC\)**
    -   New:
        -   Added entities for Sourcing Requests:
            -   Fetch shipment details for a given line ID
            -   Fetch shipment details after the updated date
    -   Changed: Enabled Integration Hub Spoke for SAP role to Integration administrator role when Primary data integration with SAP and Accounts Payable Operations integration with SAP are installed. This is enabled for the Washington version.
-   **Version 13.5.2 - October 2024**

    Changed: Turned off old ECC flows.

-   **Version 13.0.0 - August 2024**
    -   New: Introduced an integration with Coupas ERP.
    -   Changed:
        -   Transferred attachments from the ERP system staging table to the main Purchase Order table. These attachments are also visible on the purchase order.
        -   Updated some fields and processes in the Source-to-Pay Integration Framework to build connection points and to work with other ERP systems, including these:
            -   Turned off the purchase order button when the integration status in the staging table is New or In Process.
            -   Disallowed purchase order lines to be created when purchase orders haven't been brought in yet from the ERP system. Added a scheduled job to retry adding purchase order lines after a purchase order is created.
            -   Added missing columns and removed some columns in some staging and primary tables such as the outbound receipt, purchasing group primary and staging, cost center staging, and Fx currency tables. Updated the transform map logic for some of these tables to render these columns.
            -   Created the ERP plant address mapping staging table.
-   **Version 12.1.0 - August 2024 \(Washington DC\)**

    Updated the integration staging tables with additional fields and transformation maps for inbound and outbound flows.

-   **Version 12.0.3 - June 2024**
    -   Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.
    -   Bug fixes.
-   **Version 10.1.0 - June 2024 \(Vancouver\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 8.6.0 - June 2024 \(Utah\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 12.0.2 - May 2024**

    Minor fixes.

-   **Version 8.5.4 - April 2024**

    Minor fixes.

-   **Version 11.0.3 - March 2024**

    Minor fixes.

-   **Version 10.0.4 - March 2024 \(Vancouver\)**

    Minor fixes.

-   **Version 11.0.1 - February 2024**
    -   Changed: Changed the common integration framework to include:
        -   Inbound tables for purchase order, receipt, and cost allocations, which when populated create purchase orders, receipts, and cost allocations in the SPO tables.
        -   Scheduled jobs primary flow, which can be used by partners to develop jobs to fetch the data from ERP systems.
        -   Common error handling framework, which can be used as a standard framework for integrating with any ERPs. Note: There is no impact on existing customers and these changes will come in effect only with this upgrade.
-   **Version 10.0.3 - January 2024**

    New: Resubmit for errored records is now available in the respective plugins and removed from the ERP plugin.

-   **Version 10.0.1 - November 2023**

    New:

    -   A common integration framework is provided for customers to get the data into Source-to-Pay applications, and also for outbound integrations.
        -   Customers intending to integrate by getting data from other third-party products can populate the inbound staging tables, which will automatically populate the data into base tables by using the default transform maps shipped with this feature.
        -   Customers intending to push data into third-party products can refer to outbound tables from where they can pick and push the data into third-party products. This outbound table is automatically populated using the subflows shipped with this feature.Note: No impact to existing customers, and they will find these new changes in effect with this upgrade.
-   **Version 9.0.0 - August 2023**

    Changed: Some of the existing ACLs were evaluated;and rectified to ensure that the roles have the right level of access to the tables, that is, requester role versus fulfiller role. Note: This is a backend change and has no customer impact.

-   **Version 8.5.1 - July 2023**

    New:

    -   Updated the ERP source page to include the connection alias.
    -   Added a new tab for integration services, which are jobs to fetch data from SAP for entities like legal entity, GL account, supplier, material group, and so on.
    ServiceNow, the ServiceNow logo, Now, and other ServiceNow marks are trademarks and/or registered trademarks of ServiceNow, Inc., in the United States and/or other countries. Other company and product names may be trademarks of the respective companies with which they are associated.

-   **Version 8.3.1 - July 2023**

    New:

    -   Updated the ERP source page to include the connection alias.
    -   Added a new tab for integration services, which are jobs to fetch data from SAP for entities like legal entity, GL account, supplier, material group, and so on.
-   **Version 8.2.2 - May 2023**

    Renamed this application to ERP Integration Framework. This application was formerly named Finance - ERP Integration.

-   **Version 8.1.0 - May 2021**

    Minor fixes.

-   **Version 7.1.0 - September 2020**

    Fixes and minor changes.

-   **Version 6.5.1 - July 2020**

    Fixed: Minor bug fixes, along with a fix for a purchase order posting issue when the quantity is zero.

-   **Version 6.4.0 - June 2020**

    Changed: Changes for supporting Finance Operations applications.

-   **Version 6.2.0 - May 2020**

    Changed: Changes for supporting Finance Operations applications.



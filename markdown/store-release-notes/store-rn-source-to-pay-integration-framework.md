---
title: Source-to-Pay Integration Framework release notes
description: Version history for the Source-to-Pay Integration Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-source-to-pay-integration-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Source-to-Pay Integration Framework release notes

Version history for the Source-to-Pay Integration Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.2 - June 2026 \(Australia\)**
    -   New:
        -   Added Remit-to party column to the outbound invoice staging table
        -   Added Short Description and Legal Entity field mappings for outbound purchase requisitions \(PRs\).
        -   Added Supplier ERP Code, requested start date, requested end date, and maximum budget field mapping for outbound PRL.
        -   Mandated Asset ID field for Ariba at the PRL level and in outbound PRL.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs independently.
        -   Added Access Control Lists \(ACLs\) to support the Non‑Glide Cobalt Raven Brazil directive.
        -   Updated PR/PO references to support decoupled PR/PO processing.
        -   Mandated fields on Outbound PR for Ariba based on account assignment category selection
    -   Changed:
        -   Outbound flows no longer trigger for Closed Canceled and Closed Rejected PRs.
        -   Updated PR behavior to use COA field selection instead of CapEx/Expense/Prepaid account fields.
        -   Restrict cost allocation type to cost center lines only in the Shopping hub for SAP Ariba PRs.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs.
        -   Blocked edit and cancel actions on POs for the target system Ariba.
    -   Fixed: Fixed issue with UI Action retry for PR and PO processing.
-   **Version 13.0.2 - June 2026 \(Zurich\)**
    -   New:
        -   Added Remit-to party column to the outbound invoice staging table
        -   Added Short Description and Legal Entity field mappings for outbound purchase requisitions \(PRs\).
        -   Added Supplier ERP Code, requested start date, requested end date, maximum budget field mapping for outbound PRL.
        -   Mandated Asset ID field for Ariba at the PRL level and in outbound PRL.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs independently.
        -   Added Access Control Lists \(ACLs\) to support the Non‑Glide Cobalt Raven Brazil directive.
        -   Updated PR/PO references to support decoupled PR/PO processing.
        -   Mandated fields on Outbound PR for Ariba based on account assignment category selection
    -   Changed:
        -   Outbound flows no longer trigger for Closed Canceled and Closed Rejected PRs.
        -   Updated PR behavior to use COA field selection instead of CapEx/Expense/Prepaid account fields.
        -   Restrict cost allocation type to cost center lines only in the Shopping hub for SAP Ariba PRs.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs.
        -   Blocked edit and cancel actions on POs for target system Ariba.
    -   Fixed: Fixed issue with UI Action retry for PR and PO processing.
-   **Version 11.0.3 - June 2026**
    -   New:
        -   Added the Remit-to party column to the outbound invoice staging table.
        -   Added Short Description and Legal Entity field mappings for outbound purchase requisitions \(PRs\).
        -   Added Supplier ERP Code, requested start date, requested end date, and maximum budget field mapping for outbound PRL.
        -   Mandated Asset ID field for Ariba at the PRL level and in outbound PRL.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs independently.
        -   Added Access Control Lists \(ACLs\) to support the Non‑Glide Cobalt Raven Brazil directive.
        -   Updated PR/PO references to support decoupled PR/PO processing.
        -   Mandated fields on Outbound PR for Ariba based on account assignment category selection.
    -   Changed:
        -   Outbound flows no longer trigger for Closed Canceled and Closed Rejected PRs.
        -   Updated PR behavior to use COA field selection instead of CapEx/Expense/Prepaid account fields.
        -   Restrict cost allocation type to cost center lines only in the Shopping hub for SAP Ariba PRs.
        -   Enabled decoupled PR/PO flow to support outbound processing of PRs.
        -   Blocked edit and cancel actions on POs for the target system Ariba.
    -   Fixed: Fixed issue with UI Action retry for PR and PO processing.
-   **Version 12.9.0 - March 2026 \(Zurich\)**
    -   New: Added enhancements to the Purchase Requisition Line \(PRL\) outbound staging table
    -   Changed: Performance optimizations applied to the PO transform map
-   **Version 10.17.0 - March 2026**
    -   New: Added enhancements to the Purchase Requisition Line \(PRL\) outbound staging table
    -   Changed: Performance optimizations applied to the PO transform map
-   **Version 12.5.0 - January 2026 \(Zurich\)**
    -   New:
        -   Added support for outbound invoice reversal scenarios through staging and dictionary enhancements, including new reversal-related attributes such as Reversal Date and Reversal ERP Number.
        -   Introduced additional invoice status values to support the reversal lifecycle \(for example, reversal in progress and authorize payment\).
    -   Changed:
        -   Enhanced outbound ERP integration flow to support invoice reversal, cancel, and void scenarios for SAP and Oracle ERP systems, ensuring alignment with ERP-specific processing requirements
        -   Updated integration behavior and validations as defined in the acceptance criteria, with certain validations handled at the UI level.
-   **Version 10.13.0 - January 2026**
    -   New:
        -   Added missing outbound staging fields for Purchase Requisition \(PR\) and Purchase Requisition Line \(PRL\), including Buyer Group, Short Description, Requested Delivery Date, Legal Entity, and other required attributes.
        -   Added additional outbound fields required to support service requisition scenarios.
        -   Introduced the missing Purchase Requisition entity at the integration service record level.
    -   Changed:
        -   Updated outbound mappings to ensure required fields are mapped between base tables and outbound staging tables for requisitions and orders.
        -   Updated PO Header outbound staging to map Purchasing Group from the base table.
        -   Updated supplier and supplier contact data source indexing for integration configuration correctness.
    -   Fixed:
        -   Fixed missing outbound fields that blocked Purchase Requisition creation in ERP.
        -   Fixed access issues by enabling required create/update permissions on PR and PRL staging tables.
-   **Version 12.0.1 - December 2025 \(Zurich\)**
    -   New: Created a new integration table for Purchase Requisition Line outbound processing with comprehensive field mapping, including account assignment, state, costs, WBS elements, and cancellation tracking.
    -   Changed:
        -   Extended the existing Purchase Requisition and Purchase Requisition Line inbound transform maps to support ERP integration scenarios while maintaining backward compatibility with Punchout functionality.
        -   Implemented automatic assignment of the ERP Source field on Sourcing Requests and Purchase Requisition Lines upon creation. This update includes:
            -   A backfill script for existing records
            -   Updated outbound mapping to ensure accurate Target ERP values
        -   Ensured consistent ERP Source values are populated on Sourcing Requests and Purchase Requisition Lines to align with the business owner’s legal entity configuration across all SPO entities.
        -   Security fixes.
-   **Version 10.8.24 - December 2025 \(Yokohama\)**
    -   New: Created a new integration table for Purchase Requisition Line outbound processing with comprehensive field mapping, including account assignment, state, costs, WBS elements, and cancellation tracking.
    -   Changed:
        -   Extended the existing Purchase Requisition and Purchase Requisition Line inbound transform maps to support ERP integration scenarios while maintaining backward compatibility with Punchout functionality.
        -   Implemented automatic assignment of the ERP Source field on Sourcing Requests and Purchase Requisition Lines upon creation. This update includes:
            -   A backfill script for existing records
            -   Updated outbound mapping to ensure accurate Target ERP values
        -   Ensured consistent ERP Source values are populated on Sourcing Requests and Purchase Requisition Lines to align with the business owner’s legal entity configuration across all SPO entities.
        -   Security fixes.
-   **Version 10.8.21 - October 2025**
    -   Fixed: Resolved an issue that was preventing Invoice creation due to ACL \(Access Control List\) restrictions across the following integration points:
        -   SAP HANA RFC
        -   SAP ECC IDOC
        -   SAP HANA IDOC
    -   This fix ensures that invoices are now successfully created without being blocked by ACL-related constraints.
-   **Version 11.0.1 - August 2025**
    -   Updates:
        -   Application behavior change to support native ERP applications behavior - Disallow cancellation of Purchase Order Lines if the ERP mapped to legal entity is Coupa. This is to ensure functional parity with ERP
    -   Technical Changes:
        -   Cost Allocation table moved to Spend Integration scope and Supporting provided for customers with old releases - in case of Cost Allocation Table Changes
-   **Version 10.8.13 - June 2025**

    Fixed: When updating the headquarters in the Supplier Location table, a new Supplier Parent record was incorrectly being created in the Supplier Outbound table.

-   **Version 9.5.17 - June 2025 \(Xanadu\)**
    -   Fixed:
        -   Users impersonating the ERP Integration Admin \(erp.integration.admin\) role were unable to access records in the Inbound Cost Allocations table \(sn\_spend\_intg\_imp\_cost\_allocation\).
        -   Users encountered errors when creating or updating data in the Sourcing Bid Stage.
-   **Version 10.8.1 - May 2025**

    Changed: If an error occurs while syncing supplier data, an error task will be created, and the data can be submitted using the retry feature."

-   **Version 9.5.13 - May 2025 \(Xanadu\)**
    -   Fixed:
        -   Awarding purchase outbound flow issue
        -   Sourcing outbound queue flow issue
        -   Minor bugs
-   **Version 10.5.0 - March 2025**
    -   New: You can now accept sourcing bids beyond the bid closure time in exceptional instances where the source system permits a grace period for bid acceptance.
    -   Fixed: Resolved an issue causing duplicate outbound records in SR/PRL outbound tables when a Negotiation Event or Sourcing Request was canceled.
-   **Version 9.5.7 - March 2025 \(Xanadu\)**
    -   New:
        -   Added two additional fields to the Supplier Contact Outbound table as part of SLO Integration:
            -   ERP source
            -   ERP company code
        -   IT Admins now have the capability to provision additional mappings of third-party system units of measure \(UOM\) to existing UOM within ServiceNow.
    -   Deprecations: Deprecation of shipment inbound table and transform map from spend\_intg scope.
-   **Version 9.5.3 - January 2025**
    -   New: Added supplier contact outbound attributes
    -   Changed: Deprecated shipment inbound table and transform map from this scope
    -   Fixed:
        -   Addressed supplier outbound module access issue
        -   Resubmit sourcing flow issues
-   **Version 7.10.1 - January 2025 \(Washington DC\)**
    -   New: Added staging table and transform map for storing supplier product pricing details
    -   Changed: Syncing ERP numbers from the outbound staging tables back to the base tables within the Sourcing Flow.
-   **Version 9.0.3 - November 2024**
    -   New: Added an API to support invoice ingestion from external systems in JSON and cXML formats
    -   Changed: Improved outbound integrations framework by adding an outbound Invoice Cost Allocation table
-   **Version 7.9.0 - November 2024**

    New: Created a new staging table for fetching sourcing requests from ERP systems for the Washington version.

-   **Version 8.5.2 - October 2024**

    New: Added a new staging shipment table and transform map.

-   **Version 8.0.11 - August 2024**
    -   Changed:
        -   Updated the Source-to-Pay Integration Framework for integrations with third-party sourcing tools. You can now support negotiation-event-based integrations that consist of multiple sourcing requests.
        -   Updated the purchase order cancellation flow when it's updated from the purchase order outbound table.
-   **Version 7.2.1 - August 2024 \(Washington DC\)**

    New: Added the Banking Identification Number field that identifies unique bank accounts. This field is required to build integration with different ERPs like SAP, Oracle, Ariba, and so on.

-   **Version 7.1.0 - June 2024**

    Defect fixes.

-   **Version 7.0.2 - May 2024**

    New: Introduced interface tables and logic to support Level 1 cXML protocol based punchout to third-party supplier sites.

-   **Version 6.0.3 - March 2024**

    Minor fixes.

-   **Version 5.0.2 - March 2024 \(Vancouver\)**

    Minor fixes.

-   **Version 6.0.1 - February 2024**

    Changed: Introduced additional ability within the integration framework for third-party sourcing tools to know when to close bids now, before the bids end date. In addition, if a supplier award has been made in a third-party sourcing tool, the award response would return to ServiceNow. Note: Currently, only a single supplier response can return to ServiceNow. Additionally, there are default email content and in-product alert messages to inform the employee or requester and the sourcing manager or fulfiller when a Request for Quote \(RFQ\) has been created in the third-party sourcing tool, and when a supplier award can be made in ServiceNow. Existing customers are additionally impacted by a consolidation of decision tables used to trigger the third-party sourcing tool integration. While one is deprecated, another is active and in use. Existing customers need to ensure that they use the active decision table.

-   **Version 5.0.1 - November 2023**

    New: Introduced new workflows and staging tables in the integrations framework for third-party sourcing tools to integrate with Sourcing and Procurement Operations sourcing workflows for RFx and awarding use cases. Note: Existing and new customers will be able to leverage this integration framework to build integrations with third-party sourcing tools. Additionally, third-party sourcing solutions can leverage this integration framework to build sourcing integrations with Sourcing and Procurement Operations.

-   **Version 5.0.1 - November 2023**

    Provides a set of staging tables, transform maps, and workflows to integrate sourcing, third-party catalogs, ordering, shipments, and invoicing with Source-to-Pay Operations.


**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)


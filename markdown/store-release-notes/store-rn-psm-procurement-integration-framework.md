---
title: Source-to-Pay Integration Framework release notes
description: Version history for the Source-to-Pay Integration Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-procurement-integration-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Source-to-Pay Integration Framework release notes

Version history for the Source-to-Pay Integration Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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
-   **Version 3.3.4 - December 2023 \(Utah\)**

    Minor fixes.

-   **Version 4.0.1 - August 2023**

    Minor fixes.

-   **Version 3.3.3 - May 2023**

    Minor fixes.

-   **Version 3.3.1 - August 2022**

    Minor fixes.

-   **Version 3.2.1 - May 2022**

    Changed: When sourcing requests are sent out to third party solutions, the procurement team can now qualify suppliers before sourcing bid information from the third party solutions.

-   **Version 3.1.2 - February 2022**

    Standardize the way in which third-party tools and systems integrate with Procurement Service Management. This application provides a standard framework through which a partner or supplier can integrate sourcing and procurement workflows across organization silos and systems.


**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)


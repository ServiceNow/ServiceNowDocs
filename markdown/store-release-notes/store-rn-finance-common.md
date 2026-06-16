---
title: Finance Common Architecture release notes
description: Version history for the Finance Operations Management Finance Common Architecture on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-finance-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Finance Close Automation release notes, ServiceNow Store release notes]
---

# Finance Common Architecture release notes

Version history for the Finance Operations Management Finance Common Architecture on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.0.1 - June 2026**
    -   New:
        -   When creating Purchase Requisitions with Ariba as the target ERP, users can select only Cost Center as the cost allocation type. Other allocation types are not supported.
        -   When creating a Purchase Requisition line with the Asset \(A\) account assignment category and Ariba as the target ERP, the Asset ID and Cost Center fields are required. Users must select a valid Asset ID from the available assets before proceeding.
    -   Changed:
        -   Editing or canceling Purchase Orders in ServiceNow is no longer allowed when the target system is Ariba. All such actions must be performed directly in Ariba.
        -   Record‑level access controls for create, read, write, and delete operations have been added to several finance‑related tables. These controls now use the appropriate SPO roles to ensure consistent access management.
    -   Fixed:
        -   Fixed an issue that allowed duplicate ERP company codes to be created under the same ERP. The system now prevents duplicate entries.
        -   Corrected invalid roles previously used in access control lists. Access controls now reference only valid roles with the appropriate dependencies.
-   **Version 11.6.0 - March 2026**
    -   New:
        -   Assess supplier performance at scale powered by the Smart Assessment Engine:
            -   Bulk distribution via segmentation rules: Associates assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one‑off outreach.
            -   Internal stakeholder completion: Lets sourcing and procurement teams complete assessments directly in the Source‑to‑Pay Workspace, keeping evaluations centralized and auditable.
-   **Version 11.5.0 - January 2026**

    New: Introduces core tables for Buyer Group and Buyer Group Member in Finance Common Architecture, with the required fields to support downstream Buyer Group selection/population logic across PR/PO flows and integrations.

-   **Version 11.0.1 - December 2025 \(Yokohama and Zurich\)**
    -   Supplier Payment Optimization Enhancements:
        -   New: Introduced a new case type that allows updating the payment method to a credit card and capturing the terminal ID.
        -   Changed:
            -   Improved the banking form.
            -   Enhanced the payment optimization dashboard.
-   **Version 10.5.0 - October 2025**

    New: Added the capability to generate usage metrics for the FSC integration of Primary Data with SAP Ariba.

-   **Version 10.0.5 - September 2025 \(Zurich\)**

    Fixed: Minor fixes

-   **Version 9.27.5 - September 2025 \(Yokohama\)**

    Fixed: Minor fixes

-   **Version 10.0.0 - August 2025**
    -   New: Added infrastructure to enable Configurable behavior in application to support varied ERP application behaviors.
    -   Fixed: Removed tracking of Legal Entity table which can be updated not only through integration framework to ensure false positives are not included.
-   **Version 9.27.0 - June 2025**

    Minor Fix \(internal\) to update query to fetch North Star metric to display Integration usage.

-   **Version 9.22.0 - May 2025**
    -   New:
        -   Introduced the new ERP source mapping \(sn\_fin\_erp\_source\_mapping\) table to store all ERP source mappings. The table includes three fields:
            -   ERP Source: Reference to ERO source table
            -   Record: Document ID field to store the record to be mapped
            -   Record table: Table that the record belongs to
-   **Version 9.20.0 - March 2025**

    Changed: Improvement to ensure that the ERP source column is excluded from global tables and is present only in the M2M \(many-to-many\) table.

-   **Version 9.17.0 - February 2025**

    Minor fixes only.

-   **Version 9.14.0 - January 2025**
    -   New: Transform map for Supplier Product Pricing contract
    -   Fixed: Inbound sourcing flow bug fixes
-   **Version 9.6.1 - January 2025 \(Washington DC\)**

    Changed: Coupa related changes in ERP source configuration.

-   **Version 9.9.2 - December 2024**

    New: Added support to enables effortless access to supplier contact information across multiple suppliers with a single set of login credentials.

-   **Version 9.8.0 - November 2024**
    -   Introduced the "Amount Allocated" field on the Base Invoice Line table as part of the Invoice Cost Allocation feature.
    -   Added "Deny Unless" ACLs to the Invoice Base Table for improved security.
-   **Version 9.5.1 - October 2024**

    Created new ERP source mapping table.

-   **Version 9.0.2 - August 2024**
    -   New:
        -   Added the Base Invoice and Base Invoice Line tables as part of reparenting.
        -   Added the Base Tax Line, Tax Type, and Tax Code tables as part of tax compliance.
-   **Version 8.0.1 - May 2024**

    Minor fixes.

-   **Version 7.6.1 - February 2024**

    Minor fixes.

-   **Version 7.1.4 - December 2023 \(Vancouver\)**

    Minor fixes.

-   **Version 6.4.3 - December 2023 \(Utah\)**

    Minor fixes.

-   **Version 7.1.1 - November 2023**

    Changed: The Office Location table has been rescoped into Finance Common to be available as a common table. Note: Existing or new customers will not see any change, and there will not be any change to existing security or ACLs for customers.

-   **Version 7.0.2 - August 2023**

    Changed: To support multi-ERP integration, cost center values are restricted by the ERP source on the object. Legal entity from the object is considered, and the ERP source is fetched. When a user updates the record, only those cost centers that have matching ERP sources are displayed. Note: Existing customers are not impacted as these validations are enforced only when the legal entity has been set up for integration with ERPs. If customers have set up integration with an ERP, then they will see the data having the same ERP source, thereby preventing downstream errors during integration.

-   **Version 6.4.2 - July 2023**

    Minor bug fixes.

-   **Version 6.4.1 - May 2023**

    Changed:

    -   To support multi-ERP integration, the following changes are done:
        -   Conversion rates from the Finance Exchange Rates \(sn\_fin\_fx\_rate\) table are used. This table has an ERP Source column, and records like purchase requisition and purchase order can also be tied to the ERP Source column. By taking the legal entity and getting an ERP source from the legal entity, the right conversion rate is derived.
        -   FX2 currency amount fields are converted into legal entity local currency amount and legal entity reporting currency amount by using the conversion rate from the Finance Exchange Rates table. All these converted values are stored in the PSM FX Currencies \(sn\_shop\_fx\_currency\_instance\)​ table.

            **Note:** Note: Existing customers will not be impacted as this is a separate table where the conversions are captured.

-   **Version 6.3.4 - February 2023**

    Minor fixes.

-   **Version 6.3.2 - November 2022**

    Minor fixes.

-   **Version 6.3.1 - August 2022**

    Changed: Renamed this application to Finance Common Architecture. This application was formerly named Finance Common.

-   **Version 5.0.1 - September 2020**

    Fixes and minor changes.

-   **Version 4.6.0 - July 2020**

    New: Minor updates to support changes in the other Finance Operations applications.

-   **Version 4.5.0 - June 2020**

    New: Minor updates to support changes in the other Finance Operations applications.

-   **Version 4.4.0 - May 2020**

    New: Minor updates to support changes in the other Finance Operations applications.



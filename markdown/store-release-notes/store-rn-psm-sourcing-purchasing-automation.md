---
title: Sourcing and Purchasing Automation release notes
description: Version history for the Sourcing and Purchasing Automation application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-sourcing-purchasing-automation.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Sourcing and Purchasing Automation release notes

Version history for the Sourcing and Purchasing Automation application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.4.1 - June 2026 \(Australia\)**

    Changed: Remediated non‑Glide Cobalt Raven ACLs in product code \(DIRS0000421\).

-   **Version 11.2.6 - June 2026 \(Zurich\)**

    Changed: Resolved GetRefRecord scoping bypass vulnerability \(DIRS0000408\).

-   **Version 11.2.1 - June 2026**

    Changed: Resolved GetRefRecord scoping bypass vulnerability \(DIRS0000408\).

-   **Version 9.0.3 - March 2026**
    -   New: Shopping on behalf of others: Enhanced the shopping experience by allowing users to shop on behalf of others, with better visibility and management of these purchases. Users can select delegates without using the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
    -   Changed: Multi-currency support: Enhanced the multi-currency feature to display localized currencies across To-Dos, emails, and the product Bundles page, helping requesters and task owners complete actions.
-   **Version 11.0.1 - March 2026 \(Zurich\)**
    -   New: Shopping on behalf of others: Enhanced the shopping experience by allowing users to shop on behalf of others, with better visibility and management of these purchases. Users can select delegates without using the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
    -   Changed: Multi-currency support: Enhanced the multi-currency feature to display localized currencies across To-Dos, emails, and the product Bundles page, helping requesters and task owners complete actions.
-   **Version 10.1.1 - December 2025 \(Zurich\)**
    -   New:
        -   Enhanced Auto-Creation for Multiproduct Integration:
            -   Introduced automated creation of 1:1 sourcing request–event mapping within the multiproduct integration workflow. This enhancement streamlines how sourcing requests are linked to corresponding events, reducing manual effort and ensuring accurate, consistent mapping across integrated products.
        -   Visibility of RFX Tasks in Employee Centre
            -   Added support for displaying RFX-related tasks in the Employee Centre, enabling requestors to track and manage key actions directly from their portal. Tasks such as Review &amp; Publish RFX, Respond to Supplier Queries, and Award RFX now appear with complete details. Each task includes a Mark as Complete button with a confirmation tooltip, allowing requestors to close tasks once finished. This enhancement improves visibility, accountability, and navigation for RFX processing.
    -   Changed:
        -   Performance Optimization for Sourcing Operations
            -   Implemented significant performance tuning to deliver a faster and more intuitive experience in sourcing operations. Key improvements include:
                -   Supplier addition workflows optimized for speed and reliability.
                -   Sourcing request-to-event mapping refined for efficiency, reducing latency and improving responsiveness.
-   **Version 8.2.0 - December 2025 \(Yokohama\)**
    -   New:
        -   Enhanced Auto-Creation for Multiproduct Integration:
            -   Introduced automated creation of 1:1 sourcing request–event mapping within the multiproduct integration workflow. This enhancement streamlines how sourcing requests are linked to corresponding events, reducing manual effort and ensuring accurate, consistent mapping across integrated products.
        -   Visibility of RFX Tasks in Employee Centre
            -   Added support for displaying RFX-related tasks in the Employee Centre, enabling requestors to track and manage key actions directly from their portal. Tasks such as Review &amp; Publish RFX, Respond to Supplier Queries, and Award RFX now appear with complete details. Each task includes a Mark as Complete button with a confirmation tooltip, allowing requestors to close tasks once finished. This enhancement improves visibility, accountability, and navigation for RFX processing.
    -   Changed:
        -   Performance Optimization for Sourcing Operations
            -   Implemented significant performance tuning to deliver a faster and more intuitive experience in sourcing operations. Key improvements include:
                -   Supplier addition workflows optimized for speed and reliability.
                -   Sourcing request-to-event mapping refined for efficiency, reducing latency and improving responsiveness.
-   **Version 8.0.5 - November 2025**
    -   New:
        -   Enhanced Auto-Creation for Multiproduct Integration:
            -   Introduced automated creation of 1:1 sourcing request and event mapping within the multiproduct integration workflow. This enhancement streamlines the process of linking sourcing requests to corresponding events, reducing manual effort and ensuring accurate, consistent mapping across integrated products.
        -   Visibility of RFX Tasks in Employee Center:
            -   Added support for displaying RFX-related tasks in the Employee Center, enabling requestors to track and manage key actions directly from their portal. Tasks such as Review &amp; Publish RFX, Respond to Supplier Queries, and Award RFX will now appear with complete details, Each task includes a “Mark as Complete” button with a confirmation tooltip, allowing requestors to close tasks once finished. This enhancement improves visibility, accountability, and ease of navigation for RFX processing.
    -   Changed:
        -   Performance Optimization for Sourcing Operations:
            -   Implemented significant performance tuning to deliver a faster and more intuitive experience in sourcing operations. Key improvements include:
                -   Supplier addition workflows optimized for speed and reliability.
                -   Sourcing request-to-event mapping refined for efficiency, reducing latency and improving responsiveness. These changes make the overall sourcing experience more performant, seamless, and user-friendly.
-   **Version 9.0.0 - August 2025**
    -   New: Enabled decimal quantities for service items when creating purchase requisitions using quick or full checkouts in Shopping Hub and Employee Center.
    -   Changed: The creation of inventory assets for services in the alm\_asset table is disabled in the Sourcing and Purchasing Automation and Asset Management Integration for Sourcing and Procurement Operations plugins.
-   **Version 8.0.0 - May 2025**

    Added deny unless ACLs for common applications.

-   **Version 7.7.0 - March 2025**

    Fixed: Resolved an issue where punchout purchases did not have the same purchase ID across all purchase lines.

-   **Version 7.3.0 - February 2025**

    New: Added help text next to the watchlist to inform users about its purpose.

-   **Version 7.0.0 - November 2024**
    -   New:
        -   Enabling watchlist for sourcing requests and purchase requisitions:
            -   Allow users who are neither submitters nor business owners to see the status changes of purchase requisitions and sourcing requests.
            -   Configure the number of users allowed to be added to the watchlist.
            -   Enable fulfillers to add users at any stage of the request lifecycle.
            -   Configure notifications to include watchlist users regarding updates on the request.
            -   Allow business owners to add or remove users from Shopping Hub.
        -   Improved edit a purchase requisition and purchase order options, making relevant metadata visible to case fulfillers. Editable fields now include service and delivery dates, delivery addresses, and quantities on existing purchase order lines from the Edit a Purchase record producer.
        -   Configurable PR Merge Capabilities:
            -   Introduced configurable options for merging purchase requisitions \(PRs\), allowing administrators to define how PR merges are triggered.
            -   Differentiate between automatic merging conditions and manual \(user-initiated\) merging.
            -   Specify matching field conditions that must be met for PRs to be merged.
            -   Critical matching conditions essential for the proper functioning of PRs have been retained in the script layer.
            -   For existing customers, the default behavior remains consistent with the previous PR merge functionality. Existing customers can also leverage the configuration framework to align the merge conditions with their business processes.
            -   New customers can also take advantage of the default behavior that aligns with existing PR merge functionalities and can leverage the configuration framework to tailor their merge conditions accordingly.
-   **Version 6.0.1 - August 2024**

    Minor fixes.

-   **Version 5.0.0 - May 2024**
    -   New:
        -   Introduced back-end workflows to support Level 1 cXML protocol based punchout to third-party supplier sites.
        -   Introduced back-end workflows to support single supplier internal bundle purchases.
    -   Changed: Supplier risk assessment and supplier tiering assessment cases have been retired and replaced by the due diligence case, to follow the new Third-Party Risk Management \(TPRM\) data model changes.
-   **Version 4.0.1 - February 2024**
    -   Changed:
        -   Requesters or employees can now submit a request to purchase a good or service with a past date within the intake form experience. These requests will continue to be marked as "after-the-fact" purchases. Existing customers will find the past date validation removed from the intake forms, so that past dates can be captured and passsed to the database as valid responses.
        -   Addressed a workflow compliance issue where the state within the sourcing and purchasing workflows could be changed manually, bypassing automation, thus causing downstream workflow and usability issues. The State field is now made read-only, so that the stateflow can adhere to the designed workflow and automation. Existing customers can no longer change the state manually for sourcing request, purchase lines, negotiation event, negotiation, and purchase requisition tables.
-   **Version 3.1.1 - November 2023**

    New: A requester can now provide contact details for a supplier that they are interested in working with, during intake for off-catalog items. A supplier contact record is stored and created for procurement fulfillers to leverage when reviewing sourcing or purchasing details. Note: Existing and new customers will see these changes. Only customers with Supplier Lifecycle Operations will have the additional capability for supplier contacts for new suppliers to trigger the onboarding flow to invite that supplier contact into the registration process.

-   **Version 3.0.1 - August 2023**

    Changed:

    -   To support multi-ERP integration:
        -   GL account values are restricted by the ERP source on the object. Legal entity from the object is considered, and the ERP source is fetched. When a user is updating the record, only those cost centers that have matching ERP sources are displayed.Note: Existing customers are not impacted as these validations are enforced only when the legal entity has been set up for integration with ERPs. If customers have set up integration with an ERP, then they will see the data having the same ERP source, thereby preventing downstream errors during integration.
        -   If there is any record with different ERP sources, then an integration error task is raised. This is an indicator for the fulfiller to correct the record before processing it further.
    -   Updated the existing sourcing to negotiations workflow to no longer have a negotiation record independent of a negotiation event record. Going forward, if procurement professionals want to work on negotiations, they would need to work from negotiation event records. Negotiation events will auto-create negotiations per supplier and allow more complex supplier awarding scenarios.Note: For existing customers, in-progress negotiations that are independently created without negotiation events will continue to exist and proceed undisturbed. However, there will not be the ability to create new independent negotiation records without negotiation event records.
-   **Version 2.0.1 - May 2023**
    -   Changed: Updated the existing awarding workflow to create multiple purchase requisitions based on supplier and business owner combinations, to support the ability to award multiple suppliers within one negotiation event.
    -   **Note:** Existing customers currently performing a single supplier award will still be able to do so with the existing award workflow. If customers want to leverage the multiple supplier award capability, these changes will also acknowledge the more complex awarding scenario to create multiple purchase requisitions based on supplier and business owner combinations.

-   **Version 1.4.1 - February 2023**
    -   Changed: Updated the ability of procurement fulfillers working with qualified suppliers. They no longer need to manually trigger the qualification workflow in order to enter the price of a requested item within a sourcing request. However, if there are qualification cases set up in the instance, then the user action of entering price will also trigger the qualification cases to be created.
    -   **Note:** Existing customers will see this change through a business rule which was modified to trigger the qualification flow if any of the purchase lines or price details are updated.

-   **Version 1.3.7 - November 2022**
    -   New:
        -   Customers can now activate a sourcing request approval workflow within their sourcing process.
        -   Approvers can now directly complete approval to-dos for purchase requisitions and sourcing requests in Employee Center.
    -   Changed: Updated the flexibility for system administrators to configure approval rules for objects other than purchase requisitions \(such as sourcing requests, purchase orders, and invoices\) and create flexible approval trigger conditions.
-   **Version 1.2.2 - August 2022**
    -   Changed:
        -   Updated the auditability for purchase approvals to show self-approved purchases, where the shopper or employee has the authorized purchasing power to self-approve their own purchases. This is a change to the approval plans to show self-approved purchases.
        -   Minor fixes to improve the ability to award single-supplier negotiations.

**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)


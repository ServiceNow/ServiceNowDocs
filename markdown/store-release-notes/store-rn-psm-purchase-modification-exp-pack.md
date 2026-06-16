---
title: Playbooks for Sourcing and Procurement Operations release notes
description: Version history for the Playbooks for Sourcing and Procurement Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-purchase-modification-exp-pack.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Playbooks for Sourcing and Procurement Operations release notes

Version history for the Playbooks for Sourcing and Procurement Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.5.5 - March 2026**

    New: Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.

-   **Version 8.5.1 - December 2025 \(Yokohama and Zurich\)**

    Minor bug fixes.

-   **Version 8.3.1 - August 2025**
    -   Fixed:
        -   Minor bug fixes have been implemented.
        -   A hyperlink issue in the Source-to-Pay Workspace has been resolved. The issue occurred when a revised purchase requisition was converted to a purchase order, and the hyperlink was not functioning correctly.
    -   Changed: The term "Negotiation event" has been renamed to "Sourcing event" in both the Sourcing event and Sourcing request playbooks to maintain consistency in terminology.
-   **Version 8.0.9 - June 2025**

    Fixed: Minor bug fix to resolve an issue where records from the staging table sn\_fcms\_intg\_imp\_receipt had a status of "posted", but after transformation to the base table sn\_shop\_receipt, the status was incorrectly set to "pending\_submission" instead of "posted".

-   **Version 8.0.5 - May 2025**

    Minor fixes.

-   **Version 8.0.0 - February 2025**
    -   New: Edit a Receipt
    -   1.  Shopper Workflow:
    -   Shoppers can initiate an Edit Receipt Request directly from the Shopping Hub under "My Purchases" or from the "Purchase Lines" tab.
    -   By selecting the appropriate PO or purchase line, shoppers can open the Edit Receipt Form, provide required details \(e.g., business owner, PO, POL, etc.\), and submit the request.
    -   A case ID\(of Edit a receipt case type\) is generated for tracking purposes, and shoppers can monitor the request status via the Employee Center under "My Requests."
    -   Alternatively, shoppers can use the Edit a Receipt tile in the Employee Center to directly submit an edit request.
2.  Buyer/Fulfiller Workflow:
    -   Buyers/fulfillers can review and fulfill these requests via the S2P Workspace using the case playbook.
    -   The buyer reviews the details, validates the changes, communicates with relevant stakeholders, and provides closing comments before closing the case.
3.  Automated Edit Receipt Flow:
    -   If the system property sn\_spend\_cp.enable\_automated\_edit\_receipt\_flow is enabled \(default setting\), the process becomes fully automated.
    -   Delivery receipts and corresponding POL quantities are automatically updated without manual intervention, and the case is closed seamlessly.
-   **Version 7.0.0 - November 2024**

    Created a consistent playbook experience by ensuring parity across the activities for canceling a case, reviewing a case, assigning a case, notifying the requestor, and closing a case.

-   **Version 6.7.9 - August 2024**

    Minor fixes.

-   **Version 6.7.7 - May 2024**

    Minor fixes.

-   **Version 6.7.1 - March 2024**

    Minor fixes.

-   **Version 6.5.2 - February 2024**

    Minor fixes.

-   **Version 6.0.4 - December 2023 \(Vancouver\)**

    Minor fixes.

-   **Version 6.0.1 - November 2023**
    -   New:
        -   Provided a default workflow solution that enables procurement specialists to route NDAs to suppliers by leveraging default templates, and enables e-signature capabilities to facilitate the closure of the case of type Send NDA for signature.
        -   A playbook tab is added in Source-to-Pay Workspace for procurement cases of type Send NDA for Signature. This is visible when the Document Template Integration with DocuSign plugin is installed.
        -   Existing customers will now be able to automate the complete signing process.
-   **Version 5.0.0 - August 2023**

    New: Introduced a new guided experience within Workspace for procurement professionals reviewing sourcing intake information from employees and working on negotiations. Note: Existing customers will see a playbook tab within sourcing requests and negotiation events in Workspace for newly opened records. Existing records that are being worked on will not have this new tab.

-   **Version 4.0.2 - May 2023**
    -   New: Introduced a new playbook to handle delivery address review case type which identifies addresses requiring verification and company approval, as well as provides flows to handle rejected addresses.

        **Note:** Modifications were made to the default delivery address review case. If existing or new customers want to leverage this capability, they can reference the delivery address review case which incorporates a new workflow established in Process Automation Designer.

    -   Changed: Renamed this application to Playbooks for Sourcing and Procurement Operations. This application was formerly named Purchase Modification Experience Pack for Procurement Case Management.
-   **Version 3.0.1 - February 2023**

    Minor fixes.

-   **Version 3.0.0 - November 2022**

    New:

    -   New: Introduced a General Inquiry workflow to help procurement teams better triage general procurement related requests from employees.
    -   Changed: Updated the ability to return multiple product lines within one return request.
-   **Version 2.0.2 - August 2022**
    -   New
        -   Introduced a return goods Process Automation Designer \(PAD\) workflow for:
            -   Shoppers or employees, to submit a return request for a purchase that they have already received.
            -   Procurement Specialists or fulfillers, to access the eligibility of the return and to initiate the return with the supplier.
        -   SLAs are defined for the new return goods service catalog item.
    -   Changed: Modified the Receipt table to additionally track credit memos for the return of items.
-   **Version 1.3.1 - May 2022**

    Minor fixes

-   **Version 1.2.0 - February 2022**
    -   New: Shoppers can now raise a case to edit an entire purchase.
    -   Changed: The record producer to cancel a purchase now generates a case of type edit a purchase. The edit a purchase workflow and case type now support editing and canceling an entire purchase, and not just a purchase line.
    -   Removed: The workflow to exclusively cancel a purchase is now removed.


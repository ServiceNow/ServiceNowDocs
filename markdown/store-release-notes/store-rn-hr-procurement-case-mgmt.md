---
title: Procurement Case Management release notes
description: Version history for the Procurement Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-procurement-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Procurement Case Management release notes

Version history for the Procurement Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 19.0.3 - June 2026 \(Australia\)**
    -   New:
        -   Universal Request submission from Employee Center: Employees can submit procurement-related needs through Employee Center using Universal Request. This provides a consistent, cross-departmental request experience without requiring employees to navigate separate procurement portals.
        -   Procurement case creation from Universal Request: Triage and Routing Agents can create a Procurement case directly from a Universal Request. The Universal Request serves as the primary ticket, preserving traceability and keeping the original request intact throughout fulfillment.
        -   Cross-department transfer of Universal Requests: Procurement fulfillers can transfer Universal Requests to other departments or services. Non-procurement fulfillers can transfer requests to Procurement. Transfers route work to the appropriate team while preserving the original Universal Request and its associated routing rules.
        -   Associated tickets for parallel workstreams: Fulfillers across departments, including Procurement, can create associated tickets against a Universal Request to support parallel workstreams. Associated tickets allow multiple teams to work concurrently without modifying the primary ticket or disrupting existing fulfillment flows.
    -   Changed: Universal Request adoption for Sourcing and Procurement Operations: Sourcing and Procurement Operations now adopts Universal Request. Configuration is consolidated into the shared Universal Request for Source-to-Pay Operations application, alongside Supplier Lifecycle Operations \(SLO\) and Accounts Payable Operations \(APO\). This change streamlines administration and configuration management for Source-to-Pay Operations. Existing Universal Request workflows, routing rules, and the user experience for non-procurement departments are preserved.
-   **Version 16.0.2 - June 2026**
    -   New:
        -   Universal Request submission from Employee Center: Employees can submit procurement-related needs through Employee Center using Universal Request. This provides a consistent, cross-departmental request experience without requiring employees to navigate separate procurement portals.
        -   Procurement case creation from Universal Request: Triage and Routing Agents can create a Procurement case directly from a Universal Request. The Universal Request serves as the primary ticket, preserving traceability and keeping the original request intact throughout fulfillment.
        -   Cross-department transfer of Universal Requests: Procurement fulfillers can transfer Universal Requests to other departments or services. Non-procurement fulfillers can transfer requests to Procurement. Transfers route work to the appropriate team while preserving the original Universal Request and its associated routing rules.
        -   Associated tickets for parallel workstreams: Fulfillers across departments, including Procurement, can create associated tickets against a Universal Request to support parallel workstreams. Associated tickets allow multiple teams to work concurrently without modifying the primary ticket or disrupting existing fulfillment flows.
    -   Changed: Universal Request adoption for Sourcing and Procurement Operations: Sourcing and Procurement Operations now adopts Universal Request. Configuration is consolidated into the shared Universal Request for Source-to-Pay Operations application, alongside Supplier Lifecycle Operations \(SLO\) and Accounts Payable Operations \(APO\). This change streamlines administration and configuration management for Source-to-Pay Operations. Existing Universal Request workflows, routing rules, and the user experience for non-procurement departments are preserved.
-   **Version 15.1.0 - March 2026**
    -   New:
        -   Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
        -   Requestors can enter decimal quantities for service items when editing purchase requisitions or purchase orders in Shopping Hub or Employee Center. Admins enable this by updating the Unit of Measure Decimal Support decision table and setting Support decimal quantity to true for required units.
-   **Version 15.0.1 - December 2025**

    Changed: Enhanced the default experience with consistent, streamlined notifications for Procurement cases across email, the Employee Portal, and Agent Workspace.

-   **Version 14.0.0 - August 2025**
    -   New:
        -   The Case Resolution Acceptance Workflow has been improved to provide greater transparency and control in case resolution by involving the requestor during the final stage of the case lifecycle.
            -   Configurable Case Resolution Acceptance Workflow: A new decision table has been introduced, allowing system administrators to enable the case resolution acceptance process for specific case types as needed.
            -   New Case State - Awaiting Acceptance: When a case configured for this workflow is marked as Closed - Completed, it transitions to a new state called Awaiting Acceptance. This triggers an email notification to the requestor with a resolution summary and options to accept or reject the case resolution.
            -   Requestor Action via Employee Center: Requestors can now review and respond to case resolutions directly from the Employee Center &gt; My Requests page, improving accessibility and the overall user experience.
            -   Automatic Closure or Reopen Based on Requestor Action:
                -   If the requestor accepts the resolution, the case is automatically marked as Closed.
                -   If the requestor rejects the resolution, the case is moved back to the In Progress state for further action.
            -   Auto-Closure on No Response: If the requestor does not take action within the configured timeframe, the case is automatically closed to maintain workflow continuity.
            -   Buyer Notifications for Acceptance/Rejection: Buyers are notified when a requestor accepts or rejects a resolution, ensuring transparency and enabling timely follow-ups.
-   **Version 13.0.0 - May 2025**
    -   New:
        -   Support for return and replace flows from Employee Center and Shopping Hub. This enables shoppers to submit return or replacement requests for purchased items directly, without the need for agents to initiate the process on their behalf.
        -   Shoppers can modify purchase requisitions \(PRs\) and purchase orders \(POs\) while maintaining cost allocation across multiple cost centers.
-   **Version 12.0.0 - February 2025**
    -   New: Edit a Receipt.
        1.  Shopper Workflow:
            -   Shoppers can initiate an Edit Receipt Request directly from the Shopping Hub under "My Purchases" or from the "Purchase Lines" tab.
            -   By selecting the appropriate PO or purchase line, shoppers can open the Edit Receipt Form, provide required details \(e.g., business owner, PO, POL, etc.\), and submit the request.
            -   A case ID \(of Edit a receipt case type\) is generated for tracking purposes, and shoppers can monitor the request status via the Employee Center under "My Requests."
            -   Alternatively, shoppers can use the Edit a Receipt tile in the Employee Center to directly submit an edit request.
        2.  Buyer/Fulfiller Workflow:
            -   Buyers/fulfillers can review and fulfill the requests via the Source-to-pay Workspace using the case playbook.
            -   The buyer reviews the details, validates the changes, communicates with relevant stakeholders, and provides closing comments before closing the case.
        3.  Automated Edit Receipt Flow:
            -   If the system property sn\_spend\_cp.enable\_automated\_edit\_receipt\_flow is enabled \(default setting\), the process becomes fully automated.
            -   Delivery receipts and corresponding POL quantities are automatically updated without manual intervention, and the case is closed seamlessly.
-   **Version 11.8.0 - November 2024**

    Evaluated sandbox access for client-callable script and script issues with Edit a Purchase Order flow.

-   **Version 11.0.4 - October 2024**

    Granted the application-specific admin role to all system-level admin users of Procurement Case Management scoped application on Washington release.

-   **Version 11.5.1 - August 2024**

    Minor fixes.

-   **Version 11.0.1 - May 2024**

    Changed: Improved the usability such that a fulfiller can now create a case with just one click from the Source-to-Pay Workspace.

-   **Version 10.2.1 - March 2024**
    -   New:
        -   For the due diligence case type, the Related DDR field is available for tracking the DDR records created as part of the playbook activities.
        -   Two risk assessments, namely Inherent Risk Assessments and Third-party Risk Assessments, are available on the respective procurement case record.
        -   Configured in-system notifications, also known as provider notifications, that notify the requester when there is a change in the respective DDR record.
-   **Version 10.0.0 - February 2024**

    Changed: Employees can now see the completed E-sign, Upload a document, and Submit a form tasks in the Completed tab in the task page of Employee Center.

-   **Version 9.0.5 - December 2023 \(Vancouver\)**

    Minor fixes.

-   **Version 7.0.2 - December 2023 \(Utah\)**

    Minor fixes.

-   **Version 9.0.2 - November 2023**
    -   New:
        -   Provided a default workflow solution to enable employees to request a copy of contract.
        -   A playbook tab is added in Source-to-Pay Workspace for procurement cases of type Request a copy of contract.
        -   Fulfillers will be able to send the copy of the contract with the help of the playbook.
-   **Version 8.0.1 - August 2023**

    New: Sidebar and Microsoft Teams integration is now available on all SPO objects that have extended from the task tables, such as sourcing requests, purchase requisitions, negotiations, negotiation events, and so on.

-   **Version 7.0.1 - May 2023**

    Minor fixes.

-   **Version 6.0.4 - February 2023**

    Minor fixes.

-   **Version 6.0.1 - November 2022**
    -   Introduced and updated Procurement-as-a-service type feature capabilities within Procurement Workspace, such as:
        -   Agent assist, to help procurement specialists triage requests by attaching knowledge articles to the requests, or create catalog service requests on behalf of requestors.
        -   Email composer with quick message templates, to better track conversations between procurement specialists and requestors by directly sending emails from workspace with the ability to apply templated responses.
        -   Create cases within a case, to help procurement specialists create sub-cases within a procurement case record.
-   **Version 5.1.1 - August 2022**
    -   Changed:
        -   Improved Procurement Case Management demo data to:
            -   Update the procurement service catalog browsing experience with more service catalog items
            -   Have case templates for each case type
        -   Changed the prefix for Procurement Case Management records from PSREQ to PC.
-   **Version 5.0.1 - May 2022**
    -   New:
        -   Purchasing tasks are now cases. This supports case types that need their own complex workflows. Examples of case types are supplier onboarding, supplier risk assessments, supplier tiering assessments, contract reviews, and budget reviews.
        -   The supplier onboarding case is now integrated with the Supplier Lifecycle Management plugin to support a complex process automation workflow, which includes registering, qualifying, and activating suppliers.
-   **Version 4.0.1 - February 2022**
    -   New: Fulfillers can now cancel procurement case lines. Procurement case and case line short descriptions have been updated. Procurement cases now have a modification type and can be completed without playbook.
    -   Changed: Purchasing fields have been added and form views have been updated.

**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)


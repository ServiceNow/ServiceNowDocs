---
title: Source-to-Pay Common Architecture release notes
description: Version history for the Source-to-Pay Common Architecture application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-procurement-common-architecture.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 15
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Source-to-Pay Common Architecture release notes

Version history for the Source-to-Pay Common Architecture application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 24.0.0 - June 2026 \(Australia\)**

    Changed: Remediated non-Glide Cobalt Raven ACLs in product code \(DIRS0000421\) by validating platform-added ACL pull requests, confirming correct flow integration, and verifying that functional expectations are met.

-   **Version 21.2.1 - June 2026 \(Zurich\)**
    -   Changed: Updated Commit &amp; Overage \(C&amp;O\)–related role assignments for the vendor\_contact role across SPO tables to ensure consistent access control.
    -   Defect Fixes: Fixed an issue where a Purchase Line was not created in a revised Purchase Requisition when selecting Edit PO.
-   **Version 19.8.1 - June 2026**
    -   Changed:
        -   Remediated non‑Glide Cobalt Raven ACLs in product code \(DIRS0000421\).
        -   Resolved GetRefRecord scoping bypass vulnerability \(DIRS0000408\).
        -   Applied CSRF remediation for APIs \(DIRS0000406\).
        -   Implemented JavaScript sandbox replacement with API allowlist migration \(DIRS0000416\).
    -   Compliance:
        -   Updated Commit &amp; Overage \(C&amp;O\)–related role assignments for the vendor\_contact and platform\_ml\_read roles across SPO tables to ensure consistent access control and alignment with C&amp;O processes.
    -   Defect Fixes:
        -   Fixed issues with Shopping Hub checkout, including cart icon rendering, data loss in the Reason for Purchase field, and removed products reappearing in punchout purchase requisitions.
        -   Resolved issues with tax estimation not displaying for non‑SAP tax engines and failures in exchange rate–based product filtering.
        -   Fixed SLA breach time calculation and invoice query matching issues.
-   **Version 19.6.1 - March 2026**
    -   New:
        -   Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
        -   Enabled decimal quantities for service items in Shopping Hub and Employee Center, configurable through the Unit of Measure Decimal Support decision table.
    -   Changed: Enhanced multi‑currency support to display localized currencies across To‑Dos, emails, and the product Bundles page.
-   **Version 21.0.1 - March 2026 \(Zurich\)**
    -   New:
        -   Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
        -   Enabled decimal quantities for service items in Shopping Hub and Employee Center, configurable through the Unit of Measure Decimal Support decision table.
    -   Changed: Enhanced multi‑currency support to display localized currencies across To‑Dos, emails, and the product Bundles page.
-   **Version 20.5.0 - January 2026 \(Zurich\)**
    -   New:
        -   Introduced automated backfill and update capability for Buyer Group for the following:
            -   Existing active Purchase Requisition Lines \(PRLs\)
            -   Existing Purchase Order \(PO\) headers
            -   Enabled Buyer Group derivation using the finalized Buyer Group determination logic for consistency across PR, PRL, and PO lifecycle.
    -   Changed:
        -   Enhanced Buyer Group user experience:
            -   Added reference icon for Buyer Group field to improve discoverability and usability.
            -   Improved “first PRL” determination logic to ensure accurate Buyer Group validation and enforcement.
            -   Updated ERP-compatible enforcement rules to align Buyer Group validation behavior with downstream ERP requirements.
            -   Refined PO header error messaging to provide clearer, more actionable feedback when Buyer Group is missing or invalid.
    -   Fixed:
        -   Addressed inconsistencies in Buyer Group enforcement across PRLs and PO headers.
        -   Fixed edge cases where Buyer Group was not evaluated correctly due to incorrect PRL sequencing.
    -   Removed: No functionality removed in this release.
-   **Version 18.6.0 - January 2026 \(Yokohama\)**
    -   New:
        -   Introduced automated backfill and update capability for Buyer Group for the following:
            -   Existing active Purchase Requisition Lines \(PRLs\)
            -   Existing Purchase Order \(PO\) headers
            -   Enabled Buyer Group derivation using the finalized Buyer Group determination logic for consistency across PR, PRL, and PO lifecycle.
    -   Changed:
        -   Enhanced Buyer Group user experience:
            -   Added reference icon for Buyer Group field to improve discoverability and usability.
            -   Improved “first PRL” determination logic to ensure accurate Buyer Group validation and enforcement.
            -   Updated ERP-compatible enforcement rules to align Buyer Group validation behavior with downstream ERP requirements.
            -   Refined PO header error messaging to provide clearer, more actionable feedback when Buyer Group is missing or invalid.
    -   Fixed:
        -   Addressed inconsistencies in Buyer Group enforcement across PRLs and PO headers.
        -   Fixed edge cases where Buyer Group was not evaluated correctly due to incorrect PRL sequencing.
    -   Removed: No functionality removed in this release.
-   **Version 20.0.4 - December 2025 \(Zurich\)**
    -   New:
        -   Multi-currency: Supports shoppers and approvers in viewing and selecting their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, My Purchases, and Request Tracker. Currency filtering has also been enhanced as part of this capability.
        -   Additional line-level questions: Enables procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line. Selections for each unique question persist in Workspace and Platform views on both purchase requisition lines and purchase order lines.
-   **Version 18.1.0 - December 2025 \(Yokohama\)**
    -   New:
        -   Multi-currency: Supports shoppers and approvers in viewing and selecting their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, My Purchases, and Request Tracker. Currency filtering has also been enhanced as part of this capability.
        -   Additional line-level questions: Enables procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line. Selections for each unique question persist in Workspace and Platform views on both purchase requisition lines and purchase order lines.
-   **Version 19.0.0 - August 2025**

    New: Update of purchase requisition logic to support native ERP behavior: ServiceNow allows address selection at the Purchase Requisition - Line level, and multiple ERP applications support this as well. However, Coupa does not allow address selection at the line level, but only at the header level. To accommodate such specific behavior, the ServiceNow application logic has been updated to split and group Purchase Requisition lines based on address. This is achieved through a configuration infrastructure that enables developers to insert logic to modify application behavior tagged to specific ERPs.

-   **Version 18.0.25 - October 2025**

    Fixed: Minor defect fix to resolve the issue with Invoice Creation in HANA RFC, ECC IDOC, and HANA IDOC integrations, where invoices were not being created due to ACL restrictions.

-   **Version 18.0.14 - June 2025**

    Fixed: Minor bug fix to resolve an issue where records from the staging table sn\_fcms\_intg\_imp\_receipt had a status of "posted", but after transformation to the base table sn\_shop\_receipt, the status was incorrectly set to "pending\_submission" instead of "posted".

-   **Version 17.6.14 - June 2025 \(Xanadu\)**

    Changed: Minor improvements have been made to the creation of scheduled jobs to populate the ERP Source on Purchase Requisitions and Purchase Orders.

-   **Version 18.0.10 - May 2025**

    Minor fixes.

-   **Version 17.6.10 - May 2025 \(Xanadu\)**
    -   Fixed:
        -   Fixed SR line cancellation issue for close bid supplier flow
        -   Minor bug fixes
-   **Version 18.0.6 - March 2025**

    Fixed: Fixed an issue in Shopping Hub where the date filter on the Similar Products page was not functioning correctly.

-   **Version 17.6.5 - March 2025 \(Xanadu\)**

    Changed: The fix script for updating the ERP Source on historical PR and PO data encountered performance issues. To avoid this issue, you must now run the fix script via a scheduled job to populate the ERP Source on PR and PO.

-   **Version 18.0.1 - February 2025**
    -   New:
        -   Added Deny unless ACLs for subset of tables in app-spend-catalog.
        -   Introduced a new Case Type called "Edit a Receipt."
-   **Version 17.6.1 - January 2025**

    Fixed: Fixed issues for punchout PRL data population.

-   **Version 15.2.1 - January 2025**

    Fixed: ERP source not populated on PR and PO.

-   **Version 17.1.3 - December 2024**

    New: Added new ACL for sn\_shop\_shipment\_details to support effortless access to supplier contact information across multiple suppliers.

-   **Version 17.0.2 - November 2024**
    -   Improved security model adoption. Made Purchase cost allocation table common.
    -   Added the Invoice Cost Allocation table and its associated security
    -   Improved the Approval Rule Engine to accommodate Cost Center Managers approval rule for invoices
    -   Added "Deny Unless" ACLs to the Invoice table for improved security.
-   **Version 15.1.0 - November 2024**

    Created a new staging table for fetching sourcing requests from ERP systems.

-   **Version 16.0.9 - October 2024**
    -   The "Resubmit" button to trigger resubmission of record in case of Integration Failure is renamed as "Retry" in Purchase Orders and Goods Receipt.
    -   Addressed bugs.
-   **Version 16.0.2 - September 2024**

    New: Scripted DEFN for tracking compliance on Source to Pay and Contract Operations SKU.

-   **Version 16.0.1 - August 2024**

    Minor fixes.

-   **Version 15.0.5 - August 2024 \(Washington DC\)**

    Fixed an issue regarding accurately transforming delivery address location into the Locations \(cmn\_locations\) table.

-   **Version 13.1.1 - August 2024 \(Vancouver\)**

    Fixed issues with rendering supplier and category browsing in the Shopping Hub mega menu.

-   **Version 15.0.2 - June 2024**
    -   Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.
    -   Defect fixes.
-   **Version 13.1.0 - June 2024 \(Vancouver\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 11.1.0 - June 2024 \(Utah\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 15.0.1 - May 2024**
    -   New:
        -   Using Employee Center, employees or shoppers can now navigate to punchout supplier sites and make purchases from external sites. Level 1 cXML-based punchout is now supported.
        -   A separate link is available for navigating to third-party supplier sites.
        -   A new widget page that lists out all third-party punchout supplier sites is also available.
-   **Version 11.0.9 - April 2024**

    Minor fixes.

-   **Version 14.2.2 - March 2024**
    -   New: Added a TPRM user role to the procurement specialist role for enabling read access to the risk assessment related lists.
    -   Changed: Configured changes in the decision tables to create a due diligence case when a qualification process is initiated from a sourcing request and negotiation.
-   **Version 1.8.1 - March 2024 \(Vancouver\)**

    Fixed ACL issues with new CAD management tool.

-   **Version 14.0.2 - February 2024**
    -   Changed:
        -   Modified the intake form experience for requesters or employees requesting for multiple items \(goods or services\) from the employee portal. These include the "I need a good" and "I need a service" intake forms \(record producers\). Additionally, there is a new summary page within the employee portal to confirm the submission and item details. If existing customers take this new feature, they will need to apply the modified record producer payload to capture multiple items \(goods or services\). Additionally, changes were made to the out-of-the-box intake form to allow each item \(good or service\) to have the same or different delivery or service address and dates. Existing customers can apply this experience to their own intake forms with their own questions.
        -   Employees can now see to-do tasks such as E-sign, Upload a document, and Submit a form, in their task page on Employee Center.
        -   Right to left language: Minor issues in employee intake forms I need a product and I need a service are fixed as part of this capability.
-   **Version 11.0.8 - December 2023 \(Utah\)**

    Minor fixes.

-   **Version 13.0.2 - November 2023**
    -   New:
        -   Introduced a new approval rule type, which will allow the creation of approvals for multiple cost center managers to approve their cost allocation. This type of approval rule is only applicable for purchase requisitions and approvals will be sent to all the cost center managers where the cost of the purchase has been allocated to their cost center. Note: Existing and new customers would only see these new changes if they have defined the new approval rules for cost center manager approval.
        -   Fulfillers can now assign a procurement task with an action type to an employee or shopper. The action types supported are Watch Video, View Link, and Mark Complete. This feature will guide shoppers on what is expected from them to complete the task. Note: No impact to existing customers for any tasks already created, and they will find these new changes in effect with this upgrade.
        -   Supplier part number is now added in purchase order lines and can be used to import PO data with supplier part number. Note: No impact to existing customers, and they will find these new changes in effect with this upgrade.
    -   Changed:
        -   Shoppers and employees can now see the current status of a case and the remaining steps for it to be completed. Previously, shoppers and employees did not have any visibility into the current status of a case nor how many steps are remaining for the case to be marked as completed. Note: No impact to existing customers, and they will find these new changes in effect with this upgrade.
-   **Version 12.0.2 - August 2023**
    -   New:
        -   To-dos such as receipt confirmation, service acknowledgment, more information needed, and milestone acknowledgment are now rendered in Employee Center. Employees can complete these to-dos in the Employee Center portal itself.
        -   Introduced a new ability for approvers to take actions such as approve, reject, or request clarification, on line-level items in approval to-dos for purchase requisitions within Employee Center.Note: Existing customers leveraging existing approval to-dos for purchase requistions in Employee Center will see these new changes.
-   **Version 11.0.5 - June 2023**

    Fixed: Minor bug fixes.

-   **Version 11.0.3 - May 2023**
    -   New:
        -   Introduced a new playbook to handle GL coding review case type. This playbook walks the fulfiller through specific purchase requisition lines that are missing GL account details such as Capex, expense, and pre-paid accounts.

            **Note:** Modifications were made to the default GL coding review case. If existing or new customers want to leverage this capability, they can reference the GL coding review case that incorporates a new workflow established in Process Automation Designer.

        -   Introduced a new delivery address review case on the procurement case table \[sn\_spend\_psd\_procurement\_request\] to provide a single case to resolve all delivery address approval and verification activities.

            **Note:** All existing address approval and verification tasks are not impacted. By default, these tasks are replaced by the singular delivery address review case that is triggered any time a new address, or a group of addresses, is captured on a purchase requisition.

        -   Approvers can now provide their approval directly within an email notification, with the ability to link to more details of that approval task.

            **Note:** Modifications were made to the default email notifications. If existing or new customers want to leverage this capability, they can reference the new email notifications to get generated in their workflows.

    -   Changed:
        -   Renamed this application to Source-to-Pay Common Architecture. This application was formerly named Procurement Common Architecture.
        -   Updated the approval engine to allow ease of configuring the self-approval functionality through a flag, for an approval task to be explicitly created for a requester even if that requester has the correct approval authority to have self-approved that request.

            **Note:** Existing customers will not be impacted because the flag that acknowledges the existing self-approval functionality is defaulted to true. Customers who do not want the self-approval functionality in their approval rules can set the flag to false.

        -   Extended the request for clarification workflow to sourcing requests so that approvers can ask for more clarifications in their approval to-dos for sourcing request approvals. This intimates the employees or requesters on the need for clarification.

            **Note:** These changes do not impact existing requests for clarification workflows, so existing customers are not impacted. This change is available with the upgrade or installation of this plugin. This feature is also dependent on the installation or upgrade of Employee Center \(sn\_ex\_sp\) version 29.0.1 and Employee Center Core \(sn\_hr\_sp\) version 29.0.3​.

        -   he Integration Error table \(sn\_shop\_erp\_error\_task\) is now made commonly available to provide a single table to address all integration errors.

            **Note:** Existing customers will not be impacted because this change moves a table to a common scope, which existing customers already have as part of their solution's application dependency.

-   **Version 10.0.1 - February 2023**
    -   Changed:
        -   Updated the Invoice and Invoice Line tables to remove business rules that auto-calcuated invoiced amount.
        -   Updated the invoice acknowledgement task to be relabled as service acknowledgement task, with a new service acknowledgement task workflow and UI on Shopping Hub for shoppers to complete their tasks, which would track services receipts.
    -   **Note:** New customers will be impacted by these changes, and there will be a fixed script for existing customers to run if they choose to adopt the new changes.

-   **Version 9.0.6 - December 2022**

    Minor fixes.

-   **Version 9.0.5 - November 2022**

    Minor fixes.

-   **Version 8.0.1 - August 2022**
    -   Changed:
        -   Renamed this application to Procurement Common Architecture. This application was formerly named ShoppingHub.
        -   Moved specific tables to be commonly used and extended by other products. This makes this application a standalone application, with the following tables, ACLs, and form views available. When you purchase Procurement Service Management, you get both this standalone application along with core procurement workflows, business logic, and user experience. Having this standalone application alone does not make core procurement workflows, business logic, and user experience available.
        -   The following tables are made commonly available:
            -   Attribute \(sn\_shop\_attribute\)
            -   Attribute Set \(sn\_shop\_attribute\_set\)
            -   Attribute Type \(sn\_shop\_attribute\_type\)
            -   Delivery Location \(sn\_shop\_delivery\_location\)
            -   ERP Address Mapping \(sn\_shop\_erp\_address\_map\)
            -   ERP Asset Category Mapping \(sn\_shop\_erp\_asset\_category\_map\)
            -   ERP Material Group Mapping \(sn\_shop\_erp\_material\_group\_map\)
            -   Invoice \(sn\_shop\_invoice\)
            -   Invoice Line \(sn\_shop\_invoice\_line\)
            -   Job Code \(sn\_shop\_job\_code\)
            -   Milestone \(sn\_shop\_milestone\)
            -   Office Location \(sn\_shop\_office\_location\)
            -   Order Line Template \(sn\_shop\_order\_line\)
            -   Order Template \(sn\_shop\_order\)
            -   Order to Contract Relationships \(sn\_shop\_m2m\_order\_contract\)
            -   Payment Terms \(sn\_shop\_payment\_term\)
            -   Price Break \(sn\_shop\_price\_break\)
            -   Pricing \(sn\_shop\_m2m\_product\_contract\)
            -   Product Group \(sn\_shop\_product\_group\)
            -   Product Visuals \(sn\_shop\_supplier\_product\_artifact\)
            -   Purchase Order \(sn\_shop\_purchase\_order\)
            -   Purchase Order Line \(sn\_shop\_purchase\_order\_line\)
            -   Receipt \(sn\_shop\_receipt\)
            -   Shipment Details \(sn\_shop\_shipment\_details\)
            -   Shipment Product \(sn\_shop\_shipment\_product\)
            -   Shipping Method \(sn\_shop\_shipping\_method\)
-   **Version 7.0.1 - May 2022**
    -   New:
        -   New way to manage mutiple supplier negotiations through a new table \(Negotiation Events\) and workflow.
        -   New qualification task workflow and decision tables to help procurement teams define what it means to qualify the engagement of a supplier \(that is, defining task orchestration for other teams to collaborate with the procurement team\). Examples of task orchestration includes assessing the risks of a supplier, drafting new contracts with a supplier, and onboarding a supplier.
        -   New way for the procurement organization to define work prioritization by allowing the priority of work to be dynamically defined through decision tables.
    -   Changed:
        -   All purchasing tasks types, except for the need more information and procurement tasks, have been migrated over as cases. This supports case types that need their own complex workflows. Examples of case types are supplier onboarding, supplier risk assessments, supplier tiering assessments, contract reviews, and budget reviews.
        -   The supplier onboarding case is now integrated with the Supplier Lifecycle Management plugin to support a complex process automation workflow, which includes registering, qualifying, and activating suppliers.
        -   Modified the workflow such that multiple approval tasks are not created for the same approver if that approver shows up in multiple approval lists created for the same purchase.
-   **Version 6.0.1 - February 2022**
    -   New:
        -   Approvers can now request clarification and shoppers can provide clarification from ShoppingHub.
        -   Shoppers can now see the reasons for rejection and cancellation of a purchase from My Purchases.
        -   Introduced a new delivery address checkout experience for shoppers to auto-fill delivery address details.
        -   Framework created for customers to plug in an Address Validation Service \(AVS\) into the shopping and checkout experiences for shoppers.
    -   Changed:
        -   Activity stream now provides more detailed information when an item is cancelled, rejected, or clarification is requested.
        -   The purchase status on ShoppingHub is now displayed in badges.


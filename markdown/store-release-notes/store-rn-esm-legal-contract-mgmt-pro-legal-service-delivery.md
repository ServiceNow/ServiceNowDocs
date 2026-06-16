---
title: Contract Management Pro for Legal Service Delivery release notes
description: Version history for the Contract Management Pro for Legal Service Delivery application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-contract-mgmt-pro-legal-service-delivery.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Contract Management Pro for Legal Service Delivery release notes

Version history for the Contract Management Pro for Legal Service Delivery application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.6.1 - June 2026**

    Changed: Enhanced the category description for the Non-Disclosure Agreement contract.

-   **Version 3.5.0 - March 2026**
    -   Fixed:
        -   Assigned to and collaborators cannot be the same users for legal contract requests
        -   Adding collaborators to a contract request no longer triggers duplicate work note entries.
        -   The signed contract is now attached to the wet signature notification when the signature process is completed.
-   **Version 3.0.2 - December 2025**
    -   New:
        -   Initiate and manage amendment requests for existing contracts.
        -   Record producer to initiate an amendment request from the Employee Center.
    -   Fixed:
        -   When changing the company on an NDA or TPC request in the workspace, users are now prompted to update the address.
        -   Security fixes.
-   **Version 2.0.0 - August 2025**
    -   New:
        -   The value in the company field is copied from the legal contract request to the contract request table for every update.
        -   The perpetual field is hidden in legal-based contract requests.
    -   Fixed:
        -   Validation messages have been simplified whenever a legal contract request is cancelled through the employee center.
        -   Validations have been improved to check for duplicate emails for both internal and external signers when sending documents for signature.
-   **Version 1.8.1 - July 2025**

    Fixed: Resolved an issue that caused a query range error to appear when navigating away from the Expiring Contracts/Expired Contracts list in Contract Workspace after running the Writer audit script.

-   **Version 1.8.0 - May 2025**
    -   Changed: The list of dependent applications has been updated to include Contract Management Pro instead of Contracts Core.
    -   Fixed: Localization issues.
-   **Version 1.7.0 - February 2025**
    -   New:
        -   Demo data: You can choose to load demo data for contract templates while installing Contract Management Pro for Legal Service Delivery.
        -   Two new values, "Update request fields with variables" and "Initialize legal contract" are now added in the Options field within the Record Producer section of the Intake form for Practice Area.
        -   Update request fields with variables: When you submit a legal request for contract review or update the variables, the values of the field mapped to the variables are automatically updated.
        -   Initialize legal contracts: A contract request is automatically created when a legal request for contracts is submitted.
        -   A new check box, Add new company name, has been added to the Legal Contract Request form. Selecting this check box will replace the Company field with New company legal name where you can enter the company name.
    -   Changed:
        -   While creating new record producers, you can now validate the state of contract type and restrict creation of a legal request for inactive contract type on submission of the legal request by adding the Verify if Contract type is active script from the base system Non-disclosure Agreement record producer to the new record producer. Note: If Verify if Contract type is active script is not added in the new record producer, the legal request with the corresponding record producer will be created in Cancelled state and the contract request is not created.
        -   The Legal Contract Request form has been updated to display only legal fields and no longer contains any variable fields.
        -   In third-party contract review requests, the Document type field displays only active contract types.
        -   In third-party contract review requests, attached documents and their contract types are now retained when you save the record as a draft. If a contract type is deactivated while the record is in draft state, the Document type field will be blank.
        -   In non-disclosure agreement legal requests, if the contract type is inactive, there's an error while submitting the request.
        -   In Employee Center, you can now attach a document while requesting changes to a contract document in a non-disclosure agreement legal requests. The attached document is added to the Activity stream.
        -   The Activity stream of legal requests in Employee Center now displays the activities in the associated contract request.
        -   When legal fields are modified in a workspace, the updated and previous values are now displayed in the corresponding variables in the Request details tab of a legal request in the Employee Center.
        -   The 'Company legal name' field has been renamed to 'Company' in the Non-disclosure Agreement and Third-party Contract Review intake forms.
        -   The field, 'Is this for a Vendor, Customer or Partner' has been renamed to 'Contract party type'.
    -   Fixed:
        -   Some of the fields in contract repository record do not appear due to missing ACLs. This has been fixed.
        -   Security issues
-   **Version 1.6.0 - November 2024**

    Fixed: You no longer can reclassify a contract document to a supporting document, if it results as a duplicate, where a supporting file already exists with that name.

-   **Version 1.5.0 - August 2024**

    Contract Management Pro for Legal Service Delivery enables enterprises to streamline the request, authoring, review, and approval of contracts for predefined contract templates such as NDAs as well as third-party review request. Legal teams can manage and process contracts from a centralized location or cloud storage and quickly execute them by using popular eSignature integrations with a complete audit trail.



---
title: Parent-linked contract requests
description: Initiate contract, amendment, and renewal requests from a parent record such as a purchase requisition or sourcing event using the Initiate Plug and Play modal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-initiate-contract.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-09-20"
reading_time_minutes: 2
audience: sn\_cm\_core.contract\_fulfiller
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Parent-linked contract requests

Initiate contract, amendment, and renewal requests from a parent record such as a purchase requisition or sourcing event using the Initiate Plug and Play modal.

Parent-linked contract requests are initiated from a parent record such as a purchase requisition or sourcing event. The Initiate Plug and Play modal opens, allowing you to provide key contract request details. The contract request is automatically linked to the parent record, and the business unit context is preserved for assignment routing and reporting.

## Request types

You can initiate the following types of parent-linked requests:

-   **New contract requests**

    Submit a request to create a new contract.

-   **Amendment requests**

    Modify, add, or remove specific terms or clauses in an active contract due to business or regulatory changes. The amendment request is automatically linked to the original contract.

-   **Renewal requests**

    Extend a contract that is approaching or past its expiration date, with the option to update terms. The renewal request is automatically linked to the previous contract.


## Paper types

Each request type \(new contract, amendment, or renewal\) can use one of the following paper types:

-   **Own paper**

    The contract is created from your company's predefined templates. The template is automatically applied when you select the contract type.

-   **Third-party paper**

    Upload and review the contract documents provided by the other party. You must attach at least one document and classify it appropriately.


## Contract request states

The initial state of a submitted contract request depends on the request type and the details provided.

-   **New contract requests**
    -   Own paper with all required fields provided — Work in progress.
    -   Own paper with incomplete details — Draft.
    -   Third-party paper — Draft.
    -   Third-party paper — New, if complete, or Draft, if incomplete.
-   **Amendment requests**
    -   Own paper or third-party paper with all required details — New.
    -   Own paper or third-party paper with incomplete details — Draft.
-   **Renewal requests**
    -   Self-serve own paper with all required fields — Work in progress.
    -   Non-self-serve own paper with all required details — New.
    -   Non-self-serve own paper with incomplete details — Draft.
    -   Third-party paper — New, if complete, or Draft, if incomplete.

-   **[Initiate an own paper contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-self-served-contract.md)**  
Initiate an own paper contract request linked to a parent record such as a purchase requisition or sourcing event. Own paper contracts use predefined templates to generate contract documents.
-   **[Initiate a third-party paper contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-non-ss-cnt.md)**  
Initiate a third-party paper contract request linked to a parent record such as a purchase requisition or sourcing event. Third-party paper contracts are external contracts uploaded for review and signature.
-   **[Initiate an amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-amedment.md)**  
Initiate an amendment request linked to a parent record such as a purchase requisition or sourcing event. Amendment requests modify existing active contracts.
-   **[Initiate a renewal request from a parent record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-initiate-renewal.md)**  
Initiate a renewal request linked to a parent record such as a purchase requisition or sourcing event. Renewal requests extend or replace existing contracts that are active or expired.
-   **[Initiate an amendment from a contract record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-amend-from-cntr.md)**  
From an active contract record, initiate an amendment request to modify the contract terms, clauses, or details.
-   **[Initiate a renewal from a contract record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renew-from-cntr.md)**  
From an active or expired contract record, initiate a renewal request to extend or replace the contract with a new contract period.
-   **[View and track contract request details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-view-creq-details.md)**  
View the details and track the activities of the contract request.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-use-cmpro.md)


---
title: Standalone contract requests
description: Submit and track contract, amendment, and renewal requests using a record producer form without linking to a parent record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-sa-submit.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [standalone contract request, record producer]
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Standalone contract requests

Submit and track contract, amendment, and renewal requests using a record producer form without linking to a parent record.

Standalone contract requests are submitted using a record producer form that guides you through entering all required contract details. The record producer form allows you to save your work as a draft and return to complete it later. Standalone requests aren't linked to a parent record such as a purchase requisition or sourcing event.

## Entry points

You can access the record producer from the following entry points based on your role:

-   **Employee Center**

    Navigate to **Employee Center** &gt; **Help center** &gt; **Contracts** and select **Contract request**, **Contract Amendment and Renewal request**. This entry point is available to users with the sn\_cm\_core.contract\_user role.

-   **Contract Workspace and contract request listing**

    Navigate to the contract request list page and select **New**. You can access the list page either from the widgets on the Contract Workspace landing page or by opening the contract request list directly and selecting categories under it. This entry point is available only to users with the sn\_cm\_core.contract\_fulfiller role.


## Request types

You can submit the following types of standalone requests:

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


## Assignment and fulfillment

After you submit a standalone contract request, it is automatically assigned to a group or user based on the default assignment rule. A contract fulfiller can assign a contract request to themselves. A group manager can assign a contract request to any member of the assignment group.

For more information, see [Assign a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-assign-con-req.md).

## Configurations

For standalone requests the required configurations should be done on the Contract Request table \[sn\_cm\_core\_contract\_request\].

For more information on the configurations, see [Configuring Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-config-cmpro.md).

-   **[Submit a standalone own paper contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-own-paper.md)**  
Submit a new own paper contract request using a record producer form from Employee Center or a contract listing page without linking to a parent record.
-   **[Submit a standalone third-party paper contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-third-party.md)**  
Submit a new third-party paper contract request using a record producer form from Employee Center or a contract listing page without linking to a parent record.
-   **[Submit a standalone amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-amendment.md)**  
Submit an amendment request from Employee Center or a contract listing page to modify an existing active contract.
-   **[Submit a standalone renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-renewal.md)**  
Submit a renewal request from Employee Center to renew an existing contract.
-   **[View and track standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-track-req.md)**  
View the details of a contract request after it has been submitted and track the activities in the request.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-use-cmpro.md)


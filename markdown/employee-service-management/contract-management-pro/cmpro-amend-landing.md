---
title: Contract amendments
description: The contract amendment workflow enables you to initiate, manage, and track changes to existing contracts through amendment requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cmpro-amend-landing.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Amendment request, Amend contract, Amendment workflow]
audience: sn\_cm\_core.contract\_fulfiller
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract amendments

The contract amendment workflow enables you to initiate, manage, and track changes to existing contracts through amendment requests.

Amendments can be made by adding, removing, or updating terms, without the need to replace the entire contract.

You can initiate an amendment request from your workspace using the **Initiate contract** modal or from the contract repository record using the **Amend** option.

To initiate an amendment request, verify you have configured the Initiate Contract modal and Amend option.

## Types of paper for an amendment

The amendment workflow supports both own-paper and third-party amendment requests.

**Note:** Third-party amendments are supported only for single contract types.

While submitting an amendment request, you can select the **Type of paper** from initiate contract modal.

\[Omitted image "cmpro-amend-type-paper-initiate.png"\] Alt text: Select amendment type

## View contract amendment details

The following tabs are available within the contract repository record to provide amendment details:

-   Contract Documents: Provides access to all signed documents related to the contract, including those generated or updated as part of amendment processes.
-   Contract Requests: Displays all contract and amendment requests associated with the contract.
-   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.

\[Omitted image "cmpro-amend-tabs-cntr.png"\] Alt text: Contract repository record showing amendment related details

## Contract amendment workflow

The contract amendment workflow might progress as follows:

1.  The contract requester does the following:
    1.  Initiates an amendment request from the workspace.
    2.  Enters amendment details and submits the request.
    3.  Initiates an amendment request.
    4.  For third-party paper amendment request, attaches contract document. For own-paper, the document is generated from a contract template.
    5.  Link a parent contract.
    6.  Submits amendment request.
2.  The contract fulfiller does the following:
    1.  Review the details of the amendment requested.
    2.  Link a parent contract if already not linked or wants to change the linked parent contract.
    3.  Assign the amendment contract request.
    4.  Start working on the amendment request.
    5.  Update the contract details and contract document according to the amendment request.
    6.  Upload revised contract document using **Create revision** option.
    7.  Finalizes the contract amendment using the review, approval, and signature workflow.
3.  After all signatories have approved the document, the signed amendment is attached to the contract repository record.
4.  The contract repository record displays the amendment details in the Contract Documents, Contract Requests, and Amendment Field Changes tabs.
5.  The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The signed contract and its amendment documents are stored in a centralized repository under the parent contract for easy access and manage all related documents from a single location. The field values that have been modified will be updated in the amendment according to the contract configuration mapping.

## ServiceNow Otto for Contract Management Pro features for amendment documents

For amendment documents, ServiceNow Otto for Contract Management Pro features of obligation extraction or metadata extraction aren’t supported. However, Contract Analysis is supported when all the configurations are complete and valid, enabling you to review and analyze amendments effectively.

For more information, see [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md).

## Amendment and renewal interactions

You can submit both amendment and renewal requests for the same contract. The system allows parallel processing without blocking either request type. When you submit an amendment request while a renewal is in progress, or submit a renewal request while an amendment is in progress, the system displays warnings about potential conflicts.

For more information about how amendment and renewal requests interact, see [Amendment and renewal interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-amend-renewal-int.md).

-   **[Approve contracts to allow amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-approve-draft-cntr.md)**  
Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, you need to manually approve it before submitting an amendment request.
-   **[Work on amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-amend-work.md)**  
Review and work on an amendment request for an existing contract.
-   **[View amendment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-view-amend-details.md)**  
View the amendment details in the contract repository record.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-use-cmpro.md)


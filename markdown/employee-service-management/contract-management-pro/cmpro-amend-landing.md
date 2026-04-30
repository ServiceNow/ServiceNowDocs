---
title: Contract amendments
description: The contract amendment workflow enables you to initiate, manage, and track changes to existing contracts through amendment requests.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-10-19"
reading_time_minutes: 4
keywords: [Amendment request, Amend contract, Amendment workflow]
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract amendments

The contract amendment workflow enables you to initiate, manage, and track changes to existing contracts through amendment requests.

Amendments can be made by adding, removing, or updating terms, without the need to replace the entire contract.

You can initiate an amendment request from your workspace using the **Initiate contract** modal.

To initiate an amendment request from your workspace, verify you have configured the initiate contract button. For more information, see [Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md).

![Use initiate contract modal from the workspace to submit an contract amendment request](../image/cmpro-amend-initiate.png)

## Distinguish contract and amendment request

The field, **Request type**, differentiates between contract and amendment requests. For amendment request, the value is **Amendment** and for contract request it’s **New contract**.

The Request type field is displayed in the contract details secondary header, and list pages making it easy to differentiate between the two request types.

This field is also present in the configurations: Contract template rule and contract configuration records to indicate if the configuration applies to a contract or an amendment request.

![Request type field to differentiate between contract and amendment request](../image/cmpro-amend-req-type-field.png)

If you have customized the workflow to support amendments; the Request Type field may not display the correct value to differentiate between new contracts and amendments. To resolve Request type field value, update the script **Populate Request Typescript in CMR** and run it to set the request type correctly.

## Types of paper for an amendment

The amendment workflow supports both own-paper and third-party amendment requests.

**Note:** Third-party amendments are supported only for single contract types.

While submitting an amendment request, you can select the **Type of paper** from initiate contract modal.

![Select amendment type](../image/cmpro-amend-type-paper-initiate.png)

## View contract amendment details

The following tabs are available within the contract repository record to provide amendment details:

-   Contract Documents: Provides access to all signed documents related to the contract, including those generated or updated as part of amendment processes.
-   Contract Requests: Displays all contract and amendment requests associated with the contract.
-   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.

![Contract repository record showing amendment related details](../image/cmpro-amend-tabs-cntr.png)

## Contract amendment workflow

The contract amendment workflow might progress as follows:

1.  The contract requester does the following:
    1.  Initiates an amendment request from the workspace.
    2.  Enters amendment details and submits the request.
    3.  Initiates an amendment request.

        **Note:** Amendment request is created in Draft state.

    4.  For third-party paper amendment request, attaches contract document. For own-paper, the document is generated from a contract template.
    5.  Link a parent contract.
    6.  Submits amendment request.
2.  The contract fulfiller does the following:
    1.  Link a parent contract if already not linked or wants to change the linked parent contract.
    2.  Assign the amendment contract request.
    3.  Start working on the amendment request.
    4.  Review the details of the amendment requested.
    5.  Update the contract details and contract document according to the amendment request.
    6.  Upload revised contract document using **Create revision** option.
    7.  Finalizes the contract amendment using the review, approval, and signature workflow.
3.  After all signatories have approved the document, the signed amendment is attached to the contract repository record.
4.  The contract repository record displays the amendment details in the Contract Documents, Contract Requests, and Amendment Field Changes tabs.
5.  The signed contract is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The signed contract and its amendment documents are stored in a centralized repository under the parent contract for easy access and manage all related documents from a single location. The field values that have been modified will be updated in the amendment according to the contract configuration mapping.

## Now Assist in Contract Management features for amendment documents

For amendment documents, Now Assist in Contract Management features of obligation extraction or metadata extraction aren’t supported. However, Contract Analysis is supported when all the configurations are complete and valid, enabling you to review and analyze amendments effectively.

For more information, see [Now Assist in Contract Management](../concept/cncore-now-assit-landing.md).

-   **[Approve contracts to allow amendments](cmpro-approve-draft-cntr.md)**  
Amendment requests can only be submitted for contracts in the Active state. If a contract is in Draft state and Awaiting Review substate, you need to manually approve it before submitting an amendment request.
-   **[Work on amendment request](cmpro-amend-work.md)**  
Review and work on an amendment request for an existing contract.
-   **[View amendment details](cmpro-view-amend-details.md)**  
View the amendment details in the contract repository record.

**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)


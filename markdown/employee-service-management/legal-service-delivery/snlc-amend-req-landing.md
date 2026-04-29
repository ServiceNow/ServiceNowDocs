---
title: Contract amendments
description: The contract amendment workflow enhances contract lifecycle management by enabling you to initiate, track, and finalize amendments to existing contracts with an audit trail.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Amendment request, Amend contract, Amendment workflow, Contract amendment, Amendment]
breadcrumb: [Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Contract amendments

The contract amendment workflow enhances contract lifecycle management by enabling you to initiate, track, and finalize amendments to existing contracts with an audit trail.

Amendments can be made by adding, removing, or updating terms, without the need to replace the entire contract.

You can use the **Amendment request** intake form available in the Employee Center to submit an amendment request.

![Use the Amendment request record producer from Employee Center to submit an contract amendment request](../image/lsd-amend-rp.png)

## Distinguish contract and amendment request

The field, **Request type**, differentiates contract and amendment requests. For amendment request, the value is **Amendment** and for contract request its **New contract**.

The Request type field is displayed in the contract details secondary header, and list pages making it easy to differentiate between the two request types.

This field is also available in the following base system configurations \(when demo data is installed\) to indicate whether the configuration applies to a contract or an amendment request:

-   Contract template rules
-   Contract configurations

![Request type field to differentiate between contract and amendment request](../image/lsd-amend-field-request-type.png)

## Types of paper for an amendment request

The amendment workflow supports both own-paper and third-party amendment requests.

**Note:** Third-party amendments are supported only for single contract types.

While submitting an amendment request, you can select the **Type of paper** from the intake form.

![Select amendment type](../image/lsd-amend-type.png)

## Amendment intake form and record producer

The intake form and record producer for an amendment are available in the base system, enabling you to submit an amendment requests.

![Amendment intake from and record producer in the base sytem (OOB)](../image/lsd-amend-OOB-intakeform.png)

You can also create a customized record producer by copying a base system \(OOB\) record producer to reuse its existing configuration settings. For more information on how to create record producer, see [Create a legal contract intake workflow](../task/snlc-create-legal-contract.md).

While linking the record producer to an intake form, verify that the **Amendment request indicator** is selected in the **Options** field.

The following other configurations are available in the base system when demo data is installed:

-   Contract template \(Sample - NDA Amendment-SignBlocks\) used to generate amendment document for own-paper based amendment request.
-   Contract template rule \(Sample - NDA Amendment-SignBlocks\) to identify the contract template used for generating a contract document for an amendment request.
-   Contract Configuration \(Sample - NDA Amendment-SignBlocks\) to define and map the fields that will be populated in the amendment document.

## View contract amendment details

The following tabs are available within the contract repository record to provide amendment details:

-   Contract Documents: Provides access to all documents related to the signed contracts, including those generated or updated as part of amendment processes.
-   Contract Requests: Displays all contract and amendment requests associated with the contract.
-   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.

![Contract repository record showing amendment related details](../image/lsd-amend-related-lists.png)

## Contract amendment workflow

The contract amendment workflow might progress as follows:

1.  The contract requester does the following:
    1.  Initiates an amendment request from the Employee Center.
    2.  Selects a contract for amendment or enters contract details manually.

        **Note:** When a contract is selected while submitting an amendment request, it’s automatically linked as the parent contract for the amendment request.

    3.  Enters amendment details and submits the request.
2.  The contract fulfiller does the following:
    1.  Assign the amendment contract request.
    2.  Link a parent contract, if it’s already not linked.
    3.  Modify legal request.
    4.  Review the details of the amendment requested.
    5.  Update the contract details and contract document according to the amendment request.
    6.  Upload revised contract document using **Create revision** option.
    7.  Finalizes the contract amendment using the review, approval, and signature workflow.
3.  After all signatories have approved the document, the signed amendment is attached to the contract repository record.
4.  The contract repository record displays the amendment details in the Contract Documents, Contract Requests, and Amendment Field Changes tabs.
5.  The signed amendment is stored on the ServiceNow instance or an external storage system and referenced in the contract repository. The signed contract and its amendment documents are stored in a centralized repository under the parent contract for easy access and manage all related documents from a single location. The field values that have been modified is updated in the amendment according to the contract configuration mapping.

## Now Assist in Contract Management features for amendment documents

For amendment documents, Now Assist in Contract Management features of obligation extraction or metadata extraction aren’t supported. However, Contract Analysis is supported when all the configurations are complete and valid, enabling users to review and analyze amendments effectively.

For more information, see [Now Assist in Contract Management](../../contract-mgmt-pro/concept/cncore-now-assit-landing.md).

-   **[Submit amendment request](../task/snlc-amend-inititate-req.md)**  
Submit an amendment request from the Employee Center.
-   **[View and track amendment requests as a legal user](../task/snlc-view-amend-req-details.md)**  
View the details of an amendment request after it has been submitted and track the activities in the request.
-   **[Work on amendment request](../task/snlc-amend-work.md)**  
Review and work on an amendment request for an existing contract.
-   **[View amendment details](../task/lsd-view-amend-details.md)**  
View the amendment details in the contract repository record.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement requests](snlc-request-nda-1.md)

[Third-party contract review requests](snlc-request-third-party-contract-1.md)

[Linking parent-child contracts](snlc-linking-parent-child.md)

[Internal review overview](../task/snlc-expert-review.md)

[Cancel a legal request](../task/snlc-cancel-request-tpc.md)

[View and download a signed contract document](../task/snlc-preview-contract.md)

[View contract requests](../task/snlc-view-contract-requests.md)

[Manage Contract Management Pro for Legal Service Delivery](snlc-manage-sn-legal-contracts.md)


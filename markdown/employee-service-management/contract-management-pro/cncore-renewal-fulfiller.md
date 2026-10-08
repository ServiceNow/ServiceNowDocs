---
title: Work on a renewal request
description: Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 4
keywords: [Renewal request, Fulfiller, Renewal workflow, Executed renewal contract]
breadcrumb: [Contract renewals, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Work on a renewal request

Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.

## About this task

A submitted renewal request is routed by paper type and by whether a previous contract is linked:

-   An own-paper renewal that has a linked previous contract and all required details lands in the Work in Progress state, ready for the contract user or fulfiller to work on or send for signature.
-   An own-paper renewal with a previous agreement that is not linked, and a third-party-paper renewal, lands in the New state when complete, to be picked up by a contract fulfiller.
-   A renewal with incomplete details lands in the Draft state, and the requester is prompted to complete the details before it moves to the next state.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to your workspace.

2.  Open the renewal request.

3.  Assign to yourself and start working on the renewal request.

    1.  Select **Assign to me**.

    2.  Select **Start work**.

    The state of the contract request updates to Work in progress.

4.  Link the previous contract.

    1.  Navigate to the Contract request details section.

    2.  In the field, **Previous contract record**, select the Search for Record icon \(\[Omitted image "lsd-cont-rec-search.png"\] Alt text: Search for Record icon\).

    3.  Select the contract from the Previous contract pop-up window.

        The list displays active contracts with end dates and expired contracts with no pending renewal requests. Contracts are filtered by contract type and company name \(if provided\).

        When a renewal request is linked to a previous contract, the renewal does not inherit the previous contract's parent-child hierarchy or related-contract family structure. The renewed contract is a new contract connected to the previous one through the renewal link, not a child of it.

5.  Download the contract document.

    1.  Navigate to the **Contract documents** tab.

    2.  Select **Preview document**.

    3.  Select the contract type.

    4.  Select **Preview**.

        The document opens in a new tab.

    5.  Select the Download icon \(\[Omitted image "download-icon.png"\] Alt text: Download icon\).

        The document is downloaded to your system.

    6.  Edit the document for the renewal.

        While authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.

6.  Upload the revised contract document.

    1.  In the **Contract documents** tab, select **Create Revision**.

    2.  In the Create revision dialog box, select the source of the updated contract and upload a new document revision.

    3.  Add work notes to provide any information on the attached document.

    4.  Select **Create**.

    The attached document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document is listed in the **Contract documents** tab.

7.  Add or remove signatories to the contract request.

    |Options|Steps|
    |-------|-----|
    |**Add signatory**|Add signatories to the contract request by accessing the **Signatories** tab and selecting **Add**.|
    |**Remove signatory**|Remove signatories from the contract request by accessing the **Signatories** tab, selecting the signatory, and selecting **Remove**.|

    **Note:** You can add or remove signatories in own-paper based renewal requests only when the contract is generated from a template configured with signature blocks.

8.  For own paper-based contracts with metadata or signatory changes, synchronize the document by selecting **Sync document** in the **Contract documents** tab.

    A new contract document revision is created with the updated metadata and signatories. The changes made in the previous revision are retained.

9.  Finalize the renewal request using the review, approval, and signature workflows.

    |Options|Steps|
    |-------|-----|
    |**Ad hoc approval**|[Initiate an ad hoc approval for a contract document revision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-initiate-approval-cr.md)|
    |**Internal review**|[Request an internal review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-add-review-task.md).|
    |**Email communication**|Set up an email to stakeholders to have the completed contract document reviewed and the changes confirmed using the **Compose Email** option.|
    |**Signature workflow**| |

10. Send the contract document for signature.

    For more information, see [Signature workflow for a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-lsd-signature-workflow.md).


## Result

When all signatures are complete, the request moves to Contract Signed and then Closed complete.

-   A new contract repository record is created.
-   All configured field values are copied to the new contract.
-   The renewal history is available in **Contract History** tab.
-   When both amendment and renewal requests are active on the same contract, review the following to avoid conflicts:

    -   Contract dates to prevent overlapping effective periods between the amended contract and the renewed contract
    -   Terms and pricing changes in both requests
    -   Effective dates and expiration dates
    You must manually reconcile any conflicts between the amended original contract and the renewed contract.


**Parent Topic:**[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-renewal-landing.md)

**Related topics**  


[View renewal details]()

[Amendment and renewal interactions]()


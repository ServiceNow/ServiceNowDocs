---
title: Work on a non-self-served contract review request
description: Review and revise a non-self-served contract document. As a collaborator on the request, you can email the revised document to stakeholders to verify the revisions, and then send the ready document for an e-signature from within the contract request.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Use non-self-served contract request, Use Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Work on a non-self-served contract review request

Review and revise a non-self-served contract document. As a collaborator on the request, you can email the revised document to stakeholders to verify the revisions, and then send the ready document for an e-signature from within the contract request.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

## Procedure

1.  Navigate to your workspace.

2.  On the **Lists** tab, open a contract request by selecting an option under **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d562372e75">

Option

</th><th align="left" id="d562372e78">

Steps

</th></tr></thead><tbody><tr><td id="d562372e84">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state and the Contract status of the contract request is Work in progress.

</td></tr><tr><td id="d562372e113">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>3.  If you need help from other fulfillers to work on the contract request, add them in the **Collaborators** field.

    **Note:** Users with the sn\_cm\_core.contract\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a contract request.

4.  Reclassify the contract or supporting documents submitted for review.

    Examples of reclassifying the contract or supporting documents are:

    -   You can change the contract document type from a Non-disclosure Agreement to a Partnership Agreement. For more information, see [Reclassify contract documents in third-party contract request](cncore-nss-reclassify-doc.md).
    -   You can change the supporting document to a contract document. For more information, see [Reclassify supporting documents in the contract request](cncore-nss-reclassify-supdoc.md).
5.  Open an existing revision of a contract document.

    -   For internal storage: Open the document revision record by navigating to the **Contract documents** tab and then selecting the name of the document.
    -   For external storage: View the document online by navigating to the **Contract documents** tab and then selecting the link on the **URL** tab.
6.  Review the contract documents.

7.  Create document revisions.

    For more information, see [Create a document revision](cncore-create-doc-rev.md).

8.  Analyze the contract documents to identify non-standard and missing clauses by using Now Assist in Contract Management.

    For more information, see [Contract analysis using Now Assist in Contract Management](../concept/cncore-NA-review-land.md).

9.  If an approval is required from other stakeholders, send the document for ad-hoc approval.

    For more information, see [Initiate an ad hoc approval for a contract document revision](cmpro-initiate-approval-contract-request.md).

10. Set up an email to stakeholders to have the completed contract document reviewed and the changes confirmed.

    For more information, see [Send email to stakeholders](cncore-send-email.md).

11. Add the internal or external signatories needed for e-signatures on the contract by navigating to the **Signatories** tab and then selecting **Add**.

<table id="choicetable_hm4_3vk_byb"><thead><tr><th align="left" id="d562372e315">

Option

</th><th align="left" id="d562372e318">

Steps

</th></tr></thead><tbody><tr><td id="d562372e324">

**Internal**

</td><td>

1.  In the **Internal Signer** field, enter the name of the signer. The**Authorized signatory name**, **Signatory**, and **Signatory email** fields are automatically populated.
2.  In the **Order** field, enter the order in which the contract should be sent to the signer. The order value should be unique. For example: Enter the order numbers as 10, 20, 30, and so on, increasing by 10 each time. The system starts sending the contract to the internal signer with the lowest number.


</td></tr><tr><td id="d562372e357">

**External**

</td><td>

1.  In the **Authorized signatory name** field, enter the external signer's name.
2.  In the **Signatory** field, enter the external signer's title.
3.  In the **Signatory email** field, enter the external signer's email address.
4.  In the **Order** field, enter the order in which the contract should be sent to signers for an e-signature. The order value should be unique. For example: Enter the order numbers as 10, 20, 30, and so on, increasing by 10 each time. The system starts sending the contract to the external signer with the lowest number.


</td></tr></tbody>
</table>12. When all stakeholders have agreed on a contract document revision, select **Prepare for Signature** to prepare and send the document to the signatories for e-signatures.

    **Note:** The option to reorder is seen only when multiple documents are attached.

    1.  In the Reorder the document pop-up window, drag and place the documents to define the order.

    2.  Select **Prepare for Signature**.

        **Note:** When you select **Prepare for Signature**, the document opens in the configured e-signature system.

        -   For DocuSign, the document opens automatically in the e-signature portal without requiring a login.
        -   For Adobe Sign, you must log in to the e-signature portal to open the document.
    The document status updates to Preparing for Signature. The contract documents submitted in the non-self-served contract request are combined into a single document and sent for Prepare Signature.

13. Complete the document in the configured e-signature system and send it for signature.

    1.  Preview the document to ensure that the content is correct.

    2.  Add the required fields, including the **Signature** field.

    3.  Select **Send**.

    An e-signature envelope is created and sent to all signatories. If the system receives a success notification from the electronic signature provider, the State and Contract status updates to Awaiting Signature.

14. If you need to cancel the signature request before all signers have completed signing the document, select **Cancel signature**.

    The contract request State updates to Work in Progress and the Contract document Status updates to Signature canceled.


## What to do next

-   Signatories can sign or decline to sign the contract.

    For more information, see [Signature workflow for a contract request](../concept/cncore-signature-workflow.md).

-   Check the contract request state and the contract document status in the request:
    -   If all signatories sign the contract document, the contract document status updates to Contract signed. On the **Signatories** tab, the status of all signatories updates to Signed. You can access the contract repository record from the **Contracts Repository** tab.
    -   If any signatory declines to sign the contract document, the Contract Status updates to Signing Declined. If more changes are required in the contract document, update it and resend it to the signatories for their signatures.
    -   After all the signatories have signed the document, an email is sent to the signatories with the finalized contract document attached.
-   If the contract is signed by all signatories, you can close the request by selecting **Close Complete**.

**Parent Topic:**[Use non-self-served contract request](../concept/cncore-req-nss-contract-1.md)


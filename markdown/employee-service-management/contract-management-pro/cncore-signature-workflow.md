---
title: Signature workflow for a contract request
description: Contract Management Pro supports electronic signature or wet \(manual\) signature for a contract request.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Signature workflow for a contract request

Contract Management Pro supports electronic signature or wet \(manual\) signature for a contract request.

-   Electronic Signature: Enables signatories to sign the contract document electronically. For more information, see [Configure an e-signature provider](../task/cncore-integrate-esign.md).

    If you want to generate a certificate of completion, you must select the **Electronic Signature** as signature type in the contract request. For more information, see [Activate a system property to generate a certificate of completion](../task/cncore-config-system-prop-COC.md).

-   Wet Signature: Enables signatories to sign the contract document manually. You can then upload the signed document to a contract request. For more information, see [Upload a manually signed contract document](../task/cncore-upload-doc-wsignature.md).

## Electronic signature workflow

-   Send the finalized document to the signatories for signing.
    -   The state and contract status updates to Awaiting Signature and the electronic signature flow is triggered as configured in [Configure an e-signature provider](../task/cncore-integrate-esign.md).
    -   An email notification that the contract document is available for signature is sent to the first signatory. The email contains a link to the contract document that the signatory can open and sign the document through the Docusign or Adobe Acrobat Sign electronic signature provider.

        The signatories will receive signature request email according to the order set in the signatories tab.

    -   The signatory fields—such as Name, Title, and Email—are not pre-filled in the contract document before it is sent for signature. These fields will be populated by the electronic signature provider when the signatory access the document to sign it.
-   Signatories can sign or decline the contract document.

<table id="table_t4x_51l_s2c"><thead><tr><th>

Signatories action

</th><th>

Workflow

</th></tr></thead><tbody><tr><td>

All the signatories choose to do an electronic signature

</td><td>

-   First signatory signs the contract document

If there is more than one signatory,the contract document is sent to the next signatory in the order.

The status of the current signatory in the request updates from Pending Signature to Signed. The status of the next signatory updates from Not Started to Pending Signature.

-   After the last signatory has signed the document, the contract repository record is created and the signed document is attached to it.

For contract requests containing multiple contract documents, the signed contract document is split into individual documents and attached to the contract repository record for the respective contract type.

The state of the requests updates to Contract Signed.

</td></tr><tr><td>

One or more signatories decide to do a wet signature

</td><td>

-   One or more signatories decided to do a wet signature instead of electronic signature.
-   The wet signed contract document in PDF format is shared with the contract fulfiller.
-   The contract fulfiller uploads the signed document, selects the signatories who have shared the wet signed contract document and proceeds with the signature worklow by sending the document to the next signatories.

The status of the signatory in the request updates from Pending Signature to Signed. The status of the next signatory updates from Not Started to Pending Signature. The signature type is updated to Mixed signature after all the signatories have signed the document.

-   After the last signatory has signed the document, the contract repository record is automatically created and the signed document is attached to it.

For contract requests containing multiple contract documents, the signed contract document is split into individual documents and attached to the contract repository record for the respective contract type.

The state of the requests updates to Contract Signed.

</td></tr><tr><td>

The document is declined by the signatory.

</td><td>

An email notification that the signer has declined to sign the document is sent to the requester.The Signatory status in the request updates to Declined.

The State changes to Work in progress and the Contract status changes to Signing Declined.

</td></tr><tr><td>

The signature request is not delivered to a signatory.

</td><td>

The Signatory status in the contract request changes to Delivery failed.

 The state of the contract request changes to Signature delivery failed.

 An email notification is sent to the contract fulfiller informing them that the signature request could not be delivered.

 A notification appears on the contract request informing about the undelivered signature request and the available actions for the fulfiller.

-   For Docusign, you can update the signatory's information and retry, cancel the signature process to restart it, or upload a manually signed contract.
-   For Adobe Sign, you can cancel the signature process to restart it, or upload a manually signed contract.


</td></tr><tr><td>

The contract document is resent for signature.

</td><td>

For contract request fulfilled by the contract user: A contract user can submit a change request. The contract fulfiller works on the change request and sends the updated document back to the contract requester. The updated contract document is sent for signature by the contract user.

 For contract request fulfilled by contract fulfiller: The contract fulfiller creates a document revision manually or by using regenerate option and resends the document for signature.

</td></tr></tbody>
</table>    If the system property **sn\_cm\_core.enable\_executed\_contract\_audit\_certificate** is set to true, the certificate of completion is generated and attached to the contract repository record.


## Wet signature workflow

-   Send the finalized document to the signatories for signing.
    -   The state and contract status are updated to Awaiting signature.
    -   An email notification is sent to the first signatory in order and the contract documents are attached as PDFs in the email.

        The current signatory is placed in the To field of the email. The contract fulfiller, the person who opened the contract, the person for whom the contract was requested, and the initiator of send for signature action are placed in the CC field.

-   Signatories accept or decline the document.

<table id="table_bhy_sqw_cfc"><thead><tr><th>

Signatories action

</th><th>

Workflow

</th></tr></thead><tbody><tr><td>

The current signatory accepts the document and there are pending signatories

</td><td>

-   The signatory prints the contract document,signs it, and then returns it to the signature requester.
-   On receiving the signed contract document, the contract fulfiller uploads the signed contract and sends the document to the pending signatories.


</td></tr><tr><td>

The signatory declines the document

</td><td>

The signatory sends the document back to the requester for necessary correction. The signatories and the contract fulfiller can collaborate and finalize the contract document.

</td></tr><tr><td>

All the signatories have signed the document

</td><td>

-   On receiving the contract document signed by all the signatories, contract fulfiller uploads the signed contract document in PDF format.
-   The contract document is added to the repository after it is uploaded.
 For self-served contracts, the state of the request updates to Closed complete and the contract status updates to Contract signed.

 For non-self-served contracts, the state of the request and the contract status updates to Contract signed. To close the contract request, select Close complete.

 For more information, see [Upload a manually signed contract document](../task/cncore-upload-doc-wsignature.md).

</td></tr></tbody>
</table>
## Modify signatories when the signature workflow is in progress

Modify Signatories options enables you to add, remove, edit, or reorder pending signatories  while a signature workflow is in progress. Initiating this action pauses the signature workflow  for a duration defined by the system property  **maximum\_signature\_pause\_duration**. To continue the signature workflow after making changes, use the  **Resume Signature ** option to resume the workflow.

The workflow might progress as follows:

-   Use **Modify signatories** option to modify the signatories.
-   Add, remove, modify, or reorder signatories.

    **Note:**

    -   For signature block-based contract templates, you can add, modify, remove, and reorder actions, whereas for participant based templates, only modify and reorder actions are enabled.
    -   Modify signatories option is available in wet signature workflow and Electronic signature workflow with Docusign electronic signature provider integration.
-   Select **Resume signature** to resume the signature workflow once modifications are complete.

    **Note:** If the signature workflow is not resumed within the configured time duration, any changes made to the signatories are reverted, and the signature workflow resumes from its previous state.

-   Signature request email notifications are sent to the signatories.
-   After the last signatory has signed the document, the contract repository record is created and the signed document is attached to it.

For more information, see [Modify signatories](../task/cncore-pause-signature.md) and [Resend signature request](../task/cncore-resend-sign-req.md).

## Contract document access

Access to a contract document is based on the following user roles and conditions:

-   A contract fulfiller can view and update contract documents
-   Only a contract administrator can delete contract documents.
-   Requesters can view only the contract documents for which they submitted the contract request.
-   Users added to the watch list can view only contract documents for contract requests they have added.

While generating the contract repository record, mapped fields and their values are validated for data type and correctness. If validation errors are found, an email notification is sent to the contract fulfiller. The email also displays the list of fields that haven’t been copied into the final contract document and the link to the contract repository record. The fulfiller then opens the record using the link and corrects the values to resolve the validation errors.

-   **[Upload a manually signed contract document](../task/cncore-upload-doc-wsignature.md)**  
Upload the wet signed contract document that you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.
-   **[Modify signatories](../task/cncore-pause-signature.md)**  
Modify signatories while a signature workflow is in progress.
-   **[Resend signature request](../task/cncore-resend-sign-req.md)**  
Resend signature request functionality enables contract fulfillers to manually trigger signature request when needed.
-   **[Cancel the signature process](../task/cncore-cancel-a-manual-signature.md)**  
Cancel a wet signature process for contract documents that have been sent to signatories.

**Parent Topic:**[Using Contract Management Pro](cncore-use-cmpro.md)


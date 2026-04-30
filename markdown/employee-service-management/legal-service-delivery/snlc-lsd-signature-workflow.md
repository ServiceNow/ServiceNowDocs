---
title: Signature workflow for a legal request
description: Contract Management Pro for Legal Service Delivery supports electronic signature or wet \(manual\) signature for a contract request.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Use Contract Management Pro for Legal Service Delivery, Contract Management Pro for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Signature workflow for a legal request

Contract Management Pro for Legal Service Delivery supports electronic signature or wet \(manual\) signature for a contract request.

-   Electronic Signature: Enables signatories to sign the contract document electronically. For more information, see [Configure an e-signature provider for legal contracts](../task/snlc-integrate-esign.md).

    If you want to generate a certificate of completion, you must select the **Electronic Signature** as signature type in the contract request. For more information, see [Activate a system property to generate a certificate of completion](../../contract-mgmt-pro/task/cncore-config-system-prop-COC.md).

-   Wet Signature: Enables signatories to sign the contract document manually. You can then upload the signed document to a contract request. For more information, see [Upload a manually signed contract document](../task/snlc-upload-doc-wet-sign.md).

## Electronic signature workflow

-   Send the finalized document to the signatories for signing.
    -   The state and contract status updates to Awaiting Signature and the electronic signature flow is triggered as configured in [Configure an e-signature provider](../../contract-mgmt-pro/task/cncore-integrate-esign.md).
    -   An email notification that the contract document is available for signature is sent to the first signatory. The email contains a link to the contract document that the signatory can open and sign the document through the Docusign or Adobe Acrobat Sign electronic signature provider as configured in the electronic signature integration.

        The first signatory is the one whose Order value in the list of signatories is set the lowest in the contract template rule. For more information, see [Configure contract template rules](../../contract-mgmt-pro/task/cncore-config-template-rules.md).

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
-   The contract fulfiller uploads the signed document, selects the signatories who have shared the wet signed contract document and proceeds with the signature process by sending the document to the next signatories.

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

The contract document is resent for signature.

</td><td>

For contract request fulfilled by the contract user: A contract user can submit a change request. The contract fulfiller works on the change request and sends the updated document back to the contract requester. The updated contract document is sent for signature by the contract user.

 For contract request fulfilled by contract fulfiller: The contract fulfiller creates a document revision manually or by using regenerate option and resends the document for signature.

</td></tr></tbody>
</table>    If the system property **sn\_cm\_core.enable\_executed\_contract\_audit\_certificate** is set to true, the certificate of completion is generated and attached to the contract repository record.


## Wet signature workflow

-   Send the finalized document to the signatories for signing.
    -   The state and contract status are updated to Awaiting signature.
    -   An email notification is sent to the signatories and the contract documents are attached as PDFs in the email.

        The signatory with the lowest Order value in the list of signatories is the first signatory and is placed in the **To** field of the email. The other signatories are placed in the **CC** field.

-   Signatories accept or decline the document.

<table id="table_bhy_sqw_cfc"><thead><tr><th>

Signatories action

</th><th>

Workflow

</th></tr></thead><tbody><tr><td>

The signatory accepts the document.

</td><td>

-   The signatory prints the contract document,signs it, and then returns it to the signature requester.
-   If there are multiple signatories for the contract, they can collaborate and send the signed document with everyone’s signature or individually sign and send it back to the signature requester.


</td></tr><tr><td>

The document is declined by the signatory.

</td><td>

The signatory sends the document back to the requester for necessary correction. The signatories and the contract fulfiller can collaborate and finalize the contract document.

</td></tr><tr><td>

The contract fulfiller uploads the signed contract document.

</td><td>

-   On receiving the signed contract document, Contract fulfiller uploads the signed contract document in PDF format.
-   The contract document is added to the repository after it is uploaded.
 For self-served contracts, the state of the request updates to Closed complete and the contract status updates to Contract signed.

 For non-self-served contracts, the state of the request and the contract status updates to Contract signed. To close the contract request, select Close complete.

 For more information, see [Upload a manually signed contract document](../task/snlc-upload-doc-wet-sign.md).

</td></tr></tbody>
</table>
Access to a contract document is based on the following user roles and conditions:

-   A contract fulfiller can view and update contract documents
-   Only a contract administrator can delete contract documents.
-   Requesters can view only the contract documents for which they submitted the contract request.
-   Users added to the watch list can view only contract documents for contract requests they have added.

While generating the contract repository record, mapped fields and their values are validated for data type and correctness. If validation errors are found, an email notification is sent to the contract fulfiller. The email also displays the list of fields that haven’t been copied into the final contract document and the link to the contract repository record. The fulfiller then opens the record using the link and corrects the values to resolve the validation errors.

-   **[Upload a manually signed contract document](../task/snlc-upload-doc-wet-sign.md)**  
Upload the wet signed contract document that you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.
-   **[Cancel the wet signature process from the Employee Center](../task/snlc-tpc-cancel-wet-signature.md)**  
Cancel a wet signature process for a Non-disclosure agreement legal requests from the Employee Center.
-   **[Cancel the signature process from the Legal Counsel Center](../task/snlc-cancel-signature-lcc.md)**  
Cancel a signature process for a legal request from the Legal Counsel Center.

**Parent Topic:**[Use Contract Management Pro for Legal Service Delivery](snlc-use-sn-legal-cont-landing.md)

**Related topics**  


[Non-disclosure agreement legal requests](snlc-request-nda-1.md)

[Third-party contract review requests](snlc-request-third-party-contract-1.md)

[Internal review overview](../task/snlc-expert-review.md)

[Cancel a legal request](../task/snlc-cancel-request-tpc.md)

[View and download a signed contract document](../task/snlc-preview-contract.md)

[View contract requests](../task/snlc-view-contract-requests.md)


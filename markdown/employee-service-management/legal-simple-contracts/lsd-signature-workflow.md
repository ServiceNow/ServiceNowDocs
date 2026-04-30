---
title: Signature process for a legal request
description: You can require either an electronic or a wet \(manual\) signature for a legal request. The contract approval process differs depending on the signature type selected.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Non-disclosure agreement requests in Legal Simple Contracts, Requests, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Signature process for a legal request

You can require either an electronic or a wet \(manual\) signature for a legal request. The contract approval process differs depending on the signature type selected.

-   Electronic Signature: Enables users to sign contract documents electronically. For more information, see [Configure an e-signature provider for legal contracts](../task/integrate-legal-contracts-esign.md). Select the signature type as Electronic Signature if you also want to generate a certificate of completion. For more information, see [Activate a system property to generate a certificate of completion](../task/configure-system-property-COC.md).
-   Wet Signature: Enables the finalization of the contract manually rather then electronically. You can then upload the finalized document. For more information on uploading the document, see [Add a manually signed contract](../task/upload-contract-document-for-wet-signature.md).

When the contract document is finalized, it is sent it to the signatories to get it signed.

<table id="table_xst_hbd_hlb"><thead><tr><th>

For Electronic Signature

</th><th>

For Wet Signature

</th></tr></thead><tbody><tr><td>

-   The document status updates to Sent for Signature and electronic signature flow is triggered as in [legal integration](../task/integrate-legal-contracts-esign.md).

An email notification that the contract document is available for signature is sent to the first signatory. The email contains a link to the contract document that the signatory can open and sign the document through the Docusign or Adobe Acrobat Sign electronic signature provider as configured in the electronic signature legal integration.

The first signatory is the one whose Order value in the list of signatories is set the lowest in the contract template rule. For more information, see [Configure a rule for selecting a legal contract template](../task/configure-legal-contract-template-rules.md).

An email is sent to the next signatory in order after the first has signed the contract to request their signature.

-   Signatories can accept or decline the signature request. For more information, see [Sign or decline a legal contract electronically in Legal Simple Contracts](../task/sign-a-legal-contract-document.md).

</td><td>

-   The document status updates to Pending Signature.
-   An email notification is sent to the signatories with the contract document attached.
-   The signatories print the document, sign it, and return it to the legal requester.
-   The legal requester uploads the contract document in PDF format to the request. For more information, see [Add a manually signed contract](../task/upload-contract-document-for-wet-signature.md).

</td></tr></tbody>
</table>-   **[Sign or decline a legal contract electronically in Legal Simple Contracts](../task/sign-a-legal-contract-document.md)**  
As a signatory, you can review and sign or decline to sign a contract document.
-   **[Wet Signature workflow](lsd-wet-signature-workflows.md)**  
The wet signature workflow is triggered when a legal request with signature type as Wet Signature is sent to the signatories for signing.

**Parent Topic:**[Non-disclosure agreement requests in Legal Simple Contracts](legal-request-nda.md)


---
title: Sign or decline a legal contract electronically in Legal Simple Contracts
description: As a signatory, you can review and sign or decline to sign a contract document.
locale: en-US
release: xanadu
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Signature process for a legal request, Non-disclosure agreement requests in Legal Simple Contracts, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Sign or decline a legal contract electronically in Legal Simple Contracts

As a signatory, you can review and sign or decline to sign a contract document.

## Before you begin

Role required: none

## About this task

This task is applicable only for contracts that have the signature type set to **Electronic Signature**. If the contract requires a wet \(manual\) signature, the signatories receive an email with the contract attached, sign it, and return it to the legal requester. The legal requester then attaches the contract document in PDF format to the request.

## Procedure

1.  Select the link in the email notification.

2.  Review the contract document and sign it or decline to sign it.


## Result

The following table shows the results of signing the contract document and declining to sign it.

<table id="table_xst_hbd_hlb"><thead><tr><th>

Sign the contract document

</th><th>

Decline to sign the contract document

</th></tr></thead><tbody><tr><td>

-   If there are more signatories to sign the contract document, it’s sent to the next signatory in the order.

The status of current signatory in the request updates from Pending Signature to Signed. The status of the next signatory updates from Not Started to Pending Signature.

-   If the last signatory has signed the document, a legal contract record is created.

The document status updates to Contract Signed.

-   If the system property `sn_lg_contracts.enable_executed_contract_audit_certificate` is set to `true`, the certificate of completion is generated and appended to the finalized contract document.

</td><td>

-   The contract document is sent back to the requester. An email notification that the signer has declined to sign the document is sent to the requester.

The requester can review the document and request changes in the document and resend to signatories for signature.

The Signatory status in the request updates to Cancelled.

-   The document status in the request updates from Pending Signature to Contract Declined.

</td></tr></tbody>
</table>**Parent Topic:**[Signature process for a legal request](../concept/lsd-signature-workflow.md)


---
title: Upload a signed contract document
description: Upload a signed contract document that you have received from the signatories. You must upload a contract document for a wet signature workflow, an offline signature workflow when the contract was signed outside the system or if one of the signatories in the electronic signature workflow decides to do a wet signature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cncore-upload-doc-wsignature.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Signature workflow for a contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Upload a signed contract document

Upload a signed contract document that you have received from the signatories. You must upload a contract document for a wet signature workflow, an offline signature workflow when the contract was signed outside the system or if one of the signatories in the electronic signature workflow decides to do a wet signature.

## Before you begin

You can only upload a contract document in PDF format.

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

The state of the contract request and the contract status should be Awaiting signature.

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request.

3.  Select **Upload signed contract documents**.

4.  Attach the wet signed contract document received from the signatories.

    1.  In the Upload contracts step, select **Attach File**.

    2.  Select the contract document and select **Open**.

        \[Omitted image "cmpro-mixedsig-attachfile.png"\] Alt text: Attach wet signed contract document when one of the signatories decides to do a wet signature instead of electronic signature

        The attached document appears in the Upload contracts step.

    3.  Select **Next**.

    **Note:** For offline signatures, you don't need to select signatories in the upload modal.

5.  Select the signatories who have signed and share the contract document.

    1.  Select the check box next to each signatory who has signed the contract document.

    2.  Select **Next**.

        \[Omitted image "cmpro-mixedsig-selectsig.png"\] Alt text: Select signatories who have already signed the contract document.

6.  Review and upload the contract document.

    -   If all signatories have signed the contract document, select **Upload**.
    -   If some signatures are pending, select **Upload and send for signature** to send the document to the next signatory.
    \[Omitted image "cmpro-mixedsig-sendsig.png"\] Alt text: Send the contract document to signatories who still need to sign it.


## Result

After all signatories have signed, the contract document is uploaded to the contract request. A contract repository record is created and the signed contract document is attached to it.

For wet and mixed signatures, an email with the attached final contract document is sent to the signatories. For offline signatures, no email is sent.

For own paper contracts, the state of the request updates to **Closed complete** and the contract status updates to **Contract signed**.

For third-party contracts, the state of the request and the contract status updates to **Contract signed**. To close the contract request, select **Close complete**.

**Parent Topic:**[Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-signature-workflow.md)


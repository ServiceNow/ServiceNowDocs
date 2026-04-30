---
title: Upload a manually signed contract document
description: Upload the wet signed contract document that you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Signature workflow for a contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Upload a manually signed contract document

Upload the wet signed contract document that you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.

## About this task

The state of the contract request and the contract status should be Awaiting signature.

## Before you begin

You can only upload a contract document in PDF format.

Role required: sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request.

3.  Select **Upload signed contract documents**.

4.  Attach the wet signed contract document received from the signatories.

    1.  In the Upload contracts step, select **Attach File**.

    2.  Select the contract document and select **Open**.

        ![Attach wet signed contract document when one of the signatories decides to do a wet signature instead of electronic signature](../image/cmpro-mixedsig-attachfile.png "Attach wet signed contract document for upload")

        The contract document is attached.

    3.  Select **Next**.

5.  Select the signatories who have signed and share the contract document.

    1.  Select the check box for the signatories who have signed the contract document.

    2.  Select **Next**.

        ![Select signatories who have already signed the contract document.](../image/cmpro-mixedsig-selectsig.png "Select signatories")

6.  Review and upload the contract document.

    -   Upload the signed contract document - If all signatories have signed the contract document, select **Upload** to upload the document.
    -   Send the uploaded document to the next signatories - If some of the signatures are pending, select **Upload and send for signature** to upload and send the document to the next signatory in order.
    ![Send the contract document to signatories who still need to sign it.](../image/cmpro-mixedsig-sendsig.png "Send for signature")


## Result

When all the signatories have the contract document, it is uploaded to the contract request. A contract repository record is created and the signed contract document is attached to it.

An email with the attached final contract document is sent to the signatories.

For own paper contracts, the state of the request updated to **Closed complete** and the contract status updated to **Contract signed**.

For third-party contracts, the state of the request and the contract status updates to **Contract signed**. To close the contract request, select **Close complete**.

**Parent Topic:**[Signature workflow for a contract request](../concept/cncore-signature-workflow.md)


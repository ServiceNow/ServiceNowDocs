---
title: Upload a manually signed contract document
description: Upload the wet signed contract document you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Signature workflow for a request, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Upload a manually signed contract document

Upload the wet signed contract document you have received from the signatories. You need to upload a contract document for a wet signature workflow or if one of the signatories in the electronic workflow decides to do a wet signature.

## About this task

The state of the non-disclosure agreement should be Awaiting signature.

## Before you begin

You can only upload a contract document in PDF format.

Role required: sn\_lg\_cnt.contract\_fulfiller and sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal request** &gt; **Legal Counsel Center**.

2.  Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, navigate to **Legal Requests** or **Contract Requests**.

4.  If you have opened a contract request from the **Legal requests** listing, select the **Contract request** tab.

5.  Select **Upload signed contract documents**.

6.  Attach the wet signed contract document received from the signatories.

    1.  In the Upload contracts step, select **Attach File**.

    2.  Select the contract document and select **Open**.

        ![Attach wet signed contract document when one of the signatories decides to do a wet signature instead of electronic signature](../../contract-mgmt-pro/image/cmpro-mixedsig-attachfile.png "Attach wet signed contract document for upload")

        The contract document is attached.

    3.  Select **Next**.

7.  Select the signatories who have signed and share the contract document.

    1.  Select the check box for the signatories who have signed the contract document.

    2.  Select **Next**.

        ![Select signatories who have already signed the contract document.](../../contract-mgmt-pro/image/cmpro-mixedsig-selectsig.png "Select signatories")

8.  Review and upload the contract document.

    -   Upload the signed contract document - If all signatories have signed the contract document, select **Upload** to upload the document.
    -   Send the uploaded document to the next signatories - If some of the signatures are pending, select **Upload and send for signature** to upload and send the document to the pending signatories.
    ![Send the contract document to signatories who still need to sign it.](../../contract-mgmt-pro/image/cmpro-mixedsig-sendsig.png "Send for signature")


## Result

When all the signatories have signed the contract document, it is uploaded to the contract request. A contract repository record is created and the signed contract document is attached to it.

An email with the attached final contract document is sent to the signatories.

For Non-disclosure agreement legal requests, the state of the request updates to **Closed complete** and the contract status updates to **Contract signed**.

For Third-party contract review requests, the state of the request and the contract status updates to **Contract signed**. To close the contract request, select **Close complete**.

**Parent Topic:**[Signature workflow for a request](../concept/snlc-lsd-signature-workflow.md)


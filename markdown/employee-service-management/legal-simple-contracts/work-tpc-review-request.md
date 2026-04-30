---
title: Work on a TPC review request
description: As a member of the legal contracts support team, review and revise a third-party contract document. You can email the revised document to stakeholders to verify the revisions and then send the ready document for e-signature from within the legal request.
locale: en-US
release: xanadu
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Third-party contract review requests, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Work on a TPC review request

As a member of the legal contracts support team, review and revise a third-party contract document. You can email the revised document to stakeholders to verify the revisions and then send the ready document for e-signature from within the legal request.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

**Note:** During times when you're unavailable, you can [delegate your legal duties to other users](../../legal-request-management/concept/legal-services-delegation.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the list icon \(![List icon](../../human-resources/reference/images/checklist-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d256572e110">

Option

</th><th align="left" id="d256572e113">

Steps

</th></tr></thead><tbody><tr><td id="d256572e119">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d256572e148">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.

    **Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a legal request.

5.  In the **Document Revisions** tab, manage all revisions of the contract document.

<table id="choicetable_v1f_bjj_bwb"><thead><tr><th align="left" id="d256572e202">

Option

</th><th align="left" id="d256572e205">

Steps

</th></tr></thead><tbody><tr><td id="d256572e211">

**To review an existing document revision**

</td><td>

-   Select the name of the document to open the document revision record.
-   To preview the file, click the file name in the **Document** field.
-   To download the file, click the download icon \(![Download icon.](../../legal-request-management/image/download-icon.png)\).
-   To mark the document revision as ready, select **Ready**.


</td></tr><tr><td id="d256572e247">

**To create another document revision**

</td><td>

Create another document revision if more changes are required in the most recent version of the document.1.  Click **Create Revision**.

The Create Revision dialog box displays.

2.  In the **Create revision from** list, select the location of the document.
    -   **Computer**: Select a file from your local system. Click **Attach File** and upload a file.
    -   **Activity**: Select an attachment from the Activities stream. All files that are attached in the inbound emails are listed in the **Document** field.
    -   **Online**: Select a file stored in the [configured external storage system](../../legal-request-management/task/integrate-legal-ext-storage.md).
3.  Add more information about the document in the **Work notes** field. This information is added to the Activities stream along with the attachment.
4.  To make the document ready for review or sending for e-signature, select **Ready**.
5.  Click **Create**.
 The document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document revision is listed in the **Document Revisions** tab.

</td></tr></tbody>
</table>    **Note:** If you mark the current document revision as Ready, any previous document versions that were marked as Ready are cleared.

6.  [Send the document for ad-hoc approval](../../legal-request-management/task/initiate-approval-legal-request.md) when an approval is required from other stakeholders.

7.  Send an email to stakeholders to have the completed contract document reviewed and the changes confirmed.

    1.  Click **Compose Email**.

    2.  In the **New Email Draft** tab, add recipients' email addresses in the **To**, **CC**, and **BCC** fields as required.

        The **To** field is pre-populated with the third-party point of contact email entered in the request, and the **CC** field with the requester's email id.

    3.  Enter the subject of the email in **Subject**.

        The short description of the request is populated by default.

    4.  In the **Attachments** field, click the **+Add File** link to add the documents and then select the source of the file.

        If you’ve marked a contract document revision as Ready, it is attached to the email by default.

    5.  Enter the message in the email body.

    6.  Click **Send Email** to send the email immediately, or **Save as draft** to send it later.

8.  In the **Signatories** tab, add signatories to whom the contract will be sent for e-signature.

9.  When all stakeholders have agreed on a contract document revision, click **Prepare for Signature** to prepare and send the document to the signatories for e-signature.

    **Note:** When you select **Prepare for Signature**, the document opens in the configured e-signature system.

    -   For DocuSign, the document opens automatically in the e-signature portal without requiring a login.
    -   For Adobe Sign, you must log in to the e-signature portal to open the document.
    The document status updates from Internal Legal Review to Preparing for Signature.

10. Complete the document in the configured e-signature system and send it for signature.

    1.  Preview the document to ensure that the content is correct.

    2.  Add the required fields including the Signature field.

    3.  Click **Send**.

    An e-signature envelop is created and sent to all signatories. If the system receives a success notification from the electronic signature provider, the document status updates from Preparing for Signature to Pending Signature.


## What to do next

1.  Signatories can review and [sign or decline to sign the contract document](sign-a-legal-contract-document.md).
2.  You can check the document status in the request.
    -   If all signatories sign the contract document, the document status updates to Contract Signed. A [legal contracts repository record](review-contract-doc-repository.md) is created where the signed document is attached or linked. You can also access the legal contract repository record from the **Legal Contracts** tab.
    -   In the **Signatories** tab, the status of all signatories updates to Signed.
    -   If any signatory declines to sign the contract document, the document status updates to Contract Declined.If more changes are required in the contract document, update it and resend it to the signatories for signature.
3.  If the contract is signed by all parties, you can [close the request](../../legal-request-management/task/close-legal-request.md) by clicking **Close Complete.**

**Parent Topic:**[Third-party contract review requests](../concept/legal-request-third-party-contract.md)


---
title: Work on a third-party contract review request
description: As a member of the legal contracts support team, review and revise a third-party contract document. You can email the revised document to stakeholders to verify the revisions and then send the ready document for signature from within the legal request.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Third-party contract review requests, Use Contract Management Pro for Legal Service Delivery, Contract Management Pro for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Work on a third-party contract review request

As a member of the legal contracts support team, review and revise a third-party contract document. You can email the revised document to stakeholders to verify the revisions and then send the ready document for signature from within the legal request.

## Before you begin

Role required: sn\_lg\_cnt.contract\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

## Procedure

1.  Assign a legal request to yourself or to someone in your assignment group.

    For more information, see [Assign a legal request](../../legal-request-management/task/assign-legal-request-1.md)

2.  Start working on a legal request.

    1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

    2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

    3.  Select **Legal requests** option.

    4.  Select **Assign to me**.

    5.  Open the legal request from the list.

    6.  Select **Start work**

    The state of the legal request updates to Work in progress.

3.  In the **Lists** tab, navigate to **Legal Requests** or **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d626326e163">

Option

</th><th align="left" id="d626326e166">

Steps

</th></tr></thead><tbody><tr><td id="d626326e172">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a contract request to work on.


</td></tr><tr><td id="d626326e193">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a contract request to work on.


</td></tr></tbody>
</table>4.  If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.

    **Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a legal request.

5.  Reclassify the contract or supporting documents submitted for review.

    For more information, see [Reclassify contract documents in third-party contract review request as a legal fulfiller](snlc-tpc-reclassify-doc.md) and [Modify supporting documents in third-party contract review request as a legal fulfiller](snlc-tpc-mod-supporting-doc.md).

6.  If you have opened contract request from the **Legal requests** listing, select **Contract request** tab.

7.  Open an existing revision of a contract document.

    -   For internal storage:In the **Contract documents** tab, select the name of the document to open the document revision record.
    -   For external storage: In the **Contract documents** tab, click the link in the **URL** tab to view the document online.
8.  Review the contract documents.

9.  Revise the contract document if any changes are required and upload it by creating revision.

    1.  Select **Create revision**.

    2.  In the **Select contract type** field, select the contract type.

    3.  In the **Create Revision from** field, select the storage type to attach the revision.

        -   To select a file from your local system, select **Computer** and upload a file.

        -   To select an attachment from an email, select **Inbound Email**.

            Files attached to inbound emails are listed in the **Document** field.

        -   To select a file stored in the configured external storage system, select **External storage**.

            This option is displayed only if an external storage has been configured.

            \(Optional\) Add more information about the document in the **Notes** field.

            This information is added to the activity stream along with the attachment.

    4.  Select **Create**.

    The document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document revision is listed in the **Contract Documents** tab.

10. If an approval is required from other stakeholders, send the document for ad hoc approval.

    For more information, see [Initiate an ad hoc approval for a legal request or its attachment](../../legal-request-management/task/initiate-approval-legal-request.md).

11. Set up an email to stakeholders to have the completed contract document reviewed and the changes confirmed.

    1.  Select **Compose Email**.

    2.  In the Compose Email pop-up, select documents to be attached to the email.

    3.  Select **Add** to attach the document to the email.

        An email editor is displayed.

    4.  In the **New Email Draft** tab, add recipient email addresses in the **To**, **CC**, and **BCC** fields as appropriate.

        In the **To** field enter the email address of the recipient, The **CC** field will be set to requester's email address.

    5.  Enter the subject of the email in the **Subject** field.

        The short description of the request is populated by default.

    6.  In the **Attachments** field, select the **+Add File** link to add the documents and then select the source of the file.

    7.  Either enter your own message in the email body or copy and paste the content from an email response template into the email body.

        Using response templates, you can insert predefined content into the email body. Select the response template icon \(![Response template icon.](../../legal-request-management/image/response-template-email-icon.png)\) and find an appropriate response template based on the subject of your email. Copy and paste the template's content into the email body.

        **Note:** Only response templates configured for the email channel are available to use. For more information, see [Response templates configured for email channel](../../legal-request-management/task/create-lsd-response-template.md).

        For more information, see [Communicating via email](https://www.servicenow.com/docs/access?context=using-email&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    8.  Either send the email immediately or indicate that it should be sent later.

        -   To send the email immediately, select **Send email**.
        -   To indicate that the email should be sent later, select **Save as draft**.
12. In the **Signatories** tab, add signatories to whom the contract will be sent for signature by selecting **Add**.

<table id="choicetable_hm4_3vk_byb"><thead><tr><th align="left" id="d626326e596">

Option

</th><th align="left" id="d626326e599">

Steps

</th></tr></thead><tbody><tr><td id="d626326e605">

**Internal**

</td><td>

1.  In the **Internal Signer** field, enter the name of the signer. The fields **Authorized signatory name**, **Signatory**, and **Signatory email** are automatically populated.
2.  In the **Order** field, enter the order in which the email should be sent to the signer. The order value should be unique


</td></tr><tr><td id="d626326e638">

**External**

</td><td>

1.  In the **Authorized signatory name** field, enter the internal signer's name.
2.  In the **Signatory** field, enter the internal signer's title.
3.  In the **Signatory email** field, enter the internal signer's email address.
4.  In the **Order** field, enter the order in which the contract should be sent to signers for signature. The order value should be unique.


</td></tr></tbody>
</table>13. When all stakeholders have agreed on a contract document revision, select **Prepare for Signature** to prepare and send the document to the signatories for signature.

    1.  In the Reorder the document pop-up, drag and place the documents to define the order.

        The reorder option is displayed only when more than one documents are attached in the contract request.

    2.  Select **Prepare for Signature**.

        **Note:** When you select **Prepare for Signature**, the document opens in the configured e-signature system.

        -   For DocuSign, the document opens automatically in the e-signature portal without requiring a login.
        -   For Adobe Sign, you must log in to the e-signature portal to open the document.
    The Contract status and State updates to Preparing for Signature.

14. Complete the document in the configured e-signature system and send it for signature.

    1.  Preview the document to ensure that the content is correct.

        The contract documents submitted in the third-party contract review request will be combined into a single document.

    2.  Add the required fields including the Signature and Signature date field for all the signatories.

    3.  Select **Send**.

    An e-signature envelope is created and sent to all signatories. If the system receives a success notification from the electronic signature provider, the Contract status updates from Preparing for Signature to Awaiting Signature.

15. If you need to cancel the signature request before all signers have completed signing the document, select **Cancel Signatures**.

    The Contract status updates to Signature cancelled.


## What to do next

-   Signatories can review and sign or decline to sign the contract.

    For more information, see [Signature workflow for a legal request](../concept/snlc-lsd-signature-workflow.md).

-   Check the Contract status in the request.
    -   If all signatories sign the contract document, the Contract status updates to Contract Signed. In the **Signatories** tab, the status of all signatories updates to Signed. You can access the legal contract repository record from the **Legal Contracts Repository** tab.
    -   If any signatory declines to sign the contract document, the Contract status updates to Signing declined. In the **Signatories** tab, the status of all signatories updates to Declined. If more changes are required in the contract document, update it and resend it to the signatories for their signature.
    -   After all the signatories have signed the document, an email is sent to the legal signatories with the finalized contract document attached.
    -   If the certificate of completion is enabled, a certificate will be issued with the time stamp details about each signatory's action during an electronic signature.
-   If the contract is signed by all signatories, you can close the request by selecting **Close Complete**. For more information, see [Close a legal request](../../legal-request-management/task/close-legal-request.md)

**Parent Topic:**[Third-party contract review requests](../concept/snlc-request-third-party-contract-1.md)


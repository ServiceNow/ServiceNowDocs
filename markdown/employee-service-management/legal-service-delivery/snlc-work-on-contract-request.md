---
title: Work on NDA legal requests
description: As a member of the legal contracts support team, work on the legal request. Upload the revised document to the request and send the document to the requester from within the request.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Non-disclosure agreement legal requests, Use Contract Management Pro for Legal Service Delivery, Contract Management Pro for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Work on NDA legal requests

As a member of the legal contracts support team, work on the legal request. Upload the revised document to the request and send the document to the requester from within the request.

## Before you begin

The practice area lead or group manager should have assigned you the request. If not, you can open the request to [assign it to yourself or someone in the group](../../legal-request-management/task/assign-legal-request-1.md).

Role required: sn\_lg\_cnt.contract\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

## Procedure

1.  Assign a legal request to yourself or to someone in your assignment group.

    For more information, see [Assign a legal request](../../legal-request-management/task/assign-legal-request-1.md)

2.  Start working on a legal request.

    1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

    2.  Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

    3.  Select **Legal requests** option.

    4.  Select **Assign to me**.

    5.  Open the legal request from the list.

    6.  Select **Start work**

    The state of the legal request updates to Work in progress.

3.  In the **Lists** tab, navigate to **Legal Requests** or **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d488230e172">

Option

</th><th align="left" id="d488230e175">

Steps

</th></tr></thead><tbody><tr><td id="d488230e181">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a contract request to work on.


</td></tr><tr><td id="d488230e202">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a contract request to work on.


</td></tr></tbody>
</table>4.  If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.

    **Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a legal request.

5.  In the legal request, update the **Watch list**, **Collaborators**, and **Requested for**.

    Any changes done to the **Watch list**, **Collaborators**, and **Requested for** are synced to the contract request.

6.  Update a company name by selecting its name in the **Company** field.

    If the company name is not listed in the **Company** field, select the **Add new company name** check box and then enter the company name in the **New company legal name** field.

7.  If you have opened a contract request from the **Legal requests** listing, select the **Contract Requests** tab.

8.  Initiate an ad hoc approval for the contract document revision when an approval is required from other stakeholders.

    For more information, see [Initiate an ad hoc approval for a contract document revision](snlc-initiate-approval-cr.md).

9.  Add internal or external signatories to the contract request by accessing the **Signatories** tab and selecting **Add**.

    **Note:** You can add signatories in NDA legal requests only when the contract is generated from a template configured with signature blocks

<table id="choicetable_v3x_kwb_5bc"><thead><tr><th align="left" id="d488230e342">

Option

</th><th align="left" id="d488230e345">

Steps

</th></tr></thead><tbody><tr><td id="d488230e351">

**Internal**

</td><td>

1.  In the **Internal Signer** field, enter the name of the signer.

The fields **Authorized signatory name**, **Signatory**, and **Signatory email** are automatically populated.

2.  In the **Order** field, enter the order in which the contract should be sent to the signer. The order value should be unique
3.  Select **Add**.


</td></tr><tr><td id="d488230e392">

**External**

</td><td>

1.  In the **Authorized signatory name** field, enter the external signer's name.
2.  In the **Signatory** field, enter the external signer's title.
3.  In the **Signatory email** field, enter the external signer's email address.
4.  In the **Order** field, enter the order in which the contract should be sent to signers for an e-signature. The order value should be unique.
5.  Select **Add**.


</td></tr></tbody>
</table>10. Remove the signatories from the contract request by accessing the **Signatories** tab, selecting the signatory, and selecting **Remove**.

    **Note:** You can remove signatories in NDA legal requests only when the contract is generated from a template configured with signature blocks

11. In the **Signatories** tab, select **Sync signatories** to update the contract document with the latest signatory details.

    For more information, see [Updating and synchronizing signatories](snlc-update-sync-signatories.md)

    **Note:** This option is not available on Contract Management Pro starting with version 1.2.1.

12. In the Activity section, review the changes requested by the requester and make the necessary changes in the contract document.

13. Upload the revised contract document.

    1.  In the **Contract documents** tab, select **Create Revision**.

    2.  In the Create revision dialog box, select the source of the updated contract and upload a new document revision.

<table id="table_xh1_3q5_12c"><thead><tr><th>

Contract source

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Computer

</td><td>

In the **Attachment** field, select **Attach File** and upload the updated contract.

</td></tr><tr><td>

Activity stream

</td><td>

In the **Document** field, select the document in the activity stream.The activity stream includes documents attached while requesting changes for a contract or documents received through email.

</td></tr><tr><td>

External storage

</td><td>

If external storage is configured, in the **Document** field, select the document.

</td></tr></tbody>
</table>    3.  Add work notes to provide any information on the attached document.

    4.  Select **Create**.

    The attached document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document is listed in the **Contract document** tab.

14. When a legal request changes, create a new version of the contract document with updated metadata and signatories and retain the changes in the previous version by selecting **Sync document**.

    For more information, see [Synchronize a non-disclosure agreement document after modifying a self-served contract request \(Contract Management Pro 1.2.1\)](snlc-sync-doc.md).

    **Note:** This option is available on Contract Management Pro starting version 1.2.1

15. For any changes in legal request, select **Regenerate** option to create a new version of the contract document with updated metadata and signatories, and discard the changes in the previous version.

    For more information, see [Regenerate contract document after modifying request](snlcregen-contract-doc.md).

16. Set up an email to stakeholders to request to have the completed contract document reviewed and the changes confirmed.

    1.  Select **Compose Email**.

    2.  In the **New Email Draft** tab, add recipients' email addresses in the **To**, **CC**, and **BCC** fields as appropriate.

        The **CC** field is automatically populated with the requester's email address.

    3.  Enter the subject of the email in the **Subject** field.

        The short description of the request is populated by default.

    4.  In the **Attachments** field, select **+Add File**.

    5.  Select whether the file source is your computer or an attachment to a record and select the file to be attached.

        If you’ve marked a contract document revision as Ready, it’s attached to the email by default.

    6.  Either enter your own message in the email body or copy and paste the content from an email response template into the email body.

        Using response templates, you can insert predefined content into the email body. Select the response template icon \(![Response template icon.](../../legal-request-management/image/response-template-email-icon.png)\) and find an appropriate response template based on the subject of your email. Copy and paste the template's content into the email body.

        **Note:** Only response templates configured for the email channel are available to use. For more information, see [Response templates configured for email channel](../../legal-request-management/task/create-lsd-response-template.md).

        For more information, see [Communicating via email](https://www.servicenow.com/docs/access?context=using-email&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    7.  Either send the email immediately or indicate that it should be sent later.

        -   To send the email immediately, select **Send email**.
        -   To indicate that the email should be sent later, select **Save as draft**.

            If you choose to save the email as a draft, you can modify it later. If a newer document revision has been posted, you have to substitute that revision for the document you attached.


**Parent Topic:**[Non-disclosure agreement legal requests](../concept/snlc-request-nda-1.md)


---
title: Work on amendment request
description: Review and work on an amendment request for an existing contract.
locale: en-US
release: yokohama
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-10-19"
reading_time_minutes: 6
breadcrumb: [Contract amendments, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Work on amendment request

Review and work on an amendment request for an existing contract.

## Before you begin

The practice area lead or group manager should have assigned you the request. If not, you can open the request to [assign it to yourself or someone in the group](../../legal-request-management/task/assign-legal-request-1.md).

Role required: sn\_lg\_cnt.contract\_fulfiller

## About this task

A sample workflow while working on an amendment request would be:

1.  Assign the amendment contract request.
2.  Link a parent contract, if it’s already not linked or you want to change the linked contract.
3.  Modify legal request.
4.  Review the details of the amendment requested.
5.  Update the contract details and contract document according to the amendment request.
6.  Upload revised contract document using **Create revision** option.
7.  Finalizes the contract amendment using the review, approval, and signature workflow.

Identify the legal and contract requests created for amendment using the following indicators:

-   In the legal request, the subject is in the *Amendment request of &lt;contract\_type&gt; for &lt;company\_name&gt;* format.
-   In the contract request, the subject is in the *&lt;type of paper&gt; - &lt;contract type&gt; - amendment request - &lt;CMR-number&gt;* format and the **Request type** is set to Amendment

## Procedure

1.  Assign to yourself and start working on an amendment request.

    1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

    2.  Select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

    3.  In the **Legal Requests**, select **Unassigned**.

    4.  In the list of unassigned requests, open a request by selecting the request number.

    5.  Select **Assign to me**.

    6.  Select **Start work**

    The state of the legal request updates to Work in progress.

2.  Link parent contract \(Example: CNTR0010003\) when prompted with a message or you want to change the already linked parent contract.

    ![Link parent contract](../image/snlc-amend-link-cntr.png)

    -   If you didn’t select a contract while submitting the amendment request, you’re prompted to link a parent contract record.
    -   When a contract is linked, its corresponding contract request \(Example: CMR0001186\) will automatically be linked through a parent-child hierarchy. You can’t manually unlink the contract request as it depends on the contract selection.
    1.  Navigate to the Legal request details section.

    2.  In the Parent contract record field, select the Search for Record icon \(![Search for Record icon](../../contract-mgmt-pro/image/lsd-cont-rec-search.png)\).

        Only active contracts that don’t have any ongoing amendment requests are listed.

    3.  Select the contract from the list.

3.  Modify legal request.

<table id="choicetable_rxb_zfw_fhc"><thead><tr><th align="left" id="d686388e246">

Options

</th><th align="left" id="d686388e249">

Steps

</th></tr></thead><tbody><tr><td id="d686388e255">

**Add collaborators**

</td><td>

If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.**Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

The collaborators are notified via email that they’ve been added as collaborators to a legal request.

</td></tr><tr><td id="d686388e274">

**Update the users in watch list and requested for**

</td><td>

Update the **Watch list** and **Requested for**.Any changes done to the **Watch list** and **Requested for** are synced to the contract request.

</td></tr></tbody>
</table>4.  If you have opened a contract request from the **Legal requests** listing, select the **Contract Requests** tab and open the contract request.

5.  In the contract request, review the Description field for the amendments requested.![Review the description field for the amendments requested](../image/lsd-amend-description.png)

6.  Update the contract request.

    1.  Change the values of fields that must be amended.

        For example, if there was a requirement to change the end date, change the date in the **Contract end date** field.

7.  Download the contract document.

    1.  Navigate to **Contract documents** tab.

    2.  Select **Preview document**.

    3.  Select the contract type.

    4.  Select **Preview**.

        The document opens in a new tab.

    5.  Select the Download icon \(![Download icon](../../legal-request-management/image/download-icon.png)\)

        The document is downloaded into your system.

    6.  Edit the document for the amendments requested.

        While authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.

8.  Upload the revised contract document.

    1.  In the **Contract documents** tab, select **Create Revision**.

    2.  In the Create revision dialog box, select the source of the updated contract and upload a new document revision.

    3.  Add work notes to provide any information on the attached document.

    4.  Select **Create**.

    The attached document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document is listed in the **Contract document** tab.

9.  Add or remove signatories to the contract request.

    |Options|Steps|
    |-------|-----|
    |**Add signatory**|Add signatories to the contract request by accessing the **Signatories** tab and selecting **Add**.|
    |**Remove signatory**|Remove the signatories from the contract request by accessing the Signatories tab, selecting the signatory, and selecting **Remove**.|

    **Note:** You can add or remove signatories in own-paper based amendment legal requests only when the contract is generated from a template configured with signature blocks.

10. For any metadata or signatory changes, synchronize the document by selecting **Sync document** in the **Contracts documents** tab.

    A new contract document revision is created with the update metadata and signatories. The changes made in the previous revision are retained.

11. Finalize the contract amendment using the review, approval, and signature workflows.

    |Options|Steps|
    |-------|-----|
    |**Ad hoc approval**|[Initiate an ad hoc approval for a contract document revision](snlc-initiate-approval-cr.md)|
    |**Internal review**|[Request an internal review](snlc-add-review-task.md).|
    |**Email communication**|Set up an email to stakeholders to request to have the completed contract document reviewed and the changes confirmed using **Compose Email** option.|
    |**Signature workflow**| |

12. Send the contract amendment document for signature.

    For more information, see [Signature workflow for a request](../concept/snlc-lsd-signature-workflow.md)


## Result

-   When all the signatories have signed the existing Contract Repository record associated with the request is updated with the changes from the amendment.
-   The state of the amendment request updates to **Contract signed**.
-   In the Related contract request tab, you can view the parent contract child hierarchy is established between the parent contract and the amendment request. You can’t unlink the parent and the child contract.
-   The following tabs are available within the contract repository record to view the amendment details:
    -   Details: View the changes done to the contract request for the amendment request. Example: If the end date is changed, it is reflected in the details section. Example: If the end date is changes, it will be reflected in the details section.
    -   Contract Documents: Provides access to all signed documents related to the contract, including those generated or updated as part of amendment processes. The amendment contract documents have **Amend&lt;version&gt;** \(Example: CNTR0010003 - Non Disclosure Agreement - Amend001\) appended to the name. The &lt;version&gt; is automatically incremented for each signed amendment, but not for intermediate amendment versions.
    -   Contract Requests: Displays all contract and amendment requests associated with the contract repository record.
    -   Amendment Field Changes: Shows a detailed log of all field changes made through amendments. Example: Change in the contract end date is available in this tab. Example: Change in the contract end date is available in this tab.

        ![View the field changes due to amendment](../image/snlc-amend-field-changes.png)

    -   Attachment pane: View the certificate of completion for the contract and amendment requests if electronic signature was selected.

**Parent Topic:**[Contract amendments](../concept/snlc-amend-req-landing.md)


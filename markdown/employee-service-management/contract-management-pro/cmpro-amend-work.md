---
title: Work on amendment request
description: Review and work on an amendment request for an existing contract.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-10-19"
reading_time_minutes: 5
breadcrumb: [Contract amendments, Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Work on amendment request

Review and work on an amendment request for an existing contract.

## Before you begin

The practice area lead or group manager should have assigned you the request. If not, you can open the request to [assign it to yourself or someone in the group](../../legal-request-management/task/assign-legal-request-1.md).

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

A sample workflow while working on an amendment request would be:

1.  The request is assigned.
2.  Link a parent contract if you have the information.
3.  Start working on the amendment request.
4.  Link a parent contract if not already done.
5.  Review the details of the amendment requested.
6.  Update the contract details and contract document according to the amendment request.
7.  Upload revised contract document using **Create revision** option.
8.  Finalizes the contract amendment using the review, approval, and signature workflow.

## Procedure

1.  Navigate to your workspace.

2.  On the **Lists** tab, open a contract request by selecting an option under **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d84208e112">

Option

</th><th align="left" id="d84208e115">

Steps

</th></tr></thead><tbody><tr><td id="d84208e121">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state and the Contract status of the contract request is Work in progress.

</td></tr><tr><td id="d84208e150">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>3.  Assign to yourself and start working on an amendment request.

    1.  Select **Assign to me**.

    2.  Select **Start work**

    The state of the contract request updates to Work in progress.

4.  Link parent contract.

    1.  Navigate to the Contract request details section.

    2.  In the field, **Parent contract record**, select the Search for Record icon \(![Search for Record icon](../image/lsd-cont-rec-search.png)\).

    3.  Select the contract from the Parent contract pop-up window.

        -   Only active contracts and contracts with no pending amendment requests are listed.
        -   When a contract is linked, its corresponding contract request \(Example: CMR0001186\) is automatically link through a parent-child hierarchy. You can’t manually unlink the contract request as it depends on the contract selection.
5.  Update the field values according to the amendment request.

    To automatically copy values from the parent contract request to the amendment request, you must configure the fields in the ContractManagementExt extension point. The values are copied from the parent contract selected during submitting the amendment request.

    For more information, see [Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md).

6.  In the Request details section, review the Description field for the amendments requested. ![Review the description field for the amendments requested](../image/cmpro-amend-view-description.png)

7.  Update the contract request.

    1.  Change the values of fields that need to be amended.

        For example, if there was a requirement to change the end date, change the date in the **Contract end date** field.

8.  Download the contract document.

    1.  Navigate to **Contract documents** tab.

    2.  Select **Preview document**.

    3.  Select the contract type.

    4.  Select **Preview**.

        The document opens in a new tab.

    5.  Select the Download icon \(![Download icon](../../legal-request-management/image/download-icon.png)\)

        The document is downloaded into your system.

    6.  Edit the document for the amendments requested.

        While authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.

9.  Upload the revised contract document.

    1.  In the **Contract documents** tab, select **Create Revision**.

    2.  In the Create revision dialog box, select the source of the updated contract and upload a new document revision.

    3.  Add work notes to provide any information on the attached document.

    4.  Select **Create**.

    The attached document is added to the request. The revision number of the latest document is one higher than the previous document revision number. The document is listed in the **Contract document** tab.

10. Add or remove signatories to the contract request.

    |Options|Steps|
    |-------|-----|
    |**Add signatory**|Add signatories to the contract request by accessing the **Signatories** tab and selecting **Add**.|
    |**Remove signatory**|Remove the signatories from the contract request by accessing the Signatories tab, selecting the signatory, and selecting **Remove**.|

    **Note:** You can add or remove signatories in own-paper based amendment legal requests only when the contract is generated from a template configured with signature blocks.

11. For any metadata or signatory changes, synchronize the document by selecting **Sync document** in the **Contracts documents** tab.

    A new contract document revision is created with the update metadata and signatories. The changes made in the previous revision are retained.

12. Finalize the contract amendment using the review, approval, and signature workflows.

    |Options|Steps|
    |-------|-----|
    |**Ad hoc approval**|[Initiate an ad hoc approval for a contract document revision](../../lsd-sn-legal-contracts/task/snlc-initiate-approval-cr.md)|
    |**Internal review**|[Request an internal review](../../lsd-sn-legal-contracts/task/snlc-add-review-task.md).|
    |**Email communication**|Set up an email to stakeholders to request to have the completed contract document reviewed and the changes confirmed using **Compose Email** option.|
    |**Signature workflow**| |

13. Send the contract amendment document for signature.

    For more information, see [Signature workflow for a request](../../lsd-sn-legal-contracts/concept/snlc-lsd-signature-workflow.md)


## Result

-   When all the signatories have signed the existing Contract Repository record associated with the request is updated with the changes from the amendment.
-   The state of the amendment request updates to **Contract signed**.
-   In the Related contract request tab, you can view the parent contract child hierarchy is established between the parent contract and the amendment request. You can’t unlink the parent and the child contract.
-   The following tabs are available within the contract repository record to view the amendment details:
    -   Details: View the changes done to the contract request for the amendment request. Example: If the end date is changed, it is reflected in the details section. \(Example: If the end date is changed, it will be reflected in the details section.\)
    -   Contract Documents: Provides access to all signed documents related to the contract, including those generated or updated as part of amendment processes. The amendment contract documents have **Amend&lt;version&gt;** \(Example: CNTR0010003 - Non Disclosure Agreement - Amend001\) appended to the name. The &lt;version&gt; is automatically incremented for each signed amendment, but not for intermediate amendment versions.
    -   Contract Requests: Displays all contract and amendment requests associated with the contract repository record.
    -   Amendment Field Changes: Shows a detailed log of all field changes made through amendments. Example: Change in the contract end date is available in this tab.

        ![View the field changes due to amendment](../../lsd-sn-legal-contracts/image/snlc-amend-field-changes.png)

    -   Attachment pane: View the certificate of completion for the contract and amendment requests if electronic signature was selected.

**Parent Topic:**[Contract amendments](cmpro-amend-landing.md)


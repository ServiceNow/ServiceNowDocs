---
title: Work on a renewal request
description: Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-service-delivery/snlc-renewal-work.html
release: brazil
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 4
keywords: [Renewal request, Work on renewal, Renewal workflow, Contract fulfiller]
breadcrumb: [Contract renewals, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Work on a renewal request

Review and work on a renewal request for an existing contract, from assignment through review, approval, and signature to the executed renewed contract.

## Before you begin

The assigned contract fulfiller, group manager, or collaborator has edit access. The watchlist, requested for, opened by, and other fulfillers in the assignment group have view access. A contract fulfiller can assign the renewal request to themselves, and a group manager can assign it to any member of the assignment group.

Role required: sn\_lg\_cnt.contract\_fulfiller

## About this task

A sample workflow while working on a renewal request would be:

1.  Assign the renewal contract request.
2.  Link the previous contract, if not already linked.
3.  Review and update the contract document.
4.  Finalize the renewal using the review, approval, and signature workflow.

Identify the legal and contract requests created for renewal using the following indicators:

-   In the legal request, the subject is in the *Renewal request of &lt;contract\_type&gt; for &lt;company\_name&gt;* format.
-   In the contract request, the **Request type** is set to **Renewal**.

## Procedure

1.  Assign to yourself and start working on the renewal request.

    1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

    2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).

    3.  In **Legal Requests**, select **Unassigned**.

    4.  Open a request by selecting the request number.

    5.  Select **Assign to me**.

    6.  Select **Start work**.

    The state of the legal request updates to Work in progress.

2.  Link the previous contract when prompted or to change the already linked contract.

    The previous contract is optional in Draft state and mandatory in Work in Progress. Only active or expired contracts with an end date and no ongoing renewal requests are listed.

    1.  Navigate to the Legal request details section.

    2.  In the **Previous contract** field, select the Search for Record icon \(\[Omitted image "lsd-cont-rec-search.png"\] Alt text: Search for Record icon\).

    3.  Select the contract from the list.

3.  Modify the legal request.

<table id="choicetable_renewal-modify"><thead><tr><th align="left" id="d656936e226">

Options

</th><th align="left" id="d656936e229">

Steps

</th></tr></thead><tbody><tr><td id="d656936e235">

**Add collaborators**

</td><td>

Add collaborators in the **Collaborators** field to get help from other fulfillers. Collaborators are notified by email.**Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

</td></tr><tr><td id="d656936e252">

**Update watch list and requested for**

</td><td>

Update the **Watch list** and **Requested for**. Changes are synced to the contract request.

</td></tr></tbody>
</table>4.  If you opened a contract request from the **Legal requests** listing, select the **Contract Requests** tab and open the contract request.

5.  Download the contract document.

    1.  Navigate to **Contract Documents** or **Preview** tab.

    2.  Download the document by selecting the document in **Contract Documents** tab or selecting **Download document** in the Preview tab.

    3.  Edit the document for the renewal.

        While authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.

6.  Upload the revised contract document.

    1.  In the **Contract documents** tab, select **Create Revision**.

    2.  In the Create revision dialog box, select the source of the updated contract and upload a new document revision.

    3.  Add work notes to provide any information on the attached document.

    4.  Select **Create**.

    The attached document is added to the request. The revision number is one higher than the previous revision. The document is listed in the **Contract documents** tab.

7.  Add or remove signatories to the contract request.

    |Options|Steps|
    |-------|-----|
    |**Add signatory**|Add signatories by accessing the **Signatories** tab and selecting **Add**.|
    |**Remove signatory**|Remove signatories by accessing the **Signatories** tab, selecting the signatory, and selecting **Remove**.|

    **Note:** You can add or remove signatories in own-paper based renewal requests only when the contract is generated from a template configured with signature blocks.

8.  For any metadata or signatory changes, synchronize the document by selecting **Sync document** in the **Contract documents** tab.

    A new contract document revision is created with the updated metadata and signatories. The changes made in the previous revision are retained.

9.  Finalize the renewal request using the review, approval, and signature workflows.

    |Options|Steps|
    |-------|-----|
    |**Ad hoc approval**|[Initiate an ad hoc approval for a contract document revision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/legal-service-delivery/snlc-initiate-approval-cr.md)|
    |**Internal review**|[Request an internal review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/legal-service-delivery/snlc-add-review-task.md).|
    |**Email communication**|Set up an email to stakeholders to have the completed contract document reviewed and the changes confirmed using the **Compose Email** option.|
    |**Signature workflow**| |

10. Send the contract document for signature.

    For more information, see [Signature workflow for a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/legal-service-delivery/snlc-lsd-signature-workflow.md).


## Result

When all signatures are complete, the request moves to Contract Signed and then Closed complete.

-   A new contract record is created in the contract repository.
-   The executed renewed contract is available on the Contract repository tab, with the signed document accessible as a preview for internal storage or as a hyperlink for external storage.
-   All configured field values are copied to the new contract.
-   The renewal history is available in **Contract History** tab.
-   When both amendment and renewal requests are active on the same contract, review the following to avoid conflicts:

    -   Contract dates to prevent overlapping effective periods between the amended contract and the renewed contract
    -   Terms and pricing changes in both requests
    -   Effective dates and expiration dates
    You must manually reconcile any conflicts between the amended original contract and the renewed contract.


**Parent Topic:**[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/legal-service-delivery/snlc-renewal-landing.md)


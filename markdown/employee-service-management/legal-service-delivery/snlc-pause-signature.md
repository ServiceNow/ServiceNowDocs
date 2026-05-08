---
title: Modify signatories
description: Modify signatories while a signature workflow is in progress.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Signature workflow for a request, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Modify signatories

Modify signatories while a signature workflow is in progress.

## Before you begin

-   Configure the system property **maximum\_signature\_pause\_duration** to define the time duration for which the signature workflow is be paused after you select to modify signatories option. The minimum value that can be set is 8 hours and the maximum is 24 hours. For more information, see [Configure signature pause duration when modifying signatories](../../contract-mgmt-pro/task/cncore-pause-sig-property.md).
-   Modify signatories option is only available for wet signature workflow and Electronic signature workflow with Docusign electronic signature provider integration.

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

Use the **Modify signatories** option to pause the signature process when you want to add, modify, reorder or remove a signatory. If the signature process is not resumed within the configured time duration \(as defined by the system property **maximum\_signature\_pause\_duration**\), any changes made to the signatories are automatically reverted, and the signature process resumes from its previous state.

-   You can select the option to modify signatories only when the contract request is in Awaiting signature state.
-   You can only remove, modify, or reorder signatories who have not yet signed the contract document.
-   When the signature process is paused, signatories with pending signature task will not be able to access the contract document from the already received signature request email.
-   For signature block based contract requests, you can perform add modify, remove and reorder actions.
-   For participant based contract requests, you can only perform modify and reorder actions.

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request which is in Awaiting signature state.

3.  Select **Modify signatories**.

    -   The Contract Status updates to Signature Paused.
    -   The activity stream records the modify signatories action.
4.  Select **Modify** on the confirmation screen.

5.  Navigate to **Signatories** tab.

6.  Modify signatories.

<table id="choicetable_pq3_jkd_wfc"><thead><tr><th align="left" id="d537290e160">

Action

</th><th align="left" id="d537290e163">

Steps

</th></tr></thead><tbody><tr><td id="d537290e169">

**Add signatories**

</td><td>

1.  Select **Add**.
2.  Select **Internal** or **External**.
3.  Fill in the details.
4.  Select **Add**.
 **Note:** The **Add** option is not available for self-served contract requests using contract templates with participant-based signatories.

</td></tr><tr><td id="d537290e211">

**Edit signatory**

</td><td>

1.  Select a signatory from the list by clicking on the signatory order.

Signatory details page is displayed.

2.  Modify the fields.
3.  Select **Save**.


</td></tr><tr><td id="d537290e237">

**Reorder signatories**

</td><td>

1.  Select **Reorder**.

Reorder pop-up is displayed.

2.  For the signatory you want to reorder, select and hold the Reorder icon \(![Reorder icon](../../contract-mgmt-pro/image/cmpro-reorder-icon.png)\).
3.  Drag the signatory to the required order.
4.  Select **Reorder**.


</td></tr><tr><td id="d537290e275">

**Remove signatories**

</td><td>

1.  Select the signatory by checking the corresponding checkbox.
2.  Select **Remove**.
 **Note:** The **Remove** option is not available for self-served contract requests using contract templates with participant-based signatories.

</td></tr></tbody>
</table>
## Result

The signature process is paused and signatories modified.

## What to do next

Resume the signature process after you have modified the signatories. For more information, see [Resume signature process](snlc-resume-signature.md).

-   **[Resume signature process](snlc-resume-signature.md)**  
Resume the paused signature process with the modified signatories.

**Parent Topic:**[Signature workflow for a request](../concept/snlc-lsd-signature-workflow.md)


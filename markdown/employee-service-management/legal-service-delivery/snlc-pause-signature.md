---
title: Modify signatories
description: Pause an active signature workflow to add, modify, reorder, or remove signatories on a contract request that is in Awaiting signature state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-service-delivery/snlc-pause-signature.html
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Signature workflow for a request, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Modify signatories

Pause an active signature workflow to add, modify, reorder, or remove signatories on a contract request that is in Awaiting signature state.

## Before you begin

-   Configure the system property **maximum\_signature\_pause\_duration** to define the time duration for which the signature workflow is paused after you select to modify signatories option. The minimum value that can be set is 8 hours and the maximum is 24 hours. For more information, see [Configure signature pause duration when modifying signatories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-pause-sig-property.md).
-   The Modify signatories option is available only for wet signature workflows and electronic signature workflows with Docusign electronic signature provider integration.

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

Use the **Modify signatories** option to pause the signature process to add, modify, reorder, or remove a signatory. If the signature process is not resumed within the configured time duration \(as defined by the system property **maximum\_signature\_pause\_duration**\), any changes made to the signatories are automatically reverted, and the signature process resumes from its previous state.

-   You can select the option to modify signatories only when the contract request is in Awaiting signature state.
-   You can only remove, modify, or reorder signatories who have not yet signed the contract document.
-   When the signature process is paused, signatories with a pending signature task cannot access the contract document from the signature request email they already received.
-   For signature block based contract requests, you can perform add modify, remove and reorder actions.
-   For participant based contract requests, you can only perform modify and reorder actions.

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request which is in Awaiting signature state.

3.  Select **Modify signatories**.

    -   The Contract Status updates to Signature Paused.
    -   The activity stream records the modify signatories action.
4.  Select **Modify** on the confirmation screen.

5.  Select the **Signatories** tab.

6.  Modify signatories.

<table id="choicetable_pq3_jkd_wfc"><thead><tr><th align="left" id="d550443e162">

Action

</th><th align="left" id="d550443e165">

Steps

</th></tr></thead><tbody><tr><td id="d550443e171">

**Add signatories**

</td><td>

1.  Select **Add**.
2.  Select **Internal** or **External**.
3.  Fill in the details.
4.  Select **Add**.
 **Note:** The **Add** option is not available for self-served contract requests using contract templates with participant-based signatories.

</td></tr><tr><td id="d550443e213">

**Edit signatory**

</td><td>

1.  Select a signatory from the list by selecting the signatory order value.

The Signatory details page opens.

2.  Modify the fields.
3.  Select **Save**.


</td></tr><tr><td id="d550443e239">

**Reorder signatories**

</td><td>

1.  In the **Signing Order** column, select the order value for a signatory.
2.  Enter the signing order number.

To group two or more signatories to sign at the same time, assign them the same signing order.

3.  Select outside the field, or select **Save**.


</td></tr><tr><td id="d550443e268">

**Remove signatories**

</td><td>

1.  Select the check box for the signatory.
2.  Select **Remove**.
 **Note:** The **Remove** option is not available for self-served contract requests using contract templates with participant-based signatories.

</td></tr></tbody>
</table>
## Result

The signature process pauses and the signatories are updated.

## What to do next

Resume the signature process after you have modified the signatories. For more information, see [Resume signature process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/snlc-resume-signature.md).

-   **[Resume signature process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/snlc-resume-signature.md)**  
Resume the paused signature process with the modified signatories.

**Parent Topic:**[Signature workflow for a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/snlc-lsd-signature-workflow.md)


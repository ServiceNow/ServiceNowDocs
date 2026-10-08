---
title: Submit a standalone renewal request
description: Submit a renewal request from Employee Center to renew an existing contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-sa-renewal.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 4
keywords: [standalone renewal request, record producer, contract renewal]
breadcrumb: [Standalone contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Submit a standalone renewal request

Submit a renewal request from Employee Center to renew an existing contract.

## Before you begin

Role required: sn\_cm\_core.contract\_user or sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to the contract request form.

<table><thead><tr><th align="left" id="d95732e75">

Entry point

</th><th align="left" id="d95732e78">

Navigation

</th></tr></thead><tbody><tr><td id="d95732e84">

**Employee Center \(sn\_cm\_core.contract\_user\)**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Navigate to **Help center** &gt; **Contracts**.
3.  Select **Contract Amendment and Renewal request**.


</td></tr><tr><td id="d95732e126">

**Contract Workspace \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to the contract request list page and select **New**. You can access the list page either from the widgets on the Contract Workspace landing page or by opening the contract request list from the list pane.
2.  In the pop-up select **Contract request**.


</td></tr></tbody>
</table>2.  In the **Request type** field, select Renewal.

3.  Enter the contract details.

<table><thead><tr><th align="left" id="d95732e168">

Option

</th><th align="left" id="d95732e171">

Steps

</th></tr></thead><tbody><tr><td id="d95732e177">

**Select an existing contract**

</td><td>

1.  Select Company and Contract type to search for contracts.

**Note:**

    -   Only expired &amp; active contract with an end date is listed
    -   Contracts that already have a renewal request in progress cannot be selected.
    -   When a contract is selected, it is automatically linked as the previous contract for the renewal request.
    -   If the required contract is not listed, choose **Enter contract details manually** and provide the contract and renewal details.
2.  Select the contract number to view details and associated documents.
3.  Select **Select** to choose the contract.


</td></tr><tr><td id="d95732e221">

**Enter contract details manually**

</td><td>

1.  Select **Enter contract details manually**.
2.  Select **Upload** to attach the contract document.

**Note:** You can only upload one document of PDF type.

</td></tr></tbody>
</table>4.  In the **Requested for** field, select the user for whom you are submitting the request.

5.  In the **Type of paper** field, select the paper type.

    -   **Own paper**: Renewal contract created from your company's standard template.
    -   **Third-party paper**: Renewal is supported for third-party contracts with a single contract type.
6.  Attach documents.

    -   For own paper renewals: Adding documents is optional. Attached documents are classified as supporting documents.
    -   For third-party paper renewals: Attaching at least one contract document is required. Attaching a supporting document is optional. You must classify each attached document.
<table id="choicetable_eks_mwq_qkc"><thead><tr><th align="left" id="d95732e301">

Method

</th><th align="left" id="d95732e304">

Actions

</th></tr></thead><tbody><tr><td id="d95732e310">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d95732e334">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>7.  Enter renewal details.

    1.  In the **Renewal start date** field, select the date when the renewal takes effect.

        If the selected contract's end date is in the future, the start date is set automatically to the day after the end date, and you can change it only to a later date. If the selected contract has expired, or if you enter contract details manually, you can select any future date.

    2.  In the **Renewal end date** field, select the date when the renewal contract ends.

        The end date must be later than the renewal start date.

    3.  In the **Description** field, enter the purpose and terms of the renewal.

8.  In the **Signature type** field, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically.
    -   **Wet signature**: Signatories sign the contract document manually.
    -   **Offline signature**: The contract is signed outside Contract Management Pro.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

9.  Add external signatories.

    Adding an external signatory is required for own-paper renewals and optional for third-party paper renewals. You can add one or more external signatories. For each signatory, enter the name, title, and a valid email address.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
10. Save the information to submit later by selecting **Save as Draft**.

11. Select **Submit**.


## Result

-   An own-paper renewal request with a linked previous contract and all required details lands in the Work in Progress state, where you can send the contract document for signature. In the work in progress state you can send contract document for signature.
-   An own-paper renewal request without a linked previous contract, and all third-party paper renewal requests, land in the New state for a contract fulfiller to work on.
-   An incomplete renewal request lands in the Draft state. Complete the details and resubmit to move the request forward.
-   For own-paper renewal requests that land in the Work in Progress state, Version 1.0 of the renewal document is generated and listed in the **Contract documents** tab. Internal signatories based on the template are populated in the generated document. For more information, see [Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.md).

## What to do next

Work on the renewal request to complete the contract lifecycle. For more information, see [Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.md).

**Parent Topic:**[Standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-sa-submit.md)


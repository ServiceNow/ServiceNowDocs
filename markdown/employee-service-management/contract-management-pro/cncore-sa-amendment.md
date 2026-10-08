---
title: Submit a standalone amendment request
description: Submit an amendment request from Employee Center or a contract listing page to modify an existing active contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-sa-amendment.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [standalone amendment request, record producer, contract amendment]
breadcrumb: [Standalone contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Submit a standalone amendment request

Submit an amendment request from Employee Center or a contract listing page to modify an existing active contract.

## Before you begin

Role required: sn\_cm\_core.contract\_user or sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to the amendment request form.

<table><thead><tr><th align="left" id="d288053e71">

Entry point

</th><th align="left" id="d288053e74">

Navigation

</th></tr></thead><tbody><tr><td id="d288053e80">

**Employee Center \(sn\_cm\_core.contract\_user\)**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Navigate to **Help center** &gt; **Contracts**.
3.  Select **Contract Amendment and Renewal**.


</td></tr><tr><td id="d288053e119">

**Contract Workspace \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to the contract request list page and select **New**. You can access the list page either from the widgets on the Contract Workspace landing page or by opening the contract request list from the list pane.
2.  In the pop-up select **Contract request**.


</td></tr></tbody>
</table>2.  In the **Request type** field, select Amendment.

3.  Enter the contract details.

<table><thead><tr><th align="left" id="d288053e161">

Option

</th><th align="left" id="d288053e164">

Steps

</th></tr></thead><tbody><tr><td id="d288053e170">

**Select an existing contract**

</td><td>

1.  Select Company and Contract type to search for contracts.

**Note:**

    -   Only active contracts are listed. Contracts with an ongoing amendment are disabled from selection.
    -   When a contract is selected, it is automatically linked as the parent contract for the amendment request.
    -   If the required contract is not listed, choose **Enter contract details manually** and provide the contract and amendment details.
2.  Select the contract number to view details and associated documents.
3.  Select **Select** to choose the contract.


</td></tr><tr><td id="d288053e211">

**Enter contract details manually**

</td><td>

1.  Select **Enter contract details manually**.
2.  Select **Upload** to attach the contract document.

**Note:** You can only upload one document of PDF type.

</td></tr></tbody>
</table>4.  In the **Requested for** field, select the user for whom you are submitting the request.

5.  In the **Type of paper** field, select the paper type.

    -   **Own paper**: Amendment contract created from your company's standard template.
    -   **Third-party paper**: Amendment is supported for third-party contracts with a single contract type.
6.  Attach documents.

    -   For own paper amendments: Adding documents is optional. Attached documents are classified as supporting documents.
    -   For third-party paper amendments: Attaching at least one contract document is required. You must classify the attached document.
<table id="choicetable_eks_mwq_qkc"><thead><tr><th align="left" id="d288053e291">

Method

</th><th align="left" id="d288053e294">

Actions

</th></tr></thead><tbody><tr><td id="d288053e300">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d288053e324">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>7.  Enter amendment details.

    1.  In the **Effective date** field, select the date when the amendment takes effect.

        The effective date must be a future date and before the contract end date.

    2.  In the **Description** field, enter the details of the changes required to the existing contract.

8.  In the **Signature type** field, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically.
    -   **Wet signature**: Signatories sign the contract document manually.
    -   **Offline signature**: The contract is signed outside Contract Management Pro.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

9.  Add external signatories.

    Adding an external signatory is required for own paper amendments and optional for third-party paper amendments.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
10. Save the information to submit later by selecting **Save as Draft**.

11. Select **Submit**.


## Result

An amendment request is created.

-   The request is created in the New state.
-   For own paper amendments, Version 1.0 of the amendment document is generated and listed in the Contract Document tab.
-   When a contract is selected during submission, it is automatically linked as the parent contract for the amendment request.
-   Internal signatories based on the template are populated in the generated document.

## What to do next

Work on the amendment request to complete the contract lifecycle. For more information, see [Work on amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-amend-work.md).

**Parent Topic:**[Standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-sa-submit.md)


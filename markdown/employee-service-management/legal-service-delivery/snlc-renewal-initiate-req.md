---
title: Submit a renewal request
description: Submit a renewal request from the Employee Center to extend or replace an existing contract.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/legal-service-delivery/snlc-renewal-initiate-req.html
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 4
keywords: [Renewal request, Submit renewal, Own paper renewal, Third-party renewal]
breadcrumb: [Contract renewals, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a renewal request

Submit a renewal request from the Employee Center to extend or replace an existing contract.

## Before you begin

**Note:** In new deployments, the base system legal contract intake forms \(Non-disclosure agreement, Third-party contract review, and Contract Amendment and Renewal request\) are hidden by default. On enabling they will be available under **Home** &gt; **Legal Services** &gt; **Legal agreements**. If you are upgrading from an existing deployment, your current intake form visibility settings are unchanged.

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## About this task

A sample workflow while submitting a renewal request would be:

1.  Initiate a renewal request.
2.  Select a contract for renewal or enter contract details manually.
3.  Select the paper type.
4.  Enter renewal details, including the start date, end date, and description.
5.  Select the signature type.
6.  Attach documents.
7.  Add external signatories.
8.  Submit the request.

## Procedure

1.  Navigate to the contract request form.

<table id="choicetable_renewal-entry-points"><thead><tr><th align="left" id="d163396e138">

Entry point

</th><th align="left" id="d163396e141">

Navigation

</th></tr></thead><tbody><tr><td id="d163396e147">

**Employee Center \(sn\_cm\_core.contract\_user\)**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Navigate to **Help center** &gt; **Legal services** &gt; **Legal agreements**.
3.  Select **Contract Amendment and Renewal request**.


</td></tr><tr><td id="d163396e194">

**Legal Counsel Center landing page \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.
2.  On the landing page, select **New**.
3.  Select **Contract Amendment and Renewal**.


</td></tr><tr><td id="d163396e233">

**Legal Counsel Center listing page \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Legal requests** &gt; **All** from the listing panel.
4.  On the list page, select **New**.
5.  Select **Contract Amendment and Renewal**.


</td></tr></tbody>
</table>2.  In the **Request type** field, select Renewal.

3.  Enter the contract details.

<table id="choicetable_gh2_3mg_rkc"><thead><tr><th align="left" id="d163396e306">

Option

</th><th align="left" id="d163396e309">

Steps

</th></tr></thead><tbody><tr><td id="d163396e315">

**Select an existing contract**

</td><td>

1.  Select **Company** and contract type to search for contracts.
2.  If your administrator has configured additional search fields, such as Account, enter values in those fields.
3.  Select the contract number to view details and associated documents.
4.  Select **Select** to choose the contract.

**Note:**

    -   Only Active and Expired contracts with an end date are listed.
    -   Contracts that already have a renewal request in progress cannot be selected.
    -   When a contract is selected, it is automatically linked as the previous contract for the renewal request.
    -   If the required contract is not listed, choose **Enter contract details manually** and provide the contract and renewal details.


</td></tr><tr><td id="d163396e366">

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
    -   For third-party paper renewals: Adding documents is required. You must classify the attached document.
<table id="choicetable_eks_mwq_qkc"><thead><tr><th align="left" id="d163396e446">

Method

</th><th align="left" id="d163396e449">

Actions

</th></tr></thead><tbody><tr><td id="d163396e455">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d163396e479">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>7.  Enter renewal details.

    1.  In the **Renewal start date** field, select the date when the renewal takes effect.

        If the selected contract's end date is in the future, the start date is set automatically to the day after the end date, and you can change it only to a later date. If the selected contract has expired, or if you enter contract details manually, you can select any future date.

    2.  In the **Renewal end date** field, select the date when the renewal contract ends.

        The end date must be after the start date.

    3.  In the **Description** field, enter the purpose and terms of the renewal.

8.  In the **Signature type** field, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically.
    -   **Wet signature**: Signatories sign the contract document manually.
    -   **Offline signature**: The contract is signed outside Contract Management Pro.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

9.  Add external signatories.

    Adding an external signatory is required for own-paper renewals and optional for third-party paper renewals. You can add one or more external signatories. For each signatory, enter the name, title, and a valid email address.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
10. Save the information to submit later by selecting **Save as Draft**.

11. Select **Submit**.


## Result

-   An own-paper renewal request with a linked previous contract and all required details lands in the Work in Progress state.
-   An own-paper renewal request without a linked previous contract, and all third-party paper renewal requests, land in the New state for a contract fulfiller to work on.
-   An incomplete renewal request lands in the Draft state. Complete the details and resubmit to move the request forward.
-   For own-paper renewal requests that land in the Work in Progress state, Version 1.0 of the renewal document is generated and listed in the **Contract documents** tab. Internal signatories based on the template are populated in the generated document. For more information, see [Define an internal signatory rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-define-internal-signers-rule.md).

**Parent Topic:**[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/legal-service-delivery/snlc-renewal-landing.md)


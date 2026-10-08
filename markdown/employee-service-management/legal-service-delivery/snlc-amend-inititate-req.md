---
title: Submit amendment request
description: Submit an amendment request from the Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-service-delivery/snlc-amend-inititate-req.html
release: brazil
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 4
keywords: [Own paper amendment request, third-party amendment request, Amendment request]
breadcrumb: [Contract amendments, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit amendment request

Submit an amendment request from the Employee Center.

## Before you begin

**Note:** In new deployments, the base system legal contract intake forms \(Non-disclosure agreement, Third-party contract review, and Contract Amendment and Renewal request\) are hidden by default. On enabling they will be available under **Home** &gt; **Legal Services** &gt; **Legal agreements**. If you are upgrading from an existing deployment, your current intake form visibility settings are unchanged.

Role required:

-   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user
-   sn\_cm\_core.contract\_fulfiller

## About this task

A sample workflow while submitting on an amendment request would be:

1.  Initiate an amendment request.
2.  Select a contract for amendment or enters contract details manually.

    **Note:** When a contract is selected while submitting a request, it’s automatically linked as the parent contract for the amendment request.

3.  Select the paper type.
4.  Enter amendment details.
5.  Select the signature type.
6.  Attach documents.
7.  Add external signatories.
8.  Submit the request.

## Procedure

1.  Navigate to the contract request form.

<table id="choicetable_amend-entry-points"><thead><tr><th align="left" id="d130796e135">

Entry point

</th><th align="left" id="d130796e138">

Navigation

</th></tr></thead><tbody><tr><td id="d130796e144">

**Employee Center \(sn\_cm\_core.contract\_user\)**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Navigate to **Help center** &gt; **Legal services** &gt; **Legal agreements**.
3.  Select **Contract Amendment and Renewal request**.


</td></tr><tr><td id="d130796e191">

**Legal Counsel Center landing page \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.
2.  On the landing page, select **New**.
3.  Select **Contract Amendment and Renewal**.


</td></tr><tr><td id="d130796e230">

**Legal Counsel Center listing page \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.
2.  Select the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  Select **Legal requests** &gt; **All** from the listing panel.
4.  On the list page, select **New**.
5.  Select **Contract Amendment and Renewal**.


</td></tr></tbody>
</table>2.  In the **Request type** field, select Amendment.

    \[Omitted image "snlc-amend-submit-req.png"\] Alt text: Contract repository record showing amendment related details

3.  Enter the contract details.

<table id="choicetable_fv5_1mg_rkc"><thead><tr><th align="left" id="d130796e314">

Option

</th><th align="left" id="d130796e317">

Steps

</th></tr></thead><tbody><tr><td id="d130796e323">

**Select an existing contract**

</td><td>

1.  In the **Company** field, select the company.
2.  In the **Contract type** field, select the contract type.
3.  Select the contract number to view details and associated documents.
4.  Select **Select** to choose the contract.

**Note:**

    -   Only active contracts are listed. Contracts with ongoing amendment are disabled from selection.
    -   When a contract is selected, it is automatically linked as the parent contract for the amendment request.
    -   If the required contract is not listed, choose **Enter contract details manually** and provide the contract and amendment details.


</td></tr><tr><td id="d130796e374">

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
    -   For third-party paper amendments: Adding documents is required. You must classify the attached document.
<table id="choicetable_eks_mwq_qkc"><thead><tr><th align="left" id="d130796e454">

Method

</th><th align="left" id="d130796e457">

Actions

</th></tr></thead><tbody><tr><td id="d130796e463">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d130796e487">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>7.  Enter amendment details.

    1.  In the **Effective date** field, select the date when the amendment takes effect.

        The effective date must be within the original contract's start and end dates.

    2.  In the **Description** field, enter the details of the changes required to the existing contract.

8.  In the **Signature type** field, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically.
    -   **Wet signature**: Signatories sign the contract document manually.
    -   **Offline signature**: The contract is signed outside Contract Management Pro.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

9.  Add external signatories.

    Adding an external signatory is required for own paper amendments and optional for third-party paper amendments.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
10. Save the information to submit later by selecting **Save as Draft**.

11. Select **Submit**.


## Result

-   An amendment request is submitted in the New state and a contract request is created for the contract fulfiller to work on it.
-   For own paper based amendment request, Version 1.0 of the amendment document is generated and listed in the **Contract Document** tab.
-   The contract document process involves:
    -   Using the correct contract template based on contract template rules.
    -   Replacing the metadata with data from the request.
    -   Replacing the signatory information.
    -   Placing the content of the clauses in the contract document according to the clause variation rules.
-   Internal signatories based on the template are also populated in the generated document. For more information, see [Define an internal signatory rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-define-internal-signers-rule.md). View the signatories in the Signatories tab of the contract request.

**Parent Topic:**[Contract amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/legal-service-delivery/snlc-amend-req-landing.md)


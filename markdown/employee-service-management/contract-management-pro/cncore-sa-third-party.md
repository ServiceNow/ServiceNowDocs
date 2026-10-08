---
title: Submit a standalone third-party paper contract request
description: Submit a new third-party paper contract request using a record producer form from Employee Center or a contract listing page without linking to a parent record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-sa-third-party.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [standalone contract request, record producer, third-party paper]
breadcrumb: [Standalone contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Submit a standalone third-party paper contract request

Submit a new third-party paper contract request using a record producer form from Employee Center or a contract listing page without linking to a parent record.

## Before you begin

Before submitting a contract request, verify that contract types have been created. For more information, see [Create a contract type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-create-contract-type.md).

Role required: sn\_cm\_core.contract\_user or sn\_cm\_core.contract\_fulfiller

## About this task

Third-party paper contracts are created by uploading a document provided by the other party for review and signature. The record producer form guides you through entering all required contract details. You can save your work as a draft and return to complete it later.

## Procedure

1.  Navigate to the contract request form.

<table><thead><tr><th align="left" id="d638824e87">

Entry point

</th><th align="left" id="d638824e90">

Navigation

</th></tr></thead><tbody><tr><td id="d638824e96">

**Employee Center \(sn\_cm\_core.contract\_user\)**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Navigate to **Help center** &gt; **Contracts**.
3.  Select **Contract request**.


</td></tr><tr><td id="d638824e132">

**Contract Workspace \(sn\_cm\_core.contract\_fulfiller\)**

</td><td>

1.  Navigate to the contract request list page and select **New**. You can access the list page either from the widgets on the Contract Workspace landing page or by opening the contract request list from the list pane.
2.  In the pop-up select **Contract request**.


</td></tr></tbody>
</table>2.  In the **Requested for** field, verify or update the user for whom the contract is being requested.

    This field is automatically populated with your name.

3.  In the **Type of paper** list, select **Third Party Paper - Upload the other party's document for review**.

4.  In the **Contract party type** list, select the type of party you are contracting with.

    Options include Vendor, Partner, or other party types configured by your administrator.

5.  In the **Purpose of the contract** field, enter a brief description of the contract purpose.

6.  In the **Company** list, select the company for which the contract is being created.

7.  In the **Address** field, enter the address associated with the contract.

8.  In the **Country** list, select the country.

9.  In the **Contract type** list, select the type of contract.

    **Note:** Only active contract types are displayed in the list.

10. In the **Contract start date** field, enter a future date as the contract start date.

11. In the **Contract end date** field, specify the contract end date.

    The end date must be later than the start date.

12. Attach the contract document.

    Adding at least one contract document is mandatory for third-party paper requests. You must classify the attached document as either a supporting document or the contract type selected.

<table><thead><tr><th align="left" id="d638824e278">

Method

</th><th align="left" id="d638824e281">

Actions

</th></tr></thead><tbody><tr><td id="d638824e287">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d638824e311">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>13. In the **Signature type** list, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically through a configured e-signature provider.
    -   **Wet signature**: Signatories sign the contract document manually. The signed document is uploaded to the contract request.
    -   **Offline signature**: The contract is signed outside Contract Management Pro. Signature request emails are not sent.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

14. Add external signatories.

    Adding external signatories is optional for third-party paper requests.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
15. Save the information to submit later by selecting **Save as Draft**.

    **Note:** If the contract type is deactivated when the request is saved as draft, the inactive contract type is not included in the list. You must select an active contract type before submitting the request.

16. Select **Submit**.


## Result

A contract request is created and opens in a new tab in the New state.

## What to do next

As a fulfiller, work on the contract request to complete the contract lifecycle. For more information, see [Work on a non-self-served contract review request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-nss-review-request.md).

**Parent Topic:**[Standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-sa-submit.md)


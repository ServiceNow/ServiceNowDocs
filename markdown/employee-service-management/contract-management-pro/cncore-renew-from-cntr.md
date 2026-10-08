---
title: Initiate a renewal from a contract record
description: From an active or expired contract record, initiate a renewal request to extend or replace the contract with a new contract period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-renew-from-cntr.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [Renewal from contract, Contract record, Renew contract]
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate a renewal from a contract record

From an active or expired contract record, initiate a renewal request to extend or replace the contract with a new contract period.

## About this task

You can raise a renewal request directly from a contract repository record by selecting **Renew** in the contract header. This opens a record producer form with the **Request type** set to **Renewal** and contract details pre-populated from the original contract.

## Before you begin

-   Verify the Renew option is enabled for the contract repository record.
-   The contract must be in the Active state with an end date, or in the Expired state, with no pending renewal request.
-   Contracts with a completed renewal don't have the **Renew** option available.

Role required: sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to the contract repository record of the contract you want to renew.

2.  In the contract record header, select **Renew**.

    \[Omitted image "cmpro-cntr-renew.png"\] Alt text: Initiate renewal request from the contract repository record

3.  In the pop-up, select **Contract Amendment and Renewal**.

    The record producer opens. The **Request type** is set to **Renewal** and cannot be changed. The **Linked contract**, **Company**, **Contract type**, and **Requested for** fields are automatically set from the original contract.

4.  In the **Type of paper** list, select **Own paper** or **Third-party paper**.

    The type of paper determines whether the renewal uses your company's template or a third-party document. Renewal is supported for third-party contracts with a single contract type.

5.  Enter the renewal details.

    1.  In the **Renewal start date** field, select the date when the renewed contract takes effect.

        Enter a start date that is today or a future date. If the original contract has an end date, the start date is automatically set to the day after that end date.

    2.  In the **Renewal end date** field, select the date when the renewed contract ends.

        The end date must be after the start date.

    3.  In the **Description** field, enter details about the renewal.

6.  Attach contract documents.

    -   For own paper renewals: Adding documents is optional. Attached documents are classified as supporting documents.
    -   For third-party paper renewals: Adding documents is required. You must classify the attached document as either a supporting document or the contract type selected.
<table><thead><tr><th align="left" id="d263506e227">

Method

</th><th align="left" id="d263506e230">

Actions

</th></tr></thead><tbody><tr><td id="d263506e236">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d263506e260">

**Drag and drop**

</td><td>

Drag files from your local computer into the browser window to attach them to the request.

</td></tr></tbody>
</table>7.  In the **Signature type** list, select the signature type for the contract document.

    -   **Electronic signature**: Signatories sign the contract document electronically through a configured e-signature provider.
    -   **Wet signature**: Signatories sign the contract document manually. The signed document is uploaded to the contract request.
    -   **Offline signature**: The contract is signed outside Contract Management Pro. Signature request emails are not sent.
    For more information about signature workflows, see [Signature workflow for a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-signature-workflow.md).

8.  Add external signatories.

    Select the **Add signatories** check box to expand the signatories section. Adding at least one external signatory is required for own paper renewals and optional for third-party paper renewals.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
9.  Save the information to submit later by selecting **Save as Draft**.

10. Select **Submit**.


## Result

A renewal request is created. The request is automatically linked to the original contract as the parent contract.

-   For own paper renewals with all required fields provided, the request is created in the Work in Progress state. Version 1.0 of the renewal document is generated from the template.
-   For third-party paper renewals with all required fields provided, the request is created in the New state.
-   Internal signatories based on the template are populated in the generated document. For more information, see [Define an internal signatory rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-define-internal-signers-rule.md).

## What to do next

Work on the renewal request to complete the contract lifecycle. For more information, see [Work on a renewal request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-renewal-fulfiller.md).

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


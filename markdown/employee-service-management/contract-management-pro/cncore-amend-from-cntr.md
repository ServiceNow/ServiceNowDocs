---
title: Initiate an amendment from a contract record
description: From an active contract record, initiate an amendment request to modify the contract terms, clauses, or details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/contract-management-pro/cncore-amend-from-cntr.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 3
keywords: [Amendment from contract, Contract record, Amend contract]
breadcrumb: [Parent-linked contract requests, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate an amendment from a contract record

From an active contract record, initiate an amendment request to modify the contract terms, clauses, or details.

## About this task

You can raise an amendment request directly from a contract repository record by selecting **Amend** in the contract header. This opens a record producer form with the **Request type** set to **Amendment** and contract details pre-populated from the original contract.

## Before you begin

-   Verify the Amend option is enabled for the contract repository record.
-   The contract must be in the Active state with no pending amendment request.

Role required: sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Navigate to the contract repository record of the contract you want to amend.

2.  In the contract record header, select **Amend**.

    \[Omitted image "cmpro-cntr-amend.png"\] Alt text: Initiate amendment request from the contract repository record

3.  In the pop-up, select **Contract Amendment and Renewal**.

    The record producer opens. The **Request type** is set to **Amendment** and cannot be modified. The **Linked contract**, **Company**, **Contract type**, and **Requested for** fields are automatically set from the original contract.

4.  In the **Type of paper** list, select **Own paper** or **Third-party paper**.

    The type of paper determines whether the amendment uses your company's template or a third-party document.

5.  Enter the amendment details.

    1.  In the **Effective date** field, select the date when the amendment takes effect.

        The effective date must be within the original contract's start and end dates.

    2.  In the **Description** field, enter the details of the changes required to the existing contract.

6.  Attach contract documents.

    -   For own paper amendments: Adding documents is optional. Attached documents are classified as supporting documents.
    -   For third-party paper amendments: Adding documents is required. You must classify the attached document as either a supporting document or the contract type selected.
<table><thead><tr><th align="left" id="d691852e209">

Method

</th><th align="left" id="d691852e212">

Actions

</th></tr></thead><tbody><tr><td id="d691852e218">

**Choose a file**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d691852e242">

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

    Adding at least one external signatory is required for own paper amendments and optional for third-party paper amendments.

    -   To add a signatory, select **Add** and provide the signatory's details.
    -   To modify a signatory's information, select the Edit row icon and update the details.
    -   To remove a signatory, select the Remove row icon on the signatory's row.
9.  Select **Submit**.


## Result

An amendment request is created. The request is automatically linked to the original contract as the parent contract.

-   For own paper amendments with all required fields provided, the request is created in the New state. Version 1.0 of the amendment document is generated from the template.
-   For third-party paper amendments with all required fields provided, the request is created in the New state.
-   Internal signatories based on the template are populated in the generated document. For more information, see [Define an internal signatory rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-define-internal-signers-rule.md).

## What to do next

Work on the amendment request to complete the contract lifecycle. For more information, see [Work on amendment request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cmpro-amend-work.md).

**Parent Topic:**[Parent-linked contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/contract-management-pro/cncore-initiate-contract.md)


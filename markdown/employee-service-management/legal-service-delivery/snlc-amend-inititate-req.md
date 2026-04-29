---
title: Submit amendment request
description: Submit an amendment request from the Employee Center.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Own paper amendment request, third-party amendment request, Amendment request]
breadcrumb: [Contract amendments, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit amendment request

Submit an amendment request from the Employee Center.

## Before you begin

Role required: sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user

## About this task

A sample workflow while submitting on an amendment request would be:

1.  Initiate an amendment request.
2.  Select a contract for amendment or enters contract details manually.

    **Note:** When a contract is selected while submitting a request, it’s automatically linked as the parent contract for the amendment request.

3.  Select the paper type.
4.  Enters amendment details.
5.  Select the signature type.
6.  Attach documents.
7.  Submit the request.

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

2.  Select **Legal services** from the header.

3.  Search for **Amendment request** and open the intake form.![Amendment request intake form in Employee Center](../image/snlc-amend-record-producer.png)

4.  Enter the contract details.

<table id="choicetable_ihc_fgn_fhc"><thead><tr><th align="left" id="d123223e139">

Option

</th><th align="left" id="d123223e142">

Steps

</th></tr></thead><tbody><tr><td id="d123223e148">

**Select an existing contract**

</td><td>

1.  Select company in the **Company** drop-down.
2.  Select the contract type in the **Contract type** dropdown.

**Note:** Only active contracts and contracts with no pending amendment requests are listed.

3.  Select the contract number to view details and the associated documents. Although some of the fields look editable, changes made cannot be saved to the contract record.
4.  Select **Select** to choose the contract.

**Note:**

    -   You can’t select contracts that have an active amendment request.
    -   If the required contract isn’t listed, choose **Enter contract details manually** option and provide the contract and amendment details.
    -   A parent contract child hierarchy is established between the selected contract and the amendment request. You can’t unlink the parent and the child contract.


</td></tr><tr><td id="d123223e200">

**Manually enter contract details**

</td><td>

1.  Select **Enter contract details manually**.
2.  Select **Upload**.

**Note:** You can only upload one document of PDF type.

3.  Select the file to upload and select **Open**.


</td></tr></tbody>
</table>5.  Select type of paper in the **Type of paper** field.

    -   For own-paper based amendment request, select **Own paper**.
    -   For third-party paper based amendment request, select **Third Party Paper**. The amendment is supported for third-party contracts with a single contract type.
6.  Enter amendment details.

    1.  In the **Effective date** field, select a date within the existing contract’s start and end dates to indicate when the amendment takes effect.

    2.  In the **Requested for**, select the user for whom you want to submit a legal request.

    3.  In the **Description** field, enter the details of the changes required to the existing contract document and any other details.

7.  Select Electronic or Wet signature, in the **Signature type** drop-down.

    For more information on the signature flow, see [Signature workflow for a request](../concept/snlc-lsd-signature-workflow.md)

8.  Attach contract documents.

    -   For own paper based amendment requests: Adding documents isn’t required. The attached documents are classified as supporting documents.
    -   For third-party paper based amendment requests: Adding documents is required. You must classify the attached document. The options available for classification are supporting documents and contract type selected in the contract details section.
<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d123223e334">

Method

</th><th align="left" id="d123223e337">

Actions

</th></tr></thead><tbody><tr><td id="d123223e343">

**__Choose the file__**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d123223e368">

**__Drag the file__**

</td><td>

Drag files from your local computer into your browser window to attach them to the current record.

</td></tr></tbody>
</table>9.  Add external signatories.

    Adding an external signatory is required for own-paper based amendment request and optional for third-party based amendment request.

    -   To add a signatory, select **Add** and provide the signatory's details.

    -   To modify a signatory's information, select the Edit row icon \(![Edit row icon.](../../legal-digital-forensics/image/rename-icon.png)\) on the signatory's row and update the details.

    -   To remove a signatory, select the Remove row icon \(![Remove row icon.](../../legal-digital-forensics/image/delete-icon.png)\) on the signatory's row.

10. Save the information in the request to submit later in Employee Center by selecting **Save as Draft**.

    **Note:** If the contract type is deactivated when the request is saved as draft, the inactive contract type isn’t included in the list displayed in the **Contract type** and **Document type** fields. You must select an active contract type before submitting the request.

11. Select **Submit**.


## Result

-   An amendment request is submitted in the New state and a contract request is created for the contract fulfiller to work on it.
-   For own paper based amendment request, Version 1.0 of the amendment document is generated and listed in the **Contract Document** tab.
-   The contract document process involves:
    -   Using the correct contract template based on contract template rules.
    -   Replacing the metadata with data from the request.
    -   Replacing the signatory information.
    -   Placing the content of the clauses in the contract document according to the clause variation rules.
-   Internal signatories based on the template are also populated in the generated document. For more information, see [Define an internal signatory rule](../../contract-mgmt-pro/task/cncore-define-internal-signers-rule.md). View the signatories in the Signatories tab of the contract request.

For more information on how to view and track a legal request, see [View and track non-disclosure agreement requests as a legal user](snlc-view-legal-req-details.md).

**Parent Topic:**[Contract amendments](../concept/snlc-amend-req-landing.md)


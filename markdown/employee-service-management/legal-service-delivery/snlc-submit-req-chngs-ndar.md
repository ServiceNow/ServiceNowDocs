---
title: Review a contract document in Employee Center
description: As a contract user, review a contract document and submit a change request to the contract fulfiller if changes are required in the contract document.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-service-delivery/snlc-submit-req-chngs-ndar.html
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reviewing and finalizing a self-served contract document, Work on NDA legal requests, Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Review a contract document in Employee Center

As a contract user, review a contract document and submit a change request to the contract fulfiller if changes are required in the contract document.

## Before you begin

Role required: sn\_cm\_core.contract\_user and sn\_lg\_ops.legal\_user

## About this task

-   Change requests can be submitted only by the user who has initiated the contract request or for whom it was initiated.
-   The Contract state is Work in progress.
-   The **Request changes** option isn’t available if a previously submitted change request isn’t completed.

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

    **Note:** If you’re using Legal Service Portal, open the request by navigating to it and selecting **My Requests** &gt; **View all requests** from the header.

2.  Select **My Requests** from the header.

3.  Open your non-disclosure agreement request.

4.  Select the **Contract documents** tab.

5.  Access the contract document.

<table id="choicetable_vxh_nwf_t1c"><thead><tr><th align="left" id="d104606e128">

Location

</th><th align="left" id="d104606e131">

Action

</th></tr></thead><tbody><tr><td id="d104606e137">

**From internal storage**

</td><td>

1.  Select **Preview document**.
2.  In the drop-down list, select the contract type.
3.  Select **Preview** to view the document.


</td></tr><tr><td id="d104606e164">

**From external storage**

</td><td>

Select the link in the **URL** column. The document opens from the external storage.

</td></tr></tbody>
</table>6.  Review the contract document.

<table id="choicetable_h24_1ps_2bc"><thead><tr><th align="left" id="d104606e188">

Review result

</th><th align="left" id="d104606e191">

Action

</th></tr></thead><tbody><tr><td id="d104606e197">

**No change is required**

</td><td>

Send the document for signature. For more information, see [Send a non-disclosure agreement document for signature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-send-doc-sign-nda.md).

</td></tr><tr><td id="d104606e215">

**Changes are required**

</td><td>

Submit a change request.

 1.  From the Actions drop-down list, select **Request Changes**.
2.  Attach a file in the **Attachment document** field.
3.  Describe the desired changes in the **Comments** box.
4.  Select **Submit**.

The change request is submitted for the contract document. The change request details and the attached document are added to the activity stream.

 -   When a contract request has been assigned to a contract fulfiller, its status updates to Changes requested and the Contract state remain in Work in progress.
-   If a contract request isn’t assigned to anyone, its state changes to New and it is listed as unassigned in the contract workspace for a contract fulfiller to work on.


</td></tr></tbody>
</table>
**Parent Topic:**[Reviewing and finalizing a self-served contract document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-service-delivery/snlc-review-finalize-contract.md)


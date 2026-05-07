---
title: Create a legal request for a third-party contract review
description: Create a legal request for the legal team to review a third-party contract or the terms and conditions provided by the third party.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Third-party contract review requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a legal request for a third-party contract review

Create a legal request for the legal team to review a third-party contract or the terms and conditions provided by the third party.

## Before you begin

Role required: sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user

## About this task

## Procedure

1.  Access the third-party review intake form either from the Legal Service Portal or from Employee Center.

<table id="choicetable_new_tpc"><thead><tr><th align="left" id="d571560e59">

Method

</th><th align="left" id="d571560e62">

Action

</th></tr></thead><tbody><tr><td id="d571560e68">

**Legal Service Portal**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**
2.  Select **Service Catalog**.
3.  Search for and open the **Third-party review** request item.


</td></tr><tr><td id="d571560e107">

**Employee Center**

</td><td>

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**
2.  Select **Legal** &gt; **Browse all Legal** from the header.
3.  Search for and open the **Third-party review** request item.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For a description of the field values, see [Third-party Contract Review form](../reference/snlc-tpc-intake-fields.md)

3.  Add single or multiple contract and supporting documents to be reviewed by the legal department.

    1.  In the Documents section, attach documents.

<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d571560e188">

Method

</th><th align="left" id="d571560e191">

Actions

</th></tr></thead><tbody><tr><td id="d571560e197">

**__Choose the file__**

</td><td>

1.  Select **Choose a file**.
2.  Select the files to attach and select **Open**.


</td></tr><tr><td id="d571560e222">

**__Drag the file__**

</td><td>

Drag files from your local computer into your browser window to attach them to the current record.

</td></tr></tbody>
</table>4.  Classify the attached documents.

<table id="choicetable_kjj_yws_5yb"><thead><tr><th align="left" id="d571560e241">

Classification

</th><th align="left" id="d571560e244">

Actions

</th></tr></thead><tbody><tr><td id="d571560e250">

**Contract document**

</td><td>

In the **Document type** list, select the contract type that is relevant to the attached document.

 Only active contract types are displayed in the list.

 **Note:** At least one document should be classified as a contract document.

</td></tr><tr><td id="d571560e274">

**Supporting document**

</td><td>

In the **Document type** list, select **Supporting Documents**.

</td></tr></tbody>
</table>    **Note:** Adding a single contract document classifies the request as a single contract type request while adding more than one contract documents classifies it as multiple contract type requests.

5.  Save the information in the request to submit later in Employee Center by selecting **Save as Draft**.

    **Note:** If the contract type is deactivated when the request is saved as draft, the inactive contract type is not included in the list displayed in the **Document type** field. You must select an active contract type before submitting the request.

6.  Select **Submit**.


## Result

-   A legal request for reviewing the attached third-party contracts and any supporting documents is created in the New state.
-   The contract documents and supporting documents are available in the respective tabs, and the contract status is New.
-   For a custom record producer, if no documents are attached, the legal request is created in the Draft state. You must upload the documents and resubmit the contract request. For more information, see [Resubmit third-party contract request](snlc-multiple-doc-tpc.md).

For more information on how to view and track the legal request, see [View and track third-party contract review request as a legal user](snlc-tpc-view-request.md).

## What to do next

As a member of the legal department contract support team, work on the request to review the contract and get it signed. For more information, see [Work on a third-party contract review request](snlc-work-tpc-review-request.md)

.

-   **[Resubmit third-party contract request](snlc-multiple-doc-tpc.md)**  
As a legal user, resubmit contract request in draft state.

**Parent Topic:**[Third-party contract review requests](../concept/snlc-request-third-party-contract-1.md)


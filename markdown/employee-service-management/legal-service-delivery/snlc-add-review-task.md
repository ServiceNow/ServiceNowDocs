---
title: Request an internal review
description: Initiate a review task for review of the contract document by subject matter experts.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Internal review overview, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Request an internal review

Initiate a review task for review of the contract document by subject matter experts.

## Before you begin

-   For non-disclosure agreements, you may want review and feedback from the internal subject matter experts. If needed, the contract requester can submit a change request to the contract fulfiller. The contract fulfiller then submits a review task with the change request details. For more information, see [Review a contract document in Employee Center](snlc-submit-req-chngs-ndar.md).
-   For third-party contract review requests, the contract user cannot create a change request. Instead, the contract fulfiller creates a task for internal review.

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

-   You can raise a review task when the contract request State is Work in progress or Awaiting review.
-   You can create parallel review tasks for the same contract document for different reviewer groups. You can't create a review task for the same document with the same reviewer group if another active task already exists.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  Navigate to **Legal Requests** &gt; **All**.

4.  Open a legal request.

5.  Navigate to **Contract Requests** tab and open the request.

6.  Select the Reviews tab.

7.  Select **New task**.

8.  On the Create New Review Task form, fill in the details.

<table id="table_wjg_xgm_b1b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Contract type

</td><td>

Contract for which you want to submit an internal review request.**Note:** The field is auto-populated when there is only one contract type. The latest revision of contract document is sent for review

</td></tr><tr><td>

Due date

</td><td>

Date to complete the task.

</td></tr><tr><td>

Priority

</td><td>

Level of priority to address the review request.

</td></tr><tr><td>

Assignment group

</td><td>

User group with contract reviewer role to which the task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to whom the task is assigned. If an assignment group is selected, the list shows members of the selected group.

</td></tr><tr><td>

Instructions

</td><td>

Description to specify the content to be reviewed.

</td></tr></tbody>
</table>9.  Select **Create**.


## Result

A review task is created, listed in the Reviews tab and the change request details are added to the Activity stream. The Contract status updates to Awaiting review. If the new task doesn't appear in the list, click the refresh list button \(![Refresh list icon.](../../workplace-central/images/refresh-icon.png)\) to view it.

**Parent Topic:**[Internal review overview](snlc-expert-review.md)


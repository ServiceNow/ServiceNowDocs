---
title: Work on commercial claim adjuster tasks
description: Update and close the adjuster tasks of a claim case.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Adjuster tasks, Use, Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on commercial claim adjuster tasks

Update and close the adjuster tasks of a claim case.

## Before you begin

Role required: sn\_ins\_claim\_cml.auto\_adjuster

**Important:** To access the Claim workspace, Fraud score, and Summary adjuster workspace related tabs, you must activate the CSM default record page. By default, the page is set to inactive. To determine the default page for displaying records in CSM Configurable Workspace, see [CSM Configurable Workspace record pages](https://servicenow.com/docs/bundle/utah-customer-service-management/page/product/customer-service-management/concept/csm-config-workspace-record-pages.html)

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Open the task one of the following ways.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d63869e78">

Option

</th><th align="left" id="d63869e81">

Steps

</th></tr></thead><tbody><tr><td id="d63869e87">

**From the landing page**

</td><td>

Select a task from the All open claims list.

</td></tr><tr><td id="d63869e96">

**From the Commercial auto claim adjuster tasks list**

</td><td>

1.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).
2.  In the **Lists** tab, under **Commercial auto claim adjuster tasks**, select **All**.
3.  In the list, select the task that you want to open.


</td></tr></tbody>
</table>3.  Finish the work that is required to complete the evaluation or settlement task.

4.  Work on the adjuster task by completing various actions from the claim workspace.

<table id="claim-workspace-actions-table"><thead><tr><th align="left" id="d63869e147">

Claim task

</th><th align="left" id="d63869e150">

Claim workspace actions

</th></tr></thead><tbody><tr><td id="d63869e156">

**To add a document verification task**

</td><td>

1.  Select **Add document verification task**.
2.  Fill in the required fields.
3.  Select **Save**.
4.  Select **Submit document**.


</td></tr><tr><td id="d63869e191">

**To verify a document**

</td><td>

Select **Verify** to verify the document or **Reject** to reject the submitted document for verification.

</td></tr><tr><td id="d63869e206">

**To add claim coverage**

</td><td>

1.  Select **Add coverage**.
2.  Select Claim coverage and any of the following required:
    -   Claim property
    -   Claim participant
3.  Select **Save**.


</td></tr><tr><td id="d63869e241">

**To add a reserve or payment**

</td><td>

1.  In Coverages and financials, select one from the Claim coverage list:
    -   **Add reserve**
    -   **Add payment**
2.  Fill in the required fields.
3.  Select **Save**.


</td></tr><tr><td id="d63869e276">

**To add an ad-hoc claim task**

</td><td>

1.  From the Tasks list, select **Add claim task**.
2.  Fill in the required fields.
3.  Select **Save**.


</td></tr><tr><td id="d63869e303">

**To submit a reserve or payment amount for approval**

</td><td>

Select **Approve** to approve or **Reject** to reject the reserve or payment amount.1.  In Coverages and financials, for a reserve or payment in the Claim coverage list, select **Pending**.
2.  Select **Submit**.


</td></tr><tr><td id="d63869e332">

**To refer a claim for fraud evaluation**

</td><td>

Select **Send to SIU**.

</td></tr><tr><td id="d63869e344">

**To submit a claim settlement decision**

</td><td>

1.  Select **Settle claim**.
    -   Select **Approve claim** to approve the claim and send for fulfillment.
    -   Select **Deny claim** to reject the settlement.
2.  Enter comments for the settlement decision.
3.  Select **Submit**.


</td></tr></tbody>
</table>5.  Within a task, in the **Work notes** field, enter any comments that are related to your findings.

    Manually posted comments and system-generated work notes add to the Activity stream for the task and claim case.


## Result

Depending on the current stage of the case:

-   When the adjuster accepts the task, the task status sets to Work in progress.
-   When the adjuster submits a reserve or payment, if the amount is within their authorization limit, it is auto approved.
-   If the adjuster settles the claim, the claim case automatically closes, with the case status set as Closed complete, and claim stage moved to Closed rejected. System-generated work notes stating the rejection automatically add to the Activity stream for the task and claim case.
-   If one of the adjuster related tasks is approved, a task triggers to the claim processor to close the case. System-generated work notes stating the approval automatically add to the Activity stream for the task and claim case.

**Related topics**  


[Generate and view a claim's fraud score](view-claim-fraud-score.md)

[View a claim's summary](../concept/view-claim-summary.md)


---
title: Work on personal claim adjuster tasks
description: An adjuster can review a claim to verify documents, evaluate claim coverages, determine claim payment details, and approve settlement for a claim.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Adjuster tasks, Use, Personal Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on personal claim adjuster tasks

An adjuster can review a claim to verify documents, evaluate claim coverages, determine claim payment details, and approve settlement for a claim.

## Before you begin

Role required: sn\_ins\_claim\_pers.auto\_adjuster

**Important:** To access the Claim workspace, Fraud score, and Summary adjuster workspace related tabs, you must activate the CSM default record page. By default, the page is set to inactive. To determine the default page for displaying records in CSM Configurable Workspace, see [CSM Configurable Workspace record pages](https://www.servicenow.com/docs/access?context=csm-config-workspace-record-pages&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

Update and close the adjuster tasks of the claim case.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Open the task one of the following ways.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d113851e81">

Option

</th><th align="left" id="d113851e84">

Steps

</th></tr></thead><tbody><tr><td id="d113851e90">

**From the landing page**

</td><td>

Select a task from the All open claims list.

</td></tr><tr><td id="d113851e99">

**From the Personal auto claim adjuster tasks list**

</td><td>

1.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).
2.  In the **Lists** tab, under **Personal auto claim adjuster tasks**, select **All**.
3.  In the list, select the task that you want to open.


</td></tr></tbody>
</table>3.  Finish the work that is required to complete the evaluation or settlement task in your claims system.

4.  Work on the adjuster task by completing various actions from the claim workspace.

<table id="claim-workspace-actions-table"><thead><tr><th align="left" id="d113851e150">

Claim task

</th><th align="left" id="d113851e153">

Claim workspace actions

</th></tr></thead><tbody><tr><td id="d113851e162">

**To add a document verification task**

</td><td>

1.  Select **Add document verification task**.
2.  Fill in the required fields.
3.  Select **Save**.


</td></tr><tr><td id="d113851e192">

**To verify a document**

</td><td>

Select **Verify** to verify the document or **Reject** to reject the submitted document for verification.

</td></tr><tr><td id="d113851e207">

**To add claim coverage**

</td><td>

1.  Select **Add coverage**.
2.  Select Claim coverage and any of the following required:
    -   Claim property
    -   Claim participant
3.  Select **Save**.


</td></tr><tr><td id="d113851e243">

**To add a reserve or payment**

</td><td>

1.  In Coverages and financials, select one from the Claim coverage list:
    -   **Add reserve**
    -   **Add payment**
2.  Fill in the required fields.
3.  Select **Save**.


</td></tr><tr><td id="d113851e277">

**To add an ad-hoc claim task**

</td><td>

1.  From the Tasks list, select **Add claim task**.
2.  Fill in the required fields.
3.  Select **Save**.


</td></tr><tr><td id="d113851e304">

**To submit a reserve or payment amount for approval**

</td><td>

Select **Approve** to approve or **Reject** to reject the reserve or payment amount.1.  In Coverages and financials, for a reserve or payment in the Claim coverage list, select **Pending**.
2.  Select **Submit**.


</td></tr><tr><td id="d113851e333">

**To refer a claim for fraud evaluation**

</td><td>

Select **Send to SIU**.

</td></tr><tr><td id="d113851e345">

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


[Generate and view a claim's fraud score](../../fso-commercial-lines-claims/task/view-claim-fraud-score.md)

[View a claim's summary](../../fso-commercial-lines-claims/concept/view-claim-summary.md)


---
title: Work on Insurance claims adjuster tasks
description: Review a claim to verify the documents, evaluate the claim coverages, determine the claim payment details, and approve the settlement for a claim.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on Insurance claims adjuster tasks

Review a claim to verify the documents, evaluate the claim coverages, determine the claim payment details, and approve the settlement for a claim.

## Before you begin

Role required: sn\_ins\_gen\_claim.adjuster

**Important:** To access the Claim workspace, and Summary adjuster workspace related tabs, you must activate the CSM default record page. By default, the page is set to inactive. To determine the default page for displaying records in CSM Configurable Workspace, see [CSM Configurable Workspace record pages](https://www.servicenow.com/docs/access?context=csm-config-workspace-record-pages&version=australia&pubname=australia-customer-service-management&ft:locale=en-US) .

## About this task

This procedure references service definitions and products that are used in the included travel insurance claim line of business. Your workflow may vary depending on your configuration.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Open the task in one of the following ways.

<table id="choicetable_kfd_jfb_vcc"><thead><tr><th align="left" id="d87976e93">

Option

</th><th align="left" id="d87976e96">

Steps

</th></tr></thead><tbody><tr><td id="d87976e102">

**From the landing page**

</td><td>

From the All open claims list, select a task.

</td></tr><tr><td id="d87976e111">

**From the Insurance claim adjuster task list**

</td><td>

-   Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).
-   On the **Lists** tab, under **Insurance claim adjuster tasks** \(or the list category that is specific to your custom workflow\), select **All**.
-   In the list, select the task that you want to open.


</td></tr></tbody>
</table>3.  Work on the adjuster task by completing actions from the claim workspace.

<table id="choicetable_ozd_rgb_vcc"><thead><tr><th align="left" id="d87976e156">

Claim task

</th><th align="left" id="d87976e159">

Claim workspace actions

</th></tr></thead><tbody><tr><td id="d87976e165">

**Add a document verification task**

</td><td>

-   In Tasks, open the task drop-down list and select **Add document verification task**.
-   On the form, fill in the fields.
-   Select **Save**.


</td></tr><tr><td id="d87976e192">

**Verify a document**

</td><td>

In a Submitted document task, select **Verify** to verify the submitted document.

</td></tr><tr><td id="d87976e204">

**Reject a document**

</td><td>

In a Submitted document task, select **Reject** to reject the submitted document.

</td></tr><tr><td id="d87976e216">

**Add claim coverage**

</td><td>

-   In Coverages and financials, select **Add coverage**.
-   On the form, fill in the fields.
-   Select **Save**.


</td></tr><tr><td id="d87976e244">

**Add a reserve or payment**

</td><td>

-   In Coverages and financials, select one from the Claim coverages list:
    -   **Add reserve**
    -   **Add payment**
-   On the form, fill in the fields.
-   Select **Save**.


</td></tr><tr><td id="d87976e278">

**Add an ad-hoc claim task**

</td><td>

-   In Tasks, select **Add claim task**.
-   On the form, fill in the fields.
-   Select **Save**.


</td></tr><tr><td id="d87976e305">

**Submit a reserve or payment amount for approval**

</td><td>

If the reserve or payment amount is above your approval threshold, an approval task is created and assigned to your manager when you submit the amount.

</td></tr><tr><td id="d87976e317">

**Submit a claim settlement decision**

</td><td>

-   Select **Settle**.
-   -   Select **Approve claim** to approve the claim and send for fulfillment.
-   Select **Deny claim** to reject the settlement.
-   Enter comments for the settlement decision.
-   Select **Submit**.


</td></tr></tbody>
</table>4.  Within a task, in the **Work notes** field, enter any comments that are related to your findings.

    Manually posted comments and system-generated work notes add to the activity stream for the task and claim case.


## Result

-   When you accept the task, the task status is set to Work in progress.
-   When you submit a reserve or payment amount within your authorization limit, it’s auto-approved.
-   If a claim validation is rejected, the claim case closes with a case status of Closed rejected. System-generated work notes about the rejection are automatically added to the activity stream for the task and claim case.
-   If you settle the claim, the claim case automatically closes, with the case status set as Closed complete.


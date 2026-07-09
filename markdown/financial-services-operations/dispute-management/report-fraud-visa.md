---
title: Report fraud
description: Report potential fraud on a transaction to the Visa card network. If potential fraud was flagged for a transaction during manual investigation, a transaction includes the fraud reporting task within the workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/report-fraud-visa.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigate, Processing a Visa dispute, Managing disputes integrated with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Report fraud

Report potential fraud on a transaction to the Visa card network. If potential fraud was flagged for a transaction during manual investigation, a transaction includes the fraud reporting task within the workflow.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the transaction ID from the playbook.

    The **Investigate** stage is initiated for the transaction.

6.  Select the **Report fraud** activity.

7.  Fill in the required fields in the form and any other information that you have gathered.

8.  In the **Remarks** field, enter any comments.

    This step is optional.

9.  Select **Submit fraud**.

10. Select **Close task**.


## Result

Depending on the policy rule, the task moves to the next activity. The following activities are displayed based on the policy rule.

|Policy rule|Activity displayed|
|-----------|------------------|
|Immediate Provisional Credit|Issue provisional credit|
|Immediate Final Credit|Set recovery option|
|No Credit|Alert merchant task|
|Deny|Case is denied|

**Parent Topic:**[Investigate stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-stage.md)


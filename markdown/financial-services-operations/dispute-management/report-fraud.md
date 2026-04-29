---
title: Report fraud
description: Report potential fraud on a transaction to a card network. If potential fraud was flagged for a transaction during manual investigation, a transaction includes the Fraud reporting task within the workflow
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigation, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Report fraud

Report potential fraud on a transaction to a card network. If potential fraud was flagged for a transaction during manual investigation, a transaction includes the Fraud reporting task within the workflow

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  The **Investigate** stage is initiated for the transaction.

8.  Select the **Report fraud** activity.

9.  On the form, fill in the required fields and any other related information that you have gathered.

10. In the  **Remarks** field, enter any comments.

11. Select **Close task**.


## Result

Depending on the policy rule, the task moves to the next activity. The following activities are displayed based on the policy rule.

|Policy rule|Activity displayed|
|-----------|------------------|
|Immediate Provisional Credit|Issue provisional credit|
|Immediate Final Credit|Set recovery option|
|No Credit|Alert merchant task|
|Deny|Case is denied|

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)


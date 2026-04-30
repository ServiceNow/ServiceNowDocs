---
title: Report fraud
description: Report potential fraud on a transaction to a card network. If the dispute category is Fraud, the Report fraud activity is displayed for a transaction.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-03"
reading_time_minutes: 1
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Report fraud

Report potential fraud on a transaction to a card network. If the dispute category is **Fraud**, the **Report fraud** activity is displayed for a transaction.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![List icon.](../../../common/image/icon-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level of the playbook **Processing** tab, select the transaction ID.

7.  The **Investigate** stage is initiated for the transaction.

8.  Select the **Report fraud** activity.

9.  Review the dispute amount and financial transaction for fraud reporting.

10. In the  **Remarks** field, enter any comments.

11. Select **Close task**.


## Result

Depending on the policy rule, the task moves to the next activity. The following activities are displayed based on the policy rule.

|Policy rule|Activity displayed|
|-----------|------------------|
|Immediate Provisional Credit|[Issue provisional credit](provide-provisional-credit-to-customer.md)|
|Immediate Final Credit|[Set recovery option](recovery-option-for-final-credit.md)|
|No Credit|[Review participating merchant alerts](alert-merchant-regarding-dispute.md)|
|Deny|Case is denied|

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)


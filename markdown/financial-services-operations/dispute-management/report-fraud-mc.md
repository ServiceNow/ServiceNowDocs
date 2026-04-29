---
title: Report fraud to card network
description: Report potential fraud on a transaction to a card network.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigate, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Report fraud to card network

Report potential fraud on a transaction to a card network.

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

7.  Select the **Report fraud to card network** task in **Dispute Workspace**.

8.  On the form, fill in the required fields and any other related information that you have gathered.

9.  Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

10. Select **Submit fraud**.

    **Note:** If an error message displays in the **Activity stream**, the **Submit fraud** button displays again to retry.

11. Select **Close task**.


## Result

Depending on the policy rule, the transaction moves to the next task. The following tasks are displayed based on the policy rule.

|Policy|Outcome|
|------|-------|
|Immediate provisional credit \(IPC\)|[Reverse provisional credit](reverse-provisional-credit-mc.md) or [Convert provisional credit to final credit](convert-provisional-credit-to-final-credit_mc.md)|
|Immediate final credit \(IFC\)|[Provide final credit to customer](provide-final-credit-mc.md)|
|No credit|[Alert merchant regarding dispute](alert-merchant-dispute-mc.md)|
|||

**Parent Topic:**[Processing a Mastercard dispute](../concept/processing-mastercard-dispute-case.md)


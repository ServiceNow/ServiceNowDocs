---
title: Investigate the dispute
description: The Investigate stage involves tasks related to pursuing chargeback and initiate investigation of the dispute.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Investigate, Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Investigate the dispute

The Investigate stage involves tasks related to pursuing chargeback and initiate investigation of the dispute.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

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

7.  Select whether to create a chargeback request in the **Pursue chargeback** drop-down list.

    -   **Yes**: Pursue a chargeback from the merchant. The transaction dispute continues through the dispute process workflow stages.
    -   **No**: Don’t pursue chargeback from the merchant. The dispute life-cycle ends and the next task is displayed based on the policy and the task moves to Closed Complete. For more information about tasks related to policy, see [About Financial adjustments in Mastercard disputes](../concept/financial-adjustments.md).
8.  Select **Add file** to attach supporting documents to the task.

    **Note:** You must upload a single `.zip` file whenever you submit documents to Mastercard.

9.  Select **Continue**.

    The case is submitted to the dispute manager for review and approval when the chargeback eligibility is **No** and the agent sets the **Pursue Chargeback** value to **Yes**. After the manager approves the task, the user agent can continue with the dispute.


## Result

If a chargeback is pursued, then the dispute life cycle continues and a dispute is initiated, else the life cycle ends.

**Parent Topic:**[Processing a Mastercard dispute](../concept/processing-mastercard-dispute-case.md)


---
title: Review ACH dispute return recommendation
description: Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review ACH dispute return recommendation

Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

Once the merchant analysis has been conducted and Nacha guidelines have been analyzed, a final action must be taken on the ACH dispute. You can deny a refund, file a refund, or follow up with the Originating Depository Financial Institution \(ODFI\) before making a final decision.

**Note:** When the ACH disputes resolution agentic workflow in Now Assist for FSO is enabled, the ACH dispute return recommendation AI Agent is available to assist you at this step. See [Review ACH dispute return recommendation](../../fso-now-assist/task/recommendation-ai.md) for more information.

Ensure that your assignment logic, such as Advanced Work Assignment \(AWA\), is configured so that when a dispute case is assigned to an agent, all associated transactions are automatically assigned to the same agent. This alignment helps maintain consistency and speeds up case resolution.

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

7.  In **Open Tasks**, select **Review ACH dispute return recommendation**.

8.  In ACH dispute return recommendation action, select the final action:

    1.  **Deny**: The ACH dispute is determined to be invalid and is denied. The provisional credit is either canceled or reversed, depending on whether the credit has already been issued.
    2.  **File return**: The ACH dispute is determined to be valid and meets eligibility for return. A refund is initiated.
    3.  **Follow up ODFI**: More information is required from the ODFI before a refund can be either denied or issued.
9.  Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)


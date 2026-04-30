---
title: Evaluate merchant analysis
description: Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Evaluate merchant analysis

Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

**Note:** When the ACH disputes resolution agentic workflow in Now Assist for FSO is enabled, the Merchant Analysis AI agent is available to assistNow Assist for FSO you at this step. See [Merchant analysis with AI agent](../../fso-now-assist/task/merchant-analysis-ai.md) for more information.

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

7.  In **Open Tasks**, select **Evaluate merchant analysis**.

8.  In **Merchant analysis action**, indicate the final action:

    -   **Credible**: Upon analysis, the merchant is determined to be credible.
    -   **Not Credible**: Upon analysis, the merchant is determined to be not credible.
9.  Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)


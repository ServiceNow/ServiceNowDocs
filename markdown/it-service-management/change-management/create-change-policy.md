---
title: Create change approval policies
description: Use a change approval policy to define approvals that should be generated for your change.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating change approval policies, Use, Change Management, IT Service Management]
---

# Create change approval policies

Use a change approval policy to define approvals that should be generated for your change.

## Before you begin

Role required: admin or change manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; **Change Approval Policies**.

2.  Click **New** to create a new approval policy.

3.  Enter the **Name** of the policy.

4.  In the **Execution** field, select an option to determine the approach to execute your decision.

    -   **First decision that matches**: Uses the first matching decision in the ascending order of the value defined in the **Order** column of the **Decisions** list. The associated approval definition is applied.
    -   **Run all decisions that match**: Uses all matching decision and applies the associated approval definition.
5.  Click **Submit**.

6.  Select the policy you created.

7.  Add your decisions to the policy and click **Submit**.


## What to do next

To add additional policy inputs and decisions, see [Create Policy inputs](create-policy-input.md) and [Create Decision records](create-decisions.md)..

-   **[Create policy inputs](create-policy-input.md)**  
Policy inputs are variable sources that you can use while evaluating a decision to determine the approval action. You can create multiple policy inputs to evaluate the decision created, and also access the change request table and any table change request references.
-   **[Create Decision records](create-decisions.md)**  
Decision records contain the conditions that you can use to determine the change approval action. Create decisions using condition builder when creating change approval policies.

**Parent Topic:**[Creating change approval policies](../concept/using-change-approval-policies-cf.md)


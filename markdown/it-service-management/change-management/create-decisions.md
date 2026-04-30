---
title: Create Decision records
description: Decision records contain the conditions that you can use to determine the change approval action. Create decisions using condition builder when creating change approval policies.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create change approval policies, Creating change approval policies, Using Change Management, Change Management, IT Service Management]
---

# Create Decision records

Decision records contain the conditions that you can use to determine the change approval action. Create decisions using condition builder when creating change approval policies.

## Before you begin

Role required: admin or change manager

You can create decisions to evaluate conditions that reference policy inputs and apply the associated approval definition. To create a decision, perform the following steps:

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; **Change Approval Policies**.

2.  Create a change approval policy or open an existing policy.

    For more information, see [Create change approval policy](create-change-policy.md).

3.  In the **Policy inputs** tab, create a policy input or update an existing record.

    For more information, see [Create a decision](create-policy-input.md).

4.  In the **Decisions** tab, open the default decision record.

5.  Copy and modify the decision record configuration or click **New** to create a new decision record.

6.  Provide a label in the **Label** field.

7.  In the **Answer** field, select an approval definition.

8.  Add any necessary filter conditions using the condition builder.

    These conditions determine the outcome of the policy. For example, to generate approvals at the Assess state that trigger an approval definition when risk is low, set the condition to **\[Change request.state\] \[is\] \[Assess\] AND \[Change request.Risk\] \[is\] \[Low\]**.

9.  Click **Submit**.


**Parent Topic:**[Create change approval policies](create-change-policy.md)


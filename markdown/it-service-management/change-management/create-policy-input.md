---
title: Create policy inputs
description: Policy inputs are variable sources that you can use while evaluating a decision to determine the approval action. You can create multiple policy inputs to evaluate the decision created, and also access the change request table and any table change request references.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create change approval policies, Creating change approval policies, Using Change Management, Change Management, IT Service Management]
---

# Create policy inputs

Policy inputs are variable sources that you can use while evaluating a decision to determine the approval action. You can create multiple policy inputs to evaluate the decision created, and also access the change request table and any table change request references.

## Before you begin

Role required: admin or change manager

You can create multiple policy input types. By default, the **change\_request** policy input of type **Reference** is available for all change types. This policy input provides access to the change request table and to any table change request references. For a normal change policy, an extra **manager\_approved** policy input of type **True/false** is available.

To define additional policy inputs, perform the following steps:

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; **Change Approval Policies**.

2.  Create a change approval policy or open an existing policy.

    For more information, see [Create change approval policy](create-change-policy.md)

3.  In the **Policy inputs** tab, click **New** to create a record.

    The **Name** and **Application** fields are auto-populated.

4.  Click the reference lookup icon for the **Type** field and choose a Type value.

5.  Enter a name in the **Label** field.

    The column name for the new record is populated in the **Column Name** field automatically.

6.  Depending on the value of the **Type** field, you can configure the other parameters for the policy input.

7.  Click **Submit**.


## What to do next

After you create a policy input, reference it within a decision.

**Parent Topic:**[Create change approval policies](create-change-policy.md)


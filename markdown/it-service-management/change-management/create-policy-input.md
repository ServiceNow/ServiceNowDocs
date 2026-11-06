---
title: Create policy inputs
description: Policy inputs are variable sources that you can use while evaluating a decision to determine the approval action. You can create multiple policy inputs to evaluate the decision created, and also access the change request table and any table change request references.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/create-policy-input.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create change approval policies, Creating change approval policies, Use, Change Management, IT Service Management]
---

# Create policy inputs

Policy inputs are variable sources that you can use while evaluating a decision to determine the approval action. You can create multiple policy inputs to evaluate the decision created, and also access the change request table and any table change request references.

## Before you begin

Role required: admin or change\_manager

You can create multiple policy input types. By default, the **change\_request** policy input of type **Reference** is available for all change types. This policy input provides access to the change request table and to any table change request references. For a normal change policy, an extra **manager\_approved** policy input of type **True/false** is available.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; **Change Approval Policies**.

2.  Create a change approval policy or open an existing policy.

    For more information, see [Create change approval policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-change-policy.md).

3.  On the **Policy inputs** tab, select **New**.

    The **Name** and **Application** fields are populated automatically.

4.  In the **Type** field, select the reference lookup icon and select a type.

5.  In the **Label** field, enter a name.

    The column name for the new record is populated in the **Column Name** field automatically.

6.  Configure the other parameters for the policy input, which depend on the value in the **Type** field.

7.  Select **Submit**.


## What to do next

After you create a policy input, reference it within a decision.

**Parent Topic:**[Create change approval policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-change-policy.md)


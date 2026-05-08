---
title: Create a sample allocation rule
description: You can create a sample expense allocation rule that allocates the cost of an incident to the department of the caller.
locale: en-US
release: australia
product: Expense Line
classification: expense-line
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Expense lines and expense allocations, Expense Line, IT Service Management]
---

# Create a sample allocation rule

You can create a sample expense allocation rule that allocates the cost of an incident to the department of the caller.

## Before you begin

To use expense allocation rules, activate the Cost Management application.

Role required: admin, financial\_mgmt\_admin, or financial\_mgmt\_user

## Procedure

1.  **Costs** &gt; **Administration** &gt; **Expense Allocation Rules**

2.  Click **New**.

3.  In **Name**, enter `Incident Caller Department`.

4.  In **Table**, select **Incident**.

5.  In **Allocation field**, click the control, expand the **Caller** element, and select a department.

6.  In **Percentage**, enter `100` to allocate all the expense to the caller's department.

7.  Select the **Active** check box.

8.  Click **Submit**.

    After an incident expense line is created, the allocation rule processes the expense line and generates an expense allocation linking the expense and amount to the caller's department. The expense is stored in the **Target** field on the Expense Allocation record.


**Parent Topic:**[Expense lines and expense allocations](../concept/c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Create an allocation rule](t_CreateAnAllocationRule.md)

[Automatic expense line creation](../concept/c_CreateExpenseLinesAutomatically.md)

[Create expense lines manually](t_CreateExpenseLinesManually.md)

[Delete an expense line](t_DeleteAnExpenseLine.md)

[Use a scripted allocation](t_UseAScriptedAllocation.md)

[bundle-itbm.r_CostManagement]


---
title: Create an allocation rule
description: Expense allocation rules enable you to associate expenses with an item, such as a user, group, or department.
locale: en-US
release: zurich
product: Expense Line
classification: expense-line
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Expense lines and expense allocations, Expense Line, IT Service Management]
---

# Create an allocation rule

Expense allocation rules enable you to associate expenses with an item, such as a user, group, or department.

## Before you begin

To use expense allocation rules, activate [Cost Management](https://www.servicenow.com/docs/access?context=r_CostManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US).

Role required: admin, financial\_mgmt\_admin, or financial\_mgmt\_user

## About this task

**Note:** Expense Allocations are generated through the out-of-the-box scheduled job, Process Expense Allocation.

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Administration** &gt; **Expense Allocation Rules**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|The allocation rule name.|
    |Table|The table to which the allocation rule is associated.|
    |Allocation field|The field on the table to populate with the expense allocation.|
    |Inherited|Check box that indicates whether the expense allocation is inherited.|
    |Active|Check box that indicates whether the expense allocation is available to use.|
    |Percentage|The percentage of the expense line allocated to the table and field combination. Not available if the **Advanced** check box is selected.|
    |Summary type|The expense allocation category: **Grow Business**, **Run Business**, or **Transform Business**. Categorizing expense allocations can be useful for reporting.|
    |Condition|The condition under which the expense allocation is applied. Not available if the **Advanced** check box is selected.|
    |Advanced|Check box that indicates whether to display the **Script** field.|
    |Script|The script field that determines expense allocations. This field is only available if the **Advanced** check box is selected.|

4.  Click **Submit**.


**Parent Topic:**[Expense lines and expense allocations](../concept/c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Automatic expense line creation](../concept/c_CreateExpenseLinesAutomatically.md)

[Create expense lines manually](t_CreateExpenseLinesManually.md)

[Delete an expense line](t_DeleteAnExpenseLine.md)

[Create a sample allocation rule](t_SampleAllocationRule.md)

[Use a scripted allocation](t_UseAScriptedAllocation.md)

[Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)


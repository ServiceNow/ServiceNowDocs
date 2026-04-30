---
title: Use a scripted allocation
description: Scripted allocations define custom allocation amounts and targets by executing a script.
locale: en-US
release: yokohama
product: Expense Line
classification: expense-line
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Expense lines and expense allocations, Expense Line, IT Service Management]
---

# Use a scripted allocation

Scripted allocations define custom allocation amounts and targets by executing a script.

## Before you begin

Role required: admin, financial\_mgmt\_admin, or financial\_mgmt\_user

## About this task

You can use scripted allocations to perform any of the following actions.

-   Allocate an expense to all cost centers based on the current head count in the cost center.
-   Query usage data to determine the allocation amount to assign to a target.
-   Track the business users that are consuming business services.

## Procedure

1.  Navigate to **All** &gt; **Costs** &gt; **Administration** &gt; **Expense Allocation Rules**.

2.  Select an expense allocation rule.

3.  Select the **Advanced** check box.

4.  Use the following concepts to build the script

    -   Query for target records and data to use for calculating the allocation amount.
    -   Create allocation records using the ExpenseAllocation API.
    The following variables are available during the script processing:

    -   **allocation**: expense allocation object used to create allocations.
    -   **expense**: GlideRecord for the expense\_line that is being processed.
    -   **rule**: GlideRecord for this rule.
    To create an allocation record, use the allocation object already instantiated in the script scope:

    ```
    allocation.createAllocation(targetGlideRecord, amount);
    ```


**Parent Topic:**[Expense lines and expense allocations](../concept/c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Create an allocation rule](t_CreateAnAllocationRule.md)

[Automatic expense line creation](../concept/c_CreateExpenseLinesAutomatically.md)

[Create expense lines manually](t_CreateExpenseLinesManually.md)

[Delete an expense line](t_DeleteAnExpenseLine.md)

[Create a sample allocation rule](t_SampleAllocationRule.md)


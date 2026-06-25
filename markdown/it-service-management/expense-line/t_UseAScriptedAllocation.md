---
title: Use a scripted allocation
description: Scripted allocations define custom allocation amounts and targets by executing a script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/expense-line/t\_UseAScriptedAllocation.html
release: australia
product: Expense Line
classification: expense-line
topic_type: task
last_updated: "2026-03-12"
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


**Parent Topic:**[Expense lines and expense allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/expense-line/c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Create an allocation rule]()

[Automatic expense line creation]()

[Create expense lines manually]()

[Delete an expense line]()

[Create a sample allocation rule]()


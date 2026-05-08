---
title: Automatic expense line creation
description: You can automatically create expense lines to facilitate the accurate reporting of expenses.
locale: en-US
release: australia
product: Expense Line
classification: expense-line
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Expense lines and expense allocations, Expense Line, IT Service Management]
---

# Automatic expense line creation

You can automatically create expense lines to facilitate the accurate reporting of expenses.

If enabled, the following processes generate expense lines automatically.

-   Active CI rate cards are processed monthly to generate expense lines for each CI in the rate card. If a CI relationship is changed, existing expense lines are not affected. Changes are reflected in the next scheduled expense line.
-   Active distribution costs are processed monthly to generate expense lines based on distribution rule targets.
-   Closed tasks on task rate cards are processed to generate expense lines.

Expense lines can also be imported from external systems or generated from scripts. To generate an expense from a server-side script, use the ExpenseLine API.

**Parent Topic:**[Expense lines and expense allocations](c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Create an allocation rule](../task/t_CreateAnAllocationRule.md)

[Create expense lines manually](../task/t_CreateExpenseLinesManually.md)

[Delete an expense line](../task/t_DeleteAnExpenseLine.md)

[Create a sample allocation rule](../task/t_SampleAllocationRule.md)

[Use a scripted allocation](../task/t_UseAScriptedAllocation.md)

[bundle-platcap.t_CreateCIRelationship]


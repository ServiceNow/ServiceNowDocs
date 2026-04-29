---
title: Create expense lines manually
description: You can create expense lines at a single level or in a hierarchy to better organize expense information.
locale: en-US
release: australia
product: Expense Line
classification: expense-line
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Expense lines and expense allocations, Expense Line, IT Service Management]
---

# Create expense lines manually

You can create expense lines at a single level or in a hierarchy to better organize expense information.

## Before you begin

Role required: admin, financial\_mgmt\_admin, or financial\_mgmt\_user

## About this task

Use a hierarchy if it makes sense for your organization. In the example below, the last two expense lines are a level under expense line number EXP0010001.

![Expense lines hierarchy](../image/ExpenseLinesInherited.png "Expense lines in a hierarchy")

## Procedure

1.  Navigate to **All** &gt; **Costs** &gt; **Expense Lines**.

2.  Open an expense line record, or click **New** to create a new expense line.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Number|The unique number identifying the expense line.|
    |Date|The date on which the expense line was created.|
    |Rate Card|The identification number of the rate card to which the expense line is associated.|
    |Rate type|The rate type that is considered during the expense line generation. This field is read-only.|
    |Source ID|The identification number of the item associated with the expense line. If this field is filled in, corresponding information is automatically added to the **Source** fields on this form.|
    |Amount|The monetary value of the item specified in the **Source ID** field. Enter a negative value to indicate a credit.|
    |Process date|The date the expense line is processed.|
    |Inherited|Check box that indicates whether the expense line is on another expense line.|
    |State|The current state of the expense line, either **Pending** or **Processed**.|
    |Summary type|The expense line category: **Grow Business**, **Run Business**, or **Transform Business**. Categorizing expense lines can be useful for reporting.|
    |Short description|A brief description of the expense line.|
    |Asset|The identification number of the asset associated with the expense line, if any.|
    |Fixed asset|Fixed asset that contains the asset in this expense line. A fixed asset is a container that holds one or more individual assets, including hardware or software assets. The system auto-populates this field with the appropriate fixed asset if the named **Asset** is contained within that fixed asset.|
    |Contract|The identification number \(not the contract number\) of the contract associated with the **Asset**, if any.|
    |User|The name of the user associated with the **Asset**, if any.|
    |Configuration Item|The name of the configuration item associated with the expense line, if any.|
    |Task|The identification number of the task associated with the expense line, if any.|
    |Cost center|The cost center financially responsible for the item identified in **Source ID**, if any.|


**Parent Topic:**[Expense lines and expense allocations](../concept/c_ExpenseLinesAndAllocations.md)

**Related topics**  


[Create an allocation rule](t_CreateAnAllocationRule.md)

[Automatic expense line creation](../concept/c_CreateExpenseLinesAutomatically.md)

[Delete an expense line](t_DeleteAnExpenseLine.md)

[Create a sample allocation rule](t_SampleAllocationRule.md)

[Use a scripted allocation](t_UseAScriptedAllocation.md)

[c_CreatingFixedAssets]


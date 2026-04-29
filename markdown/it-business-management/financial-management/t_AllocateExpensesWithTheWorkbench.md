---
title: Allocate expenses with the workbench - Legacy
description: If any of this information looks incorrect, go back to a previous stage and make the necessary modifications.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [The Allocation Review stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocate expenses with the workbench - Legacy

If any of this information looks incorrect, go back to a previous stage and make the necessary modifications.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  [Verify your allocation settings](t_ConfigureGeneralSettings.md) on the **Configuration** tab.

2.  Navigate to the **Review** stage of the workbench.

3.  Choose what kind of allocation lines you want to generate:

4.  Click **Allocate Expenses**.

    **Note:** If you are a non-analyst licensed customer, ensure that the number of accounts in each segment and the total number of accounts in the cost model is within the threshold values 4000 and 12000 respectively.


## Result

The system allocates the expenses, creates allocation lines, and changes the **State** field on the general ledger record to **Allocated**. The values of all allocation lines created from the allocation add up to the value of the general ledger expense. If no rules apply to the general ledger expense, no allocation lines are created and the state of the general ledger record remains **Unallocated**.

**Note:** The system rounds allocation lines to two decimal places. An allocation totaling $100.495 is rounded up to $100.50. An allocation totaling $100.494 is rounded down to $100.49. If an allocation is rounded down to $0.00, the system does not create an allocation line.

**Parent Topic:**[The Allocation Review stage - Legacy](../concept/c_TheAllocationReviewStage.md)


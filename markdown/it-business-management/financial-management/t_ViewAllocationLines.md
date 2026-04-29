---
title: View allocation lines
description: After you complete an allocation, you can view the allocation lines that the application created.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Expense allocation - Legacy, Allocations - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# View allocation lines

After you complete an allocation, you can view the allocation lines that the application created.

## Before you begin

Role required: cost\_transparency\_admin

## Procedure

1.  Open the allocation line that you want to modify through either of the following methods:

    -   To access an allocation through the general ledger that created it:
    1.  Navigate to **Financial Modeling** &gt; **General Ledger** &gt; **Groomed Expenses**.

    2.  Open the expense that generated the allocation you are looking for.

    3.  In the **Cost Allocations** related list, click the allocation number.

    -   To access an allocation from a list of all allocations:
    1.  Navigate to **Financials** &gt; **Cost Models** &gt; **Allocation Lines**.

    2.  Click the allocation number.

2.  Verify or change any of the editable fields on the form \(see table\).

3.  Click **Update**.

    ![An example allocation line](../image/Cost_allocation_form.png "An example allocation line")

    |Field|Description|
    |-----|-----------|
    |Amount|The amount of this allocation.|
    |Fiscal period|The [fiscal period](t_ViewFiscalPeriods.md) [fiscal period](t_ViewFiscalPeriods.md) this expense belongs in.|
    |GL Entry|The groomed expense from which this allocation line was derived.|
    |Final|If the allocation line was processed by a rule that is marked final or if no subsequent rule can process this allocation. Reports are run on final allocation lines.|
    |Bucket|The bucket that the allocation belongs to. This bucket is taken from the expense during allocation.|
    |Sub-bucket|The sub-bucket that the allocation belongs to. The sub-bucket is also taken from the expense during allocation.|
    |\[Dimensions\]|The segments in the hierarchy of segments. The segments fields that contain values are the segments that you specified in the allocation methods that processed the allocation. If more than one method processes an allocation, all the allocated segments specified in all the methods contain a value. To make a change, click the lookup icon next for each dimension and select the relevant record.|


**Parent Topic:**[Expense allocation - Legacy](../concept/c_ExpenseAllocation.md)


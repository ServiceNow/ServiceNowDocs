---
title: Create breakdown relationship
description: Define a breakdown relationship between required segments to view cost lines generated between the segments.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [The Cost Models tab, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create breakdown relationship

Define a breakdown relationship between required segments to view cost lines generated between the segments.

## Before you begin

Role required: cost\_transparency\_admin

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Cost Models** &gt; **All**.

2.  Click **New** in the Breakdown Relationships related list.

3.  On the form, fill in the fields.

<table id="table_svm_vqz_pgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Model

</td><td>

Cost model from the list.

</td></tr><tr><td>

X Segment

</td><td>

Segment name from the list.You can also create a new segment using the Segment Definitions form.

</td></tr><tr><td>

Y Segment

</td><td>

Segment name from the list.You can also create a new segment using the Segment Definitions form.

</td></tr><tr><td>

Run On Demand Only

</td><td>

Option to manually generate the cost line breakdowns on demand.By default, the flag is set to false, which means the allocation engine generates breakdowns for the related segments of the cost model. If the flag is true, then the allocation engine will not generate the cost line breakdowns.

</td></tr></tbody>
</table>4.  Click **Submit**.

    -   **Leftover calculation for breakdowns**

        The cost lines generated for the amounts coming to the segment indirectly from other segments, which are not part of a breakdown relationship with the segment, or by direct bucket allocations to the segment are the leftovers.

        If you want to calculate the leftovers for a breakdown, then set the system property **com.glide.financial\_management.generate\_breakdown\_leftovers** to true.

    -   **Run On Demand Only**

        Use the option to generate the cost lines breakdowns on demand. This option helps in optimal usage of the allocation engine runtime.

5.  To manually generate the cost lines for a breakdown, navigate to the **Breakdown Relationships** related list of the Financial Model form.

    1.  Select the check box next to the breakdown and click **Generate Breakdown Allocations** action from the **Action on selected rows** list.

    2.  Enter the fiscal period in the Generate Breakdown Allocations dialog box.

    3.  Click **OK**.

6.  To view the cost lines of the breakdown that you manually generated, navigate to the **Review** stage of the Financial Management workbench.

7.  Click the **View Cost Line Breakdowns** link of the breakdown.

    You can view the cost lines in the Cost Allocation Breakdown list.


**Parent Topic:**[The Cost Models tab](../concept/c_TheCostModelsTab.md)

**Related topics**  


[Prescriptive cost models for shared services and business applications](../concept/preconfigured-prescriptive-cost-models.md)

[Prescriptive cost models for business services and business capabilities](../concept/preconfigured-prescriptive-cost-models-two.md)

[View settings for each cost model](t_ViewSettingsForEachCostModel.md)

[Delete a cost model](t_DeleteACostModel.md)

[Compare cost models](t_CompareCostModels.md)

[Clone a cost model](t_CloneACostModel.md)


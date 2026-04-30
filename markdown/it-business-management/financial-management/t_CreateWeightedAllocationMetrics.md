---
title: Create weighted allocation metrics
description: You can create weighted metrics using an enhanced form or a standard form.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Allocation metrics, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create weighted allocation metrics

You can create weighted metrics using an enhanced form or a standard form.

## Before you begin

Role required: cost\_transparency\_admin

## About this task

The enhanced form provides a visualization that helps you understand the relationships between the various components of the metric. Use the enhanced form that opens by default.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Consumption Metrics** &gt; **Create Weighted Metric**.

2.  On the form, fill in the fields.

    A graphical representation of the weighted allocation appears in the **Metric Visualization** section. When you make changes to the form the graphic updates dynamically.

    ![Metric weight builder](../image/MetricWeightMapReview.png "Weighted metric builder")

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name of the metric.|
    |Allocation group|Group associated with this metric. The default group is ITSM.|
    |System metric|Metric created by the application in the workbench.|
    |Refresh frequency|Frequency at which the data is refreshed.|

<table id="table_dc3_hf3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocate to

</td><td>

Segment in the hierarchy to which allocations are processed.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Apply filter \(Cost Allocation\)

</td><td>

Check box to display the condition builder. Specify the criteria that the selected **Allocate to**segment field must be met for this metric to apply.The fields available for the first part of the condition depend on the table you select for **Allocate to**. The condition builder supports dot walking, so you can select fields on another table.

</td></tr></tbody>
</table><table id="table_exb_hf3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Weight table

</td><td>

The table used to weight the allocation amounts based on aggregations.

</td></tr><tr><td>

Reference to allocate from

</td><td>

The field on the weight table that refers to the **Allocate from** segment. This field is available when the **Enforce relationship** check box is selected.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Reference to allocate to

</td><td>

The field on the weight table that refers to the **Allocate to** segment.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Aggregate

</td><td>

The type of aggregation to perform on the records in the weight table. Select from the following options:-   **Count**: A count of the number of records in the weight table that meet the weight condition.
-   **Value of**: The value of the selected field.
-   **Sum**: The sum of the values in the table for the selected field.
-   **Average**: The average of the values in the table for the selected field.
-   **Min**: The minimum value in the table for the selected field.
-   **Max**: The maximum value in the table for the selected field.


</td></tr><tr><td>

Aggregate field

</td><td>

The field on the weight table that is used for the aggregate calculation. This field is available when any aggregate other than **Count** is selected.

</td></tr><tr><td>

Apply filter \(Weight Table\)

</td><td>

Check box to display the condition builder. If the condition must be met before the application can allocate expenses using the weight table.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Enforce intermediary segment|Option to enforce intermediary segment.|
    |Intermediary Segment|Segment that is identified as intermediary segment, which is not included in cost model hierarchy.|
    |Intermediary segment reference to weight table|Relationship of the intermediary segment with the**Allocate to** segment, defined and referenced in the weight table.|
    |Aggregate|Type of aggregation performed on the records in the weight table.|

<table id="table_a5s_gf3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce relationship

</td><td>

Limits the segments that this metric allocates to based on an existing relation to another segment.

</td></tr><tr><td>

Allocate from

</td><td>

The table from which allocations are processed. This field is available when the **Enforce relationship** check box is selected.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Relation type

</td><td>

The type of relationship between the **Allocate from** table and the **Allocate to** table.-   **Allocate from**: A reference from the **Allocate from** table to the **Allocate to** table.
-   **Allocate to**: A reference from the **Allocate to** table to the **Allocate from** table.
-   **Intermediary**: A reference from an intermediary table to both the **Allocate from** and **Allocate to** tables.


</td></tr><tr><td>

Relationship field from

</td><td>

The field on the **Allocate from** table to allocate from. This field is available when the **Enforce relationship** check box and the **Allocate from** relationship type are selected.

</td></tr><tr><td>

Relationship field to

</td><td>

The field on the **Allocate to** table to allocate from. This field is available when the **Enforce relationship** check box and the **Allocate to** relationship type are selected.

</td></tr><tr><td>

Apply filter \(Relationship\)

</td><td>

Condition must be met before the application can do one of the following actions:-   Allocate expenses using the **Allocate from** table if you select the **Allocate from** relationship type
-   Allocate expenses using the **Intermediary** table if you select the **Intermediary** relationship type
 Then select this check box to display the condition builder.

</td></tr><tr><td>

Intermediary table

</td><td>

Table that is used between the **Allocate from** and **Allocate to** tables to connect them. This field is available when the **Enforce relationship** check box and the **Intermediary** relationship type are selected.

</td></tr><tr><td>

Intermediary table field from

</td><td>

The field on the intermediate table that maps to the **Allocate from** table. This field is available when the **Enforce relationship** check box and the **Intermediary** relationship type are selected.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Intermediary table field to

</td><td>

Field on the intermediate table that maps to the **Allocate to** table. This field is available when the **Enforce relationship** check box and the **Intermediary** relationship type are selected.You can access fields in related tables and the reference to the chain of field names separated by dots can go on up to any number.

</td></tr><tr><td>

Allocate from table condition filter

</td><td>

Criteria that the records in the **Allocate from** table must meet for this metric to apply. These fields are available when the **Enforce relationship** check box, the **Allocate from** relationship type, and **Apply filter** check box are selected.

</td></tr><tr><td>

Intermediate table condition filter

</td><td>

The criteria that the records in the intermediate table must meet for this metric to apply. This field is available when the **Enforce relationship** check box, the **Intermediary** relationship type, and **Apply filter** check box are selected.

</td></tr><tr><td>

Preview weight map

</td><td>

Weight Map is generated for the selected metric and the fiscal period. The preview lists the weight map review with total number of weights and the last generated date and time.

</td></tr><tr><td>

Fiscal period choice list

</td><td>

The fiscal period from the fiscal calendar.

</td></tr><tr><td>

Segment choice list

</td><td>

The account in the rollup segment.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Enforce allocation from total weight|Check box to enable enforce allocation from total weight.|
    |Total weight table|Table from which the actual consumption values are retrieved.|

    |Field|Description|
    |-----|-----------|
    |View standard form|Switches between the advanced form and the standard form.|

    |Field|Description|
    |-----|-----------|
    |Cost Allocation Methods|The allocation methods that this rule uses to break down expenses.|
    |Cost Allocations|The allocation lines that this rule created.|

    **Note:** You cannot delete a rule that is referenced by a locked allocation line.

    **Enforce allocation from total weight** is an allocation metric based on capacity. As an IT financial analyst, you can also allocate cost where the total capacity of a service is greater than the sum of what is consumed. To enable this option, you must select the **Enforce allocation from total weight** check box in the **Total weight table** section. Select a total weight table to calculate the total weight of metric based on the total consumption capacity. The weighted metric allocates cost based on the total number of available units of consumption.

    **Note:** You can either enforce allocation relationship or enforce allocation from total weight. Enforce total weight if the total allocation is greater than the sum of the consumed values. Whereas, enforce allocation relationship works when the sum of all consumption values \(of all individual entities\) in the weight table adds up to a total capacity of 100%. For more information, see [Total weight support for allocations using weighted metric](../concept/c_RollupsForAllocations.md#total-weight-support-allocation).

    **Intermediary Segment** option: Use this option when you have a segment with large number of accounts that add to numerous allocation lines. Nevertheless, the intermediary segment is still considered for the amount to rollup through it for proper allocation. However, the segment identified as intermediary is not included in the hierarchy of cost model and its allocation lines are not generated.

    The option to identify a segment as an intermediary segment is just to exclude the segment in the generation of multiple cost lines. However, you should create a metric based on the relationship between the intermediary segment and the **Allocate to** segment to include the segment for accurate amount rollup. Based on the relationship the allocation engine creates the weight, and based on the weight the allocation lines are generated for the intermediary segment.

    You must create a cost allocation metric to process the weight of the intermediary segment that is referenced in the weight table. Two sets of weight maps are generated, one for the intermediary segment and another for the Allocate to segment.

3.  Click **Submit**.


## What to do next

To [preview the weight map](preview-weight-map.md) that you created, click the **Preview Weight Map** button.

**Parent Topic:**[Allocation metrics](../concept/c_AllocationMetrics.md)


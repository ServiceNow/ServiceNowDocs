---
title: Generate unit costs
description: Associate a unit cost metric with a segment of a cost model hierarchy to generate unit costs. The mapping helps to derive unit cost based on the allocation lines from the Financial Modeling application.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a cost model from Cost Model form - Legacy, Cost models - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate unit costs

Associate a unit cost metric with a segment of a cost model hierarchy to generate unit costs. The mapping helps to derive unit cost based on the allocation lines from the Financial Modeling application.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Navigate to **Financial Modeling** &gt; **Cost Models** &gt; **All**.

2.  To associate the unit cost metric to a segment or an account of a segment of the cost model, click open a cost model.

3.  Click the **Unit Cost Metrics** related list.

4.  Click **New**.

5.  On the form, fill in the fields.

<table id="table_hjd_3hk_zz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Model

</td><td>

Cost model from the list.

</td></tr><tr><td>

Unit Cost Segment

</td><td>

The cost model segment for which the unit cost is to be generated.

</td></tr><tr><td>

Unit Cost Metric

</td><td>

Unit cost metric that has been defined in the consumption/weight table.

</td></tr><tr><td>

Unit

</td><td>

Unit of measure for the unit cost.

</td></tr><tr><td>

Transactional table

</td><td>

Segment transactional table, which cannot be edited.

</td></tr><tr><td>

Include Bucket Info

</td><td>

Option to enable the bucket information in unit costs.By default, Include Bucket Info flag is set to False. If the flag is true, then the bucket information is populated in the bucket column of the Unit Cost \[itfm\_unit\_cost\] table.

</td></tr><tr><td>

Unit Cost Accounts filter

</td><td>

Accounts filtered based on a criteria.Unit costs are generated only for the filtered accounts.

</td></tr></tbody>
</table>6.  Click **Submit**.

7.  Select the unit cost metric and click **Generate Unit Cost Metrics**.

8.  Select the fiscal period in the Generate Unit Cost Metrics pop-up that appears.

    The engine has run the allocations already for the fiscal periods that appear in the list.

9.  Click **OK**.

10. To see the unit costs, navigate to **Financial Modeling** &gt; **Cost Model Lines** &gt; **Unit Costs**.

    The unit costs are generated and populated in the Unit Cost table. The unit costs are generated for all the filtered accounts of the Unit Cost Segment in the Unit Cost Account column of the unit cost table.

    Enabling **Include Bucket Info** check box gives you a visibility of the amount coming from different buckets. You can track the bucket-wise unit cost in the bucket and sub-bucket columns of the unit cost table.

    The table also shows the total cost and quantity. Based on the enforced relationship of the metric, you can further drill down from the account unit cost.


**Parent Topic:**[Create a cost model from Cost Model form - Legacy](t_CreateACostModel.md)


---
title: Configure service offering costing cost model - Legacy
description: Configure the service offering costing cost model to allocate expenses and generate bucket cost lines for services offered at each level.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Financial Management for licensed SPM users - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure service offering costing cost model - Legacy

Configure the service offering costing cost model to allocate expenses and generate bucket cost lines for services offered at each level.

## Before you begin

Role required: cost\_transparency\_analyst

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling for SPM** &gt; **Service Offering Costing Model**.

    The field values in the Financial Model – Service Offering Costing form are pre-populated. You can choose to enter a model owner and user group for the Service Offering Costing cost model. There is no data source for this cost model.

2.  On the form, update the required fields.

<table id="table_hzs_qc5_whb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost model.

</td></tr><tr><td>

Description

</td><td>

Short description of the cost model.

</td></tr><tr><td>

Model Owner

</td><td>

User who owns the cost model.

</td></tr><tr><td>

Data Source

</td><td>

Source of data for the cost model.This cost model has no data source, hence the field is non-editable.

</td></tr><tr><td>

User Group

</td><td>

Group of users who can access the cost model.

</td></tr><tr><td>

Include Sub-Bucket info

</td><td>

Option to show sub-bucket information. If selected, the generated cost lines and breakdown lines hold sub-bucket information.

</td></tr></tbody>
</table>3.  Click **Update**.

4.  To run cost allocations, click **Allocate Expenses** button.

    **Note:** If you are a non-analyst licensed customer, ensure that the number of accounts in each segment and the total number of accounts in the cost model is within the threshold values 4000 and 12000 respectively.

    Use this option to run cost allocation from the cost model form and not necessarily from the workbench.

    1.  Select the fiscal period in the Allocate Expense dialog box.

    2.  Click **OK**.

        The allocation engine runs to generate cost allocations for the selected fiscal period. The engine does cleansing and bucketing. It allocates the expenses and creates allocation lines. However, if the cost model has no data source, the engine ignores the cleansing and bucketing stages and creates allocation lines.

5.  To generate cost lines for leaf buckets associated to the cost model, click **Generate Bucket Cost** button.

    Use this option to generate bucket amount lines for this cost model that has no data source. Cost lines are generated for each leaf bucket that has no further sub-buckets. Even if there is no amount in the bucket, the amount lines are generated in the Groomed General Ledger Data \[itfm\_gl\_data\_groomed\] table, populating zero in the **Amount** column. The table displays the bucket, sub-bucket, and amount associated with the cost model for the fiscal period that you selected.

    1.  Select the fiscal period in the Generate Bucket Cost dialog box.

    2.  Click **OK**.

        -   If there is no amount in a bucket, the allocation engine still generates a groomed line with zero expense for the selected fiscal period of the cost model.
        -   If there are pre-existing groomed lines with amounts in buckets for that fiscal period, then the engine does not overwrite those cost lines.
        You can edit the **Amount** column to enter the amount for each sub-bucket.

6.  To view the bucket amounts, navigate to **Financial Modeling for SPM** &gt; **Bucket Amounts**.

7.  To view the buckets associated to this cost model, navigate to **Financial Modeling for SPM** &gt; **Buckets**.

8.  To view the list of all service offering allocations, navigate to **Financial Modeling for SPM** &gt; **Service Offering Allocation Maps**.

9.  Use the **Allocate to Service Offering on Allocation Maps** metric and allocate expenses using weighted method.

    Calculate spend per service offering based on the consumption data stored in the service offering allocation maps table.

    To configure the service offering allocation map table and allocate expenses using weighted method, see [Allocate expenses using service offering allocation map](use-service-offering-allocation-maps.md).


**Parent Topic:**[Financial Management for licensed SPM users - Legacy](../concept/financial-management-spm.md)


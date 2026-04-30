---
title: Create a cost model from Cost Model form - Legacy
description: You can create multiple cost models to process allocations. Use the Cost Model form to configure all possible settings available to the cost model.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Cost models - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a cost model from Cost Model form - Legacy

You can create multiple cost models to process allocations. Use the Cost Model form to configure all possible settings available to the cost model.

## Before you begin

**Important:** This feature is available only when you own an ITBM Analyst license.

Role required: cost\_transparency\_admin

## About this task

You can select a cost model in [The Data Definition stage - Legacy](../concept/c_TheDataDefinitionStage.md) when you set up allocations. You can also [clone a cost model in the workbench](t_CreateACostModelSimple.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Cost Models** &gt; **All**.

2.  Click **New**.

3.  Fill in the form fields \(see table\).

<table id="table_j1x_dmg_qr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost model in accordance with its description, of up to 80 characters in length.

</td></tr><tr><td>

Description

</td><td>

Description of the cost model.

</td></tr><tr><td>

Used by Cost Allocation

</td><td>

Option to specify if the model is to be used for cost allocation.

</td></tr><tr><td>

Model Owner

</td><td>

The user who created the cost model.

</td></tr><tr><td>

Data Source

</td><td>

The source from where the data is taken.**Data Source** field is editable until financial model actions are not done.

 The application is preconfigured to point to the Budget Staged table as a data source for the Default Budget Cost Model as it is linked to ITFM Budget staged expenses.

 You also have the option not to select a data source. In such a case, the Workbench stages will not have the data cleansing stage as there is no financial data source to pull the expense lines from. Amounts would then be keyed in manually at the bucketing stage.

</td></tr><tr><td>

Used by Budgeting

</td><td>

Check box if the model is being used for budgets.

</td></tr></tbody>
</table><table id="table_lyj_kyh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fiscal Unit

</td><td>

Defines the fiscal unit to be a month, quarter, or a period based on the fiscal calendar.

</td></tr><tr><td>

Include Sub-Bucket info

</td><td>

If enabled, the generated cost lines and breakdown lines hold sub-bucket information.

</td></tr><tr><td>

User Group

</td><td>

The user group selected is associated with the cost model. This restricts access to the cost model by other user groups that are not associated with the user group of type ITFM.Users with the cost\_transparency\_analyst role can access default cost model and the cost model associated to their user group only.

 Users with cost\_transparency\_admin and system administrator roles can access all the cost models, including the default cost model.

 If the **Used by Budgeting** check box is enabled for the cost model, then users with appropriate budgeting role can view all the budget models.

 If the cost model is used for purposes of both budgeting and generating cost allocation lines, that is, if **Used by Cost Allocation** and **Used by Budgeting** check boxes are enabled, then all users can access the cost model.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  To run cost allocations, click **Allocate Expenses** button.

    **Note:** If you are a non-analyst licensed customer, ensure that the number of accounts in each segment and the total number of accounts in the cost model is within the threshold values 4000 and 12000 respectively.

    Use this option to run cost allocation from the cost model form and not necessarily from the workbench.

    1.  Select the fiscal period in the Allocate Expense dialog box.

    2.  Click **OK**.

        The allocation engine runs to generate cost allocations for the selected fiscal period. The engine does cleansing and bucketing. It allocates the expenses and creates allocation lines. However, if the cost model has no data source, the engine ignores the cleansing and bucketing stages and creates allocation lines.

6.  To download the cost model, click **Download Cost Model** button.

    You can download the cost model for uploading it to, or deploying it in another instance to do cost modeling in a different pre-production environment. You can later move the cost model to other production environments.

    With the ability to download the cost model you can also download all its related tables and the related elements such as segment definition and hierarchy, buckets, cleansing and grooming conditions, bucket allocations, rollups and rollup overrides, and consumption metrics.

7.  To generate cost lines for leaf buckets associated to the cost model, click **Generate Bucket Cost** button.

    Use this option to generate bucket amount lines for this cost model that has no data source. Cost lines are generated for each leaf bucket that has no further sub-buckets. Even if there is no amount in the bucket, the amount lines are generated in the Groomed General Ledger Data \[itfm\_gl\_data\_groomed\] table, populating zero in the **Amount** column. The table displays the bucket, sub-bucket, and amount associated with the cost model for the fiscal period that you selected.

    1.  Select the fiscal period in the Generate Bucket Cost dialog box.

    2.  Click **OK**.

        -   If there is no amount in a bucket, the allocation engine still generates a groomed line with zero expense for the selected fiscal period of the cost model.
        -   If there are pre-existing groomed lines with amounts in buckets for that fiscal period, then the engine does not overwrite those cost lines.
        You can edit the **Amount** column to enter the amount for each sub-bucket.

8.  To create model hierarchy using the interactive user interface, click **Build segment hierarchy** related link.

    Add new segments to the hierarchy or remove segments from the cost model per your requirements.

9.  To replace the top segment of the selected cost model that you want to clone:

    1.  Click the **Clone Model and Replace Top Segment** related link.

    2.  Select a segment from the choice list of the **Clone Model and Replace Top Segment** pop-up and click **OK**.

        You can replace the top segment in the cost model with another segment of your choice. Segments that have not been used in the cost model are available for you to choose to replace the top segment of the cost model. The replacing segment is from the available segments but has not been already used in the current cost model segment hierarchy. The selected segment replaces the existing top segment and will not be an addition to the existing segment levels in the hierarchy. Replacing the top segment enables you to configure the cost model specifically for the organizational structure of your enterprise.

        **Note:** The rules such as bucket assignments, rollups, rollup overrides, breakdown relationship, unit metrics, sibling relationship, and GL segment configured for the original segment become invalid for the replaced segment. Hence, you must set these rules for the replaced top segment.


## What to do next

The buckets that use this cost model are shown in the Buckets related list.

You can also [create an account bucket](t_CreateBuckets.md).

Map a unit cost metric to a segment of a cost model to [generate unit costs](generate-unit-costs.md).

The breakdown relationship to explicitly generate breakdown cost lines in the itfm\_allocation\_breakdown table for a given segment-segment mapping are shown in the [Breakdown Relationships](t_CreateBreakdownRelationship.md) related list.

You can also [define a sibling relationship](define-sibling-rollup-relationship.md) to roll up accounts at the sibling level.

-   **[Generating controlled cost lines](../concept/generating-controlled-cost-lines.md)**  
Generating controlled cost lines helps you to control the allocation lines that are required for your business needs.
-   **[Generate unit costs](generate-unit-costs.md)**  
Associate a unit cost metric with a segment of a cost model hierarchy to generate unit costs. The mapping helps to derive unit cost based on the allocation lines from the Financial Modeling application.
-   **[Define a sibling rollup relationship](define-sibling-rollup-relationship.md)**  
Define a relationship to roll up amounts to accounts in the sibling segments. You can roll up the expenses to any account in the hierarchy, not restricting to the immediate parent or grandparent in the hierarchy.
-   **[Prerequisites to modify data source of a cost model](../reference/transition-data-source-cost-model.md)**  
Clean the cost model of its existing data source and all the data collected and accumulated in the associated tables. Follow the steps to seamlessly change the data source.

**Parent Topic:**[Cost models - Legacy](../concept/c_CostModel.md)

**Related topics**  


[Choose a cost model - Legacy](t_ChooseACostModel.md)

[Cost model hierarchy - Legacy](../concept/c_SegmentHierarchy.md)


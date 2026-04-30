---
title: Clone a cost model in the workbench
description: Use the preconfigured cost models or clone one from the base cost models for your financial model activities. By cloning you can map your financial data source to the cost model as per your business requirements without affecting the original cost model.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [The Data Definition stage, Financial Management workbench, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Clone a cost model in the workbench

Use the preconfigured cost models or clone one from the base cost models for your financial model activities. By cloning you can map your financial data source to the cost model as per your business requirements without affecting the original cost model.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

**Important:**

-   This feature is available only when you own an ITBM Analyst license.
-   If you are upgrading from a previous version to Xanadu, by default, the **Generate Controlled Cost Lines** option is enabled on the new model and the **Generate GL Expense Lines** option is disabled on the new model irrespective of whether the options were disabled or enabled in the base model. These options are not editable and do not appear on the default view of the Cost Model View page.

## About this task

You can select a preconfigured basic cost model or clone a cost model from the **Data Definition** stage of the **Workbench** or from the **Cost Models** tab.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Workbench**.

2.  Do one of the following to access the basic cost model interface:

    -   Select a cost model from the **Cost Model** choice list in the **Working Set** region of the **Data Definition** stage, and click the **Clone this cost model** \(![Clone this model icon](../image/ClonethisCostModel.png)\) icon.

    -   Click the **Cost Models** tab, select the base cost model, and click the **Clone Cost Model** button or the **Clone this cost model** \(![Clone this model icon](../image/ClonethisCostModel.png)\) **Action** icon.
3.  On the form, fill in the fields.

<table id="table_mgp_2kh_hdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost model that you selected pre-populates in the field.

</td></tr><tr><td>

Description

</td><td>

Description of the cost model defaults.

</td></tr><tr><td>

Clone From

</td><td>

A cost model to clone the new one from.

</td></tr><tr><td>

Data source

</td><td>

The actual raw expense data table used for financial modeling activities. See [Financial data sources and field maps](../concept/data-sources.md). The base system options are:-   **Cost Plan Breakdown**: Maps to the raw expense data, where the actual cost and allocated cost are captured for a fiscal period in the cost plan breakdown \[cost\_plan\_breakdown\] table.
-   **General Ledger Staged**: Maps to the database column that refers to general ledger account expenses in the general ledger staged data \[itfm\_gl\_data\_staged\] table.
-   **No Data Source**: Option to manually enter the amounts in the cost model at the bucketing stage.


</td></tr></tbody>
</table>4.  Click the **Clone Cost Model** button.

    You can also [create a cost model on the cost model form](t_CreateACostModel.md).


**Parent Topic:**[The Data Definition stage](../concept/c_TheDataDefinitionStage.md)

**Related topics**  


[Choose a working set](t_ChooseAWorkingSet.md)

[Expense summary](../reference/r_ExpenseSummary.md)


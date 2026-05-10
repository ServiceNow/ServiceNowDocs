---
title: Define a table data source
description: Use the Table data source to retrieve data from internal ServiceNow tables or from external sources using Workflow Data Fabric.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Define the data source, Set up the Data Context Engine, Customer success, Customer Success Management, Customer Success Management]
---

# Define a table data source

Use the **Table** data source to retrieve data from internal ServiceNow tables or from external sources using Workflow Data Fabric.

## Before you begin

-   At least one context must be defined for each **Table** type data source with a valid mapping to the source reference table. See [Configure the Context Engine Mapper](../concept/account-lifecycle-define-context-engine-mapper.md) for details.
-   Role required: sn\_acct\_lc.customer\_success\_application\_admin

## About this task

By defining a **Table** data source, you can:

-   Retrieve data from internal and external tables \(See [Define a Workflow Data Fabric table data source](account-lifecycle-define-data-source-data-fabric-table.md) for details\).
-   Map Source IDs \(for example, User, Asset, Transaction\) to business entities such as Sold Products, Capabilities.
-   Use conditions such as Start and End dates to analyze trend data.

## Procedure

1.  Navigate to **All** &gt; **Data Context Engine** &gt; **Data Sources**.

2.  Select **** &gt; **Create New**.

3.  On the Data Source form, enter a name for the data source and fill in the following fields.

    See [Define the data source](../concept/account-lifecycle-define-data-source.md) for details on how to create a data source.

<table id="table_lt1_jy4_3hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Select **Table** from the drop down list. This option allows you to query data from internal and external tables.

</td></tr><tr><td>

Frequency

</td><td>

Select the frequency at which the data should be collected from the list.-   Daily
-   Weekly
-   Monthly
-   Quarterly


</td></tr><tr><td>

Aggregate

</td><td>

Select how the aggregate score should be calculated from the list.-   Average
-   Sum
-   Max
-   Min
-   Count: Use this option to get the total number of records in the Source table that match the filter conditions.


</td></tr><tr><td>

Source table

</td><td>

Select the table from which data is to be retrieved.**Note:** For external tables, see [Define a Workflow Data Fabric table data source](account-lifecycle-define-data-source-data-fabric-table.md)

</td></tr><tr><td>

Group by fields

</td><td>

Select one or two fields or dimensions by which the data in the Source table is to be grouped.

</td></tr><tr><td>

Conditions

</td><td>

Specify the filter conditions to be applied to the Source table while retrieving data. **Note:** A Timestamp or a Date field must be present in external Workflow Data Fabric tables to ensure that incremental data can be retrieved.

</td></tr><tr><td>

Source value

</td><td>

Select the field that should be used to calculate the aggregate score.**Note:** This is not applicable if the **Aggregate** type is **Count**.

</td></tr><tr><td>

Source reference

</td><td>

Select the source record used to resolve the **Group by fields**. This field is automatically populated if you selected a single reference type field in the **Group by fields** option.

</td></tr><tr><td>

Source reference resolver

</td><td>

You must update the **Source reference resolver** script and specify the fields that are to be mapped if the **Group by fields** contains:

-   Two fields \(maximum allowed\)
-   A non-reference field.
-   An external field.


</td></tr></tbody>
</table>4.  Select **Submit** to create this data source.


## Example

A few examples on how to configure the data source are given below:

-   **Total number of P1 cases**: To calculate the total number of P1 customer cases on a monthly basis, specify the following:
    -   Source table: customerservice\_case
    -   Conditions:
        -   Priority: 1
        -   Created between: Last month and current date
        -   Group by: sold\_product
        -   Aggregation: Count
        -   Source reference: Auto-populated to sold\_product
-   **Reassignment count sum**: To calculate the sum of reassignment count by Account and Product, select:
    -   Source table: customerservice\_case
    -   Conditions: Reassignment count is not 0
    -   Group by: Account, Product
    -   Aggregation: Sum
    -   Source value field: Reassignment count
    -   Source reference: sold\_product
    -   Source reference resolver: Specify the mapping between the **Account** and **Product** combination and the **Sold Product** table in the script as follows:
        -   `var account = groupByFieldValueMap[account]`
        -   `var product = groupByFieldValueMap[product]`

## What to do next

After defining the data source, the next step is to configure the context engine mapper. See [Configure the Context Engine Mapper](../concept/account-lifecycle-define-context-engine-mapper.md) for details.


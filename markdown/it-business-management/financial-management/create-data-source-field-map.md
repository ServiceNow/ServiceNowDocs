---
title: Create a data source field map - Legacy
description: Field maps create a reference between the data source columns and transaction columns.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Financial data import - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a data source field map - Legacy

Field maps create a reference between the data source columns and transaction columns.

## Before you begin

Role required: itfm\_plan\_analyst or cost\_transparency\_admin

## About this task

The transaction table is associated to a segment. Define a relationship between the data source and transaction fields to enable flexible data cleansing and bucket split.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Data Sources** &gt; **Setup**.

2.  Click to open a data source record.

3.  Click **New** in the **Financial Data Source Field Maps** tab to create a field map.

4.  On the form, fill in the fields.

<table id="table_cqx_cj4_dx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Auto populates the data source for which the field map is created.

</td></tr><tr><td>

Datasource field

</td><td>

Column on the data source table for field mapping.

</td></tr><tr><td>

Cleansed Column

</td><td>

Defines the mapping between the Data source table column and the Cleansed table column.If the field is None, data from the Data source table column is not copied during cleansing. For the existing General Ledger Staged data source mappings are preconfigured.

</td></tr><tr><td>

Used by cleansing

</td><td>

Check box to make this field map reference available for cleansing in financial modeling.

</td></tr><tr><td>

Segment name

</td><td>

Segment to map the transaction table.

</td></tr><tr><td>

Mapped to transaction field

</td><td>

Column on the transaction table for field mapping.

</td></tr><tr><td>

Used for Bucket split

</td><td>

Check box to make the field map reference available for cost bucket split when using the **Allocation Setup** tab of the workbench.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Financial data import - Legacy](../concept/c_FinancialManagementImport.md)


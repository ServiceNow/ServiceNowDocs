---
title: Add an FX Currency field to a table
description: Before using and configuring an FX Currency field, you first add it an existing table, or to a new one, in System Definition Tables.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up defaults required for FX Currency use, Configuring currency fields, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add an FX Currency field to a table

Before using and configuring an FX Currency field, you first add it an existing table, or to a new one, in **System Definition** &gt; **Tables.**

## Before you begin

Role required: admin

## About this task

For example, you create a new custom table, named `transactions`, that stores transactional information and contains an FX Currency field called `cost`.

## Procedure

1.  Follow the normal procedures to add a table, or access an existing table.

    To learn more about creating and modifying tables in an instance, see [Create a table](../../table-administration/task/t_CreateATable.md).

2.  In the **Columns** section, use the **Table Columns** embedded list to add columns to the table.

3.  In the **Column label** field, enter the column name.

    For example, `cost`.

4.  In the **Type** field, select **FX Currency** as the field type.

    ![FX Currency field](../images/fx-currency-table-field.png)

5.  As needed, enter other required parameters.

    **Note:** Do not change the **Max length** value for **FX Currency** in custom tables. **Max length** must be 32 \(default\).

6.  Click **Submit**.


**Parent Topic:**[Setting up defaults required for FX Currency use](../concept/setting-up-defaults-fx-currency-use.md)

**Related topics**  


[Add conversion rates using a custom rate table](custom-rate-table.md)

[Configuring FX Currency global settings](fx-currency-configure.md)

[Configuring FX Currency field behavior](../concept/configure-fx-currency-field-behavior.md)

[Update a Currency Instance record](updating-fx-currency-instance-record.md)


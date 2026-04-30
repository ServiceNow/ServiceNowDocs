---
title: Use multi-table data generator
description: The multi-table data generator enables you to create synthetic test data across multiple related ServiceNow tables in a single run. It automatically maintains referential integrity between tables and generates semantically consistent data based on scenarios you define.
locale: en-US
release: zurich
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-02-25"
reading_time_minutes: 1
breadcrumb: [Generate synthetic data, Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Use multi-table data generator

The multi-table data generator enables you to create synthetic test data across multiple related ServiceNow tables in a single run. It automatically maintains referential integrity between tables and generates semantically consistent data based on scenarios you define.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  From the Synthetic datasets tab, select**Generate dataset**.

3.  Select **Multi-table data generator**.

4.  Configure the dataset.

    1.  Name the dataset.

    2.  Enter the industry or department the data is being generated for.

5.  Select **Continue**.

6.  Select the tables and columns.

    ![Select table screen for using the multi-table data generator.](../image/nadk-select-tables.png)

7.  Select **next**.

8.  Configure the tables.

    For each selected table, fill in the form fields.

    |Field|Description|
    |-----|-----------|
    |Data type|Select Transaction for records that change over time. Select Master for reference data that rarely changes.|
    |Generation method|Synthetic generates new records. Existing pulls records already in the system. Use Existing for tables where you want to reference real users rather than create new ones.|
    |Filter conditions|Optional. Narrows the existing records to pull from. For example, active = true or department = IT.|
    |Record count|The number of records to generate for this table. The system supports up to 15 tables and 100 records per table per run.|

9.  Select **next**.

10. Define scenarios.

    Scenarios guide the content of the generated data. The system generates records that are semantically consistent with the scenario you describe across all related tables.

    ![The scenarios screen for the multi-table data generator.](../image/nadk-scenarios.png)

11. Select **next**.

12. Select **Generate preview**.

13. Select **Review summary**.

14. Select **Start generation**.

15. Select **Start**.



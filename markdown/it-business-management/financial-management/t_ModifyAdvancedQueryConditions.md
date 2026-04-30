---
title: Modify advanced query conditions
description: You can modify existing advanced query conditions, which define how expenses are added to buckets.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Grooming and cleansing conditions, Allocations, Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Modify advanced query conditions

You can modify existing advanced query conditions, which define how expenses are added to buckets.

## Before you begin

Role required: cost\_transparency\_admin

## About this task

**Note:** Grooming conditions are automatically created in the workbench.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Cost Models** &gt; **Grooming Conditions**.

    The resulting list of records is filtered to show only advanced query conditions.

2.  Click the grooming condition number to open it.

3.  Modify the fields on the form as appropriate \(see table\).

4.  Click **Update**.

    ![Example grooming condition](../image/Advanced_query_condition.png "Example grooming condition")

    |Field|Description|
    |-----|-----------|
    |Number|Auto-generated identification number for the bucket.|
    |Name|Descriptive name for the bucket.|
    |Priority|A code for the bucket that the system uses to identify it. Enter any alphanumerical code. Bucket codes cannot have duplicates.|
    |Description|If the bucket is not used for allocations.|
    |Bucket|The buckets that use this bucket as a parent. To create a sub-bucket, click **New** and fill out the fields on the form. The fields are the same as on the Bucket form, except that the **Parent bucket** field is visible.|
    |Condition Type|The type of grooming condition. Select **Advanced Query condition**.|
    |Table|The table containing the expenses that are filtered when put into the bucket. By default, the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table is selected. Do not change the table.|
    |Advanced bucketing condition|The condition that determines the financial data that must meet the advanced query condition. Use the condition builder to create the filter.|


**Parent Topic:**[Grooming and cleansing conditions](../concept/c_GroomingConditions.md)


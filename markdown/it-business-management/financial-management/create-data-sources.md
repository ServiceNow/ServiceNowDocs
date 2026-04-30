---
title: Create a financial data source - Legacy
description: Database columns referring to raw expense details must be identified to create a new data source in Financial Management.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Financial data import - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a financial data source - Legacy

Database columns referring to raw expense details must be identified to create a new data source in Financial Management.

## Before you begin

Role required: itfm\_plan\_analyst, admin, cost\_transparency\_admin

## About this task

Data sources are available for both Financial Modeling and Financial Planning applications.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Data Sources** &gt; **Setup**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kq1_mkg_cx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for the new data source record.

</td></tr><tr><td>

GL Account

</td><td>

Select the database column that refers to general ledger account expenses.

</td></tr><tr><td>

Amount

</td><td>

Select the database column that refers to actual expense amount.

</td></tr><tr><td>

Table

</td><td>

Select a database table with actual raw expense data.The **Table** field shows the source from where the financial data is retrieved. The source of the Financial Modeling application is no longer confined to the General Ledger Staged table alone, but can point to any table with financial transaction information. Any table in the platform can be used as long as the mandatory column requirements of representing amount, account number and date are met.

</td></tr><tr><td>

Currency

</td><td>

Select the database column that refers to currency values for the expenses.

</td></tr><tr><td>

Posting date

</td><td>

Select the database column that refers to the date when the expense was incurred.

</td></tr><tr><td>

Condition

</td><td>

Apply conditions to filter records.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Create field maps for the data source.

**Parent Topic:**[Financial data import - Legacy](../concept/c_FinancialManagementImport.md)


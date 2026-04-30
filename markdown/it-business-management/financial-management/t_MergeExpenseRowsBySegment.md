---
title: Merge expense rows by segment - Legacy
description: Merging expenses means taking the expenses that are associated with one segment record.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [The Data Cleansing stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Merge expense rows by segment - Legacy

Merging expenses means taking the expenses that are associated with one segment record.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## About this task

For example, you can take vendor ABC and associate expenses for this vendor with another segment record, like vendor XYZ. Effectively, you are changing the value for the Vendor field on the expenses from ABC to XYZ.

## Procedure

1.  Click one or more expense rows to select them.

    These rows can be referred to as the source expenses.

2.  Drag them onto another expense.

    This row can be referred to as the destination expense.

    The general ledger expense records for the source expenses are modified. The field that is modified is the segment you are currently working with, such as **Vendor**. The value for the field is changed to whatever value that field had on the destination expense.

    **Note:** When you merge expenses, you are only modifying the segment value, such as the vendor or the cost center. You are not modifying the account numbers associated with the general ledger expenses that comprise the expense row.

3.  Click the number of entries in the **Merge Count** column.

4.  To ignore a merged expense row, click the delete icon \(![The delete icon](../image/Delete_icon.png)\) next to the entry in the Merged Segments window.

    The expense row reappears in the list of all expenses.


**Parent Topic:**[The Data Cleansing stage - Legacy](../concept/c_TheDataCleansingStage.md)

**Related topics**  


[Review expenses before cleansing - Legacy](t_ReviewExpenses.md)

[Map segment records to expense rows - Legacy](t_MapSegmentRecordsToExpenseRows.md)

[Cleanse data - Legacy](t_CleanseData.md)


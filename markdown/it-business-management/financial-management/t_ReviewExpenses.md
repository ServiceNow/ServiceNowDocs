---
title: Review expenses before cleansing - Legacy
description: You can view several additional details about the expenses that you imported into the application.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [The Data Cleansing stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Review expenses before cleansing - Legacy

You can view several additional details about the expenses that you imported into the application.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## Procedure

1.  Select a segment from the **Attributes** choice list and review the data \(see table for column descriptions\).

    |Column|Description|
    |------|-----------|
    |Name|Name of the specific item in the selected segment, such as the name of the vendor or location.|
    |Amount|Amount of the imported expense associated with the item in the segment.|
    |Merge Count|Number of other expenses have been combined with the expense in that row. By default, the value for each record is **None**. When you merge expenses, the value changes to show the number of expenses merged.|
    |Mapped to|If the application can find a match between the name of the specific item in the selected segment, such as the same vendor or cost center, already in your instance. If the application cannot find a matching record, a new one is created when you cleanse the data.|

    Each expense row is not a record in the system, but rather an aggregate view of the expenses in the General Ledger Staged Data table that contain the same value for a segment that you select. For example, if you select the **Cost center** segment, each expense row is actually the sum of all the general ledger expenses that have the same cost center.

    ![Expenses in the data cleansing table](../image/IstanbulDataCleansingExpenses.png "Expenses in the data cleansing table")

2.  You can do any of the following on the list of expenses that appear:

    -   Filter the list of expense rows by typing text into the search field at the top-right of the list. The field searches the text in the **Name** column.
    -   Click the expense amount in the **Amount** column to view the expense records in the General Ledger Staged Data table that comprise the row.
    -   Click the delete icon \(![The delete icon](../image/Delete_icon.png)\) on the left of the expense to ignore the row. The expenses that you ignore here are not carried over to the next stage to be assigned to buckets.

**Parent Topic:**[The Data Cleansing stage - Legacy](../concept/c_TheDataCleansingStage.md)

**Related topics**  


[Merge expense rows by segment - Legacy](t_MergeExpenseRowsBySegment.md)

[Map segment records to expense rows - Legacy](t_MapSegmentRecordsToExpenseRows.md)

[Cleanse data - Legacy](t_CleanseData.md)


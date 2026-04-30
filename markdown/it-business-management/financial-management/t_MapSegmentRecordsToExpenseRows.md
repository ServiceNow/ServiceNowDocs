---
title: Map segment records to expense rows - Legacy
description: The application attempts to map the expense row to an existing record in the segment that you selected and gives you the option of creating a new record in the segment's table, as long as the expense row segment field has a value.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [The Data Cleansing stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Map segment records to expense rows - Legacy

The application attempts to map the expense row to an existing record in the segment that you selected and gives you the option of creating a new record in the segment's table, as long as the expense row segment field has a value.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## About this task

For example:

-   If you are cleansing data based on the Vendor segment, and the expense row's vendor is already in the Company \[core\_company\] table, the **Mapped to** column shows **Existing vendor**.
-   If the expense's vendor does not exist in the Company table, the **Mapped to** column shows **A new vendor will be created**. This message tells you that when you finally cleanse the data, the application creates a record for the vendor in the Company table.
-   If the expense **Vendor** field is empty, the expense does not show up in any expense rows when **Vendor** is selected.

If a match is found, you can view the matching record and make changes by clicking the edit icon \(![The edit icon](../image/Edit_icon.png)\) and modifying the form.

If no match is found and you want the system to create a record, simply leave the field as it is. Later, when you click **Cleanse Data**, the record is automatically created.

If no match is found and you do not want to create a record, you can manually associate an existing record with the expense:

## Procedure

1.  Click the lookup icon next to the value in the **Mapped to** column.

2.  Filter the list by typing keywords in the search field.

3.  Select an existing record from the list.

    ![Associating a vendor with an expense](../image/Segment_item_list.png "Associating a vendor with an expense")


**Parent Topic:**[The Data Cleansing stage - Legacy](../concept/c_TheDataCleansingStage.md)

**Related topics**  


[Review expenses before cleansing - Legacy](t_ReviewExpenses.md)

[Merge expense rows by segment - Legacy](t_MergeExpenseRowsBySegment.md)

[Cleanse data - Legacy](t_CleanseData.md)


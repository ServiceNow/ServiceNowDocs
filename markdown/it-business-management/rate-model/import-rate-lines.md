---
title: Import rate lines into a rate model
description: Use the import rate lines function to quickly add multiple rate lines from an export file into a rate model.
locale: en-US
release: australia
product: Rate Model
classification: rate-model
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rate Models, Project Portfolio Management, Strategic Portfolio Management]
---

# Import rate lines into a rate model

Use the import rate lines function to quickly add multiple rate lines from an export file into a rate model.

## Before you begin

Set the **glide.import\_set\_row.dynamically\_add\_fields** system property to true.

Role required: pps\_admin or it\_rate\_model\_admin

## About this task

After adding or updating rate lines in a file created using the [export function](export-rate-lines.md), you can import the rate lines from the file into the rate model.

**Note:** Rate lines fail to import in the following circumstances:

-   Overlapping effective dates for the same set of criteria values.
-   Criteria values with no matching data in the system. For example, a rate line might have Business Analyst as the **Role** criteria but that role does not exist in the system.
-   Rates in non-functional \(non-default\) currency but no corresponding [budget reference rates](../../project-management/concept/c_BudgetReferenceRates.md) for the required period exist in the system.

## Procedure

1.  Import rate lines from an import file into the rate model in one of the following ways:

    -   Navigate to **All** &gt; **Project Administration** &gt; **Rate Model** &gt; **Import Rate Line**.
    -   Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **Import Rate Line**.
    -   Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **All**, open a rate model record, and click the **Import Rate Line** related link.
2.  Click **Choose File** to select the import file.

3.  If you are importing from an Excel file containing multiple sheets, enter the sheet number that contains the data to import in the **Sheet number** field.

    **Note:** If you are importing from a CSV file, then the data from the last saved CSV file is considered for import irrespective of the specified sheet number.

4.  If the import file has a header row, enter the row number that has the header information in the **Header row** field.

5.  Click **Submit**.

6.  Click **Run Transform** to import the data.

    For more information, see Run an import.


## Result

-   New rate lines are appended to the rate lines list in the rate model.
-   Existing rate lines in the rate model are updated with the latest values.

**Parent Topic:**[Rate Models](../concept/rate-model.md)


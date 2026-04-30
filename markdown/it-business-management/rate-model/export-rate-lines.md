---
title: Export rate lines to a file
description: Export rate lines to a Microsoft Excel or CSV file to quickly update or add new rate lines and import them back into the rate model.
locale: en-US
release: zurich
product: Rate Model
classification: rate-model
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Rate Models, Project Portfolio Management, Strategic Portfolio Management]
---

# Export rate lines to a file

Export rate lines to a Microsoft Excel or CSV file to quickly update or add new rate lines and import them back into the rate model.

## Before you begin

Before exporting rate lines, define the criteria of the rate model by adding attributes to it. The downloaded export file includes columns corresponding to the selected attributes and the following default columns:

Role required: pps\_admin or it\_rate\_model\_admin.

## About this task

Besides [creating rate lines](create-rate-line.md) one at a time, you can add multiple rate lines into a rate model using the export and import rate lines functions.

-   Rate Model
-   Number
-   Start Date
-   End Date
-   Currency
-   Rate
-   Rate Type

    **Note:** The **Rate Type** column is available only if the **Rate type** check box is selected for the rate model.


The number of criteria columns depends on the number of attributes added in the rate model.

## Procedure

1.  Open a rate model by performing one of the following actions:

    -   Navigate to **All** &gt; **Project Administration** &gt; **Rate Model** &gt; **All**.
    -   Navigate to **All** &gt; **Time Sheets** &gt; **Rate Model** &gt; **All**.
2.  On the Rate Model form, select the **View Rate Lines** related link.

3.  Select the more actions icon \(![More actions icon](../image/MoreActionsIcon.png)\) and then select the **Export to CSV** option.

    A dialog box might prompt you to save or open the export file. By default, the file has the same name as the rate model. However, you can specify a different file name. Save the file either as a CSV file or Microsoft Excel \(.XLSX\) file.

    **Note:** Depending on your browser setting, the browser might automatically save the file to your Download folder.

4.  Open the downloaded file using your preferred application.

    Enter new rate lines or update the existing ones and save the file either as a CSV file or Microsoft Excel \(.XLSX\) file.


## Result

All rate lines in the rate model are exported to the file. If there is no rate line in the rate model, the file is an empty template containing only the column names in the first row.

## What to do next

[Import rate lines](import-rate-lines.md) from the file into a rate model.

**Parent Topic:**[Rate Models](../concept/rate-model.md)


---
title: Create a unique metric definition name
description: Specify the value formula in the sn\_grc\_metric\_definition in the required record table to create unique metric definition names to import data from an external source such as Watershed spreadsheets.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a unique metric definition name

Specify the value formula in the sn\_grc\_metric\_definition in the required record table to create unique metric definition names to import data from an external source such as Watershed spreadsheets.

## Before you begin

Role required: sn\_grc\_metric.admin

## About this task

Any external source that contains data must be imported into the metric definitions and each metric definition must have a unique name. The metric definition name can either use a single column from the spreadsheet or it can be a combination of multiple columns. This procedure uses the Operational Sustainability Integration with Watershed and the sn\_grc\_metric\_definition table as an example. You can specify the formulae in the sn\_grc\_metric\_definition table to create the unique metric definition names. The same procedure can be repeated for the other tables as well. The following tables are installed by default.

-   sn\_grc\_profile
-   sn\_grc\_profile\_type
-   sn\_grc\_metric\_definition

The following image shows the string and value columns from a sample spreadsheet.

![Sample strings and values from a spreadsheet.](../image/value-formula.png "Value formula combinations")

## Procedure

1.  Navigate to **All** &gt; **Metrics** &gt; **Metric Integrations**.

2.  Select **Watershed Integration**.

3.  In the Data Mappings section, select the data mapping for which you want to specify the formula.

4.  On the Required Records form, in the Value Formulas section select **New**.

5.  On the form, fill in the fields.

<table id="table_tcw_htp_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source table.

</td><td>

Name of the source table. This field is automatically set to **Watershed Data \[sn\_esg\_watershed\_data\]**.

</td></tr><tr><td>

Required record

</td><td>

Name of the table being modified.**Note:** In this procedure, the example used is the sn\_grc\_metric\_definition table.

</td></tr><tr><td>

Column

</td><td>

Column containing GHG protocol category.

</td></tr><tr><td>

Format

</td><td>

Format of the name. The choices are as follows-   **String**: Use this option to specify a text string.
-   **Value**: Use this option to use any value of the column.
-   **String+Value**: Use this option prepend text to beginning of column value.
-   **Value+String**: Use this option to append text to end of column value. Specify the text in the **String** field.


</td></tr><tr><td>

String

</td><td>

Text to use in the format.

</td></tr><tr><td>

Sequence

</td><td>

Specify the sequence of the formula. Multiple value formula under same required record will be concatenated following the sequence specified.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Using GRC: Metrics to provide data](../concept/using-grc-metrics.md)


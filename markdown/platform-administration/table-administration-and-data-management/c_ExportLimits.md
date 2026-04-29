---
title: Export limits
description: The platform provides a default upper limit for data exports.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Data export reference, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Export limits

The platform provides a default upper limit for data exports.

The purpose of the upper limit is to avoid creating performance issues when a table is excessively large. If you must export more records than the threshold permits, [Break up a large export](../task/t_BreakUpALargeExport.md) into separate manageable chunks.

## Export limit properties

You can set the number of records to return during an export using the **sysparm\_record\_count** URL parameter.

However, the system analyzes the following settings to determine whether an export limit should be applied.

1.  First, the platform checks the property that defines the format-specific export limit. Each format can have a different limit. Although this property can be set to any value, exceeding the default export limit can impact system performance. You may want to set the property at or below the default limit and have users [Break up a large export](../task/t_BreakUpALargeExport.md) to export large amounts of data.
2.  If the format-specific property is not set, the system checks the property for the general export limit. This property can also be set to any value, but exceeding the default export limit can impact system performance.
3.  If both the format-specific export limit and the general export limit property aren't set, the system enforces the default export limit.

**Important:** To set these properties, navigate to **System Properties** &gt; **Import Export**.

<table id="table_iqm_t5l_2r"><thead><tr><th>

Format

</th><th>

Format-specific export limit

</th><th>

General export limit

</th><th>

Default export limit

</th></tr></thead><tbody><tr><td>

XML

</td><td>

glide.xml.export.limit

</td><td>

glide.ui.export.limit

</td><td>

10,000

</td></tr><tr><td>

CSV

</td><td>

glide.csv.export.limit

</td><td>

glide.ui.export.limit

</td><td>

10,000

</td></tr><tr><td>

EXCEL \(XLSX\)

</td><td>

glide.xlsx.export.limit

</td><td>

glide.ui.export.limit

</td><td>

10,000

</td></tr><tr><td>

EXCEL \(XLS\)

</td><td>

glide.excel.export.limit

</td><td>

glide.ui.export.limit

</td><td>

10,000

</td></tr><tr><td>

EXCEL \(XLSX\)

</td><td>

glide.xlsx.max\_cells

</td><td>

N/A

</td><td>

500,000

</td></tr><tr><td>

EXCEL \(XLS\)

</td><td>

glide.excel.max\_cells

</td><td>

N/A

</td><td>

500,000

</td></tr><tr><td>

PDF

</td><td>

glide.pdf.max\_detail\_pages**Note:** The number of rows can be set from 0 to 250. If no value is specified, the default is 250. If a value greater than 250 is specified, the default value of 250 is used.

</td><td>

250

</td><td>

250

</td></tr><tr><td>

PDF

</td><td>

glide.pdf.max\_rows**Note:** The number of rows can be set from 0 to 5,000. If no value is specified, the default is 1,000. If a value greater than 5,000 is specified, the default value of 1,000 is used.

</td><td>

N/A

</td><td>

1,000

</td></tr><tr><td>

PDF

</td><td>

glide.pdf.max\_columns**Note:** Only 25 header labels fit on a page.

</td><td>

N/A

</td><td>

25

</td></tr><tr><td>

JSON

</td><td>

glide.json.export.limit

</td><td>

glide.ui.export.limit

</td><td>

10,000

</td></tr></tbody>
</table>A warning threshold property called **glide.ui.export.warn.threshold** controls how the records are exported. When you export enough records from a list to exceed the threshold, a choice dialog appears. You can choose to wait for the export to complete or email the exported records as an attachment. The warning threshold can be changed in the system property. The email attachment must not exceed the maximum [Email size limits](../../notification/concept/c_EmailAttachmentLimits.md).

<table id="table_jyw_zvl_2r"><thead><tr><th>

Example

</th><th>

Property

</th><th>

Breaking export limits

</th></tr></thead><tbody><tr><td>

Exporting to CSV

</td><td>

-   glide.csv.export.limit = 20,000
-   glide.ui.export.limit = 10,000
-   com.glide.processors.XMLProcessor.max\_record\_count = 20,000
-   Default export limit for CSV = 10,000

</td><td>

If you export 30,000 records, the number of records returned from the database is 20,000. The number of records specified for export exceeds the value set in the glide.csv.export.limit property.

</td></tr><tr><td>

Exporting to Excel \(XLSX\)

</td><td>

-   glide.xlsx.export.limit = no entry
-   glide.ui.export.limit = no entry
-   Default export limit for Excel \(XLSX\) = 10,000

</td><td>

If you export 30,000 records, the number of records returned from the database is 10,000. The number of records specified for export exceeds the default export limit for Excel.

</td></tr><tr><td>

Exporting to PDF

</td><td>

-   glide.pdf.max\_rows = 1,000
-   Default export limit for PDF = 1,000
-   Maximum export limit for PDF = 5,000

</td><td>

If you export 5,000 records, the number of records returned from the database is 1,000. The number of records returned is limited because the number of records specified for export exceeds the default value in the glide.pdf.max\_rows property.

</td></tr></tbody>
</table>## Excel export threshold

Excel exports are intended for relatively small exports with fewer than 500,000 cells. CSV can handle larger exports.

If an exported spreadsheet has more than 500,000 cells, the export process stops. You receive the Excel file at that point. The following message displays in the bottom row: `Export stopped due to excessive size. Use CSV for a complete export`.

The Excel export cell threshold is customizable using the **glide.xlsx.max\_cells** integer property \(or **glide.excel.max\_cells** if using XLS\).

**Note:** Increasing this threshold may cause a memory issue in your instance. The threshold is set at an appropriate level to prevent resource issues.

The export puts the information into the Excel document with 32,000 rows per spreadsheet.


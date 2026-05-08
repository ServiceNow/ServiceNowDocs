---
title: Exporting data
description: Export data from the ServiceNow AI Platform in a variety of formats.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Exporting data

Export data from the ServiceNow AI Platform in a variety of formats.

## Key benefits

-   Export an individual record to a PDF or XML file directly from a form. See [Export data from a record](../task/export-form-data.md).
-   Export multiple records to a CSV, Excel, PDF, XML, or Google Sheets file directly from a list. See [Export data from a list](../task/export-list-data.md).
-   Export multiple records from a table using the CSV, Excel, PDF, or XML processor in a URL with optional parameters. See [Export directly from a URL](../task/t_ExportDirectlyFromTheURL.md).

You can also export data from your instance using the following options:

-   Export multiple records from a table via a web services request. For example, you can create an external application or process to automate the retrieval of data from an instance via web services such as REST or SOAP. For more information, see Web services.
-   Push all the data that you want to export to an external file by creating an export set. For more information, see Export sets.

## Associated roles

You can export form data to PDF or XML, depending on your role.

-   The PDF options are available to all users.
-   The XML option is only available to users with the admin role.

You can export records in a list to Excel, CSV, XML, JSON, PDF, or an Export Set depending on your role.

-   The Excel, CSV, JSON, PDF, and Google Sheets options are available to all users.
-   The XML option is only available to users with the admin role.
-   The Export Set option is only available to users with the export\_set\_admin or admin role.

## Export formats

<table id="table_bfs_4kk_2r"><thead><tr><th>

Export format

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSV

</td><td>

Export table records as a comma-separated value text file. Use this option to export the currently displayed fields in the list or form as a text file. Configure the list or form to add or remove fields from the export. When exported to CSV, dot-walked fields appear using their full field name, such as u\_assignment\_group.parent.

 **Note:** By default, ServiceNow exports all CSV files in Windows-1252 encoding. If you need to export translated data, set the **glide.export.csv.charset** [system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) to UTF-8.

</td></tr><tr><td>

Excel

</td><td>

Export table records as a Microsoft Excel spreadsheet. Use this option to export the currently displayed fields in the list or form as an Excel spreadsheet. Configure the list or form to add or remove fields from the export.

</td></tr><tr><td>

XML

</td><td>

Export table records as an XML document. Use this option to export all data from a table or all data for a particular record. The XML file has an XML element for each column in the table. See [Exporting and importing data via XML](../../development-best-practices/concept/c_ExportAndImportXMLFiles.md).**Note:** Image field data is not preserved when exporting to XML.

</td></tr><tr><td>

PDF

</td><td>

Export table records as a Portable Document Format file. Use this option to export the currently displayed fields in the list or form as a PDF file. Configure the list or form to add or remove fields from the export.

 **Note:** The PDF export processor prints data from left-to-right, which can produce rendering errors when displaying right-to-left language data.

</td></tr><tr><td>

JSON

</td><td>

Export the table records as a JSON string. The JSON file has an element for each column in the table.

</td></tr><tr><td>

Google Sheets

</td><td>

Export table records directly to cloud-based spreadsheets in Google Drive without going through extra steps. The exported file retains the structure of the original table, including rows and columns. You can view, edit and share these Google Sheets online in real time.

</td></tr></tbody>
</table>## Column headers

The file type you export to, such as CSV or PDF, determines how column headers are exported. In general, formats meant for human consumption such as PDF display the column label, whereas formats meant for machine use, such as CSV, use the database field\_name.

|File type|Column header format|
|---------|--------------------|
|Excel|Label|
|PDF|Label|
|CSV|field\_name|
|XML|field\_name|
|JSON|field\_name|


---
title: Import sets key concepts
description: Learn about import sets before importing data to your instance.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Import sets, Imports, Data and Automation]
---

# Import sets key concepts

Learn about import sets before importing data to your instance.

The import sets table acts as a staging area for records imported from a data source.

**Note:** Do not import data in extremely large chunks. Creating an extremely large import set can cause delays and system outages.

A transform map determines the relationships between fields displaying in an import set table and fields in an existing ServiceNow table, such as the Incidents or Users table.

Importing sets skip records when the data in the instance matches the data being imported.

**Note:** Import sets run as user System and therefore cannot add data to encrypted fields.

## Import sets terminology

<table id="table_rv4_gxf_f5"><thead><tr><th>

Term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Import Set table

</td><td>

A table that acts as a staging location for records imported from a data source before transforming those records. Fields on these tables are generated automatically based on imported data and should not be modified manually.

 **Note:** Columns in an import set table are generated automatically and shouldn't be added manually. Manually adding columns can negatively impact the table's scheduled cleanup and may lead to an incomplete cleanup and orphaned records.

 If you need to add columns to an import set table, first add the column to the input data, then select **Test Load 20 Records** or **Load All Records** to auto generate the columns in the import set table.

 Columns in an import set table might not have the same type as the input data. For example, a currency column may be represented as a string column in an import set table until it's assigned to a target table column that is of type currency.

</td></tr><tr><td>

Data source

</td><td>

A record that defines where to get the data to import. A data source may point to a file, a JDBC-compatible database, or an LDAP organizational unit.

</td></tr><tr><td>

Transformation

</td><td>

The conversion of data from an import set table to another table according to the rules defined in a transform map.

</td></tr><tr><td>

Transform map

</td><td>

A set of field maps that define the relationships between fields in an import set and fields on a table, such as Incident.During transformation, data is copied from the Import Set table to the destination table based on the transform map.

 A single import set field may be mapped to multiple fields on other tables.

</td></tr><tr><td>

Robust import set transformer

</td><td>

Extract, transform, and load data to one or more target tables. Separate the transform and processing functions, providing a more flexible alternative to transform maps.

</td></tr><tr><td>

Foreign record insert

</td><td>

A foreign record insert occurs when an import makes a change to a table that is not the target table for that import.This change happens when updating a reference field on a table. For example, when updating a value for the caller on an incident, the import is actually updating the sys\_user table.

</td></tr><tr><td>

Coalesce

</td><td>

Lets you update existing target table records when transforming import data.You can specify whether a **Target field** should be used to coalesce on when import set records are transformed. If the field map **Coalesce** option is selected, when the import set row is transformed, the instance checks for an existing record in the target table that has the same value in the **Target field** as the import set row **Source field**.

If an existing record with a matching value in the target table is found, that record is updated. If no matching record is found, then a new record is created in the target table.

</td></tr></tbody>
</table>## Supported import formats

You can import data from several different file formats or external data sources.

<table id="table_mwq_nl1_kr"><thead><tr><th>

Format

</th><th>

Limitations

</th></tr></thead><tbody><tr><td>

CSV

</td><td>

CSV files must comply with the proposed CSV standard in [RFC4180](http://tools.ietf.org/pdf/rfc4180.pdf). In particular, this means that double quotes may not appear inside fields. The first row of data in an imported CSV file becomes the header row and defines the columns for that import set.

</td></tr><tr><td>

Excel

</td><td>

Excel files must have the XLS or XLSX extension.

</td></tr><tr><td>

XML

</td><td>

XML files must have a consistent XPath for each data row.

</td></tr><tr><td>

JSON

</td><td>

-   For JSON arrays, the path for each row must specify the array root element twice, such as `/incidents/incidents`.
-   JSON files should follow [RFC-4627](https://www.ietf.org/rfc/rfc4627.txt). For example, a single comma should separate a value from the following name. Names within an object should be unique.
-   Predicates such as `@element`, `[index]`, or `text()`, as well as Axis such as children, siblings, or ancestors are not supported.

</td></tr><tr><td>

Custom \(Parse by Script\)

</td><td>

You can write custom JavaScript to parse input lines into the list of maps.

</td></tr></tbody>
</table>The ServiceNow® platform can import data from the following external data sources.

|Data Source|Limitations|
|-----------|-----------|
|JDBC|JDBC imports require a valid transform map. Some network configurations may require a ServiceNow® MID Server.|
|LDAP|LDAP imports require a valid transform map.|
|OIDC|OIDC imports require a valid transform map.|
|ServiceNow® REST \(Integration Hub\)|REST imports require a valid transform map.|
|Custom \(Load by Script\)|Custom imports require a valid transform map.|

For more details about the different data sources, see [Data sources](c_DataSources.md).

## Transform maps versus robust import set transformers

Both transform maps and robust import set transformers convert data. Transform maps convert data from the staging table to the destination file. Robust import set transformers convert data from a source table to a message listener. If a data source has both a transform map and a robust import set transformer, the system uses the robust import set transformer instead of the transform map.

## Import set scheduled cleanup

The **Import Set Deleter** scheduled job cleans up old import set data every day at midnight.

By default, the job deletes all import sets that are older than 7 days, as well as the associated import set table records. If this scheduled job is not active on your instance, activate it to mitigate the growing import set tables you may have, especially when using recurring imports.

**Note:** If scheduled cleanup is not currently active on your system, you must ensure that your import set tables are not too large \(&gt; 5 million records total across all tables\) before enabling this cleanup. If the tables are too large, manually delete the records first before proceeding. Contact Customer Service and Support to coordinate the deletion of this data.

![Import Set Deleter.](../image/import-set-scheduled-cleanup.png "Scheduled Script Execution")

For procedures, see [Delete import sets](../task/delete-import-sets.md).

## Import set table deleter

You can manually delete any or all of the following import set tables:

-   Computer
-   User
-   Notification
-   Location

You can also delete the related transform maps, or you can delete data only and preserve the table structure.

![Import set table deleter.](../image/cleanup-import-set-tables.png "Tables available for deletion")

For procedures, see [Delete import set tables](../task/delete-import-set-tables.md).

**Parent Topic:**[Import sets](../reference/import-sets-landing-page.md)


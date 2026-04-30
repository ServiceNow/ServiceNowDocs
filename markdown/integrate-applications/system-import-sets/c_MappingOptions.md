---
title: Mapping options
description: You can map fields in a number of ways depending on the circumstances of the import and whether data must be transformed prior to loading onto a production table.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Importing data using import sets, Import sets, Imports, Data and Automation]
---

# Mapping options

You can map fields in a number of ways depending on the circumstances of the import and whether data must be transformed prior to loading onto a production table.

It is also important to note that any given import operation may require taking advantage of multiple mapping methods, and these methods can be readily used in conjunction with one another.

## Automatic Mapping Utility

The simplest mapping method is where all of the field names of the import sets match the names of the fields on the production tables onto which the data will be transformed. In this case, simply click **Auto map matching fields** in the related list in the Table Transform Map form and confirm proper matching. If there are any discrepancies in terms of how fields were automatically matched, use the mapping assist utility to correct them. When all fields are matched properly, click the **Transform** related link to begin transforming data onto the destination table.

## Mapping Assist Utility

The mapping assist utility provides a visually intuitive environment for specifying mapping between import set fields and production table fields. The mapping assist utility makes it possible to map a single source field \(field on an import set table\) to multiple destination fields \(fields on a production table\).

![](../image/MappingAssist.png "Mapping assist")

## Changing the Date Format

If the date format of the source field does not match the format of the target field, you can set a date format mapping to transform dates from one format to another. For example, this mapping specifies that the date format of the CSV source file uses the **MM-dd-yyyy** format.

![](../image/FieldMapDateFormat.png "Field map date format")

![](../image/FieldMapDateFormatOptions.png "Field map date format options")

Date format options include:

|Date Format|Description|
|-----------|-----------|
|dd-MM-yyyy|Day-month-year|
|dd-MM-yyyy hh:mm:ss|Day-month-year hours-minutes-seconds|
|dd-MM-yyyy hh:mm:ss z|Day-month-year hours-minutes-seconds timezone|
|MM-dd-yyyy|Month-day-year|
|MM-dd-yyyy hh:mm:ss|Month-day-year hours-minutes-seconds|
|MM-dd-yyyy hh:mm:ss z|Month-day-year hours-minutes-seconds timezone|
|yyyy-dd-MM|Year-day-month|
|yyyy-MM-dd|Year-month-day|
|yyyy-MM-dd hh:mm:ss|Year-month-day hours-minutes-seconds|

To denote 24 hour time format, specify a custom date format using **HH:mm:ss** instead of hh:mm:ss.

**Note:**

Converting from a 24-hour to 12-hour date format might cause times from 12:00 to 23:59 to be formatted as 00:00 to 11:59.

## Mapping to a Duration Field

ServiceNow duration fields use a special data type that lists the number of milliseconds the duration value is. To map import data to a duration field use one of the following methods to transform source values into a duration.

-   Calculate the duration from a start and end date
-   Convert an existing duration value into a ServiceNow duration value

## Calculating a Duration Value from a Start and End Date

If the import source has a start and end date, you can calculate a duration with JavaScript.

1.  Navigate to **System Import Sets** &gt; **Transform Maps**.
2.  Select the transform map you want to calculate a duration value. For example, the Notification transform map that imports into the Incident table.
3.  Select the **Run script** check box.
4.  Enter JavaScript to transform the start and end dates into a duration. See the sample script.
5.  Click **Update**.

This sample script transforms the source.u\_start and source.u\_end fields to a duration value in the target.duration field. Change the field names to match your source and target fields as needed.

```
target.duration = gs.dateDiff(source.u_start.getDisplayValue(), source.u_end.getDisplayValue(), false);
```

## Convert a Duration Value into a ServiceNow Duration Value

If the import source already contains a start date and a duration value, you can convert the existing duration into a ServiceNow duration. For example, you might have an Excel data source that lists a duration in seconds. ServiceNow expects durations to have millisecond values.

1.  Navigate to **System Import Sets** &gt; **Transform Maps**.
2.  Select a transform map.

    For example, the Notification transform map that imports into the Incident table.

3.  Select the **Run script** check box.
4.  Enter JavaScript to convert existing duration values into a ServiceNow duration values. See the sample script.
5.  Click **Update**.

This sample script converts a duration in seconds \(from the **source.u\_duration** field\) to a duration in milliseconds \(in the **target.duration** field\). Change the field names to match your source and target fields, as needed.

```
//Transform the value in source.u_duration from seconds to milliseconds
target.duration.setDateNumericValue(source.u_duration * 1000);
```

This sample script converts a duration already in milliseconds \(from the **source.u\_duration** field\) to a ServiceNow duration \(in the **target.duration** field\). Change the field names to match your source and target fields, as needed.

```
//Transform the value in source.u_duration to ServiceNow format
target.duration.setDateNumericValue(source.u_duration);
```

## Using a Script to Calculate a Source Value

You may want to use a source script instead of the **Source field** when:

-   The source value is not in the format for the mapped target value.
-   You want to look up a value before mapping to the target field.
-   The source value must be computed from multiple fields.
-   You need to create a compounded or calculated coalesce value in the target field.

For example, this example source script computes the value of the user\_name field when it is blank in the source.

![](../image/FieldMapSourceScript.png "Field map source script")

A source script expects the calculated value to be set in the global variable `answer`.

## Mapping Binary or BLOB Fields

ServiceNow uses a special process to import binary and binary large object \(BLOB\) data from JDBC data sources. All binary data is automatically converted into a record in the Attachment \[sys\_attachment\] table before the transformation occurs. The import set table only stores the attachment record's sys\_id value in the import table field instead of the actual binary value. For example, suppose you use a JDBC data source to import data from a CA Service Desk system, which stores each record's key value as binary data. When you import the Service Desk key values into a ServiceNow table, the ServiceNow field only contains a sys\_id reference to the corresponding binary data in the Attachment Record \[sys\_attachment\] table rather than the actual binary data.

To have a transform map access the attachment, use the GlideRecord API in an `onAfter` script. The script needs to run in an `onAfter` event because the `target.sys_id` object is only available after the data is placed in the import set table. For example, to map the resulting attachment to the target transform record, you can use the following script.

```
var agr = new GlideRecord("sys_attachment");
  agr.addQuery("sys_id", source.u_blob_field);
  // the source field needs to be mapped to the source that is the BLOB
  agr.query();
   if(agr.next()) {
    agr.table_name = "cmdb_ci"; // the target table of the transform map
    agr.table_sys_id = target.sys_id; // the target record
    agr.content_type = source.u_contentype; 
    // the content type string if available,  
    // this becomes the mime encoding when clicking an attachment link
    agr.update(); // finally, move/re-attach the attachment to the target row }
```

If you are mapping directly to the `db_image` table, run the following `onAfter` script to display the image:

```
var strTemp = source.u_file_name; 
var fType = strTemp.substr(- 3); 
var iCont = "" ;
 
 if(fType == 'jpg') {
  iCont = 'jpeg' ; } 
 else {
  iCont = fType; }
 
 var agr = new GlideRecord("sys_attachment");
 agr.addQuery("sys_id", source.u_blob_field);
 agr.query();
 
 if(agr.next()) {
  agr.table_name = "ZZ_YYdb_image";
  agr.table_sys_id = target.sys_id;
  agr.content_type = 'image/' + iCont;
  agr.file_name = 'image';
  agr.update(); }
```

**Parent Topic:**[Importing data using import sets](../../../administer/import-sets/concept/c_ImportDataUsingImportSets.md)


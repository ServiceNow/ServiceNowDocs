---
title: Test the Excel Service Graph connector
description: The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Test the Excel Service Graph connector

The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.

These logs can be used to debug any issues or to find the SGC steps are executed properly.

<table><thead><tr><th>

Issue

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

If there is an issue while loading data for `SG-OT Device Excel Import` ETL on ETL guided setup

</td><td>

From the Related links list, try loading the data. 1.  Navigate to the `SG-OT Excel Import` data source and select **Test Load 20 Records** or **Load All Records**.
2.  Return to ETL and try loading the data again.

</td></tr><tr><td>

If there are entries in the Partial payload tab after test running the Service Graph connector from ETL guided setup

</td><td>

Due to the following conditions: -   Missing values for the required fields of an device.
-   Control Modules without a parent device associated with it - Check that the type of the device and control module parent id field is filled properly in the staging table.

</td></tr><tr><td>

If there are entries in the Incomplete payload tab after test running the Service Graph connector from ETL guided setup

</td><td>

Due to the missing values for fields that are used uniquely to identify an device.

</td></tr><tr><td>

After easy import is executed, users may see records that are imported from the current run. When validations are executed, they are run on all records of the staging table not only on records from the current import run.

</td><td>

Before running the validations, the user must click **ALL** on the list view breadcrumb of the staging table.

</td></tr><tr><td>

If the timestamp column appears empty on the staging table

</td><td>

The user must use the UTC format \(YYYY-MM-DD hh:mm:ss\) to enter the date and time.

</td></tr><tr><td>

If the validation state update on records is not visible after click Run Validations button.

</td><td>

The user must manually refresh the page.

</td></tr><tr><td>

When the user changes the existing data of the records in the staging table, the validation state is not set to Pending Validation.

</td><td>

The validation state is set to Pending validation, when the following attributes are changed:-   Identifier fields \(Mac-address \(1-9\)\)
-   Serial Number
-   Name
-   Correlation ID
-   Type
-   Control module parent correlation ID
-   Fields used in transformed name computation
-   Rack Number
-   Slot Number

 For more information about the system properties, see [System properties that impact SG-OT Device Excel Import processing](../task/system-properties-sg-ot-asset-excel-import.md).

</td></tr><tr><td>

After records are imported into the staging table, the updates done in the system properties related to transformed name computation are not reflected in the staging table records.

</td><td>

Change the system properties before importing the data into the staging table.

</td></tr><tr><td>

If the multiple error banners are shown when users select few records and click **Run Validation**.

</td><td>

The validations are executed for all the records available in the staging table. Do not select the single record for validation.

</td></tr><tr><td>

If the duplicate records exist in CMDB, the staging table does not detect it as duplicate.

</td><td>

The validations are executed only for the data available in the staging table.

 The validations are not executed for the data available CMDB.

</td></tr><tr><td>

The site name is provided in the spreadsheet or staging table, but not shown on the OT devices after the import of the spreadsheet.

</td><td>

Only the existing site records in the CMDB are considered.

 The entity\_name for the site \(ISA Equipment model entity\) must match the value provided in the site column in the excel or staging table.

 If the entity\_name for the site does not match, the value is set to empty.

</td></tr><tr><td>

When users click **Load All** the records on the data source, no records are imported into the import set.

</td><td>

No records are available in the staging table.

 The records are present in the staging table, but the records are not in Valid or Partially valid state.

 Access all the logs related to Excel SGC in **All** &gt; **System logs** &gt; **System log** &gt; **All**. Search for the string SGOTExcel in the Message column.

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for Microsoft Excel](../concept/service-graph-connector-for-OT-excel.md)


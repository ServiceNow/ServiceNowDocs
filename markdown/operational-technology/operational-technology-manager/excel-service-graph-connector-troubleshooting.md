---
title: Test the Service Graph Connector for Microsoft Excel
description: The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Test the Service Graph Connector for Microsoft Excel

The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.

These logs can be used to debug any issues or to find the Service Graph Connector steps are executed properly.

<table><thead><tr><th>

Issue

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

If there are entries in the Partial payload tab after test running the Service Graph Connector from ETL Guided Setup

</td><td>

Due to the following conditions: -   Missing values for the required fields of an device.
-   Control Modules without a parent device associated with it - Check that the type of the device and control module parent id field is filled properly in the staging table.

</td></tr><tr><td>

If there are entries in the Incomplete payload tab after test running the Service Graph Connector from the ETL Guided Setup

</td><td>

Due to the missing values for fields that are used uniquely to identify an device.

</td></tr><tr><td>

If the timestamp column appears empty on the staging table

</td><td>

The user must use the UTC format \(YYYY-MM-DD hh:mm:ss\) to enter the date and time.

</td></tr><tr><td>

If the validation state update on records isn't visible after the validation process

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

 For more information about the system properties, see [Review the system properties used by the Service Graph Connector for Microsoft Excel](../task/access-system-properties-used-by-service-graph-connector.md).

</td></tr><tr><td>

After records are imported into the staging table, the updates done in the system properties related to transformed name computation are not reflected in the staging table records.

</td><td>

Change the system properties before importing the data into the staging table.

</td></tr><tr><td>

If the duplicate records exist in CMDB, the staging table does not detect it as duplicate.

</td><td>

The validations are executed only for the data available in the staging table.

 The validations are not executed for the data available in the CMDB.

</td></tr><tr><td>

The site name is provided in the spreadsheet or staging table but isn't shown on the OT devices after the import of the spreadsheet.

</td><td>

Only the existing site records in the CMDB are considered.

 The entity\_name for the site \(ISA Equipment model entity\) must match the value provided in the site column in the excel or staging table.

 If the entity\_name for the site does not match, the value is set to empty.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)


---
title: Bulk import of your enterprise models and assets
description: Use a subflow to import enterprise models and assets of multiple types to your ServiceNow instance at one go. You can also perform a bulk update on existing models and assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Bulk import of your enterprise models and assets

Use a subflow to import enterprise models and assets of multiple types to your ServiceNow instance at one go. You can also perform a bulk update on existing models and assets.

## Overview

Use the Enterprise Asset workspace to do a bulk transfer of all your enterprise models and asset from a different database to the ServiceNow instance.

Create an import record by downloading a template in the form of a spreadsheet \(.xlsx\). Ensure that you enter valid values in all the mandatory fields before uploading the template. Attach the template to the import record and select **Import** to begin the import process.

After you select **Import**, the EAM Bulk Import subflow gets triggered. Scheduled jobs are initiated and data in the spreadsheet is copied to the appropriate staging tables. The staging tables are validated and records are created in the ServiceNow instance.

## Modes

Modes refer to the type of import that you want to process. There are modes for only importing models, assets, and a combined mode for both models and assets. You can choose from the following available modes:

-   Create models
-   Update models
-   Create assets
-   Update assets
-   Create models and assets
-   Update models and assets

## Templates

Based on the mode you select in the import record, you can download the corresponding template.

**Note:** Ensure that you enter valid values in all the mandatory fields for the import process to run effectively. For a list of all the mandatory fields, see [Mandatory fields in the bulk import spreadsheets](../reference/mandatory-bulk-fields.md).

<table id="table_ofy_kbk_3xb"><thead><tr><th>

Modes

</th><th>

Corresponding template

</th></tr></thead><tbody><tr><td>

-   Create models
-   Update models

</td><td>

Model template

</td></tr><tr><td>

-   Create assets
-   Update assets

</td><td>

Asset template

</td></tr><tr><td>

-   Create models and assets
-   Update models and assets

</td><td>

Model and asset template

</td></tr></tbody>
</table>You can customize the templates to add more columns. Make the following modifications to add more columns:

1.  Add the new columns to the staging tables.
2.  Modify the list view on the Database view table \[sn\_eam\_import\_template\] to include the columns you want to display in the spreadsheet. Enter the string `sn_eam_import_template.list` in the filter field on your instance's navigation bar.
3.  Add field mappings in the Model or Asset transform map.

## Scheduled jobs

The following scheduled jobs execute as part of the EAM Bulk Import subflow.

![Scheduled jobs for bulk import](../image/bulk-import-scheduledjobs.png)

The scheduled jobs execute based on the mode that you select.

The EAM Bulk Import - Upload File job is executed for all modes. For the Create Model or Update Model modes, the EAM Bulk Import - Transform Asset doesn't execute. Similarly, for the Create asset or Update asset modes, the EAM Bulk Import - Transform Model doesn't execute.

For example, if you select the Create models and assets mode, the scheduled job, **EAM Bulk Import - Upload file** uploads the data from the spreadsheet to the three staging tables. Then the Scheduled job, **EAM Bulk Import - Transform Model** executes the model and model component transform maps. After the model transform maps are complete, the **EAM Bulk Import -Transform Asset** scheduled job executes the asset transform map.

## Staging tables

The data that you enter in the spreadsheet is copied to one or more of the following staging tables:

-   Model Import Staging \[sn\_eam\_model\_import\_row\]​
-   Model Component Import Staging \[sn\_eam\_mc\_import\_row\]​
-   Asset Import Staging \[sn\_eam\_asset\_import\_row\]​


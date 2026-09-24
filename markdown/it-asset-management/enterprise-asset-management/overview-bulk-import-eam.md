---
title: Bulk import of your enterprise models and assets
description: You can use the EAM Bulk Import subflow to import multiple enterprise models and assets into your ServiceNow instance in one go. You can also use this subflow to bulk update existing models and assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/overview-bulk-import-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Bulk import of your enterprise models and assets

You can use the EAM Bulk Import subflow to import multiple enterprise models and assets into your ServiceNow instance in one go. You can also use this subflow to bulk update existing models and assets.

## Bulk import overview

You can bulk import enterprise model and asset data from an external database to your ServiceNow instance. The database must be in the format of a spreadsheet \(.xlsx or .xls\).

To perform a bulk import, you must create an import record that contains all necessary information and data for the import. You must upload a spreadsheet of your enterprise model and asset data to this record, ensuring that all mandatory fields contain valid values. After all necessary information and data is added to your import record, you can initiate the import.

When you initiate an import, the EAM Bulk Import subflow triggers. This subflow initiates scheduled jobs that copy all spreadsheet data to the appropriate staging tables, validate the data in these tables, and create corresponding records in your target tables.

**Note:** When the OT Asset Management application is activated, you can bulk import hardware assets and models in both the Enterprise Asset Workspace and the OT Asset Workspace only if the OT entity column is marked as **TRUE**.

## Import modes

Import modes are the types of imports that you can process. You can choose to import only models, only assets, or both models and assets. You can also choose to create additional models and assets or to update existing models and assets.

## Scheduled jobs

The following scheduled jobs execute as part of the EAM Bulk Import subflow.

\[Omitted image "bulk-import-scheduledjobs.png"\] Alt text: Scheduled jobs for bulk import

These scheduled jobs execute based on the import mode that you use.

-   The EAM Bulk Import - Upload File scheduled job executes for all import modes.
-   The EAM Bulk Import - Transform Model scheduled job executes only when you're creating or updating enterprise models.
-   The EAM Bulk Import - Transform Asset scheduled job executes only when you're creating or updating enterprise assets.

For example, if you choose to create both enterprise models and assets, the EAM Bulk Import - Upload file scheduled job uploads the data from the spreadsheet to the three staging tables. Then the EAM Bulk Import - Transform Model scheduled job executes the model and model component transform maps. After the model transform maps are complete, the EAM Bulk Import -Transform Asset scheduled job executes the asset transform map.

## Staging tables

The data that you enter in your spreadsheet is copied to one or more of the following staging tables:

-   Model Import Staging \[sn\_eam\_model\_import\_row\]​
-   Model Component Import Staging \[sn\_eam\_mc\_import\_row\]​
-   Asset Import Staging \[sn\_eam\_asset\_import\_row\]​


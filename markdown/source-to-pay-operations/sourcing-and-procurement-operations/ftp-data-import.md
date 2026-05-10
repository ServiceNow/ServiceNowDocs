---
title: Import data using FTP server
description: Import a file from a local source, a remote network server, or another instance by providing a path and authentication information. Transfer and manage procurement data in a principled structure that administrators can use for various data management operations.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Procurement File Transfer Framework, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Import data using FTP server

Import a file from a local source, a remote network server, or another instance by providing a path and authentication information. Transfer and manage procurement data in a principled structure that administrators can use for various data management operations.

## Before you begin

-   Understand the data import workflows and FTP functionality.
-   Ensure that you install and configure an FTP client.
-   Ensure that you install and configure MID Server in your ServiceNow instance to connect to the ERP server. See [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md) for details.

    **Note:** The MID Server integration is required only for an ERP integration using SOAP services.

-   Ensure you have permissions to access and pull data from FTP.

Role required: import\_admin or admin

## Procedure

1.  Navigate to **All**.

2.  On the left navigation pane, enter `sys_data_source_list.do`.

    The entire list of available data sources is displayed.

3.  In the **Name** search field, enter **spend** to find and select the spend data sources you want to configure.

4.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for this data source.|
    |Import set table label|Specify a label for the import set staging table to use.|
    |Import set table name|ServiceNow uses the label to construct a unique table name to prevent namespace collision with an existing table. This table stores the data from any third-party sources.|
    |Type|Select **File** as the type of data that you are importing from.|
    |Format|Select **JSON** as format.|
    |File retrieval method|Select **SFTP** as format for data transfer.|
    |File path|Specify the file path for querying.|

5.  Set additional fields based on the selected **Type**.

    See the documentation for each data source type for additional field information. The Table transform map is associated with the table to transform the `File Based Catalog Import [sn_spend_ftp_intg_catalog_stage]` data into `Catalog Import [sn_spend_intg_imp_catalog]`. For more information on the table transform map, see the [Data source table information](../reference/data-sources-info.md).


## What to do next

-   Manage the data integration by scheduled import and export jobs on a daily, weekly, or monthly basis. Perform the **Scheduled Imports** based on your business needs. See [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md).
-   Verify the accuracy of the data import and share the errors on the FTP server. The reseller can fix the posted errors using [Perform export steps](validate-errors.md).

-   **[Run scheduled imports](run-scheduled-imports.md)**  
A scheduled import allows administrators to import data on a regular schedule. Run import operations on a daily, weekly, or monthly basis based on your business requirements. Scheduled import runs a datasource similar to how a scheduler job runs the script.

**Parent Topic:**[Procurement File Transfer Framework](../concept/procurement-file-transfer-framework.md)


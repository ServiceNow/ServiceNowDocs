---
title: Import your Microsoft Excel spreadsheet using the staging table
description: Import your Microsoft Excel spreadsheet into the staging table using easy import to create the required data in the staging table from the spreadsheet.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Import your Microsoft Excel spreadsheet using the staging table

Import your Microsoft Excel spreadsheet into the staging table using easy import to create the required data in the staging table from the spreadsheet.

## Before you begin

This process requires the IntegrationHub ETL \(com. sn\_int\_studio\) plugin.

Before you perform this process, you must properly prepare a Microsoft Excel spreadsheet for import. To learn more, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

When the data is ready to be imported, you can schedule the import into the Configuration Management Database \(CMDB\). This process creates unique records in the Configuration Management Database \(CMDB\) for the OT devices that are included in your spreadsheet.

Roles required: cmdb\_inst\_admin, import\_admin, import\_scheduler, admin

## About this task

When you run the Integration Hub Extract Transform Load \(ETL\), you can also refer to the embedded content in the Industrial Guided Setup for additional assistance.

Execute the validations in the staging table to check for duplicates and inconsistencies in the data.

To access the Industrial Guided Setup, navigate to **Industrial Workspace Admin** &gt; **Guided Setup**.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**.

2.  Select the **CMDB Application: SG-OT Excel Import** ETL.

3.  On the ETL Transform Map Assistant form, select **Import Source Data and Basic Details**.

4.  On the Provide Basic Information for the ETL Transform Map form, in the **Sample Import Set** field, select **Auto-pull a new import set**.

5.  Return to the Integration Hub ETL form.

    **Note:** The remaining steps for creating an ETL transform map are automatically completed. However, you can select a specific step to review it before performing the actual import. For example, select **Prepare and Preview Data** to view the nested data structure and raw source data.

    **Note:** For more details, see [Create an ETL Transform Map](https://www.servicenow.com/docs/access?context=create-etl-transform-map&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

6.  To perform the actual Excel spreadsheet import, select **Test and Rollback Integration Results**.

7.  Select **Run Integration**.

    **Note:** This import tests 100 records. To run a full import of more than 100 records, you must schedule the import. You can schedule the import to run on a regular set schedule by selecting **Set Import Schedule**.

    After the data import is complete, the Test and Rollback Integration Results form appears with import statistics, including:

    -   Classes Mapped
    -   Relationships between classes
    -   New Records created from this integration run.
    -   Records updated from this integration run.
    -   Partial records created from this integration run.
    -   Incomplete records created from this integration run.
8.  Exit the Test and Rollback Integration Results form.

    The Rollback Options dialog box is displayed.

    ![Rollback Options dialog box.](../image/rollback-options.png)

9.  Select **Retain Data** to retain the imported data, or select **Perform Rollback** to roll back the imported data and reattempt the Microsoft Excel import.

10. To formally import your spreadsheet data to the ServiceNow AI Platform:

    1.  Select **Set Import Schedule**.
    2.  Select **Set Schedule**.
    3.  In the Scheduled Data Imports list, select **SG-OT Devices Schedule Import using Spreadsheet**.
    4.  On the Schedule Data Import form, select **Execute Now**.

## What to do next

After all steps are completed, from the SG-OT Device Import ETL Guided setup homepage, select **Activate** to activate the ETL.

**Parent Topic:**[Service Graph Connector for Microsoft Excel](../concept/service-graph-connector-for-OT-excel.md)


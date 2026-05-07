---
title: View ERP extraction tables
description: Work with ETL \(extract, transform, and load\) processes in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to extract large amounts of data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extraction, table, etl, transform]
breadcrumb: [Extracting and transforming data, Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# View ERP extraction tables

Work with ETL \(extract, transform, and load\) processes in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to extract large amounts of data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.

## Before you begin

Role required: sn\_erp\_integration.erp\_user

## About this task

ERP extraction tables extract and save data to a transform table on the ServiceNow AI Platform. The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the extraction tables icon ![](../image/erpc-extraction-table-icon.png) in the side panel.

    ![ERP extraction tables list.](../image/erpc-extraction-tables-ys2.png)

3.  View the list of ERP extraction tables.

<table id="table_gd5_xfz_wxb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL process.

</td></tr><tr><td>

Table transform map link

</td><td>

Table that the extracted data is cached and stored in.Select the table name to view the table on the ServiceNow AI Platform in a new browser tab.

For more information on creating table transform maps, see [Create a transform map](../../../script/server-scripting/task/t_CreateATransformMap.md).

</td></tr><tr><td>

ERP model

</td><td>

ERP model used in the ETL extraction.Select the ERP model name to view the details. For more information, see [View and edit the foundation of ERP models](view-and-work-with-erp-data-models.md).

</td></tr><tr><td>

Page size

</td><td>

Amount of data to read from the ERP system at a time. The default is 1000. Increasing the size may impact MID Server memory space.

</td></tr><tr><td>

Updated

</td><td>

Date and time the extraction table record was last saved.

</td></tr></tbody>
</table>4.  View the details for an extraction table by selecting the table name.


## What to do next

After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](../../../administer/import-sets/reference/import-sets-landing-page.md).

**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md)


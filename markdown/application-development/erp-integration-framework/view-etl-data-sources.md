---
title: View ERP extraction tables
description: Work with ETL \(extract, transform, and load\) processes in Zero Copy Connector for ERP to extract large amounts of ERP \(Enterprise Resource Planning\) data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/view-etl-data-sources.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Extracting and transforming data in Zero Copy Connector for ERP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# View ERP extraction tables

Work with ETL \(extract, transform, and load\) processes in Zero Copy Connector for ERP to extract large amounts of ERP \(Enterprise Resource Planning\) data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.

## Before you begin

Role required: sn\_erp\_integration.erp\_user

## About this task

ERP extraction tables extract and save data to a transform table on the ServiceNow AI Platform. The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the ERP extraction tables icon \(\[Omitted image "erpc-extraction-table-icon.png"\] Alt text: ERP extraction tables navigation icon\) in the side panel.

    \[Omitted image "erpc-extraction-tables-ys2.png"\] Alt text: ERP extraction tables list.

3.  View the list of ERP extraction tables and note the tables that you can use to build your ERP model.

<table id="table_gd5_xfz_wxb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL process.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the purpose of the ETL process.

</td></tr><tr><td>

Tables transform map link

</td><td>

Table that the extracted data is cached and stored in.Select the table name to view the table on the ServiceNow AI Platform in a new browser tab.

For more information on creating table transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).

</td></tr><tr><td>

ERP model

</td><td>

ERP model used in the ETL extraction.Select the ERP model name to view the details. For more information, see [View and edit the foundation of ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/view-and-work-with-erp-data-models.md).

</td></tr></tbody>
</table>4.  View the details for an extraction table by selecting the table name.


## What to do next

After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/import-sets-landing-page.md).

**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-extraction-tables.md)


---
title: Extracting and transforming data in Zero Copy Connector for ERP
description: ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in Zero Copy Connector for ERP.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extract, extraction table]
breadcrumb: [Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Extracting and transforming data in Zero Copy Connector for ERP

ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in Zero Copy Connector for ERP.

## Hold large amounts of data in extraction tables

Use extraction tables, which are ETL \(extract, transform, and load\) data sources, to extract large amounts of data regularly.

For example, you can extract all open purchase orders for the current month from an SAP system into a Glide table once a day at a set time. You can then access that data via ServiceNow AI Platform, such as Source-to-Pay Operations or a PO workspace created in App Engine Studio.

After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](../../../administer/import-sets/reference/import-sets-landing-page.md).

## Extraction tables use transform table maps

ERP extraction tables save data to a local transform table on the ServiceNow AI Platform. The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination. For example, after import, the extraction table can run a Glide query on a transform table and save the output to several different target tables.

If you use a custom transform table, you must first create the table on the ServiceNow AI Platform, and the table must be in the application scope. For more information on creating table transform maps, see [Create a transform map](../../../script/server-scripting/task/t_CreateATransformMap.md).

ETL processes in Zero Copy Connector for ERP are configured in the ServiceNow AI Platform app that needs the data, not Zero Copy Connector for ERP. For example, you can configure an extraction process in a flow in Workflow Studio.

## Automatically available standard extraction tables

When you install Zero Copy Connector for ERP, the ServiceNow AI Platform automatically loads standard ERP extraction tables for you to work with. For example, sales, delivery, and procurement tables. For a list of standard extraction tables, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md).

If you installed ERP Semantic Mining, that app populates some additional extraction tables, such as ERP application activity, Collector directory data, and Namespace data.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

-   **[View ERP extraction tables](../task/view-etl-data-sources.md)**  
Work with ETL \(extract, transform, and load\) processes in Zero Copy Connector for ERP \(Enterprise Resource Planning\) to extract large amounts of data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.
-   **[Add a new ERP extraction table in Zero Copy Connector for ERP](../task/erp-canvas-add-new-extraction-table.md)**  
Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.
-   **[Select fields for an extraction table in Zero Copy Connector for ERP](../task/erpc-select-extraction-table-fields.md)**  
Add or remove fields for an extraction table in Zero Copy Connector for ERP\(Enterprise Resource Planning\). For example, you may want to remove fields with sensitive information, such as birthdays.
-   **[Create a table transform map from an extraction table](../task/erpc-create-table-transform-map-from-extraction-table.md)**  
In Zero Copy Connector for ERP \(Enterprise Resource Planning\), create a table transform map from an extraction table and map the source fields with target fields.
-   **[Create a scheduled extraction in Zero Copy Connector for ERP](../task/erpc-create-a-scheduled-extraction.md)**  
Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.
-   **[Monitor Zero Copy Connector for ERP transactions and logged errors](../task/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md)**  
Use the monitoring feature to track the progress of each ERP \(Enterprise Resource Planning\) transaction and view logged errors.

**Parent Topic:**[Retrieving data](erp-retrieving-data.md)


---
title: Extracting and transforming data in ERP Data Hub
description: ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Extracting and transforming data in ERP Data Hub

ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in ERP Data Hub.

## Hold large amounts of data in extraction tables

Use extraction tables, which are ETL \(extract, transform, and load\) data sources, to extract large amounts of data on a regular basis.

For example, you can extract all open purchase orders for the current month from an SAP system into a Glide table once a day at a set time. You can then access that data via ServiceNow AI Platform, such as Source-to-Pay Operations or a PO workspace created in App Engine Studio.

After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

## Extraction tables use transform table maps

ERP extraction tables save data to a local transform table on the ServiceNow AI Platform. The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination. For example, after import, the extraction table can run a Glide query on a transform table and save the output to several different target tables.

If you use a custom transform table, you must first create the table on the ServiceNow AI Platform, and the table must be in the application scope. For more information on creating table transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

ETL processes in ERP Data Hub are configured in the ServiceNow AI Platform app that needs the data, not ERP Data Hub. For example, you can configure an extraction process in a flow in Workflow Studio.

## Automatically available standard extraction tables

When you install ERP Data Hub, the ServiceNow AI Platform automatically loads standard ERP extraction tables for you to work with. For example, sales, delivery, and procurement tables. For a list of standard extraction tables, see [Standard ERP models and extraction tables for ERP Data Hub](../reference/erp-canvas-standard-extraction-tables.md).

If you installed ERP Customization Mining, that app populates some additional extraction tables, such as ERP application activity, Collector directory data, and Namespace data.

-   **[View ERP extraction tables](../task/view-etl-data-sources.md)**  
Work with ETL \(extract, transform, and load\) processes in ERP Data Hub to extract large amounts of ERP \(Enterprise Resource Planning\) data from the ERP system. Extracted data is stored in Glide tables in the ServiceNow AI Platform.
-   **[Add a new ERP extraction table in ERP Data Hub](../task/erp-canvas-add-new-extraction-table.md)**  
Create an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record every day, and save the data to a transformation \(staging\) table. The data is then available on the ServiceNow AI Platform, and you can add the extracted data to an ERP model or remote table.
-   **[Select fields for an extraction table in ERP Data Hub](../task/erpc-select-extraction-table-fields.md)**  
Add or remove fields for an extraction table in ERP Data Hub. For example, you may want to remove fields with sensitive information, such as birthdays.
-   **[Create a scheduled extraction](../task/erpc-create-a-scheduled-extraction.md)**  
Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.
-   **[Monitor ERP Data Hub logged extraction and remote lookup transactions](../task/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md)**  
Use the new monitoring feature to track each ERP transaction and its progress. Filter the ERP Data Hub task information, such as successes, failures, and more, as needed.

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)


---
title: ERP data extraction and transformation
description: ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in Zero Copy Connector for ERP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extract, extraction table]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# ERP data extraction and transformation

ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in Zero Copy Connector for ERP.

## Hold large amounts of data in extraction tables

Use extraction tables, which are ETL \(extract, transform, and load\) data sources, to extract large amounts of data regularly.

For example, you can extract all open purchase orders for the current month from an SAP system into a Glide table once a day at a set time. You can then access that data via ServiceNow AI Platform, such as Source-to-Pay Operations or a PO workspace created in App Engine Studio.

After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/import-sets-landing-page.md).

## Extraction tables use transform table maps

ERP extraction tables save data to a local transform table on the ServiceNow AI Platform. The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination. For example, after import, the extraction table can run a Glide query on a transform table and save the output to several different target tables.

If you use a custom transform table, you must first create the table on the ServiceNow AI Platform, and the table must be in the application scope. For more information on creating table transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).

ETL processes in Zero Copy Connector for ERP are configured in the ServiceNow AI Platform app that needs the data, not Zero Copy Connector for ERP. For example, you can configure an extraction process in a flow in Workflow Studio.

## Automatically available standard extraction tables

When you install Zero Copy Connector for ERP, the ServiceNow AI Platform automatically loads a standard set of ERP extraction tables, including sales, delivery, and procurement tables. For a list of standard extraction tables, see [Standard extraction tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-standard-extraction-tables.md).

If you installed ERP Semantic Mining, that app populates some additional extraction tables, such as ERP application activity, Collector directory data, and Namespace data.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.


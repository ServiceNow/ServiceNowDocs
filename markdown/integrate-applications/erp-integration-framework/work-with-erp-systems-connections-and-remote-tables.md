---
title: Using Zero Copy Connector for ERP
description: Use Zero Copy Connector for ERP to work with ERP \(Enterprise Resource Planning\) models, remote tables, and extraction tables to integrate ERP data from the system of record onto the ServiceNow AI Platform.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, connect, remote, table, remote table, model, extract, extraction table]
breadcrumb: [Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Using Zero Copy Connector for ERP

Use Zero Copy Connector for ERP to work with ERP \(Enterprise Resource Planning\) models, remote tables, and extraction tables to integrate ERP data from the system of record onto the ServiceNow AI Platform.

The workflow of Zero Copy Connector for ERP generally follows its main sections, each of which you access by selecting the section icon in the contextual side panel.

You can also build flows in Workflow Studio to use retrieved ERP data for processes or tasks outside of Zero Copy Connector for ERP. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

Build an ERP model using remote tables and extraction tables to organize, load, and transform ERP data, as well as flows to query the ERP system.

<table id="table_fjx_zj2_5xb"><thead><tr><th>

Zero Copy Connector for ERP section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP models

</td><td>

Models function as templates for sets of tables that give you access to ERP data. You can use the standard Zero Copy Connector for ERP models as-is, or clone them to make changes.Manage models to map input and output data for reading and updating the ERP system using wither table read operations or BAPIs \(Business Application Programming Interface\).

For more information, see [Building and managing models to work with ERP data](work-with-erp-data-models.md).

</td></tr><tr><td>

Flows to query ERP data

</td><td>

Build a flow in Workflow Studio to specify details for querying the ERP system using the parameters specified in the model.

</td></tr><tr><td>

Remote tables

</td><td>

Remote tables enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.For more information, see [Using ERP remote tables in Zero Copy Connector for ERP](erp-canvas-work-with-remote-tables.md).

</td></tr><tr><td>

ERP extraction tables

</td><td>

Extraction tables use an ETL process to extract large amounts of data from the ERP system at regular intervals and transform and save them to a Glide table.For more information, see [Extracting and transforming data in Zero Copy Connector for ERP](erp-canvas-extraction-tables.md).

</td></tr></tbody>
</table>-   **[Building and managing models to work with ERP data](work-with-erp-data-models.md)**  
Models in Zero Copy Connector for ERP function as templates for sets of tables that give you access to ERP data. Use model management to build read, update, and create operations that access the ERP system. The operations have specified inputs and outputs to map fields for use on the ServiceNow AI Platform.
-   **[Next steps after extracting data from your ERP system using Zero Copy Connector for ERP](erpi-next-steps-replatforming.md)**  
After you identify and extract ERP data with Zero Copy Connector for ERP, you can use that data on the ServiceNow AI Platform as the data source for products and apps.
-   **[Managing ERP development pipelines in Zero Copy Connector for ERP](manage-erp-tables-pipelines.md)**  
Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.
-   **[Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md)**  
After you configure an operation in Zero Copy Connector for ERP, you can build a flow in Workflow Studio to specify details for querying the ERP \(Enterprise Resource Planning\) system. For example, build a flow that filters by Order ID.
-   **[Using ERP remote tables in Zero Copy Connector for ERP](erp-canvas-work-with-remote-tables.md)**  
Enterprise Resource Planning \(ERP\) remote tables in Zero Copy Connector for ERP enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.
-   **[Extracting and transforming data in Zero Copy Connector for ERP](erp-canvas-extraction-tables.md)**  
ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in Zero Copy Connector for ERP.

**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)


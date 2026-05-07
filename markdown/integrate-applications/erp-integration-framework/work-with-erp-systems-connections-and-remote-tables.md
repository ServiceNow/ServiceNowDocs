---
title: Using Zero Copy Connector for ERP
description: Use Zero Copy Connector for ERP \(Enterprise Resource Planning\) to work with ERP models, remote tables, and extraction tables, and integrate ERP data from the system of record onto the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, connect, remote, table, remote table, model, extract, extraction table]
breadcrumb: [Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Using Zero Copy Connector for ERP

Use Zero Copy Connector for ERP \(Enterprise Resource Planning\) to work with ERP models, remote tables, and extraction tables, and integrate ERP data from the system of record onto the ServiceNow AI Platform.

The workflow of Zero Copy Connector for ERP generally follows its main sections, each of which you access by selecting the section icon in the contextual side panel.

You can also build flows in Workflow Studio to use retrieved ERP data for processes or tasks outside of Zero Copy Connector for ERP.

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
Models in Zero Copy Connector for ERP \(Enterprise Resource Planning\) function as templates for sets of tables that give you access to ERP data. Use model management to build read, update, and create operations that access the ERP system. The operations have specified inputs and outputs to map fields for use on the ServiceNow AI Platform.
-   **[Retrieving data](erp-retrieving-data.md)**  
To retrieve data from an ERP \(Enterprise Resource Planning\) system, use remote tables or extraction tables.
-   **[Building with ERP data](erp-canvas-building-with-erp-data.md)**  
Use data extracted from ERP systems, such as SAP, to build applications, workflows, playbooks, and more.

**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)


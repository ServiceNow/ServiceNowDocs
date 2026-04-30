---
title: Using ERP models, extraction tables, and remote tables
description: Use ERP Data Hub to work with ERP \(Enterprise Resource Planning\) models, remote tables, and extraction tables to integrate ERP data from the system of record onto the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Using ERP models, extraction tables, and remote tables

Use ERP Data Hub to work with ERP \(Enterprise Resource Planning\) models, remote tables, and extraction tables to integrate ERP data from the system of record onto the ServiceNow AI Platform.

The workflow of ERP Data Hub generally follows its main sections, each of which you access by selecting the section icon in the contextual side panel.

![ERP data models refer to extraction tables and remote tables to create data used by apps](../image/erp-data-model-infographic.jpg "Data models and ERP data")

You can also build flows in Workflow Studio to use retrieved ERP data for processes or tasks outside of ERP Data Hub. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

Build an ERP model using remote tables and extraction tables to organize, load, and transform ERP data, as well as flows to query the ERP system.

<table id="table_fjx_zj2_5xb"><thead><tr><th>

ERP Data Hub section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP models

</td><td>

ERP models function as templates for sets of tables that give you access to ERP data. You can use the standard ERP Data Hub models as-is, or clone them to make changes.Manage models to map input and output data for reading and updating the ERP system using wither table read operations or BAPIs \(Business Application Programming Interface\).

For more information, see [Building and managing ERP models to work with ERP data](work-with-erp-data-models.md).

</td></tr><tr><td>

Flows to query ERP data

</td><td>

Build a flow in Workflow Studio to specify details for querying the ERP system using the parameters specified in the model.

</td></tr><tr><td>

Remote tables

</td><td>

Remote tables enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.For more information, see [Using ERP remote tables in ERP Data Hub](erp-canvas-work-with-remote-tables.md).

</td></tr><tr><td>

ERP extraction tables

</td><td>

Extraction tables use an ETL process to extract large amounts of data from the ERP system at regular intervals and transform and save them to a Glide table.For more information, see [Extracting and transforming data in ERP Data Hub](erp-canvas-extraction-tables.md).

</td></tr></tbody>
</table>-   **[Building and managing ERP models to work with ERP data](work-with-erp-data-models.md)**  
ERP \(Enterprise Resource Planning\) models function as templates for sets of tables that give you access to ERP data. Use model management to create read and update operations that access the ERP system with specified inputs and outputs to map fields for use on the ServiceNow AI Platform.
-   **[Next steps after extracting data from your ERP system using ERP Data Hub](erpi-next-steps-replatforming.md)**  
After you identify and extract ERP \(Enterprise Resource Planning\) data with ERP Data Hub, you can use that data on the ServiceNow AI Platform as the data source for products and apps.
-   **[Managing ERP development pipelines in ERP Data Hub](manage-erp-tables-pipelines.md)**  
Move your ERP \(Enterprise Resource Planning\) systems, ERP models, tables, operations, and flows from a development instance to a production environment when they're ready.
-   **[Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md)**  
After you configure an operation in ERP Data Hub, you can build a flow in Workflow Studio to specify details for querying the ERP \(Enterprise Resource Planning\) system. For example, build a flow that filters by Order ID.
-   **[Connect ERP Data Hub to SAP using OData and HTTP](erp-canvas-use-odata-and-http-connection.md)**  
Extract data securely from ERP OData APIs using ETL for use in remote tables and extraction tables. OData connects to SAP via HTTP.
-   **[Using ERP remote tables in ERP Data Hub](erp-canvas-work-with-remote-tables.md)**  
ERP \(Enterprise Resource Planning\) remote tables in ERP Data Hub enable you to view and query data from the ERP system of record on the ServiceNow AI Platform.
-   **[Extracting and transforming data in ERP Data Hub](erp-canvas-extraction-tables.md)**  
ERP \(Enterprise Resource Planning\) extraction tables enable you to create daily processes that extract large amounts of data. You can then include the extracted data in an ERP model in ERP Data Hub.

**Parent Topic:**[ERP Data Hub](erp-integration-overview.md)


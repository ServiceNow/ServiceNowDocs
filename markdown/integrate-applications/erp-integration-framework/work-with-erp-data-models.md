---
title: Building and managing models to work with ERP data
description: Models in Zero Copy Connector for ERP function as templates for sets of tables that give you access to ERP data. Use model management to build read, update, and create operations that access the ERP system. The operations have specified inputs and outputs to map fields for use on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, platform, entity, entities, operation, input, output, map, field, data]
breadcrumb: [Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Building and managing models to work with ERP data

Models in Zero Copy Connector for ERP function as templates for sets of tables that give you access to ERP data. Use model management to build read, update, and create operations that access the ERP system. The operations have specified inputs and outputs to map fields for use on the ServiceNow AI Platform.

## Models represent datasets and create a staging area

A model represents the logical structure and organization of data coming from the ERP system. Models define the entities, attributes, read/update operations, and table join relationships that capture and represent business processes and data elements in the ERP system.When you first open Zero Copy Connector for ERP, you view a list of the models for your instance.

There are two types of models:

-   Platform model: Model with input and output fields mapped to an already existing platform table. These models standardize ERP data by mapping it to ServiceNow standardized platform tables.
-   ERP model: New, custom ERP model. These models follow the data structures defined by the connected, external ERP system. ERP models accommodate the unique formats of each ERP system.

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard ERP models and extraction tables for Zero Copy Connector for ERP](../reference/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a new ERP model](../task/erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](erp-canvas-content-packs.md).

A model serves as a blueprint for configuring, customizing, and integrating the ERP system to meet your business requirements. A model functions as a staging area that contains all potential fields you can add to remote and extraction tables, as well as, create, read, and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

You can also build flows in Workflow Studio to use retrieved ERP data for processes or tasks outside of Zero Copy Connector for ERP.

You can view the list of existing models or add a new one to create a custom dataset. After you add a remote table, you can manage models to map input and output parameters, update the ERP system using BAPIs, and create table joins. You can also create extraction tables that regularly pull large amounts of filtered data from the ERP system. Another option is to use a custom ERP action in Workflow Studio to use queried ERP data in other ServiceNow AI Platform processes.

You can create as many models as needed, though you can't edit their field names. The sn\_erp\_integration.erp\_admin role is required to create and edit models.

## How models are structured

Each model is linked to ERP tables on the system of record, as well as remote tables and ERP extraction tables on the ServiceNow AI Platform. You can connect the same table to multiple different models.

Models are connected to an ERP system, one ERP system for each model. The connected ERP system:

-   Enables access to field and table information.
-   Helps coordinate data synchronization, sharing, and collaboration, enabling seamless integration and operation between the model and the ERP system.

Models encompass remote tables from the system of record, as well as APIs, ERP extraction tables, and create/read/update operations, to create a holistic dataset. For example, you can have one model for sales orders and another for inventory.

**Note:**

After installing Zero Copy Connector for ERP, an admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property so users can customize models. After enabling the **sn\_erp\_integration.enableModelModification** property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or by directly entering `sys_properties.list` in the Navigator Filter.

## Managing models to perform create, read, and update operations on ERP systems

After you create or clone a model, you can specify how Zero Copy Connector for ERP reads, writes, and creates on the ERP system using the model manager page. When managing models, you have the option to use a BAPI, which is a remote procedure SAP function call that's similar to an API.

Each model can have only one create, one read, and one update operation defined.

For more information, see [Managing how models read and update the ERP system](erpc-managing-models-read.md).

-   **[Zero Copy Connector for ERP content packs](erp-canvas-content-packs.md)**  
Use Zero Copy Connector for ERP content packs as examples to help you implement and deploy applications with less manual work.
-   **[View and edit the foundation of ERP models](../task/view-and-work-with-erp-data-models.md)**  
Create a holistic dataset by building ERP models in Zero Copy Connector for ERP, which encompasses remote tables and extraction tables from the ERP system, as well as create, read, and update operations.
-   **[Using model versioning](../task/erp-use-model-versioning.md)**  
Use model versioning in Zero Copy Connector for ERP to determine the version of a model on development and production instances.
-   **[Clone an ERP model in Zero Copy Connector for ERP](../task/erp-canvas-clone-data-model.md)**  
Clone a standard ERP \(Enterprise Resource Planning\) model that ships with Zero Copy Connector for ERP. After you clone the model you can make modifications, such as adding new fields or tables.
-   **[Create a new ERP model](../task/erpc-add-new-data-model.md)**  
Add a model in Zero Copy Connector for ERP to create a dataset containing ERP tables from the system of record to read and send updates to the ERP system.
-   **[Export and import custom models in Zero Copy Connector for ERP](../task/erpc-export-and-import-custom-models.md)**  
Move a custom ERP model from one instance to another by exporting and importing a remote update set.
-   **[Managing how models read and update the ERP system](erpc-managing-models-read.md)**  
After you create an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP, you can specify how it reads and updates the ERP system using parameters.
-   **[Add an operation to a model in Zero Copy Connector for ERP](../task/erpc-manage-models-read-op.md)**  
Add an operation to an ERP model in Zero Copy Connector for ERP to define how the model retrieves data, writes data, or creates a new instance of the business object.
-   **[Set operation-level security on a model](erp-canvas-set-operation-level-security-on-a-model.md)**  
Control access to model operations with user roles and groups.
-   **[Add an entity to a model](add-an-entity-to-model.md)**  
Specify the operation entity that Zero Copy Connector for ERP uses for read, update, or create operations.
-   **[Add joins between ERP tables](../task/erp-canvas-add-join-data-model.md)**  
Link multiple ERP \(Enterprise Resource Planning\) tables from the system of record to build an ERP model in Zero Copy Connector for ERP using table joins.
-   **[Manage input parameters for a Zero Copy Connector for ERP model operation](../task/erpc-manage-model-inputs.md)**  
Specify how fields on the ERP system map to input parameters and their values to define the inputs for an operation that reads, creates, or updates the system of record from Zero Copy Connector for ERP.
-   **[Choose output parameters for a model](../task/erp-canvas-manage-outputs.md)**  
Specify output parameters for a read or update operation in Zero Copy Connector for ERP to define how fields and parameters are mapped from the ERP system to the ServiceNow AI Platform. Output parameters also define how returned data is stored on the ServiceNow AI Platform.
-   **[Edit input and output mapped value name in Zero Copy Connector for ERP](../task/erp-edit-mapped-value-name-in-model-manager.md)**  
Manually edit mapped value field names for input and output when managing models.
-   **[Specifying where ERP system data is saved](erpc-call-response-data.md)**  
Data that Zero Copy Connector for ERP retrieves from ERP \(Enterprise Resource Planning\) systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.
-   **[Debug Zero Copy Connector for ERP models](../task/debug-zero-copy-connector-for-erp-models.md)**  
Use the debug models option in Zero Copy Connector for ERP to see a log capturing the probe payload, payload response, status, and other information.

**Parent Topic:**[Using Zero Copy Connector for ERP](work-with-erp-systems-connections-and-remote-tables.md)


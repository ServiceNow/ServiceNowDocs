---
title: Building and managing ERP models to work with ERP data
description: ERP \(Enterprise Resource Planning\) models function as templates for sets of tables that give you access to ERP data. Use model management to create read and update operations that access the ERP system with specified inputs and outputs to map fields for use on the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Building and managing ERP models to work with ERP data

ERP \(Enterprise Resource Planning\) models function as templates for sets of tables that give you access to ERP data. Use model management to create read and update operations that access the ERP system with specified inputs and outputs to map fields for use on the ServiceNow AI Platform.

## ERP models represent data sets and create a staging area

An ERP model represents the logical structure and organization of data coming from the Enterprise Resource Planning system. ERP models define the entities, attributes, read/update operations, and table join relationships that capture and represent business processes and data elements in the ERP system.When you first open ERP Data Hub, you view a list of the ERP models for your instance.

ERP Data Hub provides a standard set of ERP models, such as SAP Material Stock and SAP Purchase Document. You can also build new models. For a list of standard ERP models, which you must clone to modify, see [Standard ERP models and extraction tables for ERP Data Hub](../reference/erp-canvas-standard-extraction-tables.md).

The ERP model serves as a blueprint for configuring, customizing, and integrating the ERP system to meet your business requirements. An ERP model functions as a staging area that contains all potential fields you can add to remote and extraction tables, and read and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform.

You can also build flows in Workflow Studio to use retrieved ERP data for processes or tasks outside of ERP Data Hub. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

You can view the list of existing ERP models or add a new one to create a custom data set. After you add a remote table, you can manage models to map input and output parameters, update the ERP system using BAPIs \(Business Application Programming Interface\), and create table joins. You can also create extraction tables that regularly pull large amounts of filtered data from the ERP system. Another option is to use a custom ERP action in Workflow Studio to use queried ERP data in other ServiceNow AI Platform processes.

You can create as many ERP models as needed, though you can't edit their field names.

## How ERP models are structured

Each model is linked to ERP tables on the system of record, as well as remote tables and ERP extraction tables on the ServiceNow AI Platform. You can connect the same table to multiple, different ERP models.

ERP models are connected to an ERP system, one ERP system for each model. The connected ERP system:

-   Enables access to field and table information.
-   Helps coordinate data synchronization, sharing, and collaboration, enabling seamless integration and operation between the ERP model and the ERP system.

ERP models in ERP Data Hub encompass remote tables from the system of record, as well as APIs and ERP extraction tables and read/update operations, to create a holistic data set. For example, you can have one ERP model for sales orders and another for inventory.

**Note:**

After you install ERP Data Hub, you must enable the **sn\_erp\_integration.enableModelModification** property so users can customize ERP models. After you enable the **sn\_erp\_integration.enableModelModification** property, ERP Data Hub retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or by directly typing `sys_properties.list` in the Navigator Filter.

## Managing models to read and update ERP systems

After you create or clone an ERP model, you can specify how ERP Data Hub reads and writes to the ERP system using the ERP model manager page. When managing models, you have the option to use a BAPI, which is a remote procedure SAP function call that's similar to an API.

Each model can have only one read and one update operation defined.

For more information, see [Managing how models read and update the ERP system](erpc-managing-models-read.md).

-   **[View and edit the foundation of ERP models](../task/view-and-work-with-erp-data-models.md)**  
Create a holistic data set by building ERP \(Enterprise Resource Planning\) models in ERP Data Hub, which encompasses remote tables and extraction tables from the ERP system, as well as read and update operations.
-   **[Clone an ERP model in ERP Data Hub](../task/erp-canvas-clone-data-model.md)**  
Clone a standard ERP \(Enterprise Resource Planning\) model that ships with ERP Data Hub. After you clone the model you can make modifications, for example, by adding new fields or tables.
-   **[Add a new ERP model](../task/erpc-add-new-data-model.md)**  
Add an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to create a data set that contains ERP tables from the system of record, and enables you to read and send updates to the ERP system.
-   **[Managing how models read and update the ERP system](erpc-managing-models-read.md)**  
After you create an ERP \(Enterprise Resource Planning\) model in ERP Data Hub, you can specify how it reads and updates the ERP system using parameters.
-   **[Add an operation to a model in ERP Data Hub](../task/erpc-manage-models-read-op.md)**  
Add an operation to an ERP \(Enterprise Resource Planning\) model in ERP Data Hub to define how it retrieves data from or writes data to the ERP system, or creates a new instance of the business object.
-   **[Add a read, update, or create entity to a model in ERP Data Hub](../task/erpc-add-entity-to-model-op.md)**  
Specify the operation entity, which is the table or BAPI \(Business Application Programming Interface\) that ERP Data Hub uses for read, update, or create operations.
-   **[Add joins between ERP tables](../task/erp-canvas-add-join-data-model.md)**  
Link multiple ERP \(Enterprise Resource Planning\) tables from the system of record to build an ERP model in ERP Data Hub using table joins.
-   **[Manage input parameters for an ERP Data Hub model operation](../task/erpc-manage-model-inputs.md)**  
Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values to define the inputs for an operation that reads or updates the system of record from ERP Data Hub.
-   **[Choose output parameters for an ERP model](../task/erp-canvas-manage-outputs.md)**  
Specify output parameters for an ERP \(Enterprise Resource Planning\) system read or update operation in ERP Data Hub to define how fields and parameters are mapped from the ERP system to the ServiceNow AI Platform. Output parameters also define how returned data is stored on the ServiceNow AI Platform.
-   **[Specifying where the ERP system data is saved](erpc-call-response-data.md)**  
Data that ERP Data Hub retrieves from ERP \(Enterprise Resource Planning\) systems can be used in remote tables, extraction tables, and added to flows as data pills in Workflow Studio.

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)


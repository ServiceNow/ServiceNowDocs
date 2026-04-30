---
title: Managing how models read and update the ERP system
description: After you create an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP, you can specify how it reads and updates the ERP system using parameters.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, read, update, operation, entity, entities]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Managing how models read and update the ERP system

After you create an ERP \(Enterprise Resource Planning\) model in Zero Copy Connector for ERP, you can specify how it reads and updates the ERP system using parameters.

You must have the sn\_erp\_integration.erp\_admin role to create and edit models.

When creating a read or update operation, first add the operation. Then define operation entities and parameters in the following tabs of the ERP model manager page.

-   **Manage entities**: Specify the table to read, OData service, or BAPI \(remote procedure call that's similar to an API\) to use for reading or updating the ERP system.
-   **Specify inputs**: Define how fields on the ERP system map to parameters to specify how data is queried. If parameters can't be retrieved, you can also define any default values to pass to the ERP system.
-   **Choose output**: Define parameters for how returned data is stored on the ServiceNow AI Platform by specifying outputs.

## Create, read, and update operations for ERP system

Zero Copy Connector for ERP contacts the ERP system using create, read, and update operations.

-   Use a BAPI, RFC, read table, or OData to read the ERP system.
-   Add either table reads or a BAPI function call to a model for read operations, but not both.
-   You can add multiple tables to a table read operation, but you can specify only one BAPI for a function call read operation.
-   Use a BAPI, RFC, OData, or IDoc for update operations.
-   Use a BAPI, RFC, OData, or IDoc for create operations.

## Managing tables and entities for ERP operations

An entity is the foundation of how the operation accesses the ERP system to read or update it. Use the **Manage entities** tab to define requests and the content of their responses by specifying the BAPI or name of the table.

When you add an entity to an operation, you must specify the following information:

-   How Zero Copy Connector for ERP retrieves data from or sends updates to the ERP system.
-   The name of the entity.

For instructions on adding entities, see [Add an operation to a model in Zero Copy Connector for ERP](../task/erpc-manage-models-read-op.md).

## Managing operation input parameters

After you specify the entity, Zero Copy Connector for ERP automatically populates the **Specify inputs** tab with the required input parameters.

Zero Copy Connector for ERP uses parameters as part of the method/function call to define and map data that's passed to the ERP system.

-   The Output parameters section is where you enter optional default values for parameters that are used to query the ERP system. If no input value is provided when querying the model, the **Default value** for each parameter is used as a fallback. Default values can also be used for mapping constants.
-   The Tables \(for read operations\)/Function call \(for BAPI operations\) section is where you define and map fields from the ERP system that Zero Copy Connector for ERP sends as parameters in the operation. When you select a field, use the automap functionality to update its **Mapped value** automatically and add a row for the parameter to the Output parameters section. If you define a `Constant` as the **Type** and enter the constant value in the **Mapped value** field, mapped inputs can act as filter criteria. You can add and nest as many related parameters as needed.

    If you're adding a complex, nested parameter, such as an address that includes other parameters \(for street, for city, etc.\), Zero Copy Connector for ERP automatically identifies that it needs additional related parameters. Zero Copy Connector for ERP creates new, nested parameter rows that you must then populate with the related values. You can nest only parameters with **Object** or **Array** as the **Data type**.


The available data types for parameters are:

-   Object
-   Array
-   String
-   Date Time
-   Date
-   Time
-   Char
-   Decimal

**Note:**

An example use case is running a sales order BAPI to find out what items are in an order. You must specify the order ID as a mapped field in the Tables \(for read operations\)/Function call \(for BAPI operations\) section, using the automap option to define which field is referenced in the **Mapped value** field. After defining all operation inputs and outputs, you can build a flow in Workflow Studio. In the flow, enter the order ID as the parameter in use when the flow runs to call the ERP system.

Another example would be adding a parameter for **Order billing dates** in the Table fields \(for table read operations\)/Function call \(for BAPI operations\) section. Then build a flow in Workflow Studio that enables you to specify a date or date range to retrieve all orders from that time period.

**Note:** It doesn't matter what order you define parameters in. Zero Copy Connector for ERP displays optional parameters in alphabetical order when you save.

For instructions on managing inputs, see [Manage input parameters for a Zero Copy Connector for ERP model operation](../task/erpc-manage-model-inputs.md).

## Selecting outputs for a read operation

You must create output parameters to define how the data is mapped to the ERP system and stored on the ServiceNow AI Platform.

For instructions on managing outputs, see [Choose output parameters for a model](../task/erp-canvas-manage-outputs.md).

## Adding retrieved ERP fields to tables

When you add mapped fields or parameters as outputs and successfully read or update the ERP system, each parameter appears as a field. You can then add the field to a remote table or an extraction table. Manage the fields for the remote table or extraction table to add the retrieved parameters. For more information, see the following topics:

-   [Customize fields for an ERP remote table in Zero Copy Connector for ERP](../task/erp-canvas-build-remote-table.md)
-   [Select fields for an extraction table in Zero Copy Connector for ERP](../task/erpc-select-extraction-table-fields.md)

## Building flows to call the ERP system

After all parameters are defined and you have built and run the read or update operation, build a flow in Workflow Studio that uses the defined parameters.

Enter any filter criteria by specifying a value when you select the parameter in the **Mandatory Field** of the flow's action. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

**Parent Topic:**[Building and managing models to work with ERP data](work-with-erp-data-models.md)


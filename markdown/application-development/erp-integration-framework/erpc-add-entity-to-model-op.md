---
title: Add a read, update, or create entity to a model in ERP Data Hub
description: Specify the operation entity, which is the table or BAPI \(Business Application Programming Interface\) that ERP Data Hub uses for read, update, or create operations.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Add a read, update, or create entity to a model in ERP Data Hub

Specify the operation entity, which is the table or BAPI \(Business Application Programming Interface\) that ERP Data Hub uses for read, update, or create operations.

## Before you begin

You must have already added the read, write, or create operation before you can add an entity to it. For more information, see [Add an operation to a model in ERP Data Hub](erpc-manage-models-read-op.md).

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

-   Read operations retrieve ERP data by either reading a table or using a BAPI.
-   Update operations use a BAPI to write updates to the ERP system.
-   Create operation creates a new instance of the business object in the SAP system. \(Available starting in Xanadu Store Release 2\)

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP model page by selecting the ERP model icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the model that you want to add an operation entity to.

4.  Select the **Manage model** button.

5.  Select **Add entity** on the **Manage entities** tab.



    ![Add operation entities on the Manage entities tab](../image/erpc-manage-entities-manager.png)

6.  For read operations, specify the type of read operation in **Select type**.

    -   **Read table** defines a read operation entity that retrieves data by reading it directly from a table on the ERP system.
    -   **Function call \(BAPIs\)** defines a read operation entity that uses a BAPI remote procedure call.
    -   **Function call \(RFCs\)** defines a read operation entity that uses an RFC call.
    -   **OData** enables you to work with various business objects \(for example, read, create, update, and delete\) defined in the ERP system.
    **Note:** Update operation entities must use a BAPI Function call, so this field is read only for update operations.

    ![Select the type of entity you're adding](../image/erpc-add-entity-manager.png "Add an entity")

7.  Define the entity by specifying the name of the table to read or BAPI to use in **Select entity**.

    The AI Search for this field can help you find what you're looking for faster, for example by entering `Countries` instead of `T005`. AI Search also suggests tables and BAPIs that are in the connected ERP system.

    For table read operations, you may need to check the **Model entities** tab of the current or another, related model to get the table name, or ask your SAP admin. For more information, see [View and edit the foundation of ERP models](view-and-work-with-erp-data-models.md).

8.  When you're finished, select **Add entity**.

9.  Rearrange and delete table entities as needed.

    **Important:** Reordering deletes any existing table joins for the reordered entities.

    1.  Select **Rearrange order**.

    2.  Drag the tables to the order that you want.

    3.  Select the delete icon \(![Delete icon](../../../reuse/icons/product-icons/trash-outline-24.svg)\) on the card for a table to remove any tables you don't need.

        Deleting an entity removes all of its related field mappings and table joins.

    4.  Select **Confirm reorder**.


## Result

The entity is added to the operation. ERP Data Hub connects to the ERP system using the specified entity and retrieves data that you can use to define input and output parameters.

When you view the entity on the **Manage operation entities** page, a status shows whether the ServiceNow AI Platform is retrieving data or has finished retrieving data.

If you added a **Read table** operation, you can repeat this process to add as many tables as necessary to the operation. Then you can add joins to create relationships between tables.

**Note:** If you have more than one table for an operation, you must join the tables.

For more information, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).

The **Entity fields** tab for the ERP model automatically populates for the new table when the table is connected to an ERP system. View their details as needed. For more information, see [ERP Data Hub ERP model table field descriptions](../reference/erp-canvas-erp-data-model-table-fields.md).

## What to do next

Next, you must specify the input parameters for the operation. For details, see [Manage input parameters for an ERP Data Hub model operation](erpc-manage-model-inputs.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)


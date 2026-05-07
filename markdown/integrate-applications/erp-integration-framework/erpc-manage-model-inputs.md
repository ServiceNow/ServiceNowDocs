---
title: Manage input parameters for a Zero Copy Connector for ERP model operation
description: Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values to define the inputs for an operation that reads, creates, or updates the system of record from Zero Copy Connector for ERP.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, input, parameter, operation, read, create, update, crud]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Manage input parameters for a Zero Copy Connector for ERP model operation

Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values to define the inputs for an operation that reads, creates, or updates the system of record from Zero Copy Connector for ERP.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

If you're already in the process of managing a model and ready to specify inputs, you can skip to step 5.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model with the operation that you want to add inputs to.

4.  Select **Manage model**.

5.  Open a model operation.

    If you don't have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

6.  Check that at least one entity is listed.

    If you don't have an entity, add one to the operation. For more information, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

7.  Select **Specify inputs**.

    The required parameters for the operation appear in both of the following places:

    -   The Operation parameters section.
    -   The Table/Functioncall section, where you define the parameters the operation uses. The Table section appears for read operations, and the Functioncall section appears for BAPI \(Business Application Programming Interface\) operations.

        Zero Copy Connector for ERP automatically suggests mappings between table fields in source systems and target models. For example, map the fields of source table "purchase order - v2" with the fields of a relevant target table such as "platform table purchase order." This reduces the amount of manual work to do, while still giving you control to edit the mappings as needed. For more information, see [Zero Copy Connector for ERP semantic mapping](../reference/erp-semantic-mapping.md).

        Mapped value names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](erp-edit-mapped-value-name-in-model-manager.md).

    ![Specify inputs page with validation rules and table sections expanded.](../image/erpc-specify-inputs-manager-ys2.png)

8.  Define whether the operation inputs are required by expanding the **Validation rules** section and selecting an option in **Query validation rule**.

    -   **All inputs are mandatory**
    -   **At least one input is mandatory**
    -   **No inputs are mandatory**
9.  Review the required and optional parameters that are already defined for the operation to understand what you must add.

10. Define a new input parameter to be sent when querying the ERP system.

    For table read operations, a Tables section appears in the mapped table fields section for each defined table entity. Make sure that you're adding the parameter for the correct table.

    **Note:** It doesn't matter what order you define parameters in. Zero Copy Connector for ERP displays optional parameters in alphabetical order when you save.

    1.  Select **+ New input** below the last-defined parameter in the table.

        ![Table expanded to show inputs and new input button highlighted.](../image/erpc-specify-input-new-input.png)

        **Note:** When you add an input field, the field is automatically added as a field in the output. The field is listed and is read only in the **Prepopulated outputs** section on the output page.

    2.  Fill in the fields to define the parameter.

<table id="table_jp5_t43_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field label

</td><td>

Name of the field from the ERP system that you're defining as a parameter. Zero Copy Connector for ERP automatically retrieves fields from the table defined in the operation entity.

</td></tr><tr><td>

Field name

</td><td>

\(Read-only\) Name of the field in the ERP system.

</td></tr><tr><td>

Data type

</td><td>

\(Read-only\) Automatically populated value that specifies the type of data the parameter contains.

</td></tr><tr><td>

Mapping type

</td><td>

Definition of how the parameter is sent.-   **Input** parameters have their **Mapped value** automatically populated.
-   **Constant** defines a parameter whose value never changes, for example, to use as filter criteria. You must specify the value in the parameter's **Mapped value** field.
-   **Outer or Inner Join** \(table read operations only\) indicates that you're creating a table join. For more information, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).


</td></tr><tr><td>

Mapped value

</td><td>

Specific value of the parameter.-   For **Input** parameters, accept the system-generated name or edit the name. For more information about editing mapped values, see [Edit input and output mapped value name in Zero Copy Connector for ERP](erp-edit-mapped-value-name-in-model-manager.md).
-   For **Constant** parameters, enter a set value that's always sent for the parameter.
-   For **Outer or Inner Join** parameters, select the field to join the parameter with. For details on creating joins, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).


</td></tr></tbody>
</table>    If you're adding a complex, nested parameter, such as an address that includes other parameters \(for street, for city, etc.\), Zero Copy Connector for ERP automatically identifies that it needs additional related parameters. Zero Copy Connector for ERP creates new, nested parameter rows that you must then populate with the related values. You can nest only parameters with **Object** or **Array** as the **Data type**.

11. Remove any optional parameters that you don't need when querying the ERP system by selecting the remove \(X\) icon.

12. Make any additional edits to existing parameters.

    The following example shows an input with nested inputs for a BAPI.

    ![Table expanded to show inputs with a nested input highlighted.](../image/erpc-specify-input-nested.png)

13. Select **Save**.


## What to do next

Next, check the output parameters for the operation and update as needed. For more information, see [Choose output parameters for a model](erp-canvas-manage-outputs.md).

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)


---
title: Manage input parameters for an ERP Data Hub model operation
description: Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values to define the inputs for an operation that reads or updates the system of record from ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Manage input parameters for an ERP Data Hub model operation

Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values to define the inputs for an operation that reads or updates the system of record from ERP Data Hub.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

If you're already in the process of managing a model and ready to specify inputs, you can skip to step 5.

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub** &gt; **ERP Data Hub Home**.

2.  Open the ERP model page by selecting the ERP model icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the model with the operation that you want to add inputs to.

4.  Select the **Manage model** button.

5.  Open a model operation.

    If you do not have a model operation, add one to the model. For more information, see [Add an operation to a model in ERP Data Hub](erpc-manage-models-read-op.md).

6.  Open an entity.

    If you do not have an entity, add one to the operation. For more information, see [Add a read, update, or create entity to a model in ERP Data Hub](erpc-add-entity-to-model-op.md)

7.  Select **Specify inputs**.

    The required parameters for the operation appear in both of the following places:

    -   The Operation parameters section, where you define any default values to use if the operation fails.
    -   The Tables/Function call section, where you define the parameters the operation uses. The Table section appears for read operations, and the Function call section appears for BAPI \(Business Application Programming Interface\) operations.
    ![Specify input parameters](../image/erpc-specify-inputs-manager.png "Manage inputs")

8.  Define whether the operation inputs are required in the **Query validation rule** field.

    -   **All inputs are mandatory**
    -   **At least one input is mandatory**
    -   **No inputs are mandatory**
9.  Review the required and optional parameters that are already defined for the operation and note what you must add.

10. Define a new input parameter to be sent when querying the ERP system.

    For table read operations, a Tables section appears in the mapped table fields section for each defined table entity. Make sure that you're adding the parameter for the correct table.

    **Note:** It doesn't matter what order you define parameters in. ERP Data Hub displays optional parameters in alphabetical order when you save.

    1.  Select the add icon \(+\) next to the last-defined parameter.

    2.  Fill in the fields to define the parameter.

<table id="table_jp5_t43_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name of the field from the ERP system that you're defining as a parameter. ERP Data Hub automatically retrieves fields from the table defined in the operation entity.

</td></tr><tr><td>

Data type

</td><td>

\(Read-only\) Automatically populated value that specifies the type of data the parameter contains.

</td></tr><tr><td>

Type

</td><td>

Definition of how the parameter is sent.-   **Input** parameters have their **Mapped value** automatically populated.
-   **Constant** defines a parameter whose value never changes, for example, to use as filter criteria. You must specify the value in the parameter's **Mapped value** field.
-   **Join** \(Table read operations only\) indicates that you're creating a table join. For more information, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).


</td></tr><tr><td>

Mapped value

</td><td>

Specific value of the parameter.-   For **Input** parameters, accept the system-generated name.
-   For **Constant** parameters, enter a set value that's always sent for the parameter.
-   For **Join** parameters, select the field to join the parameter with. For details on creating joins, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).


</td></tr></tbody>
</table>    If you're adding a complex, nested parameter, such as an address that includes several other parameters \(one for street, one for city, one for country\), ERP Data Hub automatically identifies that it needs additional related parameters and creates new, nested parameter rows that you must then populate with the related values. You can nest only parameters with **Object** or **Array** as the **Data type**.

11. Include the newly defined parameter in the Output parameters section by selecting the automap icon \(![Automap icon](../image/erpc-automap-icon.png)\).

    ERP Data Hub automatically updates the **Mapped value** for the Tables/Function call parameter, and adds a row for the parameter to the Output parameters section.

12. Specify a **Default value** to be used for the parameter in the newly added **Optional parameter** row in the Output parameters section.

    The **Default value** is used when the input parameter isn't specified in the query.

13. Remove any optional parameters that you don't need when querying the ERP system by selecting the remove \(-\) icon.

    You can't remove any **Required parameters**.

14. Make any additional edits to existing parameters.

15. Select **Save**.


## What to do next

Next, check the output parameters for the operation and update as needed. For more information, see [Choose output parameters for an ERP model](erp-canvas-manage-outputs.md).

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)


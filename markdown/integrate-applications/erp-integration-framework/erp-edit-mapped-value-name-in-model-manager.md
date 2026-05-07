---
title: Edit input and output mapped value name in Zero Copy Connector for ERP
description: Manually edit mapped value field names for input and output when managing models in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, input, output, value, map, name, edit, model]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Edit input and output mapped value name in Zero Copy Connector for ERP

Manually edit mapped value field names for input and output when managing models in Zero Copy Connector for ERP \(Enterprise Resource Planning\).

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

In ERP model manager, the mapped value name in inputs and outputs is system-generated automatically. Edit the value manually as needed. Specify a unique value. You can revert to the system-generated name at any time.

Let's step through an example. In Zero Copy Connector for ERP, create a model. For more information, see [Create a model](erpc-add-new-data-model.md).

## Procedure

1.  On the new model, select **Manage Model** and add a read operation.

    For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

2.  On the read operation, add a read table entity, for example, on the T005 Countries table.

    ![Add entity page with T005 entity selected.](../image/erpc-mapped-value-example1.png)

    For more information, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

3.  After data is retrieved, select **Specify inputs**.

4.  Select **Select mandatory inputs**.

5.  Select **Country/Region Key** and select **OK**.

    ![Mandatory inputs for countries organized into available columns and selected columns.](../image/erpc-mapped-value-example2.png)

    The system-generated mapped value is countries\_country\_region\_key. The operation parameter value is set to the same name.

    ![Specify inputs page with required parameter and mapped value fields highlighted.](../image/erpc-mapped-value-example3-ys2.png)

6.  Change the mapped value to, for example, **country\_region\_key** and select **Save**.

    The updated mapped value is displayed and the operation parameter value changes to match automatically.

    ![Updated field with edited mapped value and updated, matching required parameter.](../image/erpc-mapped-value-example4-ys2.png)

7.  If a new input is added, the mapped value is system-generated but is editable.

    For example, add the **Nationality** field and edit the name from **countries\_nationality** to **country\_nationality** so it's more consistent with the **country\_region\_key** name.

    ![New field added and mapped value is displayed as editable.](../image/erpc-mapped-value-example5-ys2.png)


-   If a new child \(nested\) input is added, the system-generated mapped value doesn't contain the parent name. You can edit the child name for inputs and outputs. For input, the edited name is used in the operational parameter. In this example, the **UDAT** and **BASXML\_SUPPORTED** fields were added and their system-generated names can be edited to contain or more closely match the parent name.

    ![Function call displayed with function names parent field and several child fields.](../image/erpc-mapped-value-example6-ys2.png)

-   If a join is used, the changed name should be available on the join fields as well. For more information about joins, see [Add joins between ERP tables](erp-canvas-add-join-data-model.md).
-   If the same field exists in both input and output, but they have different mapped values, the name of the output field is given precedence and used.
-   If you want to revert to the system-generated name at any time, remove the field and then add it again. Another option is to change the mapping type and then change it back.

**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)


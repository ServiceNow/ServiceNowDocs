---
title: Choose output parameters for an ERP model
description: Specify output parameters for an ERP \(Enterprise Resource Planning\) system read or update operation in Zero Copy Connector for ERP to define how fields and parameters are mapped from the ERP system to the ServiceNow AI Platform. Output parameters also define how returned data is stored on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Choose output parameters for an ERP model

Specify output parameters for an ERP \(Enterprise Resource Planning\) system read or update operation in Zero Copy Connector for ERP to define how fields and parameters are mapped from the ERP system to the ServiceNow AI Platform. Output parameters also define how returned data is stored on the ServiceNow AI Platform.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin, sn\_erp\_integration.erp\_user

## About this task

If you're already in the process of managing a model and ready to specify outputs, you can skip to step 5.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the ERP model icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

3.  Select the model that you want to add a read operation to.

4.  Select the **Manage model** button.

5.  Open a model operation.

    If you do not have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

6.  Open an entity.

    If you do not have an entity, add one to the operation. For more information, see [Add a read, update, or create entity to a model in Zero Copy Connector for ERP](erpc-add-entity-to-model-op.md)

7.  Select the **Choose outputs** tab.

8.  Review the existing outputs to see if you must add any additional parameters.

    ![Specify operation outputs.](../image/erpc-output-parameters-manager-ys2.png)

    The **Prepopulated outputs** section lists any fields that were added to the inputs. The fields are read-only on the output page, but can be edited and removed on the input page.

    **Note:** Prepopulated output applies to only to table and Odata entities.

    ![Outpage page with prepopulated outputs section expanded to show read-only fields.](../image/erpc-output-prepopulated-outpus.png)

    **Note:** Mapped value names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](../concept/erpc-edit-mapped-value-name-in-model-manager.md).

9.  Add a new output field or parameter.

    1.  Select the add icon \(+\) next to the last-defined parameter.

        If you're adding a mapped field for a table read operation, make sure to add the field to the applicable table section.

    2.  Search for and select the **Field name** for table reads or **Parameter name** for BAPI \(Business Application Programming Interface\) operations.

        The **Data type** field is automatically updated with the applicable values for your selection.

    3.  Enter the corresponding value in the **Mapped value** field.

    If you're adding a complex, nested parameter, such as an address that includes several other parameters \(one for street, one for city, one for country\), Zero Copy Connector for ERP automatically identifies that it needs additional related parameters and creates new, nested parameter rows that you must then populate with the related values. You can nest only parameters with **Object** or **Array** as the **Data type**.

    The following example shows outputs and nested outputs for a BAPI.

    ![BAPI output with two fields that each have nested outputs.](../image/erpc-output-bapi-nested.png)

10. Add any nested output fields or parameters to choose what data to include from a complex parameter.

    For example, you may have a full billing address in the object parameters but only need to include the city and postal code as output.

    1.  Specify the parent output field or parameter.

    2.  Select the settings \(![ERP settings icon](../image/erpc-output-indent-icon.png)\) or add icon \(+\) for the parent row.

    3.  In the modal that appears, select any additional, related fields or parameters to include.

    The parent automatically updates with the related, nested fields or parameters you selected.

11. Select **Save**.


## Result

When you add mapped fields or parameters as outputs and successfully read or update the ERP system, each parameter appears as a field that you can then add to a remote table or an extraction table. Manage the fields for the remote table or extraction table to add the retrieved parameters. For more information, see the following topics:

-   [Customize fields for an ERP remote table in Zero Copy Connector for ERP](erp-canvas-build-remote-table.md)
-   [Select fields for an extraction table in Zero Copy Connector for ERP](erpc-select-extraction-table-fields.md)

**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)


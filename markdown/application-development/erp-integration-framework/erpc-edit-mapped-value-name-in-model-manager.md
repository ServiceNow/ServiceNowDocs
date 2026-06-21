---
title: Edit input and output mapped value name in Zero Copy Connector for ERP
description: Manually edit mapped value field names for input and output when managing models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erpc-edit-mapped-value-name-in-model-manager.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Edit input and output mapped value name in Zero Copy Connector for ERP

Manually edit mapped value field names for input and output when managing models.

In ERP model manager, the mapped value name in inputs and outputs is system-generated automatically. Edit the value manually as needed. Specify a unique value. You can revert to the system-generated name at any time.

Let's step through an example. In Zero Copy Connector for ERP, create a model. For more information, see [Add a new ERP model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-add-new-data-model.md).

On the new model, select **Manage Model** and add a read operation. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-manage-models-read-op.md).

On the read operation, add a read table entity, for example, on the T005 Countries table. For more information, see [Add a read, update, or create entity to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-add-entity-to-model-op.md).

\[Omitted image "erpc-mapped-value-example1.png"\] Alt text: Add entity options.

After data is retrieved, select **Specify inputs**.

Select **Select mandatory inputs**.

Select **Country/Region Key** and select **OK**.

\[Omitted image "erpc-mapped-value-example2.png"\] Alt text: Select mandatory inputs option.

The system-generated mapped value is countries\_country\_region\_key. The operation parameter value is set to the same name.

\[Omitted image "erpc-mapped-value-example3-ys2.png"\] Alt text: Mandatory field with matching mapped value and required parameter fields.

Change the mapped value to, for example, **country\_region\_key** and select **Save**. The updated mapped value is displayed and the operation parameter value changes to match automatically.

\[Omitted image "erpc-mapped-value-example4-ys2.png"\] Alt text: Updated field with edited mapped value and updated, matching required parameter.

If a new input is added, the mapped value is system-generated but is editable. For example, add the **Nationality** field and edit the name from **countries\_nationality** to **country\_nationality** so it's more consistent with the **country\_region\_key** name.

\[Omitted image "erpc-mapped-value-example5-ys2.png"\] Alt text: New field added and mapped value is displayed as editable.

## Keep the following in mind

-   If a new child \(nested\) input is added, the system-generated mapped value doesn't contain the parent name. You can edit the child name for inputs and outputs. For input, the edited name is used in the operational parameter. In this example, the **UDAT** and **BASXML\_SUPPORTED** fields were added and their system-generated names can be edited to contain or more closely match the parent name.

    \[Omitted image "erpc-mapped-value-example6-ys2.png"\] Alt text: Function call displayed with function names parent field and several child fields.

-   If a join is used, the changed name should be available on the join fields as well. For more information about joins, see [Add joins between ERP tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-add-join-data-model.md).
-   If the same field exists in both input and output, but they have different mapped values, the name of the output field is given precedence and used.
-   If you want to revert to the system-generated name at any time, remove the field and then add it again. Another option is to change the mapping type and then change it back.

**Parent Topic:**[Building and managing ERP models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/work-with-erp-data-models.md)


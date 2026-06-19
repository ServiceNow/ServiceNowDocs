---
title: Select model output parameters for REST
description: Specify how fields on the ERP \(Enterprise Resource Planning\) system map to output parameters and their values. This defines the outputs for an operation that reads, creates, or updates the system of record using REST.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-rest.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-04-26"
reading_time_minutes: 3
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Select model output parameters for REST

Specify how fields on the ERP \(Enterprise Resource Planning\) system map to output parameters and their values. This defines the outputs for an operation that reads, creates, or updates the system of record using REST.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model that you want to add an operation to.

4.  Select the **Manage model** button.

5.  Open a model operation with a REST entity.

    If you don't have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

6.  Check that at least one REST entity is listed.

    If you don't have a REST entity, add one to the operation. For more information, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

7.  Select **Choose outputs**.

8.  In **Selection**, select a listed REST service.

9.  Select **Select mandatory fields**, add fields, and select **OK**.

10. Select **Select fields** and add fields.

11. Select **OK**.

    Zero Copy Connector for ERP automatically suggests mappings between source fields and mapped fields. This reduces the amount of manual work to do, while still giving you control to edit the mappings as needed. For more information, see [Zero Copy Connector for ERP semantic mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-semantic-mapping.md).

    Mapped field names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-edit-mapped-value-name-in-model-manager.md).

12. If needed, add a field.

    1.  Select **+ Add field**.

    2.  In **Source field**, select a field from the drop-down list.

        Field information is added to **Data type**, **Required**, and **Mapped field** automatically.

        The **Data type** field contains a variety of types including string, integer, array, and Boolean. For general information, see .

    3.  Select **OK**.

13. Add any nested output fields or parameters to choose what data to include from a complex parameter.

    1.  Select the nesting options icon.

        \[Omitted image "erp-manage-outputs-rest1.jpg"\] Alt text: Choose outputs screen with nesting options icon highlighted.

    2.  Select **+ Add field**.

    3.  In **Source field**, select a field from the drop-down list.

        Field information is added to **Data type**, **Required**, **Mapping type**, and **Mapped field** automatically.

    The following example shows full data options, but only some have been specified as output.

    \[Omitted image "erp-manage-outputs-rest2.jpg"\] Alt text: Output selection page with all field options and selected fields highlighted.

14. Select **Save**.


**Parent Topic:**[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)


---
title: Manage input parameters for model operation with a REST entity
description: Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values. This defines the inputs for an operation that reads, creates, or updates the ERP system using REST.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-rest.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-04-26"
reading_time_minutes: 3
breadcrumb: [Connecting to ERP with REST, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Manage input parameters for model operation with a REST entity

Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values. This defines the inputs for an operation that reads, creates, or updates the ERP system using REST.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model with the operation that you want to add inputs to.

4.  Select **Manage model**.

5.  Open a model operation with a REST entity.

    If you don't have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

6.  Check that at least one REST entity is listed.

    If you don't have a REST entity, add one to the operation. For more information, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

7.  Select **Specify inputs**.

    There are two tabs, which you complete in order:

    -   In **Step 1: Configuration**, set the validation rules and pagination.
    -   In **Step 2: Select fields**, map fields and define the inputs for the operation.
    \[Omitted image "erp-manage-inputs-rest1.jpg"\] Alt text: Manage model page, with specify input tab displayed and configuration/selection options highlighted.

8.  In **Step 1**, define whether operation inputs are required by expanding the **Validation rules** section and selecting an option in **Query validation rule**.

    -   **All required inputs are mandatory**
    -   **At least one required input is mandatory**
    -   **No validation on inputs**
9.  Expand the **Pagination** section and select an option to configure pagination parameters and control how data is retrieved in batches.

    -   Select **None \(no pagination\)** to not use any pagination.
    -   Select **Offset-based** to import data in batches based on time intervals.
    -   Select **Page-based** to specify the number of records \(limit\) that can be fetched at a time.
10. Select **Save**.

11. In **Step 2**, select the entity.

    \[Omitted image "erp-manage-inputs-rest4.jpg"\] Alt text: Entity highlighted in step 2 select fields.

12. Select **Select mandatory fields**.

    \[Omitted image "erp-manage-inputs-rest5.jpg"\] Alt text: Specify inputs are with select mandatory fields button highlighted.

13. Add fields.

    \[Omitted image "erp-manage-inputs-rest2.jpg"\] Alt text: Available and selected inputs.

    After adding fields, you can rearrange their order in the **Selected columns** list by dragging the field card to a new location.

14. Select **OK**.

    Zero Copy Connector for ERP automatically suggests mappings between source fields and mapped fields. This reduces the amount of manual work to do, while still giving you control to edit the mappings as needed. For more information, see [Zero Copy Connector for ERP AI semantic field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-semantic-mapping.md).

    Mapped field names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-edit-mapped-value-name-in-model-manager.md).

15. Select **Select fields**.

16. For the non-mandatory fields, repeat steps 13-14.

17. Select **Save**.

18. If needed, add a field.

    1.  Select **+ Add field**.

        \[Omitted image "erp-manage-inputs-rest3.jpg"\] Alt text: Field list with add field button highlighted.

    2.  In **Source field**, select a field from the drop-down list.

        Field information is added to **Data type**, **Required**, **Mapping type**, and **Mapped field** automatically.

        The **Data type** field contains a variety of types including string, integer, array, and Boolean. For general information, see [Workflow Studio input and output data variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/action-inputs-outputs.md).

19. Select **Save**.


## What to do next

Next, check the output parameters for the operation and update as needed. For more information, see [Select model output parameters for REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-rest.md).


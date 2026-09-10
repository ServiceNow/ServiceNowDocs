---
title: Manage input parameters for model operation with Oracle REST entity
description: Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values. This defines the inputs for an operation that reads, creates, or updates the Oracle ERP system using REST.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-oracle-rest.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 4
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Manage input parameters for model operation with Oracle REST entity

Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values. This defines the inputs for an operation that reads, creates, or updates the Oracle ERP system using REST.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model with the operation that you want to add inputs to.

4.  Select **Manage model**.

5.  Open a model operation with an Oracle REST entity.

    If you don't have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

6.  Check that at least one Oracle REST entity is listed.

    If you don't have an Oracle REST entity, add one to the operation. For more information, see [Add an Oracle REST entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-oracle-rest-entity-to-a-model-operation.md).

7.  Select **Specify inputs**.

    Complete the two tabs in order:

    -   In **Step 1: Configuration**, set the validation rules and pagination.
    -   In **Step 2: Select fields**, map fields and define the inputs for the operation.
    \[Omitted image "erp-manage-inputs-oracle-rest1.jpg"\] Alt text: Manage model page, with specify input tab displayed.

8.  In **Step 1**, define whether operation inputs are required by expanding the **Validation rules** section and selecting an option in **Query validation rule**.

    -   **All required inputs are mandatory**
    -   **At least one required input is mandatory**
    -   **No validation on inputs**
9.  Expand the **Pagination** section and select an option to configure pagination parameters and control how data is retrieved in batches.

    -   Select **None \(no pagination\)** to skip pagination.
    -   Select **Offset-based** to import data in batches based on time intervals.
    -   Select **Page-based** to specify the number of records \(limit\) that can be fetched at a time.
10. Select **Save**.

11. In **Step 2**, select the entity.

    \[Omitted image "erp-manage-inputs-oracle-rest2.jpg"\] Alt text: Entity highlighted in step 2 select fields.

12. Select **Select mandatory fields**.

    \[Omitted image "erp-manage-inputs-oracle-rest3.jpg"\] Alt text: Specify inputs area with select mandatory fields button highlighted.

13. Add fields.

    \[Omitted image "erp-manage-inputs-oracle-rest4.jpg"\] Alt text: Available and selected inputs.

14. Select **OK**.

    Zero Copy Connector for ERP automatically displays suggested mappings between source fields and mapped fields. This reduces the amount of manual work to do, while still giving you control to edit the mappings as needed. For more information, see [Zero Copy Connector for ERP AI semantic field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-semantic-mapping.md).

    Mapped field names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-edit-mapped-value-name-in-model-manager.md).

15. Select **Select fields**.

16. For the non-mandatory fields, repeat steps 13-14.

17. Select **Save**.

18. Add a field.

    1.  Select **+ Add field**.

        \[Omitted image "erp-manage-inputs-oracle-rest5.jpg"\] Alt text: Field list with add field button highlighted.

    2.  In **Source field**, select a field from the drop-down list.

        The system adds field information to **Data type**, **Required**, **Mapping type**, and **Mapped field** automatically.

        The **Data type** field contains a variety of types including string, integer, array, and Boolean. For general information, see [Workflow Studio input and output data variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/action-inputs-outputs.md).

19. Select **Save**.

20. Define the input parameters for the operation.

    For more information, see [Manage input parameters for model operation with a REST entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-rest.md).

21. Add any request headers that the Oracle service requires.

    For Oracle EBS services described by WADL, the Oracle context values are encoded automatically and don't need to be added by hand. How they're sent depends on the HTTP method: GET operations send them as individual query parameters, and POST operations send them as a single nested header structure.

22. Define the payload template for create and update operations.

23. Map the response fields to the model output.

    For more information, see [Select model output parameters for REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-rest.md).

24. Select **Save**.

    Model validation runs automatically when REST is the selected protocol.



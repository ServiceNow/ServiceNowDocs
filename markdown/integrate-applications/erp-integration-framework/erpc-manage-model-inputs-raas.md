---
title: Manage input parameters for RaaS
description: Specify how fields on the enterprise resource planning \(ERP\) system map to input parameters and their values. This mapping defines the inputs for an operation that reads the ERP system using Workday Reports as a Service \(RaaS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-raas.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, workday, raas]
breadcrumb: [Connecting to Workday with RaaS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Manage input parameters for RaaS

Specify how fields on the enterprise resource planning \(ERP\) system map to input parameters and their values. This mapping defines the inputs for an operation that reads the ERP system using Workday Reports as a Service \(RaaS\).

## Before you begin

The RaaS report must be added as a service. For more information, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

Inputs are derived from the query parameters in the request URL that you entered when you added the service. Every input is created as an optional string, because a URL carries only text, so the required settings and data types might differ from what the report expects.

Before you use the model, the inputs must match the query parameters that the report accepts.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model with the operation that you want to add inputs to.

4.  Select **Manage model**.

5.  Open a model operation with a Workday RaaS entity.

    If you don't have a model operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

6.  Check that a Workday RaaS entity is listed.

    If you don't have a Workday RaaS entity, add one to the operation. For more information, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md).

7.  Select **Specify inputs**.

    There are two tabs, which you complete in order:

    -   In **Step 1: Configuration**, set the validation rules and pagination.
    -   In **Step 2: Select fields**, select the root entity, map fields, and define the inputs for the operation. The root entity is named for the last segment of the report path. Its fields are the query parameters from the input URL, such as `Start_Date`, `End_Date`, and `format`.
    \[Omitted image "erp-manage-inputs-raas2.png"\] Alt text: Manage model page, with specify input tab displayed and configuration/selection options highlighted.

8.  In **Step 1**, define whether operation inputs are required by expanding the **Validation rules** section and selecting an option in **Query validation rule**.

    -   **All required inputs are mandatory**
    -   **At least one required input is mandatory**
    -   **No validation on inputs**
9.  Expand the **Pagination** section and select an option to configure pagination parameters and control how data is retrieved in batches.

    -   Select **None \(no pagination\)** to turn off pagination.
    -   Select **Offset-based** to import data in batches based on time intervals.
    -   Select **Page-based** to specify the number of records \(limit\) that can be fetched at a time.
10. Select **Save**.

11. In **Step 2**, select the entity.

    \[Omitted image "erp-manage-inputs-raas3.png"\] Alt text: Entity highlighted on the Step 2: Select fields tab.

12. Select **Select mandatory fields**.

    \[Omitted image "erp-manage-inputs-raas4.png"\] Alt text: Specify inputs tab with the Select mandatory fields button highlighted.

13. Add fields by selecting them in the **Available columns** list.

    After adding fields, you can rearrange their order in the **Selected columns** list by dragging the field card to a new location.

14. Select **OK**.

    Zero Copy Connector for ERP automatically displays suggested mappings between source fields and mapped fields. This reduces the amount of manual work to do, while still giving you control to edit the mappings as needed. For more information, see [Zero Copy Connector for ERP AI semantic field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-semantic-mapping.md).

    Mapped field names in inputs and outputs are generated automatically, but you can edit the names manually. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-edit-mapped-value-name-in-model-manager.md).

15. Select **Select fields**.

16. For the non-mandatory fields, repeat steps 13-14, adding the fields from the **Available columns** list and selecting **OK**.

    The fields in the **Available columns** list come directly from the URL entered when adding the service manually. For details about the URL, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md).

    \[Omitted image "erp-manage-inputs-raas5.png"\] Alt text: Available and selected inputs.

17. Select **Save**.

18. If needed, add a field.

    1.  Select **+ Add field**.

        \[Omitted image "erp-manage-inputs-raas6.png"\] Alt text: Field list with add field button highlighted.

    2.  In **Source field**, select a field from the drop-down list.

        Field information is added to **Data type**, **Required**, **Mapping type**, and **Mapped field** automatically.

        The **Data type** field contains a variety of types including string, integer, array, and Boolean. For general information, see .

19. Select **Save**.


## Result

Your changes are saved to the model entity and its field records and apply the next time the model runs.

## What to do next

Next, check the output parameters for the operation and update them as needed. For more information, see [Manage model output parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-raas.md).


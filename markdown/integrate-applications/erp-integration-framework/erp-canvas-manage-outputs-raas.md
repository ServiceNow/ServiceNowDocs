---
title: Manage model output parameters for RaaS
description: Specify how fields on the enterprise resource planning \(ERP\) system map to output parameters and their values. This mapping defines the outputs for an operation that reads the ERP system using Workday Reports as a Service \(RaaS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-raas.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, workday, raas]
breadcrumb: [Connecting to Workday with RaaS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Manage model output parameters for RaaS

Specify how fields on the enterprise resource planning \(ERP\) system map to output parameters and their values. This mapping defines the outputs for an operation that reads the ERP system using Workday Reports as a Service \(RaaS\).

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

Outputs derived from a Workday RaaS sample response reflect only the fields present in that sample. Because Workday RaaS omits a field entirely when it has no value, a field that is empty in every sampled row does not appear. Data types and lengths inferred from sample values might also differ from how the field is defined in Workday.

Before you use the model, the outputs must match the fields that the report returns.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model with the read operation that you want to add outputs to.

4.  Select **Manage model**.

5.  Open a read operation with a Workday RaaS entity.

    If you don't have a read operation, add one to the model. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

6.  Check that a Workday RaaS entity is listed.

    If you don't have a Workday RaaS entity, add one to the operation. For more information, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md) .

7.  Select **Choose outputs**.

8.  Select the root entity, for example, CR\_Worker\_s\_Termination\_event.

9.  Select **Select fields**.

    \[Omitted image "erp-manage-outputs-raas3.png"\] Alt text: Choose outputs screen with root entity and select fields button highlighted.

10. Select **Report\_Entry** in the **Available columns** list.

11. Select **OK**.

    \[Omitted image "erp-manage-outputs-raas4.png"\] Alt text: Available and selected inputs.

12. Select **Save**.

13. In **Step 2: Select fields**, select **Report\_Entry**.

    \[Omitted image "erp-manage-outputs-raas5.png"\] Alt text: Entity highlighted on the Step 2: Select fields tab.

    **Report\_Entry** field is derived as an array because it holds the report rows.

14. Select **Select fields**.

15. Select all of the fields in the **Available columns** list.

16. Select **OK**.

    \[Omitted image "erp-manage-outputs-raas6.png"\] Alt text: Available and selected inputs for the report entry field.

17. Select **Save**.


## Result

Your changes are saved to the model entity and its field records. The changes are applied the next time the model runs.


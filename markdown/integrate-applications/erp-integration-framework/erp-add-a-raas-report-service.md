---
title: Add a Workday RaaS entity to a model operation
description: Use a Workday Reports as a Service \(RaaS\) report in a read model operation by entering the report request URL and a sample response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, workday, raas]
breadcrumb: [Connecting to Workday with RaaS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a Workday RaaS entity to a model operation

Use a Workday Reports as a Service \(RaaS\) report in a read model operation by entering the report request URL and a sample response.

## Before you begin

The following items must be in place before you add a RaaS report service:

-   The **sn\_erp\_integration.enableModelModification** property must be enabled. For more information, see [Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/install-erp-integration.md).
-   A connection and credential alias must exist, with REST specified as the **Connection type**. For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md).
-   A REST connection must exist for the Workday tenant, with the connection alias and the connection URL added to it.
-   A system that uses the REST connection must exist. For more information, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/create-an-erp-system.md).
-   A model that uses the Workday system and software must exist, with a read operation added to it. For more information, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

Role required: sn\_erp\_integration.erp\_admin

## About this task

You can add a RaaS report only to a read operation, not to a create or update operation.

Prepare the following before you start:

-   The request URL for the report, including its query parameters.
-   A sample JSON response from that request. Use a sample with enough rows to include every field the report can return. A field that is empty in every sampled row does not appear in the derived schema.

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model to which you want to add an operation entity.

4.  In the **ERP system** field, verify that the correct system is selected.

5.  Select the **Manage model** button.

    \[Omitted image "erp-add-raas-entity-to-model3.png"\] Alt text: Workday RaaS model form with the Manage model button highlighted.

6.  Select the read operation.

    If you don't have a read operation, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

7.  Select **Select entity** on the **Manage entities** tab.

8.  In **Select type**, select **REST**.

9.  Select **+ Add service manually**.

    The **Add REST service manually** dialog box opens.

10. Select **Custom**.

    \[Omitted image "erp-add-raas-entity-to-model1.png"\] Alt text: Add REST service manually dialog box with the Custom option highlighted.

    The **Custom** option is available only for read operations.

    \[Omitted image "erp-add-raas-entity-to-model2.png"\] Alt text: Add REST service manually dialog box showing the Input URL and Output example fields with the Add service button.

11. In the **Input URL** field, enter the request URL for the report, including its query parameters.

    Enter either a full URL that starts with `http://` or `https://`, for example, `https://wd2-impl-services1.workday.com/ccx/service/customreport2/{tenant}/{report_owner}/CR_Worker_s_Termination_event?Start_date=2026-01-01T01%3A05%3A00.000-08%3A00&End_Date=2026-09-11T14%3A00%3A00.000-07%3A00&format=json`. Alternatively, add a path that starts with a forward slash. The system connection on the model supplies the host, so a path is enough.

    Each query parameter in the URL \(all information in the URL after the question mark\) becomes an input field. For example, start date, end date, and format.

    For more details about inputs, see [Manage input parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-raas.md).

12. In the **Output example** field, paste a sample JSON response from the report.

    Fields are created as strings, numbers, or Boolean values. When the rows contain different types for a field, or a field has no value in one of the rows, the field is created as a string.

    For more details about outputs, see [Manage model output parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-raas.md).

    \[Omitted image "erp-add-raas-entity-to-model5.png"\] Alt text: Add REST service manually dialog box with a sample report URL in the Input URL field and JSON pasted in the Output example field.

13. Select **Add service**.

    A message confirms that the service was uploaded.


## Result

The data derived from the input URL and the output example is retrieved.

\[Omitted image "erp-add-raas-entity-to-model4.png"\] Alt text: Manage entities tab showing a retrieved data entity listed under Operation entities.

## What to do next

Next, select the input and output fields that the operation uses. For the inputs, see [Manage input parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-raas.md). For the outputs, see [Manage model output parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-raas.md).


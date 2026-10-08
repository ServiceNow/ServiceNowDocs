---
title: Obtaining data from Workday using RaaS reports
description: Workday Reports as a Service \(RaaS\) exposes a Workday custom report as a callable endpoint, so you can obtain report data that no standard Workday API returns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-raas.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, workday, raas, rest, report]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Obtaining data from Workday using RaaS reports

Workday Reports as a Service \(RaaS\) exposes a Workday custom report as a callable endpoint, so you can obtain report data that no standard Workday API returns.

## What RaaS reports provide

Workday Reports as a Service \(RaaS\) exposes a Workday custom report as an endpoint that returns the report output as data. Where a standard Workday REST API returns records from a defined business object, a RaaS endpoint returns whatever columns the report author configured.

Use RaaS when the data you need is already assembled in a Workday custom report and no equivalent standard API exists.

For standard Workday REST connectivity, see [Obtaining data from Workday using REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-rest-api.md).

## Using a RaaS report

When adding a RaaS report to a read model operation, supply the following:

-   The report request URL, including its query parameters. Each query parameter in the URL becomes an input field.
-   A sample JSON response from that request. The fields found across the rows in the sample become the output fields.

For the steps, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md).

## Reviewing the inputs and outputs

After the service is added, you choose which of the derived fields the operation uses. The output fields include only the fields that appear in the sample response that you supply.

Review and adjust the inputs and outputs before you use the model. For the steps, see [Manage input parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-raas.md) and [Manage model output parameters for RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs-raas.md).

## Running a RaaS model from a script

After the model is configured, you can run the report from a server-side script through the scriptable API. Because the input variable names are generated from the report's query parameters, look them up with `getAvailableInputs()` before you pass values with `withJSON()`. Pass date values in the format that the report expects.

```javascript
// Look up the generated input variable names for the report
const inputs = new API()
  .system('workday')
  .model('workday_raas_report')
  .operation('read')
  .getAvailableInputs();

// Run the report with values for its query-parameter inputs
const rows = new API()
  .system('workday')
  .model('workday_raas_report')
  .operation('read')
  .withJSON({
    start_date_input: '2026-01-01',
    end_date_input: '2026-03-31'
  })
  .execute();
```

For the full method reference, see [sn\_erp\_integration API - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/sn_erp_integrationBothAPI.md).


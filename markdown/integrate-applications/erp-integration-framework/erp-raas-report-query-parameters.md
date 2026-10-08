---
title: Workday RaaS report query parameters
description: Workday Reports as a Service \(RaaS\) reports take their filters as query parameters rather than path parameters, and each report defines its own set of parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-raas-report-query-parameters.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, workday, raas, query, parameter]
breadcrumb: [Connecting to Workday with RaaS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Workday RaaS report query parameters

Workday Reports as a Service \(RaaS\) reports take their filters as query parameters rather than path parameters, and each report defines its own set of parameters.

## Query-parameter filters

Filters for a RaaS report are passed as query parameters on the request URL, rather than as path parameters. Other entity types in Zero Copy Connector for ERP continue to use path-parameter filtering.

Because each RaaS report defines its own parameters with no shared convention, the parameter names are captured per report from the request URL you enter. Every parameter is created as an optional string, because a URL carries only text. For the steps, see [Add a Workday RaaS entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-add-a-raas-report-service.md).

## URL and parameter handling

<table id="table-raas-url-handling"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report path

</td><td>

Requests use the RaaS path: `/ccx/service/customreport2/{tenant}/{report_owner}/{report_name}`.

 The host and the tenant come from the system connection on the model, so the stored path holds neither.

</td></tr><tr><td>

Response format

</td><td>

A valid, sample JSON response from the request.

</td></tr></tbody>
</table>
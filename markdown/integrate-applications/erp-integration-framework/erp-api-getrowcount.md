---
title: API – getRowCount\(\)
description: Returns the total number of rows that a Zero Copy Connector for ERP model operation would return, without retrieving the records themselves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-api-getrowcount.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, zero, copy, connector, api, row count, scripting]
breadcrumb: [Data retrieval, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# API – getRowCount\(\)

Returns the total number of rows that a Zero Copy Connector for ERP model operation would return, without retrieving the records themselves.

Use getRowCount\(\) as a terminal method in place of execute\(\) when you need only a count. You configure the query the same way you would for a normal run, then call getRowCount\(\) instead.

## How the count is determined

The count is protocol-specific:

|Protocol|Source of the count|
|--------|-------------------|
|Read table|Total record count reported in the connector response metadata.|
|OData|The OData count endpoint. Supported for both direct execution and execution through a MID Server.|
|BAPI|Uses the default fallback. SAP provides no native count capability for BAPI calls.|
|REST|Uses the default fallback.|
|Default fallback|Counts the items actually returned in the response, which is equivalent to counting the rows that would land in a remote table.|

**Note:** Where the default fallback applies, the response is still retrieved to be counted. Only the read table and OData paths avoid fetching the records.

## Related methods

The same count behavior is available at two lower levels. The query engine exposes a row count method alongside its execute method. The API handler provides count methods that accept either an encoded query or a JSON filter, parallel to its existing query and filter methods.

## Limitations

For REST services, designating a specific response field as the count is not supported.


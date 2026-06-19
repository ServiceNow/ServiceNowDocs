---
title: REST API connector for Zero Copy Connector for ERP tables
description: Find details on REST API connector tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-rest-api-tables.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [zero, copy, connector, erp, canvas, data hub, integration, rest, api, table]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# REST API connector for Zero Copy Connector for ERP tables

Find details on REST API connector tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\).

For an overview of the REST API connector, see [REST API for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-connector.md).

For process details, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

For information about adding a service, see [Add a REST service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.md).

|Table|Description|
|-----|-----------|
|sn\_erp\_integration\_rest\_service\_catalog|Stores imported REST API service definitions \(name, version, base URL\).|
|sn\_erp\_integration\_rest\_service\_endpoint|Stores individual endpoint definitions \(path, HTTP method, inputs, outputs, return type\).|
|sn\_erp\_integration\_model\_operation|Contains new 'rest' operation type, pagination\_type choice field, and http\_method column.|
|sn\_erp\_integration\_model\_entity|Contains new 'rest' entity type for REST API operations.|
|sn\_erp\_integration\_input\_mapping|Contains pagination type field and pagination\_operator for offset/limit tracking.|
|sn\_erp\_integration\_model\_table\_field|Contains field metadata from parsed OpenAPI specs.|

**Parent Topic:**[Zero Copy Connector for ERP field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-field-descriptions.md)


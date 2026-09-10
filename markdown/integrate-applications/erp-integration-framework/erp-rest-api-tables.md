---
title: REST API connector tables for Zero Copy Connector for ERP
description: The REST API connector in Zero Copy Connector for ERP \(Enterprise Resource Planning\) uses these tables to store service definitions, endpoint definitions, and model metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-rest-api-tables.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
keywords: [zero, copy, connector, erp, canvas, data hub, integration, rest, api, table]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# REST API connector tables for Zero Copy Connector for ERP

The REST API connector in Zero Copy Connector for ERP \(Enterprise Resource Planning\) uses these tables to store service definitions, endpoint definitions, and model metadata.

For an overview of the REST API connector, see [REST API for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-connector.md).

For process details, see [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

For information about adding a service, see [Add a REST service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.md).

Oracle E-Business Suite services described by WADL documents use their own set of tables.

|Table|Description|
|-----|-----------|
|sn\_erp\_integration\_rest\_service\_catalog|Stores imported REST API service definitions \(name, version, base URL\).|
|sn\_erp\_integration\_rest\_service\_endpoint|Stores individual endpoint definitions \(path, HTTP method, inputs, outputs, return type\).|
|sn\_erp\_integration\_model\_operation|Stores model operations, including the **rest** operation type, the pagination\_type choice field, and the http\_method column.|
|sn\_erp\_integration\_model\_entity|Stores model entities, including the **rest** entity type used for REST API operations. A WADL entity type is also available for Oracle E-Business Suite services.|
|sn\_erp\_integration\_input\_mapping|Stores input mappings, including the pagination\_type field and the pagination\_operator field used for offset and limit tracking.|
|sn\_erp\_integration\_model\_table\_field|Stores field metadata parsed from service definitions, whether OpenAPI specifications or WADL and XML Schema Definition documents.|

